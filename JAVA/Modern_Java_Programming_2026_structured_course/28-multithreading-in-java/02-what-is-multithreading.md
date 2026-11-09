# 28.2 — What is MultiThreading

> Section 28: MultiThreading in Java

[00:00] Many times we go for a lunch or dinner to one of our favourite restaurants, and these restaurants might
[00:07] be super busy to serve your food.
[00:10] So when a restaurant is receiving lot many orders from the people.
[00:14] So what is going to happen behind the scenes?
[00:16] Behind the scenes there will be a kitchen with multiple chefs.
[00:20] So all these chefs, they will be working tirelessly to prepare the food and serve the same as soon
[00:26] as possible.
[00:27] So few chefs, they will be focusing on cutting the vegetables to prepare a particular dish, whereas
[00:33] other kind of chefs, they'll be focusing on cooking the food, and similarly few chefs, they'll be
[00:39] focusing on preparing the food for the delivery.
[00:42] So they'll be working on beautifying the product.
[00:45] So if you see there'll be multiple task is going to happen behind the scenes in a busy restaurant.
[00:50] You might be scratching your head, why this fellow right now is talking about the restaurant and a
[00:55] busy kitchen.
[00:56] So there is a very important concept that we are going to discuss throughout this section.
[01:00] Since there is a similarity between this restaurant and the new concept that we are going to discuss.
[01:05] I'm trying to give this example right now.
[01:07] So let me reveal what is our concept that we are going to discuss inside this section.
[01:12] Inside this section we are going to focus on MultiThreading concept.
[01:16] So what is MultiThreading.
[01:18] In simple words the definition of multi threading is refers to the concurrent execution of multiple
[01:25] threads within a Java program.
[01:27] So just like how a restaurant have a situation where multiple chefs they have to prepare the food to
[01:33] deliver the orders on time.
[01:35] Very similarly in Java programs
[01:37] also, sometimes we may have to execute a very complex business logic within a short period of time.
[01:44] For all these kind of scenarios, we can create multiple threads which can work parallelly on multiple
[01:51] tasks.
[01:52] So thread is a lightweight sub process that we can create inside Java to improve the overall efficiency
[01:59] of the program
[02:00] when we are trying to perform multiple tasks simultaneously.
[02:03] So this is the simplest definition that you can give to any person who are trying to understand multithreading.
[02:09] But I know you may have lot many questions how to create the threads, how to run them parallelly.
[02:14] So don't worry, we are going to discuss all these concepts one by one.
[02:18] But for now, let me show you what is going to happen in a normal Java program where we are not using
[02:24] threads or multithreading concept.
[02:26] Since we are into the new section, I have created a Java project with the name section_28.
[02:31] The same,
[02:32] I'm going to check in into the GitHub repo as well.
[02:34] So first let me try to create a package with the name com.eazybytes.multithreading.
[02:41] So this the package,
[02:43] inside these package I want to create a normal Java class which is capable of printing various numbers
[02:51] with a for loop.
[02:52] I can mention the class name as NonThreadDemo.
[02:56] So inside this class I'm not going to use any threads.
[03:00] I'll just try to create a main method post that I'll try to write a for block inside this for block
[03:07] I'll just try to create int i = 0, followed by i <
[03:13] I'll just mention 100, followed by i++ and post that.
[03:17] I'm going to print out each of the indexer element with the help of this System.out.println().
[03:24] I have a mistake inside my for block.
[03:26] Let me remove this comma and put semicolon.
[03:29] With that
[03:30] you can see I have a four block ready.
[03:32] And similarly I'll create one more for block, which is going to print the numbers from 100 to 200.
[03:40] So since I want to print the numbers till 200, I'm trying to mention 201 here because I have a check,
[03:47] which is I less than 201.
[03:48] So if I execute this program, you will be able to see
[03:51] first I'll be having the output from the very first for loop like first, it will try to start printing
[03:58] right from 0 to 99, followed by I have the output from the second for loop.
[04:04] So what is happening with this program?
[04:06] So with this program, the instructions that we have mentioned inside the business logic, they are
[04:12] getting executed sequentially.
[04:14] So first this first block is going to be executed.
[04:17] Once these four block is executed then only the second for block is going to be executed.
[04:23] Similarly, regardless whether your method has 1000 lines of code or 10,000 lines of code, in a normal
[04:29] Java program, always the execution is going to happen sequentially, like one line at a time.
[04:34] So this kind of programming style may work for most of the scenarios, but in some rare scenarios,
[04:41] you may want to write a program that can execute your business logic parallelly with the multiple threads.
[04:48] So to handle these kind of scenarios, we need to implement multithreading inside our Java program.
[04:54] So this is what we are going to learn throughout this section.
[04:57] So as of now our program they are going to be
[05:00] executed only with a single default thread, which is the main thread.
[05:04] I can also show you this main thread for the same
[05:07] we can keep a breakpoint anywhere inside the program, and if you try to debug this program, you'll
[05:12] be able to see inside the debugger.
[05:14] The thread name is main, so if you right click on these and select the option which is Export to threads,
[05:21] you'll be able to see behind the scenes that JVM or Java.
[05:26] It created a single thread for your program with the name main.
[05:30] Using the same thread
[05:31] all your code is being executed. But if needed,
[05:35] like we discussed, Java also supports multithreading program before we try to learn how to build a
[05:40] Java program with multiple threads
[05:42] first we need to understand how these threads they are going to work behind the scenes.
[05:47] So thread is not a concept which is specific to only Java.
[05:50] So thread is a concept which belongs to the operating system.
[05:54] So first we need to understand the surrounding concepts of multithreading, like how the operating system
[06:00] it is going to create the threads, how it is going to leverage threads.
[06:04] So once we are clear about these basic concepts, then we can try to understand how Java is going to
[06:10] help us to create our own threads inside a Java program.
[06:14] I hope you are clear with the agenda of this session.
[06:17] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
