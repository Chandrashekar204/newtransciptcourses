# 29.11 — [JAVA 24] Finisher in a Stream Gatherer

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] The next component of stream gatherers that we're going to focus is Finisher.
[00:05] Providing this Finisher is also optional, just like Initializer.
[00:09] But there are certain scenarios where you should definitely provide Finisher.
[00:13] Let's try to understand what are those scenarios and what is the purpose of this Finisher.
[00:18] As I said before, the Finisher is an optional part of a Gatherer that is called after all elements
[00:25] have been processed by the stream.
[00:28] Whatever logic that you're going to define inside the Finisher.
[00:31] It is only going to be executed once. Even if your Gatherer is trying to process 1 million input elements
[00:37] from the upstream.
[00:39] Still, the logic inside the Finisher is going to be executed only once.
[00:43] With the help of this Finisher, we can Flush out any remaining data from the mutable state.
[00:49] It is also useful when your buffer elements using a greedy integrator.
[00:54] We're going to discuss about these greedy integrator in a few minutes.
[00:57] Finishers can also be used in the scenarios where the final output depends on the end of the stream
[01:04] logic.
[01:04] When is this Finisher is going to be called ? after the stream is done
[01:08] consuming elements.
[01:09] When I say the stream, the intermediate operation that you are going to develop with the help of Gatherer.
[01:15] Once it process all the elements, then only this finisher logic is going to be executed once per entire
[01:23] stream run.
[01:23] Using finisher, we can emit anything left inside the memory or state that was not yet pushed to the
[01:29] downstream.
[01:30] I know you may have too many questions around the finisher.
[01:33] That's why I'm going to show you an example, which is going to clear all your doubts.
[01:37] The main objective of this program is when I receive an input like 1, 2, 3, 4, 5,
[01:43] 6, 7 inside the output, I want to batch the elements with a size of 3.
[01:48] As you can see here, my output is a list.
[01:51] Inside that list I have inner list as well.
[01:53] The very first list it is having 3 elements by batching the first 3 element values, followed
[01:59] by the next list batches the next 3 elements.
[02:03] Any leftover elements like these 7.
[02:05] We should also push them into the output.
[02:08] This kind of complex requirements can be easily achieved with the help of finisher.
[02:13] Here my requirement is very simple, but think like inside your real application,
[02:17] you're trying to make a rest API invocation for 100 different input elements.
[02:22] Instead of invoking the rest API 100 different times, you can batch the rest API invocations like every
[02:28] 3 elements
[02:29] you can batch them and send as an input to the rest API.
[02:32] Such kind of complex problems can be easily solved with the help of Gatherer API and the finisher that
[02:39] we are going to talk. Here
[02:40] If you see, I'm trying to create a Gatherer with the help of ofSequential() factory method, because
[02:46] I want to process these elements sequentially.
[02:48] If I try to process them parallelly, random threads will try to pick random elements, which is against
[02:55] my business logic.
[02:56] That's why here I should definitely make sure I'm passing ofSequential() as a very first input to this
[03:01] ofSequential(), I'm trying to pass initial mutable state value using a Supplier lambda expression.
[03:08] I'm trying to pass an empty ArrayList as a second input parameter.
[03:12] I'm trying to pass my integrator logic.
[03:15] Inside the integrator logic, the state is being represented with the help of these buffer, followed
[03:21] by the upstream element is going to be represented with the help of this item.
[03:24] And at last I also have downstream.
[03:26] So first whatever item that I'm going to receive from the upstream, I'm going to add to the buffer
[03:31] whenever the buffer size or the Array list size is = 3, I'm going to push my entire buffer
[03:39] with the help of one more Array list to the downstream.
[03:42] Once the pushing is completed, I'm going to clear the buffer, and towards the end I'm trying to return
[03:47] the true so that the next elements from the upstream will be passed to my integrator
[03:52] logic. With this logic, what is going to happen?
[03:55] The pushing of the elements only happen in the batch size of 3.
[03:58] When these 7 element is being processed, it is only going to be added to the buffer since the buffer
[04:04] size is not equal to 3.
[04:06] This pushing logic is not going to execute, followed by we are returning true.
[04:10] And with that, all the elements inside my input are processed with my integrator logic.
[04:16] If I don't have the finisher in my program, the 7 will be left and it will never be pushed into
[04:23] the output .To handle this scenario,
[04:25] as a third parameter to my ofSequential() factory method.I can pass a lambda expression, which is going
[04:32] to accept the state and downstream as an input.
[04:36] Inside my finisher business logic, I'm going to check if the buffer is not empty.
[04:41] If yes, I will simply push the remaining elements inside the buffer to the downstream.
[04:46] Here, with the help of this finisher, I'm trying to flush any leftover elements. Whatever integrator
[04:53] that we have developed here, these kind of integrators, they're going to be called as Greedy Integrator.
[04:59] Let's try to understand why they are called as greedy integrator.
[05:02] A greedy Integrator is an integrator that may consume multiple elements from the upstream before pushing
[05:10] anything to the downstream.
[05:11] They are called so because they greedily pull the elements from the upstream without immediately sending
[05:18] them downstream. Anytime
[05:19] If you build an integrator which is not pushing the elements one by one, instead of pushing the elements
[05:25] one by one, if the integrator is accumulating the elements and try to push them to downstream in a
[05:31] batch,
[05:32] such integrators, we can call them as GreedyIintegrator Greedy Integrators,
[05:36] they are going to allow us to hold on to the elements inside an internal state.
[05:41] Push only to the downstream. When we are ready,
[05:43] like after collecting N items, implement a complex patterns like windowing, batching, delaying the
[05:49] push until a certain condition is met.
[05:51] But when we are using Greedy Integrators, you need to make sure you are manually handling the last
[05:57] remaining elements by using a finisher, as we saw in the previous example.
[06:02] Let's try to implement this logic using a Java program.
[06:07] I created a new Java class with the name E_FinisherGatherer.
[06:11] This is how I'm going to receive the input, and this will be the output that I'm expecting.
[06:16] First, let me create a Gatherer. To this Gatherer,
[06:20] I will mention Integer as a first data type, because from my source I'm going to receive the elements
[06:26] of type Integer. Followed by the data type of my mutable state will be list of integer and to the downstream,
[06:34] since I'm going to push the elements as a list, I need to mention list of Integer as the data type
[06:42] for the downstream.
[06:43] Let me import this list.
[06:45] I will mention the variable name for the gatherer as batch gatherer.
[06:50] Let me first import Gatherer.ofSequential().
[06:56] As a very first parameter
[06:58] I'm trying to pass a brand new ArrayLst, so this will be my supplier.
[07:03] Instead of writing a lambda expression, I can also use the method reference. As a second parameter,
[07:08] I'm going to pass my integrator logic.
[07:11] First, let me mention the state variable name as buffer, followed by item after the item I'm mentioning
[07:19] downstream variable name.
[07:20] Inside this lambda expression, I'll write some business logic.
[07:25] I'm going to paste a few lines of code just to save some time,
[07:27] whatever logic that we have discussed previously, the same I have mentioned here. Maybe we can try
[07:32] to execute this program without finisher and we'll see what is the behavior.
[07:36] Once we saw the bug inside the output, we can try to implement the finisher as well.
[07:41] I'll try to create an stream with the help of stream.of() to the same.
[07:47] I'll try to pass the input by mentioning all these integers.
[07:52] With the help of the stream, I'm going to invoke the Gather and to this Gather I'll pass batchGatherer
[07:59] as an input, and towards the end I'm trying to invoke toList() method.
[08:03] The output I'm going to catch with the help of var result.
[08:07] Let me print the same onto the console with the help of the System.out.println().
[08:12] If I execute this program, I'm going to get this output inside the output.
[08:17] The 7 is completely ignored because we didn't handle that inside our business logic.
[08:22] This bug can be handled by providing a finisher to our gatherer.
[08:27] Let me go to the Gatherer interface.
[08:29] Inside the Gatherer interface we have a method with the name finisher().
[08:33] By default, it is going to have some default logic.
[08:36] If you see the return type from this finisher() should be always a BiConsumer.
[08:41] We should pass two parameters as an input.
[08:44] The first parameter will be your intermediate state, followed by the DownStream object.
[08:50] Let's follow the same syntax and build a finisher for our gatherer.
[08:55] I'm defining a lambda expression for BiConsumer interface.
[09:00] The first parameter will be buffer followed by downstream.
[09:06] Inside the lambda expression business logic, I will check if the buffer is not empty.
[09:12] If yes, please push the remaining elements in the buffer into the downstream,
[09:18] by using this new ArrayList of buffer.
[09:20] Now if I execute this program this time we are going to get the expected output.
[09:25] I'm showing many examples.
[09:27] In all these examples I'm trying to use only gatherer which is a single intermediate operation.
[09:33] With this, don't be under the assumption we can only use a single intermediate operation while using
[09:38] gatherer API.
[09:40] It is perfectly possible to use any number of intermediate operations.
[09:44] For example, here, just before this gatherer, I can define another intermediate operation,
[09:50] with the help of map.
[09:51] To this map, I'll try to provide an lambda expression where I'm accepting the input and multiplying
[09:59] the input with 2.
[10:01] The newly calculated values will be feed to these gatherer intermediate operation. I have written a map
[10:07] intermediate operation which is going to double each of the element, followed by I'm trying to invoke
[10:11] my gatherer intermediate operation. In this scenario,
[10:14] for my gatherer, this map will act as a upstream, and the downstream can be another intermediate operation,
[10:22] or it can be a terminal operation.
[10:23] As of now, we're trying to use a terminal operation, but if required, you can have another intermediate
[10:29] operation which is going to act as a downstream for your gatherer.
[10:33] Let me save this and execute the program,
[10:36] and you can see we received expected output.

----------------------------------------
