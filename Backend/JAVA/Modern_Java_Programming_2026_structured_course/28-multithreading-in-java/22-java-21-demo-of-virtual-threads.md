# 28.22 — [JAVA 21] Demo of Virtual Threads

> Section 28: MultiThreading in Java

[00:00] Inside this lecture
[00:01] let's see the demo of virtual thread for the same
[00:03] I'm trying to create a Java class with the name VirtualThreadDemo. Inside this class,
[00:10] first let me create the main() method, followed by
[00:13] I'm going to create a Runnable object with the help of a lambda expression, so that the same Runnable
[00:19] object I can try to pass as an input to the threads that I'm going to create.
[00:23] First, let me create the object of Random class because I want to generate some random values, was
[00:30] that I'll try to create the object of Runnable with the variable name as runnable, and to this I'll
[00:36] try to assign a lambda expression, which is not going to accept any input parameter.
[00:41] And inside the body of lambda expression, I'm going to write a business logic, which is to generate
[00:48] two different double values and multiply them.
[00:51] And once the multiplication is completed, I want to assign the result to some other double variable.
[00:57] So let me first create a double variable with with the name as result.
[01:02] Now on the right hand side, with the help of random object, I'll be invoking the nextDouble() method.
[01:10] To this nextDouble() method
[01:12] I'm trying to pass a bound value which is 1000.
[01:15] That means any random double number that is going to be generated.
[01:18] It is going to be within the range of 1000.
[01:22] In the similar lines, I also want to generate one more double value and both these double values.
[01:29] I'm trying to multiply with the help of these asterisk symbol.
[01:32] So the result I'll try to store inside these result variable.
[01:36] And for that I'll try to print out the same onto the console.
[01:40] So these are simple Runnable object that I have created.
[01:43] Now I'll try to create a for loop and inside these for loop
[01:47] during each loop iteration I'm going to create a Thread.
[01:51] So first let me mention int i = 0 followed by i < 500000.
[02:00] So here I'm trying to mention five zeros followed by i++.
[02:05] First let me try to create a normal threads with the help of our old approach which is Thread class.
[02:12] So using Thread class I'm trying to create a normal thread and to the constructor of thread I'll try
[02:17] to pass the object Runnable. Post that
[02:20] I'll try to start the thread with the help of start() method.
[02:23] For this, I'm trying to invoke the join() method.
[02:27] As soon as I'm trying to invoke the join() method, I'm getting an error to handle the checked exception.
[02:32] So to fix the error, I added these throws InterruptedException to the main() method.
[02:37] So basically what I'm trying to do here is, I'm trying to create five lakh different normal platform
[02:44] or native threads.
[02:45] That means this logic that I have written, it is going to be executed five lakhs different times and
[02:52] in the same process.
[02:52] Whenever the for loop is iterating, every time the platform thread is going to be created, it's going
[02:58] to be assigned to a kernel thread.
[03:00] And once the execution is completed, the platform thread is going to be destroyed.
[03:04] So there is a lot of heavy operations is going to happen.
[03:07] We are going to check how much time a normal thread is going to take to execute this entire Java program.
[03:13] Post that
[03:14] I'll also migrate these program to use the virtual threads.
[03:18] Once we migrated to the virtual threads, we can also see how much time virtual threads they are taking.
[03:23] But here you may have question which is, Madan you said, each normal platform or native thread it
[03:30] is required some 10MB or 1MB of Ram memory and you're trying to create five lakhs different threads.
[03:37] Don't you think we are going to get a memory related error?
[03:40] That's a great question
[03:42] if you see here I'm not trying to create all these five lakh threads at the same time.
[03:46] So during each iteration we are creating the thread, we are starting the thread and we are waiting
[03:52] for this thread to complete its execution.
[03:54] Then only the next iteration will happen.
[03:57] So if you try to execute this program without this joint statement, definitely you will get at some
[04:02] point of time memory related problem inside the console.
[04:06] Because platform threads are native threads, they are going to require a lot of memory.
[04:10] I hope you're clear.
[04:11] Let me try to add some time related logic.
[04:14] So first I'll try to create a variable which is startTime.
[04:18] And to this startTime I can try to assign the output that I'm getting from the method current time
[04:24] milliseconds.
[04:25] So the same I can paste in the end as well with the variable name as endTime.
[04:32] And at last I can have a System.out.println() statement printing a String value which is total time,
[04:41] followed by colon followed by space.
[04:43] And to this I'll try to append the difference from the endTime - startTime.
[04:49] So let me execute this program and you can see all the threads are getting created.
[04:54] They are generating random double values.
[04:57] They are performing the product and they are printing.
[05:00] The product output onto the console.
[05:02] So this is going to take a good amount of time.
[05:05] Let's see how much time it is going to take.
[05:07] I'm going to wait behind the scenes after 30s my program execution is completed.
[05:12] That's why you can see total time
[05:14] this program it took is 30,563 milliseconds.
[05:20] That means it took 30s.
[05:22] So let's make a note of this.
[05:23] Inside the program, I'll just mention 30,563 is the time against to this Thread object.
[05:31] So this is the normal thread.
[05:32] But we want to leverage the virtual threads.
[05:36] Since virtual threads are introduced as part of Java 21, please make sure you are using Java 21 JDK
[05:41] inside your IntelliJ Idea.
[05:44] So to show you the demo on how to create the virtual threads, first let me comment all these lines
[05:49] related to the normal threads.
[05:50] So creating a virtual thread is super simple.
[05:53] There are multiple approaches that you have to create a virtual thread, but I'll be showing two different
[05:58] most commonly used approaches.
[06:00] The very first approach is we have a static method inside the Thread class.
[06:06] This static method name is startVirtualThread().
[06:09] To the startVirtualThread().
[06:11] We can pass a runnable task.
[06:12] So with this line of code, what is going to happen is, behind the scenes, a new virtual thread is going
[06:19] to be created, the same object you're going to get as an output.
[06:23] So using the same object, I want to invoke the join() method so that my for loop is going to wait for
[06:29] these threads to complete their execution.
[06:31] So if you try to open the startVirtualThread(), you can see it is introduced as part of Java 21.
[06:37] So what it is going to do is it is going to create a virtual thread to execute a task and schedule its
[06:42] execute.
[06:43] So the return type from this method is Thread.
[06:46] So let me open a class VirtualThread that is available inside the Java library.
[06:53] You can see there is a new class introduced inside the Java dot lang package with the name VirtualThread.
[06:58] So it is extending a class with the name BaseVirtualThread and this BaseVirtualThread,
[07:04] it is extending a class Thread.
[07:06] That's why though the return type of this method is Thread, we're not getting any compilation error
[07:11] even though a virtual thread is getting created behind the scenes.
[07:15] I hope you are clear now if I try to execute this program, let's see the output this time.
[07:21] So I'm trying to execute this time.
[07:23] This time you can see the program is executed within 8844 seconds.
[07:30] So where is 30s?
[07:32] Where is nine seconds.
[07:33] So there is a lot of drastic improvement and how this improvement came into picture
[07:39] like I said, creating of virtual threads and destroying them and assigning a CPU time for them.
[07:45] Everything is going to be super quick because virtual threads are lightweight in nature compared to
[07:52] the normal threads.
[07:53] On top of this, the memory footprint required by the virtual threads compared to the native or platform
[07:59] threads is going to be very less so.
[08:01] With all these advantages, we are able to execute the program in almost nine seconds compared to the
[08:07] 30s of normal platform or native threads.
[08:11] So let me copy this value and paste it here.
[08:15] The next approach that I want to show you is with the help of Thread class only, we can invoke another
[08:23] static method which is ofVirtual() and this is going to convert to a normal Java thread into a virtual
[08:30] thread.
[08:31] Post this we can invoke the start() method to the start() method
[08:34] we can pass the Runnable object and after this I can invoke the join() method.
[08:38] So if I try to execute this time also I should get the output very quickly.
[08:43] You can see this time also the program executed within nine seconds.
[08:48] So let me copy this value also inside this class though the numbers are not similar, but they are almost
[08:54] same like they are taking around nine seconds regardless of which approach you're trying to use.
[09:00] So every time you execute this program, you may get some different output, but the output should be
[09:06] is within the range of nine seconds.
[09:08] And this also depends upon the capacity of your system.
[09:11] But overall, I'm assuming you are clear with the virtual threads, the power that they provide to the
[09:17] concurrent applications that we can build with the help of multiple threads concept.
[09:21] So please execute this program inside your system.
[09:24] Also to see the advantages provided by the virtual thread.
[09:27] I'm also going to check in this program into the GitHub repo.
[09:31] Inside this slide, I have highlighted both the approaches that we have used to create the virtual threads.
[09:37] So always use the static methods like startVirtualThread() or ofVirtual() to create virtual threads
[09:44] to these virtual threads, you can pass the business logic in the form of runnable object, or you can
[09:49] also pass a direct lambda expression.
[09:52] Apart from these methods, thread also has one static method which is isVirtual(), so using these
[09:58] isVirtual() method
[09:59] third, we can identify whether a given thread is a virtual thread or not.
[10:04] So these are all the helper or static methods introduced as part of the Java 21 inside the same thread
[10:10] class.
[10:11] The reason why Java team introduced all these methods inside the same class is a lot, many developers
[10:16] and lot many projects.
[10:17] They might be using this thread to a great extent inside their multithreading program, so they don't
[10:24] want to make the creation of virtual threads complex in nature
[10:29] that requires a lot of learning curve.
[10:31] Instead of that, they want to keep the thing simple.
[10:33] That's why they added these helper static methods using which we can easily create virtual threads.
[10:39] I hope you are clear with the virtual threads concept.
[10:41] If you are using Java 21 inside your real projects, always feel free to use the virtual threads.
[10:48] Thank you and I'll catch you in the next lecture, bye.


########################################
