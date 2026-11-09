# 28.10 — Demo of Thread method join, getPriority, setPriority

> Section 28: MultiThreading in Java

[00:00] The next important thread method that we are going to discuss is join() method.
[00:04] We already saw the demo of this join() method previously, when we were discussing a multithreading example
[00:10] that is capable of adding all the inter numbers.
[00:13] So what is the purpose of the join() method?
[00:15] Using this join() method, we can synchronize the execution of the threads and wait for a specific thread
[00:21] to complete its processing.
[00:23] For example, like you can see here, I have an class with the name JoinExample.
[00:29] And inside this I'm trying to create my own thread by passing the lambda expression to the constructor
[00:35] of the Thread class.
[00:36] So the logic that I have written is,
[00:38] here it is a simple for loop, which is going to iterate five times during each iteration
[00:43] I'm trying to print a statement which is Thread A - Count, and after the count, I'm trying to
[00:49] print the index number and post that
[00:51] I'm trying to make my thread to sleep for half a second.
[00:55] You can see here I'm trying to pass 500 milliseconds as an input to the sleep() method.
[01:00] Now, using this Thread object, I'm trying to start the thread by invoking the start() method.
[01:07] Post the start() method
[01:08] I'm trying to invoke the join() method using the same Thread object.
[01:12] If I don't have this join related logic, what is going to happen is my main() method is never going to
[01:19] wait for this thread to complete its execution.
[01:22] So always we are going to get this as an first output which is Main Thread Ended.
[01:27] Many times you will have scenario where you may want to make your main() method to wait for the other
[01:34] threads to complete their execution.
[01:36] In all those scenarios you can happily use the join() method.
[01:40] I hope this is clear.
[01:41] Moving on to the next set of methods which are setPriority() and getPriority().
[01:46] We know JVM and operating system and CPU cores
[01:51] they are capable of processing multiple threads many times will try to execute our Java program with
[01:57] multiple threads.
[01:58] So if you're trying to feed a multiple threads to your operating system or to your JVM or to the CPU
[02:04] cores, sometimes we may want to tell to the JVM or operating system that I want a specific thread to
[02:12] give some more priority, so that the logic associated to it is going to be executed sooner than expected.
[02:19] So in all such scenarios, we can leverage these priority related methods.
[02:23] By default, each thread that you're going to create, it is going to have the normal priority, which
[02:29] is indicated by the int value five.
[02:32] Like I highlighted here in Java programming language, a thread's priority is represented by an integer
[02:37] within the range of 1 to 10.
[02:39] So one indicates minimum priority and the maximum priority is indicated by ten.
[02:45] So whenever you are using the setPriority() method, we can only pass the int values right from 1 to
[02:52] 10, and by default each thread.
[02:54] When it is going to get created, it is going to have the priority as five, which means it is going
[03:00] to have a normal priority.
[03:01] But here you need to make a very important note, which is think like
[03:06] as a developer, I'm very greedy and I'm trying to mark all my threads as highest priority with the
[03:12] value ten with that operating system or JVM, they are never going to always give priority to my highest
[03:19] priority threads.
[03:19] Only behind the scenes operating system also will do its own due diligence.
[03:24] It will make sure that no thread starvation scenario is happening.
[03:29] So what is a thread starvation scenario?
[03:31] Think like someone is trying to execute a program with the lowest priority threads, and the other developer
[03:36] is trying to execute the program with the highest priority threads.
[03:39] So in this kind of scenario, operating system is not going to give priority only to the highest priority
[03:45] threads.
[03:46] It will make sure even the lowest priority threads, they are getting enough CPU time.
[03:51] Otherwise the lowest priority threads always they are going to keep on waiting and that will result
[03:56] into the thread starvation scenario.
[03:59] That's why don't be under the assumption since you marked your thread as highest priority, it is not
[04:04] guaranteed that the JVM or operating system is going to execute your thread on priority.
[04:09] We can only let JVM or operating system know that my thread has highest priority, and it's up to the
[04:16] operating system or JVM on how to handle it.
[04:20] And in the scenarios where two threads have the same priority, then JVM or operating system, they
[04:26] are going to execute the threads in the Fifo order.
[04:29] So what is Fifo order First In First Out order?
[04:32] So here I have an example to show you the demo of these methods.
[04:36] So first I have created a class with the name PriorityExample that implements Runnable interface.
[04:42] Inside this class I have a constructor that is accepting one parameter as an input, which is the thread
[04:48] name post that you can see.
[04:50] I override the run() method, which has a logic of iterating the for loop five times, and during the
[04:56] each iteration it is going to print a statement, which is.
[04:59] Is what is the name of the thread?
[05:01] What is the current account from the for loop index followed by what is the priority of the thread?
[05:07] So how to get the priority of a given thread?
[05:09] First we need to invoke the current thread, which will give me the object of current thread that is
[05:14] being executed in the background using the same object
[05:17] I need to invoke the getPriority() because this System.out.println().
[05:21] I also have a statement to sleep my thread for 500 milliseconds.
[05:25] Now using this priority example, I'm trying to create a multiple threads.
[05:30] You can see to the Thread() constructor
[05:32] I'm trying to pass the object of PriorityExample.
[05:35] So this should be fine because PriorityExample is an implementation of Runnable interface.
[05:40] Once these three threads are created by default, we know they are going to have a default priority,
[05:45] which is normal priority.
[05:47] But with the help of setPriority(), I'm trying to set various priorities like MIN_PRIORITY, NORMAL_PRIORITY,
[05:53] and MAX_PRIORITY.
[05:55] And after that I'm trying to start all these threads.
[05:58] We will be able to see what is the priority for each thread whenever this for loop is executed.
[06:03] So when we see the demo of this example, it is going to make more sense to you.
[06:07] Let's see the demo of these priority methods and join method very quickly.
[06:11] Inside my intelliJ, I'm going to create a new Java class with the name JoinExample.
[06:17] Inside this JoinExample class.
[06:19] First let me create the main() method followed by
[06:22] I'm going to create a object of Thread with the variable name as thread a.
[06:27] So to the constructor of Thread, I'm going to pass the lambda expression as an input.
[06:32] So let me pass a lambda expression which which is going to accept empty input parameters.
[06:37] Post that a lambda symbol followed by
[06:40] I'm going to write a for loop inside my lambda expression, which is int i = 1, followed
[06:47] by i < 5, followed by i++.
[06:52] So during the each iteration I'm going to print a statement with the help of System.out.println().
[06:58] So the statement is thread a - count : and what is the current index number?
[07:06] With the help of I was that I'll try to invoke the sleep() method to make my Thread to sleep for 500 milliseconds.
[07:14] Since we are invoking the sleep() method, we need to make sure we are handling and checked exception
[07:19] which is interrupted exception.
[07:21] Let me try to surround the sleep related logic with the try and catch like you can see here.
[07:25] Once these object of Thread is created, what I'm going to do is I'll try to invoke the start() method
[07:32] with the help of thread a, followed by.
[07:35] I'll try to print out a statement which is main() thread ended.
[07:41] So first let's see the demo without the help of join() method.
[07:45] So if I execute this program first, you'll be able to see that main thread ended statement and the
[07:51] console followed by
[07:52] for every 500 milliseconds you'll be able to see these statements.
[07:56] So the problem right now I have inside my class is my main thread
[08:01] it is never waiting for the other thread to complete its execution.
[08:05] So how to fix this issue?
[08:06] It's very simple.
[08:07] We just have to invoke the join() method using the Thread object.
[08:12] And this is going to make main thread to wait until the ThreadA object completes its execution.
[08:18] So here also we need to handle the checked exception which is InterruptedException.
[08:22] Let me click on this
[08:23] more actions and surround with the try and catch.
[08:27] So with this we should be good.
[08:28] Now let me execute this program and this time you'll be able to see first my 3D object completed its
[08:34] execution.
[08:35] After that the main thread executed its execution.
[08:39] So this confirms at this point of time which is at the line number 20, the main thread, it is going
[08:46] to wait for the ThreadA object to complete its execution.
[08:49] That's why we are getting this output at the end.
[08:52] I hope you are clear with these JoinExample.
[08:54] Now let me show you the demo of priority related methods.
[08:59] So here first I'm going to create a Java class with the name PriorityExample.
[09:05] Inside this class I'm going to implement the Runnable interface.
[09:10] And with that I need to override the run() abstract method.
[09:14] So let me try to implement these abstract methods.
[09:17] As of now you can see it has empty logic.
[09:19] But before I try to implement some business logic inside the run() method, first let me create a private
[09:26] instance variable of type String with the variable name as name.
[09:31] Post this, I'm going to create the constructor of PriorityExample and to this constructor I'm going
[09:37] to accept an input parameter, which is the name of the Thread.
[09:40] The same I'm going to set into the name instance variable that I have created previously.
[09:46] With the help of this
[09:47] this.name = name.
[09:49] Now to write some business logic inside this run() method, what I can do is, I can try to copy the business
[09:54] logic that I have here.
[09:56] So let me copy these for loop and
[09:59] paste it inside my PriorityExample, run() method.
[10:03] So here I need to make some changes.
[10:06] So first I'll try to print out what is the name of the thread with the help of instance variable name
[10:12] followed by I'll just mention - followed by count.
[10:17] After count I'll just mention colon, and to this count I'll try to add the index value, followed by.
[10:24] I'll try to mention comma followed by priority.
[10:28] And to this priority I can append the output that I'm going to get from the Thread.currentThread().getPriority().
[10:35] .
[10:37] So these are System.out.println() statement that I want to print.
[10:41] And after this I'll try to make my thread to sleep for 500 milliseconds.
[10:46] Now using these PriorityExample class I'm going to create three different thread objects.
[10:51] So to create the same I'm going to create a new Java class with the name ThreadPriorityDemo.
[10:59] Inside this class
[11:00] first I need to create the main() method followed by
[11:03] I'll try to create the object of Thread with the variable name as thread one, and on the right hand
[11:09] side to the constructor of Thread().
[11:11] I'll try to pass the object of PriorityExample, and to this I'll try to pass the name as thread a
[11:18] in the similar lines.
[11:19] Let me create a couple of more threads with the variable name as thread two and thread three, and the
[11:25] thread name as thread b and thread c.
[11:29] Now before I try to start these threads, I want to set different priorities for my threads, like here.
[11:35] I'll try to use a setPriority() method and to the thread one I'll try to mention the lowest priority
[11:42] with the help of MIN_PRIORITY example.
[11:44] So here you can see we only have three different properties like MIN_PRIORITY, NORMAL_PRIORITY and
[11:50] MAX_PRIORITY.
[11:51] But if you are looking for an int value other than one, five and ten, you don't have to worry much.
[11:57] What you can do is you can simply try to add plus one or plus two based upon your business requirements.
[12:03] So with this the thread one, it is going to get the priority as two.
[12:07] But I'm fine with the MIN_PRIORITY.
[12:08] That's why I'm trying to roll back here.
[12:10] Post that in the similar lines, but the other threads I'm going to set other priorities, like for
[12:16] thread two and thread three.
[12:18] I will set the priorities like NORM_PRIORITY and MAX_PRIORITY.
[12:24] And after setting these priorities, let me try to start all my threads with the help of start() method.
[12:30] The same I'll try to do for other threads as well by renaming these variable names to thread two and
[12:36] thread three.
[12:37] So now if I execute this program, you'll be able to see the JVM at the operating system
[12:43] It is not always giving the priority to the thread to see which has highest priority, so it is executing
[12:50] randomly based upon its own business logic.
[12:52] So that's why don't be under the assumption that always the thread with the highest priority is going
[12:58] to be executed.
[12:59] It's just an indication that we can give to the JVM or operating system which your JVM may follow or
[13:06] may not follow.
[13:07] So whenever you run this program, you may not get the same output every time.
[13:11] So this time you can see we are getting 5, 10, 1, 5, 10, 1 .
[13:17] And here 1, 10, 5, 1, 10, 5.
[13:21] But if I try to execute this time, you can see I'm getting a different output like 1, 5, 10,
[13:27] 1, 5, 10.
[13:28] So it's very random.
[13:29] So that's why always don't depend your business logic on this priority related values.
[13:35] We can only let JVM know, but we can't rely on the JVM to follow our orders.
[13:42] With this, I'm assuming your super clear about the join() and priority related methods.
[13:46] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
