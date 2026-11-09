# 28.7 — Creating Threads in Java - Part 2

> Section 28: MultiThreading in Java

[00:00] Java provides multiple options to developers to create a Thread object.
[00:05] In the previous lecture, we leveraged the constructor of the Thread class to create the Thread object.
[00:11] But inside this lecture, let me show you the other approaches that we have so that you can use any
[00:17] of them based upon your business logic inside your real projects.
[00:21] Like you can see here
[00:22] the very first approach that I'm going to discuss is by extending the Thread class.
[00:27] We know Thread is a class, and we can extends it with the help of inheritance.
[00:32] So the custom class that I'm trying to create here is MyHelloThread.
[00:36] So whenever we are extending the Thread class, we can override the run() method with our own business
[00:43] logic.
[00:44] So here I'm trying to have a simple statement which is System.out.println().
[00:48] But you can't use this approach if your class is already inheriting another class, because inside Java
[00:56] at the max, we can only extend a single class.
[01:00] So whenever you are into the scenarios where your custom class is already extending some other class,
[01:07] then you can switch to the next approach, which is by implementing their Runnable interface.
[01:14] We know inside Java we can implement any number of interface.
[01:18] That's why you can happily use this approach without any restrictions.
[01:23] So once you add custom class, it is trying to implement the Runnable interface.
[01:28] Since the Runnable has a abstract method with the name, run your custom class, which is MyHelloThread
[01:35] it needs to override the run() method and provide the business logic like you can see here.
[01:40] If you feel defining the custom class and implementing this interface and overriding this run() method
[01:46] is a lengthy approach.
[01:47] Like we discussed in the previous lecture, you can follow these shortcut approach, which is you can
[01:54] directly pass the lambda expression as an input to the thread class constructor.
[01:58] So this is the quickest and easiest way to create the Thread object.
[02:03] But for complex business requirements where you have some good amount of lines of code inside your business
[02:09] logic, then obviously it is always recommended to create a separate class, either by extending the
[02:16] Thread class or by implementing the Runnable interface, and the last approach is with the help of method
[02:22] reference.
[02:23] So if you already have your business logic that you're planning to execute with the help of a Thread
[02:28] in some other class or in some other method, you can happily use the method reference that we have
[02:34] discussed as part of the functional programming.
[02:37] So here you can see I have a class with the name Hello.
[02:40] And inside this I have a static method with the name sayHello().
[02:43] Inside this I have a logic which I want to execute as part of my Thread by using my Thread object.
[02:50] So in this scenario, instead of writing the lambda expression again, what we can do is to the Thread()
[02:55] constructor we can pass this method reference as an input.
[02:59] Since the sayHello() is a static method, I'm not creating the object of Hello class.
[03:03] I'm trying to directly mention the class name followed by method reference symbol followed by what is
[03:08] the method name
[03:09] sayHello().
[03:10] I hope you are clear with these three approaches that we have discussed so far inside this lecture.
[03:15] Regardless of which approach you are trying to use, the process of starting the thread is always the
[03:22] same.
[03:22] You should always invoke the start() method and you should never invoke the run() method directly.
[03:28] Let's see the demo of all these approaches very quickly inside our intelliJ.
[03:33] So what I'm going to do is, I'll try to create a class with the name HelloThread.
[03:39] And inside this class I'm going to extends the Thread class and post that
[03:45] what I'm going to do is, I'll try to override the run() method by not accepting any input parameter.
[03:52] And on top of this method I can mention override.
[03:55] Inside this method I can try to have a statement saying that HelloThread class
[04:02] I'll press enter and inside the next line I'll just mention which extends thread.
[04:08] So this is the statement I want to keep.
[04:10] In the similar lines
[04:11] I'll try to create one more class by copying the same class inside the same package, but this time
[04:17] I'll try to give the name as HelloThread1 as the class name.
[04:21] So inside this HelloThread1 I'll try to implement Runnable functional interface.
[04:28] So whenever I'm trying to implement this Runnable function interface, I need to override the run() method.
[04:32] And this time I'll just mention hello from HelloThread1 class which implements Runnable.
[04:40] And for the third approach I'm going to create a Java class with the name Hello.
[04:46] Inside this class I'm going to create a static method which returns void and with a method name as
[04:55] sayHello().
[04:56] Now as part of this method business logic, I'll simply have
[05:00] System.out.println().
[05:01] With a statement saying that Hello from method Reference Approach.
[05:08] So now I have three different classes ready, which I built by using three different approaches.
[05:14] Now using these three different classes, I can try to create the objects of Thread. For the same,
[05:20] let me go to the ThreadDemo.
[05:22] So since my HelloThread class already extends the Thread class, I can directly create the object of
[05:30] HelloThread with the variable name as Thread3.
[05:33] So let me use the constructor of HelloThread().
[05:37] Now you can see I have a thread ready and using this Thread3 I can try to invoke the start() method.
[05:43] As a next step,
[05:44] I can try to create Thread4 object with the help of the object of HelloThread1.
[05:50] So what I need to do is, I need to create the object of Thread with the variable name as Thread4.
[05:56] But to the constructor of Thread(), I need to pass the object of HelloThread1, which is the implementation
[06:03] of Runnable interface.
[06:05] So now using this Thread4, I'll be able to invoke the start() method.
[06:10] So these are second approach.
[06:11] Now moving on to the last and final approach, we can simply pass a lambda expression with the help
[06:18] of method reference.
[06:19] So first I'm trying to mention the class name followed by method reference symbol, followed by
[06:24] sayHello().
[06:24] And at last I'll try to rename this variable name to Thread5.
[06:27] And using the same I'll try to invoke the start() method.
[06:30] So if I execute this program, you'll be able to see that.
[06:35] First I got an output which is hi from Java thread, followed by help from HelloThread class which
[06:41] extends Thread.
[06:42] Did I make any mistake,
[06:43] let me check.
[06:44] Sorry I mentioned hell here so let me correct it to hello.
[06:48] Similarly, I'll also need to check inside this class as well here
[06:53] also I made a mistake.
[06:54] Let me mention hello.
[06:55] Now let me check inside the hello here
[06:58] also I mentioned hell I'm not sure why I mentioned hell.
[07:01] Now I can go to ThreadDemo and try to execute the program and you'll be able to see that we are seeing
[07:07] the output like hello from HelloThread class which extends thread and hello from HelloThread1 class
[07:14] which implements Runnable and at last we also have Hello from method reference approach.
[07:19] With this, I'm assuming your super clear about all the approaches that you can follow to create a Thread
[07:25] object.
[07:25] As of now, we just explored the baby steps inside the multithreading concept from the next lecture.
[07:30] Let's try to increase the complexity to better understand about the multithreading concept.
[07:36] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
