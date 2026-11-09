# 28.9 — Demo of Thread methods getId, threadId, getName, setName, currentThread, sleep

> Section 28: MultiThreading in Java

[00:00] The example that we have discussed in the previous lecture, I have mentioned inside this slide for
[00:06] your reference.
[00:07] As a next step, we are going to discuss all the important methods supported by the Thread class.
[00:14] There are more than 50 different methods supported by Thread class.
[00:18] I'm not going to discuss all of them, but I'll try to discuss most commonly used methods inside this
[00:24] lecture.
[00:24] Let's try to focus on few methods later on in the coming lectures, we can try to focus on other methods.
[00:31] The very first set of methods that I want to discuss are getId(), getName(), and the setName().
[00:38] So whenever you try to create a Thread object and whenever you're trying to start your Thread object
[00:44] behind the scenes JVM, it is going to assign a ID and a name to your Thread.
[00:50] If needed
[00:50] you can define your own name to your thread with the help of these setName() method.
[00:56] But we can't set our own ID.
[00:58] That's why there is no setId() method available inside the Thread class.
[01:03] To understand what is our thread id and the thread name, we can use this get id and getName().
[01:10] All these are instance methods.
[01:12] We should be able to invoke them with the help of the Thread objects.
[01:17] So you can see I have provided an example as well for your reference.
[01:21] I'm going to show you a demo around these in few seconds as well.
[01:24] So I'm trying to create various threads by invoking the default constructor of Thread().
[01:29] And with that, we're not going to execute any business logic later on.
[01:33] For the third thread, I'm trying to set my own name with the help of this setName() method, and after
[01:39] that, I'm trying to get all the ID details of the threads and their names with the help of getId() and
[01:46] getName() and the same I'm trying to print out onto the console.
[01:49] So this is how my output is going to look like.
[01:52] So you're going to get some random thread ID values and some random ID names.
[01:58] But for the third thread I'm going to get my thread as the name because I intentionally overrated that
[02:05] thread name with the help of setName() method.
[02:08] I hope you're clear about this method.
[02:10] Let's see what is the next method.
[02:12] Sometimes when your program is running multiple threads, you want to understand at a specific point
[02:18] of time what is the current thread is getting executed.
[02:21] It can be a thread one, or it can be thread two, or it can be a main thread.
[02:25] So to get some clarity which thread is executing at a specific point of time, you can invoke a static
[02:32] method which is current thread with the help of Thread class.
[02:36] So this method is going to return the object of Thread, which is referred to the current thread that
[02:42] is being executed.
[02:43] And using this current thread, you can try to understand more details about your current thread by
[02:48] invoking what is the ID,
[02:49] what is the name?
[02:51] So this method especially it is very useful if your program is dealing with a lot many threads.
[02:56] And if you want to understand which specific thread is causing a bug, I hope you're clear about this
[03:02] method.
[03:02] Now let's go to the next method.
[03:05] The next method is sleep() method, like the name itself is self-explanatory.
[03:10] So with the help of this method, we can make a thread to sleep for a certain amount of time.
[03:16] Sometimes a thread may have to wait to the other thread to complete its business logic.
[03:22] In all such scenarios, we can make a particular thread to sleep for one second or 2 seconds or 5 seconds
[03:29] based upon our business requirements.
[03:31] So to this sleep() method, we need to pass the time in milliseconds.
[03:36] So you can see here during each iteration of my for loop, I'm making my current thread to sleep for
[03:43] 1000 milliseconds, which is one second.
[03:46] So here what is a thread that is going to be executed?
[03:49] It is going to be the main() thread.
[03:51] I'm not creating any of my own custom threads, so that's why when we execute these program, the main
[03:58] thread is going to sleep for one second during each iteration.
[04:03] Let's see the demo of all these methods that we have discussed so far.
[04:07] Here I'm going to create a new Java class with the name ThreadIdNameDemo.
[04:15] Inside this I'm going to create a main() method followed by
[04:17] I'm going to create good amount of threads with the help of default constructor.
[04:23] I just don't want to write any business logic for now.
[04:26] Just to keep things simple. Post that I'm going to rename this variable names to t2 and t3.
[04:32] Once I created these objects, let me try to invoke the setName() method by using one of the Thread object.
[04:39] If you try to open this method, you will be able to see the documentation saying that changes the name
[04:45] of this thread to be equal to the argument name.
[04:48] So let's mention the name of this thread as MyThread.
[04:53] So let me make this t as capital followed by.
[04:57] I'll try to print out the ID details and the name
[05:00] details of all the threads.
[05:01] So here I'll just mention the String as thread one ID is followed by colon followed by space.
[05:10] After this I'll just mention plus
[05:12] now using t1, I'll try to invoke that getId() method.
[05:16] Let's see the documentation of this method by invoking these get id if you see here this method is deprecated
[05:23] since the Java 19.
[05:25] They're saying
[05:26] the reason is this method is not final and may be overridden to return a value that is not the thread
[05:32] id.
[05:32] Instead, use the threadId() method.
[05:35] So this is an important note about this method.
[05:37] This method is deprecated from Java 19.
[05:40] That's why I don't use this method.
[05:42] Instead, use the thread id.
[05:43] I'll try to use the thread id method for other threads.
[05:46] For now, let's use this getId() only. Followed by,
[05:49] I'm going to mention String with a comma followed by name : place
[05:56] and at last I'll try to invoke that t.getName() method.
[06:01] So now let me try to repeat these statements a couple of times.
[06:05] And here I'll try to change this to thread two and thread three.
[06:10] Now this time instead of getId() I'll try to invoke the threadId() method. Post that I'll rename this variable
[06:17] name to t2, and here also I'll rename to t2.
[06:21] And here I'll try to rename this to t3.
[06:24] Similarly I'll just mention t3.
[06:26] So let me copy this threadId() to here as well.
[06:29] So if I execute this program you'll be able to see the ID details like 23, 24, 25.
[06:36] And the name of the first thread is thread zero.
[06:39] This is a random name assigned by my JVM and similarly thread one.
[06:43] For the last thread you can see the name is whatever I have provided to the setName() method.
[06:49] I hope you are clear about this demo.
[06:50] Instead of this getId() the recommendation is to use the threadId().
[06:54] I will also try to update the slides about this information, but your reference.
[06:59] Now as a next step, let's see the demo of current thread method demo.
[07:03] For the same, I'm going to create a Java class which is CurrentThreadDemo.
[07:08] Inside this class I'm going to create the main() method post that I'll right away try to invoke the current
[07:16] CurrentThread static class. Post that I'll try to invoke this documentation
[07:21] this documentation says returns the Thread object for the current thread.
[07:25] So let me go to the CurrentThreadDemo.
[07:27] As of now you can see I'm not creating any threads.
[07:29] The main thread only is present inside my program, so I should get the object related to the main Thread
[07:36] only.
[07:37] So let me catch the output on the left hand side with the variable name as main thread.
[07:42] Post that I'll try to print out main thread id with the help of thread id followed by
[07:49] I'll try to invoke other method which is getName() method.
[07:54] So if I execute this program you'll be able to see the thread id is one and the thread name is main.
[08:00] So this confirms the currentThread() method always going to give you the CurrentThread object reference.
[08:06] So using this object you should be able to invoke any other method supported by the Thread object.
[08:12] As a last step, let's see the demo of sleep().
[08:15] So here I'm going to create a Java class with the name SleepDemo.
[08:21] So first what I'm going to do is, I'll try to invoke the System.currentTimeMillis() to understand
[08:27] what is the start time of this program.
[08:30] Similarly, I'll try to invoke currentTimeMillis() one more time to get the end time.
[08:36] And in between these two statements, I'm going to write a for loop, which is going to iterate five
[08:43] times.
[08:44] So let me write int I is equal to zero, i < 5, followed by i++.
[08:52] And inside the for loop I'm going to print out a statement which is hello from main() method.
[08:59] And to this statement I'll just try to append the index value.
[09:03] So if I execute this program, I should be able to get the output very quickly.
[09:08] We can also confirm the same by printing the total time with the statement, which is total time taken
[09:16] colon.
[09:17] And to this I'll try to send the output that I'm going to get from the subtraction of
[09:25] endTime - startTime.
[09:26] So if I execute this program, you'll be able to see the output.
[09:29] And you can see the program is executed within four milliseconds.
[09:33] So that's super fast.
[09:34] So now let me show you the power off sleep() method.
[09:37] So inside my for loop during each iteration I'll try to make my thread to sleep for 1000 milliseconds,
[09:45] which is like one second.
[09:47] So whenever we are invoking these method, we need to handle and check it exception which is
[09:53] InterruptedException.
[09:53] So let me add this to the method signature to resolve this error.
[09:57] So this time if I execute this you'll
[10:00] be able to see the output I'm going to get after five seconds.
[10:04] And in fact, you also saw that each statement is getting displayed after a pass of one second.
[10:10] You can also see the total time taken is 5033 milliseconds.
[10:15] So this because we're trying to sleep the thread for 1000 milliseconds during each iteration.
[10:22] So whenever you have a requirement to make a thread to sleep for a certain amount of time, you can
[10:27] happily use the sleep method in multi-threading environment.
[10:30] Making a method to sleep is most common because when you're dealing with the multiple threads, you
[10:36] may get some scenarios where you want to make a particular thread to sleep for some time, so that in
[10:42] the meantime, the other thread can complete its execution and the output from the other thread you
[10:47] can take as an input to the current sleeping thread after specified time.
[10:52] I hope you are clear with all the three methods that we have discussed so far.
[10:56] Let's explore more methods in the next lecture as well.
[11:00] Thank you,
[11:00] bye.

----------------------------------------
