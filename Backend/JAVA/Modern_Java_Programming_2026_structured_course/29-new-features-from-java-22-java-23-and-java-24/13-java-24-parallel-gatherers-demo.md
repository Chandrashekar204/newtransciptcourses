# 29.13 — [JAVA 24] Parallel Gatherers - Demo

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] To see the demo of Parallel Gatherers, I have created a class with the name F_ParallelGatherer.
[00:06] Under this main() method
[00:08] first I'm going to create a gatherer, which is going to accept Integer as a first data type, followed
[00:15] by,
[00:15] I can mention ?, conveying that I'm fine with any data type for my mutable state, and
[00:22] at last I'm trying to mention integer again, which is the data type that I'm going to push to my downstream.
[00:28] Let me mention the variable name as parallel Sum.
[00:32] Here I need to invoke the gatherer.of() factory method to this of() factory method
[00:38] as a first input parameter,
[00:40] I'm going to pass my initializer implementation.
[00:44] Let me type AtomicInteger with the method reference new followed by new operator.
[00:51] So this is going to create an mutable state of type AtomicInteger that holds an initial into value
[00:58] zero.
[00:59] After the initializer, I'm going to write my integrator logic.
[01:03] Let me first catch the variables with the name, sum, number and downstream. Inside the business logic
[01:11] of my integrator, I'm going to write a couple of lines where I'm trying to get add and get() method with
[01:18] the help of some, and to this method I'm trying to pass number as an input.
[01:23] We're getting some compilation errors.
[01:24] Don't worry, by the time we develop this gatherer completely, all the errors will get resolved. After
[01:29] the integrator,
[01:30] as a third parameter, we need to provide a combiner component as well.
[01:35] Let's go to Gatherer interface and look for a method combiner().
[01:39] This combiner() abstract method.
[01:41] It is expecting an lambda expression implementation that adhere to the Binary operator.
[01:48] What is BinaryOperator function interface?
[01:50] It is going to accept two input values and return a single output value.
[01:54] The data type of the input and output will be the same .By adhering to this BinaryOperator,
[02:00] let's try to build a lambda expression as a third parameter to the of() factory method.
[02:05] I'll mention the variable names as s1, s2 inside the business logic of lambda expression.
[02:12] I'll simply invoke the same addAndGet() method and return the S1 object.
[02:18] Since these addAndGet() method, it is going to accept int value as an input,
[02:23] we need to make sure we are invoking these get() method by using these S2 AtomicInteger object.
[02:30] Towards the end, I need to define the finisher as well.
[02:34] The finisher is going to receive sum, which is the state as an input, followed by downstream. Inside
[02:41] the lambda expression logic,
[02:42] by using downstream, I'm going to invoke the push() method. To this push() method,
[02:47] I'll try to provide int value available inside the sum object.
[02:52] How to do that?
[02:53] By invoking sum.get() method.
[02:55] Let me mention semicolon towards the end, which is going to resolve all my compilation problems.
[03:01] I have built my parallelSum gatherer as a next step,
[03:04] I need to use the same as an intermediate operation.
[03:07] First, let me create a Stream object with the help of stream.of().
[03:12] To this of(), I'm going to provide some int elements as an input, followed by I'm going to invoke gatherer,
[03:19] to this gatherer I'm going to pass parallelSum variable name,
[03:23] and towards the end I'm going to invoke toList() method.
[03:26] The output I'm going to catch with the variable name as result,
[03:30] and the same I can print onto the console.
[03:34] If I execute this program, we are going to get the output 210. Behind the scenes,
[03:40] all our business logic they are executing parallelly with the multiple threads.
[03:45] I can also show you the proof as well by adding some System.out.println() statements. Inside my integrator
[03:52] logic,
[03:52] just above this line I'm trying to add System.out.printf() statement. Where it is going to print,
[03:58] what is the Thread number right now that is processing the business logic along with the number element
[04:05] that the integrator is processing.
[04:07] In the similar lines, let's try to mention a statement inside the combiner as well.
[04:11] Just above this line, I'll try to add similar line where we are going to print this combiner along
[04:18] with the thread details,
[04:19] we're also going to mention what intermediate state values that my combiner is trying to combine, and
[04:26] towards the end inside my finisher,
[04:28] also, I can have an System.out.printf() statement just to above this downstream.push(),
[04:35] I'll add System.out .printf() statement.
[04:38] Let me execute this program,
[04:40] Inside the output, I'm able to see that my integrator is being processed with the help of a single
[04:47] thread name.
[04:48] Since my program is not executing parallelly, let me check what is the problem.
[04:53] While I'm trying to create my Stream object, I'm trying to create it as a normal stream.
[04:59] But if I want to use parallel capabilities of my stream, I should make sure I'm also invoking the parallel()
[05:07] method that is available inside the stream API.
[05:11] After this parallel, I should invoke my gatherer() method.
[05:15] With the help of this parallel, we are telling to the upstream also to send the elements to multiple
[05:20] threads that my gatherer is going to leverage.
[05:23] After saving these changes and execute this program, this time you'll be able to see multiple threads
[05:28] are running my integrator logic.
[05:31] So these are the thread details.
[05:33] Once all multiple threads executed my integrator logic, the combiner logic also is getting executed
[05:40] multiple times for multiple intermediate state values.
[05:44] And towards the end the finisher logic is getting executed and the output 210,we are able to see
[05:50] on the console.
[05:51] I hope you are clear on how to build a parallel gatherers.
[05:55] Here you may have a question which is, after invoking parallel,
[05:58] If I am trying to pass an intermediate operation that is built with the help of sequential gatherer,
[06:05] what is going to happen?
[06:06] That can be your question.
[06:07] Let's try to understand the same as a first important thumb rule.
[06:11] You should make sure to invoke the parallel() method against your Stream object to process your elements
[06:18] parallelly. Once you invoke the parallel() methods, it's up to you whether you want to provide a sequential
[06:23] gatherer or a parallel gatherer.
[06:25] In case if your gatherer is built with the help of of() method, which is going to provide parallel gatherer
[06:31] in this kind of scenario, your entire stream pipeline is going to be executed fully in parallel, including
[06:39] the gatherer logic.
[06:40] Whereas let's imagine you're trying to provide a sequential gather to one of the parallel stream.
[06:46] In this kind of setup, whatever operations that you have inside your stream pipeline before your sequential
[06:53] gather. They are all going to run in parallel, followed by your gather logic itself,
[06:58] It is going to run in a single thread after the gather Intermit operation all the further operations,
[07:04] they are going to continue again in parallel.
[07:07] Do you see how beautifully this API is designed?
[07:09] Even when we are using sequential gathers, still we can benefit from parallel execution before and
[07:16] after gather operation.
[07:18] This is an unique feature of the Gatherer API.
[07:21] If you try to visualize how this is going to work, let's imagine there is an intermediate operation
[07:27] followed by gatherer operation with the name G2.
[07:31] And towards the end we have another intermediate operation with the name i3.
[07:35] In this kind of setup, the very first intermediate operation, it is going to be processed with the
[07:41] help of multiple threads.
[07:43] Once this i1 is executed, when coming to the gatherer intermediate operation, it is going to be executed
[07:50] as a single thread.
[07:51] Once the gatherer logic is executed again, the intermediate three operation, it is going to be executed
[07:58] parallelly by using multiple threads.
[08:01] This is how it is going to happen behind the scenes.

----------------------------------------
