# 29.10 — [JAVA 24] Gatherers with Mutable State & Initializer

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] As a next step, we're going to focus on understanding the purpose of Mutable State inside gatherers
[00:06] API . Some stream operations,
[00:08] they need to remember things between elements processing like running count or previous items.
[00:15] Sometimes we also need to Track accumulations like sum, group size,
[00:20] last item seen. Achieving all these inside traditional streams.
[00:24] This was hard without the collectors.
[00:27] Inside collectors, there are certain options to developers using them all these days,
[00:31] developers.
[00:32] They try to remember the state between elements processing, but with the help of gatherers, we can
[00:37] do this part inside the intermediate step itself.
[00:41] Here you may have a question what's wrong of achieving the same with the help of terminal operation.
[00:46] Why should we learn new option where we can manage with the help of intermediate operation?
[00:51] That's a great question.
[00:52] Let's try to understand the same when we are trying to process something with a terminal operation,
[00:57] as soon as the terminal operation is completed.
[01:01] You're going to get the output. On top of that output if you want to process some more business logic.
[01:06] You need to again create the stream object from the Stream object.
[01:09] You need to again invoke the intermediate operation.
[01:13] Whereas if you able to manage the state within the intermediate operation itself, you can happily invoke
[01:19] the next intermediate operation for the next business logic instead of following the lengthy approach
[01:24] of terminal operation.
[01:26] I hope you are clear with the advantages of intermediate operations.
[01:30] Now let's try to understand how these mutable states can be used inside the gatherers API.
[01:36] Mutable state is a variable that the integrator can use and update across elements,
[01:43] processing.
[01:43] The initial value of this Mutable State can be provided with the help of the Initializer component.
[01:51] Previously, we discussed inside Gatherer interface, we have an Initializer component which is optional
[01:57] in nature. Whenever you need a mutable state inside your gatherer business logic, such a mutable state,
[02:05] initial values can be created with the help of these Initializer component.
[02:09] For example, you can initialize an empty Array list to store largest number seen so far inside a stream.
[02:16] The requirement can be anything, regardless of your requirement.
[02:19] With the help of these Initializer component, you should be able to create the initial value of the
[02:27] mutable state.
[02:28] Once you define the initial mutable state value, you're going to provide the actual intermediate operation
[02:34] business logic with the help of Integrator to the Integrator integrate() method,
[02:39] anyway, we're going to pass the state as the very first parameter.
[02:43] The same mutable state can be used inside the business logic.
[02:47] I have mentioned an example here.
[02:49] The same we are going to build in few minutes.
[02:51] I'll try to discuss this entire code while we are developing the same program.
[02:55] What I'm trying to do with this program is, initially I'm going to get the output as 10,20, 30,
[03:01] 40.
[03:02] Values from my upstream.
[03:04] By the end, my stream pipeline processed the data I want the,
[03:08] output in this format.
[03:09] If you see every element in the output, it is going to be,
[03:12] calculated by summing with the previous element value. For 10,
[03:17] since there is no,
[03:17] previous element, we are going to have ten itself, whereas for 20 we are going to add this 20,
[03:23] With the previous element which is 10.
[03:25] And with that we are going to have 30.
[03:27] Whereas for the third element for this 30, we are going to add to this 30, which will make the third
[03:33] element as 60.
[03:34] Coming to the last element for this 40, we are going to append the 60, which will make,
[03:39] the fourth element as 100.
[03:41] If you see this logic requires remembering the,
[03:44] previously calculated value.
[03:46] I can easily achieve this with the help of these,
[03:49] Mutable state. I mentioned a table as well on how this is going to work.
[03:54] So these are my source element.
[03:55] .
[03:55] These are the elements that my gatherer intermediate operation is going to push to the downstream.
[04:01] So initially, with the help of initializer I will set the mutable state value as 0.
[04:07] When my intermediate operation is processing the very first element, it will append these zero with
[04:12] 10 and the 10 will be the new state value.
[04:15] The same state 10 value will be used during the second element processing.
[04:21] When the element 20 is being processed, the state before will be 10.
[04:25] If you sum both of them, the output will be 30.
[04:28] The new value will be stored inside the previous state.
[04:31] Along with that, we are also going to push the same to the output.
[04:34] So this way each of the elements they are going to be processed inside my intermediate operation.
[04:39] If you closely look at this program this time, instead of invoking the of() method, I'm trying to invoke
[04:45] the ofSequential() factory method.
[04:48] There is a reason why I'm trying to do this.
[04:50] If I simply use the of() factory method of gatherer, all my elements are going to be processed parallelly,
[04:56] but right now I don't want them to be processed to parallelly because if I process them with multiple
[05:02] threads, all those multiple threads, they are going to get the initial state value as 0.
[05:07] With these 0, they are going to perform the calculations.
[05:11] And with that, I'm not going to get the expected output.
[05:14] In this kind of scenario, processing the elements parallelly is not possible because the business logic
[05:20] will be correct only if I process these elements sequentially.
[05:24] If I try to process them randomly parallelly, I'm not going to get the expected output.
[05:29] Whenever you are looking to execute your intricate operation sequentially.
[05:34] Under such scenarios, you need to use the ofSequential() method.
[05:39] Since a single thread is going to process all these elements one by one, the mutable state value will
[05:45] be shared to the same single thread, and it can happily execute our business logic and prepare this
[05:50] output.
[05:50] In case if there are some scenarios where you want to process the elements parallelly.
[05:55] By using of() method, you can also pass the state variable as well.
[05:59] But when you are trying to process the elements parallelly by providing a mutable state under such scenarios,
[06:05] you should also take care of providing a combiner component which is going to match the output from
[06:11] all the multiple threads into a single value.
[06:13] We are going to discuss about this combiner and how to use mutable state while processing the elements
[06:19] parallelly in the upcoming parts.
[06:20] For now, let's try to focus on understanding on how to process the elements sequentially by using a
[06:26] mutable state with the help of these ofSequential() method.
[06:30] Let's try to build this program so that we will be clear with the demo as well.
[06:35] I created a new Java class with the name D_ MutableStateGatherer.
[06:40] Let me type Gatherer.ofSequential().
[06:44] There are multiple overloaded methods ofSequential().
[06:48] I want to invoke the method which is going to accept an initializer, followed by the Integrator logic.
[06:54] If I open this ofSequential(), there is a overloaded method which is accepting a Supplier and Integrator.
[07:00] Let me click on the same this ofsequential(),
[07:03] it is accepting a Supplier as an first parameter with the help of the supplier only,
[07:09] we are going to supply initial mutable state value.
[07:13] If you try to understand the initializer() method, it is also returning a value with the help of Supplier
[07:19] functional interface.
[07:21] The same is getting used inside the ofSequential() as well.
[07:25] What is the purpose of Supplier functional interface?
[07:27] Without taking any input as an input, it is always going to supply a value or a producer value.
[07:32] When we are invoking these ofSequential() method, we need to pass a lambda expression, which is going
[07:37] to supply a value that is going to act as an initial mutable state value. Followed by,
[07:43] we need to pass the integrator logic. For this ofSequential() method.
[07:48] As a very first input value, I'll provide a lambda expression which is going to return initial mutable
[07:54] state value.
[07:55] Let me type AtomicInteger with the method reference syntax followed by new.
[08:01] With the help of these method reference or the lambda expression, I'm trying to create an AtomicInteger
[08:07] value, which is going to hold 0 as the initial value.
[08:10] If you go to the constructor, it is going to create a new AtomicInteger with the initial value as
[08:16] 0.
[08:16] The same highlighted here as well.
[08:18] Here you may have question why I'm trying to create an int value with the help of this AtomicInteger.
[08:23] Why I'm not using normal Integer.
[08:26] The reason is Integer is an immutable class.
[08:30] Whenever you want to change a value inside this Integer object, a new immutable object is going to
[08:36] be created, which is going to create some issues inside our business logic.
[08:41] We want to maintain a state variable that can be mutated inside our business logic, since Integer objects
[08:47] cannot be muted.
[08:49] I'm trying to use AtomicInteger.
[08:51] The data inside the AtomicInteger can be changed because it is a mutable object.
[08:56] Once we supply an initial value for our mutable state value, we need to pass the integrator lambda
[09:03] expression as well.
[09:04] The integrate,
[09:05] It is going to accept the state as a very first parameter, followed by element.
[09:11] After the element we are going to have downstream.
[09:14] Let me bring this to the next line.
[09:16] As part of this lambda expression, I'm going to write some business logic to achieve this output.
[09:21] Maybe here instead of element, I'll name this variable as number, which I'm going to receive from
[09:27] the upstream. To calculate the output,
[09:29] every time I need to add the state and number that I'm receiving.
[09:33] So the state is an AtomicInteger with the help of the same AtomicInteger object, I need to invoke
[09:39] a method add() And get() this method
[09:43] it is going to accept an int as an input.
[09:46] The same I'm trying to pass by using the number and this method, it is going to return a new int value.
[09:53] Along with that, the newly calculated int value will also be stored inside the state object.
[09:59] Let me catch the newly calculated into value with the variable name as updated the same updated I need
[10:07] to push to the downstream.
[10:08] Let me type return downstream.push(updated) whatever boolean value that my push is going to return.
[10:16] the same,
[10:16] I'm trying to return from my integrator as well.
[10:19] Here we are getting a compilation error because we have not defined the input data types for our Gatherer.
[10:26] Let me catch the output with a Gatherer and I'll mention the upstream element data type as Integer followed
[10:34] by ? for the mutable state and the last parameter.
[10:38] also, I'm going to define as Integer because we are trying to push the int values to the downstream
[10:43] as well.
[10:44] Let me mention the variable name as cumulative sum.
[10:47] And with this the error that we have is resolved if required.
[10:51] Instead of mentioning this wild card for the mutable state, we can also mention AtomicInteger which
[10:57] is matching with the Supplier return type.
[11:00] So now I have the Gatherer ready.
[11:02] I can use this while building my stream pipeline.
[11:05] First, with the help of Stream.of(), I'm going to provide all my integer values like 10, 20,
[11:12] 30 and 40, followed by,
[11:14] We need to invoke the gather and to this gather we can pass cumulative sum, and towards the end we
[11:22] can invoke the terminal operation or some other intermediate operation as well.
[11:27] Here I will try to invoke two list and the output I'm going to catch with the variable name as result.
[11:35] Let me print the output onto the console with the help of System.out.println().
[11:40] Let's hope for a valid output.
[11:42] I'm trying to execute my program.
[11:44] Hooray!
[11:45] We got an expected output, which is 10, 30, 60 and 100.
[11:51] I hope you're clear on how to use mutable state value inside your gatherer intermediate operation.
[11:58] Always
[11:59] you need to make sure to provide the initial value of the state with the help of the Supplier, followed
[12:04] by,
[12:04] You can provide your Integrator logic. In the upcoming parts,
[12:08] we are going to discuss on how to use the mutable state when we are trying to process the elements.
[12:13] Parallelly, with the help of the of() factory method for these business logic, if you try to use
[12:18] of, you're going to get compilation errors because the gatherer it is expecting you to provide a combiner
[12:25] component as well. Which is going to combine all the output from the multiple threads.
[12:30] But right now, since we have not defined the combiner component inside our gatherer, we are getting
[12:35] this compilation error.
[12:36] Let me roll back to the ofSequential().
[12:39] Please make sure to execute this program in your local as well, so that this concept will be clear
[12:44] for you.

----------------------------------------
