# 28.6 — Creating Threads in Java - Part 1

> Section 28: MultiThreading in Java

[00:00] Finally, we are going to make our hands dirty by building some Java programs with the help of threads
[00:07] inside Java.
[00:08] To get started around threads inside Java, first let me create a Java class with the name ThreadDemo.
[00:14] Creating a thread inside Java is very easy.
[00:18] First, I'll show you the most basic approach post that we'll try to discuss
[00:23] what are the various options we have inside Java to create a Java thread.
[00:28] So here inside my class I'm trying to create a main() method followed by with the help of Thread class
[00:35] which is available inside the java.lang package.
[00:39] I'm going to create an object with the variable name as thread itself.
[00:45] So to this thread constructor you can see I'm not passing anything as an input.
[00:49] That means I'm trying to invoke the default empty constructor of Thread class.
[00:55] So with this a basic Thread is going to be created behind the scenes.
[01:00] So this is the most simple way of creating the Thread inside Java.
[01:04] It is as simple as creating an object of any class.
[01:08] So once the thread is created as a next step, you may want to run your thread so that it will enter
[01:15] into the race of getting the CPU time from the operating system.
[01:19] So whenever we are trying to create an object of thread behind the scenes, JVM is going to taking the
[01:25] responsibility of creating these Thread objects inside the heap memory post that the JVM is going to
[01:31] request the operating system to schedule this thread to get a CPU time, so that it is going to execute
[01:39] some instructions.
[01:40] So by default, JVM is not going to interact with the operating system, and it is not going to request
[01:47] operating system to schedule the given Thread object.
[01:50] It is going to do this job only when we invoke the start() method available inside the Thread object.
[01:57] So with the help of this Thread object, I'm trying to invoke the start() method.
[02:01] So if you try to see the documentation of this start() method, once the start method is going to invoked,
[02:07] it is going to schedules this thread to begin execution.
[02:11] The thread will execute independently of the current thread.
[02:15] A thread can be started at most once.
[02:17] That means once a thread is started, we can't invoke the start one more time.
[02:22] We are going to get a runtime exception.
[02:24] I'm also going to show you the demo around this in few seconds, but if you see here what is going to
[02:28] happen with this thread()
[02:29] is behind the scenes
[02:31] JVM is going to request the operating system to schedule this Thread object to begin the execution,
[02:38] and there is also a statement saying that the thread will execute independently of the current thread.
[02:43] This means though, we are trying to create the Thread object inside another thread which is main thread.
[02:50] Still, this Thread object is going to execute its business logic independently.
[02:56] So that's the meaning of the statement that we have here.
[02:59] Now let me try to execute this program and see what is going to happen.
[03:03] You can see I'm getting an runtime exception which is IllegalThreadStateException because I'm trying
[03:10] to start the thread couple of times, which is not correct.
[03:14] We can only start a given thread only once in its lifetime.
[03:18] So that's why
[03:19] let me remove this line of code post that if I try to execute this program, you can see nothing is
[03:25] happening.
[03:25] I didn't get anything on the output and also the program is terminated without showing me any output.
[03:32] The reason is, I created a thread, but I didn't tell to my thread what logic it has to execute.
[03:39] So whenever we are trying to create a Thread object with the default constructor, we are telling that
[03:45] I don't have any business logic to execute anything as part of my thread.
[03:50] I'm just trying to have some fun and I'm just trying to create the thread for some fun sake.
[03:55] That's what is going to happen right now here.
[03:58] But on the serious note, whenever we want to create a Thread object, we should tell what logic it
[04:02] has to execute whenever the thread is going to start executing its instructions when it gets the CPU
[04:09] time.
[04:10] So if you try to look inside the same class, you can see there is another constructor which is accepting
[04:16] a Runnable object.
[04:17] So what is this
[04:18] Runnable?
[04:19] Runnable is a functional interface.
[04:22] That means we can pass a lambda expression adhering to these abstract method.
[04:27] So this abstract method, it is not accepting any input parameter.
[04:31] And it is also not returning anything as an output.
[04:34] So let me try to send a lambda expression as an input to the Thread constructor.
[04:40] So what I can do here is, I can start one more thread, but this time I will name this object as
[04:47] thread1.
[04:48] And to the constructor I'm trying to pass the lambda expression with the empty parentheses followed
[04:54] by lambda symbol and post that
[04:56] I'll try to have a System.out.println() with
[04:59] the statement saying that hello from Java Thread.
[05:04] So this is a simple logic that I want my thread to be executed.
[05:08] So right now things may look very simple to you, but don't worry, I'll show you some good examples
[05:13] in the coming lectures, which is going to show you the benefit of threads and multithreading.
[05:19] Till that time, please hold your thought and let's learn these basics.
[05:23] So here I need to replace this thread with thread1.
[05:26] Let me create one more thread as well.
[05:28] This time I'll just mention thread2 as an variable name and the same I'll try to mention here.
[05:34] We can also pass the lambda expression as an Runnable object.
[05:39] So here I'm trying to pass the lambda expression directly to the constructor, which sometimes may look
[05:46] clumsy.
[05:46] So what I'm going to do is, I'll try to create an object of Runnable with the variable name as runnable.
[05:52] And to this I can assign the lambda expression.
[05:55] So here I'll say hi from Java thread.
[05:58] So this Runnable object I can try to pass as an input to the Thread() constructor.
[06:03] So now this time if I try to execute this program, you can see from the very first thread we are not
[06:09] getting any output because we are invoking the default constructor.
[06:12] But from the second thread we are getting hello from Java world and from the third thread we are getting
[06:18] hi from Java thread.
[06:19] I hope you are clear with these example.
[06:22] Let me show you a demo which confirms that these threads they are going to execute independent to these
[06:29] main() thread.
[06:30] So what I'm going to do is, I'm going to mention a System.out.println().
[06:34] Towards the end of my main() method, I'll just mention a statement which is hello from Main Thread.
[06:41] So the main() method is going to run inside a main() thread
[06:44] inside this main() thread we are trying to create three more threads which has various business logic.
[06:50] You're going to be surprised this time when I execute this program and show you the output.
[06:55] Let me surprise you
[06:56] first post that I'll try to explain what is happening.
[06:59] So if I execute this program, you can see I'm getting the hello from the main() method before hi from
[07:07] Java thread, but this should come at the end, right?
[07:10] Then why it is coming in between.
[07:12] So let me execute one more time.
[07:14] So this time also I'm getting somewhere in the middle only if I try to execute the program any number
[07:19] of times
[07:20] always it is coming in between the reason why I'm getting these hello from main thread before this output
[07:27] is like we saw inside the documentation of the start() method.
[07:31] The start() method is going to schedule the thread to begin its execution independent of the current thread,
[07:38] which is the main() method.
[07:39] By considering this statement, let's try to understand what is happening here.
[07:43] So whenever we invoke the start() method of the thread my JVM, it is not going to wait for the thread
[07:50] to complete its execution or complete its business logic.
[07:55] It will only invoke the start() method and let JVM know to schedule this thread and the outer thread.
[08:01] It is never going to wait for the inner threads to complete their business logic.
[08:06] And with that, what did we achieved?
[08:08] We achieved parallel execution or concurrent execution.
[08:12] We are no more in the sequential execution.
[08:14] If we are in the sequential execution, we should get first this output followed by this output, followed
[08:20] by this output
[08:21] But that is not happening.
[08:22] First we are getting this output which is from the thread1, followed by
[08:26] we are getting this last statement as an output and at last we are getting the output from this thread2.
[08:31] You may also ask me a question here.
[08:34] If the main() thread is not waiting for the other threads to complete their business logic, then these
[08:40] statements should come at the very first, right
[08:42] then why
[08:42] I'm getting this statement as a very first statement inside my output.
[08:46] So that's what you can see here.
[08:48] So that's a very good question.
[08:50] Usually whenever we invoke the start() method behind the scenes, it is going to take a fraction of second
[08:56] to communicate with the JVM about the scheduling of this thread.
[09:00] So when this start() method is invoked, think like my JVM is working with operating system to schedule
[09:06] a CPU.
[09:07] Time for this thread.
[09:08] So this thread it is going to keep on waiting till it gets the CPU time.
[09:13] Meanwhile, we are executing this line of code and here also we are invoking the start() method and JVM
[09:21] is trying to communicate with the OS to schedule this thread as well.
[09:24] So whatever fraction of seconds of time that JVM is taking at this point of time to schedule this thread
[09:30] onto the OS in that fraction of seconds
[09:34] this thread, which is the thread1, it got some CPU time.
[09:37] That's why it's completed its execution.
[09:40] And after that we are seeing the output from the last statement.
[09:43] The reason is the start() method is only going to schedule the thread onto the operating system, but
[09:49] it is never going to wait the actual logic to get completed.
[09:52] That's why here this thread is completed and at last this thread also got some time on the CPU and it
[09:59] also completed its output.
[10:01] That's why we are seeing this kind of output.
[10:03] So there are some mechanisms inside trading concept to make the main thread to wait for the other threads
[10:10] to complete their execution.
[10:12] I'm going to show you that in the coming lectures.
[10:15] For now, I want to address one more question that you may have, which is, we are trying to pass the
[10:20] lambda expression as an input to the Thread() constructor.
[10:23] So inside the Runnable function interface we have a method which is run(), but nowhere we are invoking
[10:29] the run() method, we are simply invoking the start() method.
[10:32] So then who is invoking the run() method?
[10:35] Can I execute directly the run() method?
[10:37] Let's see what is going to happen.
[10:39] If I try to execute the run() method directly, I'm going to get the output as a normal Java code.
[10:46] My code is not going to execute on the threads.
[10:49] So you can see I'm getting the sequential output, which is
[10:52] Hello from the Java thread, hi from the Java thread and hello from main() method.
[10:56] That means whenever you try to directly invoke the run() method, you're going to lose the benefits that
[11:02] multi-threading is going to provide.
[11:04] The reason is, if you directly invoke the run() method, that means you're trying to execute your business
[11:09] logic yourself with the help of main() thread in a sequential manner.
[11:14] So to get the benefits of multi-threading and to make sure that your Thread object is going to be executed
[11:21] independently, we should always invoke the start() method.
[11:25] So what start() method is going to do behind the scenes is it is going to work with the JVM to schedule
[11:31] this thread as a separate thread inside operating system, and whenever this thread receives the CPU
[11:36] time, it is going to execute its own business logic.
[11:39] So once the CPU time is received by my thread internally, it is going to invoke the run() method.
[11:47] That's why we should never try to manually invoke the run() method, always invoke the start() method.
[11:52] I hope this makes sense to you.
[11:54] We need to discuss a lot about threads, but with whatever basic discussion that we have done inside
[11:59] this lecture, I'm assuming you are clear.
[12:01] I also mentioned all the points that we have discussed inside this slide
[12:05] for your reference.
[12:06] I'm also trying to provide a flow chart.
[12:08] What is going to happen if you try to create an object with the default constructor of Thread() ?
[12:13] So if you try to create an object of default thread first, the Thread object is going to be created
[12:18] inside the heap memory post that when you invoke the start() method, a thread gets created and scheduled
[12:25] for execution to get the CPU time.
[12:27] So once the thread receives CPU time, it is going to invoke the run() method of the given thread.
[12:33] Since with the default constructor we are not providing any business logic, it is going to simply terminate
[12:38] itself immediately
[12:40] that's why thread is going to dead.
[12:41] Whereas in the scenario where we are trying to provide our own business logic with the help of a lambda
[12:46] expression, in such scenario, before the thread is going to dead, it is going to execute the business
[12:52] logic defined as part of the run method or as part of that lambda expression.
[12:56] I hope this flowchart helpful.
[12:58] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
