# 29.12 — [JAVA 24] Parallel Gatherers - Theory

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] So far we discussed the basic concepts of gatherers API.
[00:04] As a next step, let's try to understand how to build the Parallel Gatherers.
[00:09] In the same process, we're also going to explore about the combiner optional component that we can
[00:14] provide while we are building an intermediate operation with the help of Gatherers API.
[00:19] By using Parallel Gatherers, we should be able to process our elements inside our intermediate operation
[00:27] in multiple threads.
[00:29] Java provides different ways to define parallel gatherers depending on whether we want to use internal
[00:35] state inside our business logic.
[00:38] If you're not using any internal state inside your business logic, then building parallel gatherers
[00:44] is very simple.
[00:44] Otherwise, you need to take care of merging all the internal mutable states that you are receiving
[00:51] from multiple threads before pushing the output to the downstream.
[00:55] On a high level, there are three different flavors that we can use to build the parallel gatherers.
[01:00] The very first flavor is ,when you are invoking the of() factory method of gatherer.
[01:05] If you are passing only the integrator logic, then all the elements from the upstream, they are going
[01:11] to be processed parallelly by executing your intermediate operator logic.
[01:16] When you are using this flavor, it means you don't want to use any mutable state inside your business
[01:22] logic,
[01:22] there won't be any finisher and this kind of parallel gathers,
[01:25] they are simple and safe for parallel execution.
[01:28] Whatever logic that you are going to define inside your integrator, the same logic will be executed
[01:33] parallelly for all the elements that is being received from the upstream.
[01:37] Here I also have an example.
[01:38] I created a gatherer with the name eventFilter.
[01:41] Inside this gatherer logic, I'm just checking whether given input element is divisible by two.
[01:48] If yes, then only push the element to the downstream,
[01:51] otherwise don't push the same.
[01:52] Here,
[01:53] the logic inside my intermediate operator can be executed parallelly and independently.
[01:58] Since there is no dependency on the mutable state, I don't have to provide any combiner as well.
[02:04] We already saw the demo of this flavor,
[02:06] please remember always the thumb rule is if you are using the of() factory method from the Gatherer interface
[02:12] behind the scenes, the gatherer logic is going to be executed parallelly by using multiple threads.
[02:19] In case if your business logic does not support parallel processing, and if you want to make sure to
[02:24] run the logic sequentially one by one.
[02:27] Under such scenarios, you need to make sure you are using the ofSequential() factory method.
[02:33] Let's move on to the second flavor,
[02:34] the second flavor is,
[02:36] along with the integrator.
[02:37] You can also pass the finisher logic as well.
[02:41] Sometimes you may have a requirement to execute some finitial logic once you are done processing all
[02:46] the elements parallelly.
[02:48] For example, after invoking a Rest API for 100 different input elements parallelly, at the end, you
[02:53] may want to send an email or confirmation message to someone else.
[02:58] Under such scenarios, you can use this flavor. While using this flavor,
[03:02] also, there won't be any mutable state involved if there is no mutable state is involved, you don't
[03:07] have to,
[03:08] provide any combiner component. Here I have mentioned a simple example.
[03:12] My
[03:12] Gatherer,
[03:13] It is going to simply push the elements whatever it receives from the,
[03:18] upstream.
[03:18] Apart from pushing the elements, it is not going to do anything else.
[03:22] Once, pushing all the elements to the downstream is completed at the end.
[03:26] I'm,
[03:26] going to execute my finished logic where I'm trying to push a message to the,
[03:30] downstream saying that all items are processed.
[03:33] These are simple flavors. I
[03:35] hope you are clear with these examples.
[03:37] Now let's try to look at the complex flavor where we are going to use some mutable state as well while
[03:44] we are trying to process the elements parallelly.
[03:47] As you can see this flavor, it is going to accept an initializer using which you can provide an initial
[03:54] mutable state value followed by integrated logic.
[03:58] As a third parameter, you should also provide combiner component logic.
[04:03] I'll explain the purpose of this combiner in few seconds and towards the end,
[04:07] we should also provide the finisher logic as well.
[04:10] We need to use this flavor when you want to inspect or transform elements parallelly by using a mutable
[04:18] state value.
[04:19] Here I have an example where I'm trying to provide an initial int value zero with the help of the object
[04:26] of AtomicInteger. Whatever initial value that I'm trying to provide with my initializer.
[04:32] The same initial value will be fed to all the multiple threads that are going to execute my integrated
[04:39] logic.
[04:39] For example, if your integrator logic is being executed by three different multiple threads, the same
[04:46] initial mutable state value like 0 ,0will be set to all the threads.
[04:51] By using these initial state value, all the threads they are going to execute the logic present inside
[04:57] the integrator.
[04:58] Inside my integrator logic, I'm trying to simply add the given input number to the initial state value.
[05:06] So if you see I'm trying to invoke add() and to get() method and to the same, I'm passing the input received
[05:13] element which is number.
[05:15] The output will be saved into this some state object.
[05:18] And towards the end I'm trying to return the true.
[05:20] So this is my integrator logic.
[05:22] After the integrator logic I have provided the combiner logic.
[05:26] What is the purpose of combiner component?
[05:28] This combiner component, it is going to combine the different intermediate state values into a single
[05:36] value.
[05:37] The logic of combiner component needs to be provided by using a lambda expression that adheres to the
[05:43] Binary operator functional interface.
[05:47] I'll share more details while we are trying to build this example inside our IntelliJ.
[05:51] So this combiner, it is always going to accept two different intermediate state values as an input.
[05:58] And based upon these two different intermediate state values, it is going to combine them based upon
[06:04] the logic that we have defined.
[06:05] And at the end it is going to return a single state value. For example.
[06:10] Let's imagine initially there are four threads started executing our intermediate logic.
[06:16] There will be T1, there will be T2, T3, and T4.
[06:21] These are the multiple threads that are processing integrator logic.
[06:24] Every thread they're going to have their own intermediate state value.
[06:28] In our scenario it will be zero.
[06:30] So let's imagine this is S1, S2 and S3 and S4.
[06:35] As soon as two different threads that are done with their execution, the intermediate state values
[06:41] like S1 and S2, they are going to be passed to our combiner.
[06:45] These S1 and S2 will be combined to a value.
[06:49] Let's imagine this is S5.
[06:52] The same applies here as well.
[06:54] These intermediate state values are also going to be combined with the help of combiner components,
[06:59] and a new state value will be S6.
[07:02] Now we have two more intermediate state values S5 and S6.
[07:06] These will be again combined to get an and final state value.
[07:12] The same final state value will be feed to the finisher component. If you see,
[07:17] at last we are trying to define a finisher.
[07:19] So this sum represents the total sum value that is calculated by all the multiple threads along with
[07:26] the combiner component.
[07:27] This sum we are trying to push into the downstream with the help of this code.
[07:31] So if you see here, the actual pushing of the data into the downstream is happening only inside the
[07:37] finisher.
[07:38] As a thumb rule, you need to make sure to provide the combiner component.
[07:42] If you are trying to use an mutable state value inside your business logic while you are trying to implement
[07:48] parallel gatherers.
[07:49] In case if you don't want to combine the state by using a combiner component, then you can't run the
[07:55] gatherer in parallel,
[07:57] you just have to go with the ofSequential() option.
[08:00] Inside this slide, I have mentioned a table which is going to give you a summary on how parallel gatherers
[08:06] and sequential gatherers are going to work.
[08:09] The parallel support will only possible if you are using these of() factory method.
[08:13] That's why for the first three rows. The Yes is mentioned here.
[08:18] Whereas for the ofSequential() factory methods the parallel support will be no.
[08:23] Let's try to understand about other components as well.
[08:26] If you are using of() factory method with simple integrator logic, there won't be any mutable state,
[08:32] there won't be any finisher, and there won't be any combiner.
[08:36] Whereas for the next flavor where you're trying to provide finisher as well in this scenario, also,
[08:41] there won't be any mutable state, there won't be any combiner, but there will be a finisher.
[08:46] Whereas if you are using this third flavor mutable state finisher, combiner, parallel support all
[08:52] of them, they are going to be present.
[08:54] Now coming to the ofSequential() factory method, there is an option for you to use an mutable state
[09:01] or not,
[09:01] that's why here I have mentioned yes or no.
[09:04] The same applies for finisher also, but combiner and parallel support.
[09:08] They are not applicable when you are using ofSequential() factory methods.

----------------------------------------
