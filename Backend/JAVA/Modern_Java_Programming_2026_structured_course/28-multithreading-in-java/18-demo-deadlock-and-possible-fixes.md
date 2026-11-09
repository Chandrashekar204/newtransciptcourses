# 28.18 — Demo Deadlock & possible fixes

> Section 28: MultiThreading in Java

[00:00] Let's see the demo of deadlock for the same
[00:03] I'm going to create a new Java class with the name DeadlockDemo inside this class
[00:10] first I'm going to create couple of String objects.
[00:13] The very first one is public static final String R1 = Hello.
[00:21] .
[00:21] So this is just a static string object in the similar line
[00:25] let me try to create one more String object with the name R2.
[00:28] And inside this R2 I'm going to have a data which is high.
[00:32] Let's imagine this is the resource one and this is the resource two.
[00:35] So the resource can be anything,
[00:37] it can be a variable,
[00:38] it can be an object,
[00:39] it can be an static variable or instance variable.
[00:42] Regardless of what is the type of resource
[00:44] the deadlock may always happen if two threads are waiting for other threads to release a certain resource.
[00:52] After defining these variables, I'm going to create the main() method inside this main() method.
[00:57] First, I'm going to create a thread with the variable name as thread1, followed by
[01:02] I'll try to pass a lambda expression to the constructor of Thread().
[01:07] So inside my constructor I'll just write a empty parentheses followed by lambda symbol followed by curly
[01:13] braces.
[01:14] Now inside the lambda expression body I'm going to use the synchronized() keyword.
[01:20] So what is the purpose of synchronized() keyword?
[01:22] Using synchronized() block or synchronized() methods we can get a lock on a particular resource.
[01:28] So in this scenario first my T1, it will try to get a lock on the R1.
[01:35] Inside the synchronized block I'll write a System.out.println() saying that thread T1 locked
[01:42] :resource R1.
[01:44] After defining the synchronized() block inside the synchronized() block, I'll try to define one more nested
[01:51] synchronized block, this time with this second synchronized block, my thread one will try to get a
[01:58] lock on R2.
[01:59] So that's why inside these are two synchronized block.
[02:03] I'll try to have a System.out.println() saying that Thread T1 locked : Resource R2.
[02:09] After defining this thread 1, I'll try to define one more thread with the similar logic.
[02:14] So first let me copy all this code.
[02:17] This time I'll try to give the variable name as thread2 and thread2
[02:21] first it will try to get a lock on R2, followed by
[02:25] it will try to get a lock on R1.
[02:27] So with this what is going to happen is, when thread one started its execution, it is going to get a
[02:33] lock on R1.
[02:34] Similarly thread2 it is going to get a lock on R2.
[02:37] Post that thread one will look for a lock on R2 and in the similar lines thread two it is going to
[02:44] look for a lock on R1.
[02:45] So once the second object lock acquired, they can release the lock on the other shared object like
[02:52] R2 and R1.
[02:53] But this is never going to happen because these two threads like T1 and T2, they are going to
[02:59] wait to mutually for the other thread to release the lock first.
[03:02] I can also show you the demo of deadlock here for the same
[03:06] let me start the thread1 by invoking the start() method.
[03:11] In the similar lines, I can also invoke the start() method with the help of thread2 object.
[03:16] Before I try to execute this program, I need to update the System.out.println() saying that thread
[03:22] T2
[03:23] lock the resource one.
[03:24] And here also I need to update from T1 to T2.
[03:27] Once I updated the thread names, I should also update the resource names because first my thread T2
[03:33] is trying to get the lock on resource two.
[03:36] That's why I need to mention R2 here and R1 here.
[03:39] Now if I execute this program, you'll be able to see an output which is thread T1 acquired the lock
[03:44] on resource one and thread2 acquired the lock on resource two.
[03:49] After this nothing is happening
[03:51] you can see my program stack and the threads are keep waiting forever.
[03:56] You can also see my program is running behind the scenes, because you will be able to see that this
[04:00] stop is enabled.
[04:02] That means behind the scenes, the program is still running and this T1 is waiting for the lock on
[04:07] R2, and the T2 is waiting for the lock on R1.
[04:10] So this way they are going to wait continuously which is resulted into deadlock scenario.
[04:16] So how to resolve this kind of scenarios?
[04:18] I'll explain you how to resolve them in few seconds.
[04:21] But before that, let me stop this program by clicking on the stop button.
[04:25] You can see I'm trying to forcefully stop this program.
[04:28] Now let me show you how to fix the deadlock scenario
[04:33] in this program there are multiple other approaches also available, which I'm going to explain you
[04:38] in few minutes.
[04:38] But from this program perspective, we can fix it by making the thread2
[04:44] also to get the lock first on R1.
[04:47] Post that it can also look for the R2 resource lock.
[04:50] So with this the circular dependency will never happen because think like first thread one got the lock
[04:57] on R1 and in this
[04:59] scenario thread 2 when it is trying to get a lock on R1, it is going to wait for thread 1
[05:05] to release the R1.
[05:06] As soon as thread one acquired the R2, then R1 is going to be free and thread two can get the R1.
[05:13] Once these thread1 executed these business logic and come out of this block, then R2 also is going
[05:19] to become free.
[05:20] And with that, the thread two also is going to acquire the lock of R2.
[05:24] So I'm just trying to make sure that there is no circular dependency.
[05:28] So if I execute this program.
[05:30] So with this output, I'm assuming you are clear that both the threads are able to acquire the resources
[05:36] and they are able to execute the business logic without any deadlock.
[05:40] So this is because we avoided the circular dependency.
[05:43] But if I try to revert this to R1 and here Rtwo, then again the circular dependency is going to
[05:49] come into picture and that may result into deadlock in my scenario like you can see here.
[05:55] So what I'm going to do is I'll just keep this program as it is and check in into the GitHub repo so
[06:00] that this program may act as a reference for deadlock scenario.
[06:04] If you're looking to fix this scenario, the solution is very simple.
[06:07] You just have to swap these variables like R1 here and R2 here.
[06:11] Let me show you what are the other approaches that you have to avoid the deadlock.
[06:15] Before I try to explain you about the other approaches to solve a deadlock, let me highlight you that
[06:20] the program that we have discussed inside this lecture, I have mentioned in this slide for your reference,
[06:26] along with the explanation, I also highlighted here what is a possible fix for this program to avoid
[06:32] the deadlock scenario.
[06:33] Now moving on to the next slide.
[06:35] The very first best practice that you need to follow to avoid the deadlock is,
[06:39] try to avoid nested locks.
[06:42] So how we are getting a lock with the help of synchronized block or with the help of synchronized methods.
[06:47] So don't try to use synchronized keyword in a nested way.
[06:52] Inside the example that we discussed inside this lecture, we are trying to have nested synchronized
[06:57] blocks.
[06:58] With that we are trying to have nested locks.
[07:00] So with the nested locks there is a good chance that we may result into a deadlock.
[07:05] Moving on to the next best practice which is avoid unnecessary locks.
[07:10] Don't try to apply synchronized unnecessarily wherever you want.
[07:14] Only apply in the places where your business logic requires a lock on an object.
[07:20] If you try to have too many locks with the help of synchronized keyword, then obviously the probability
[07:25] of getting a deadlock is also going to be too high.
[07:28] The next best practice is always check the lock hierarchy.
[07:33] How your Java program is applying the lock.
[07:35] If you follow a proper hierarchy that avoids circular waiting scenarios, then there won't be any deadlock
[07:42] scenario.
[07:42] Inside this program, you can see we are not following the proper locking hierarchy inside thread2.
[07:48] That's why we are creating a circular waiting scenario.
[07:51] And with that a deadlock came into picture.
[07:53] If I correct this lock hierarchy, then there won't be any circular waiting scenario or there won't
[07:58] be any deadlock scenario.
[08:00] So this is what this lock hierarchy is conveying.
[08:03] So these are all the best practice.
[08:05] Apart from these best practices.
[08:07] You can also leverage the classes and methods present inside the package java.util.concurrent.
[08:15] So inside these package there are certain good amount of classes and methods using which you can build
[08:23] a better multithreading Java programs.
[08:25] For example, there is a class with the name ReentrantLock.
[08:30] Inside this ReentrantLock there is a method with the name tryLock().
[08:35] To this tryLock() method, we can pass that time in milliseconds or in seconds.
[08:41] So with this what is going to happen is your thread.
[08:44] It is going to wait to acquire a lock only up to a maximum of 100 milliseconds, which we have configured
[08:50] here.
[08:51] So if you configure 1000 milliseconds then in that scenario the thread will wait for a maximum period
[08:56] of 1000 milliseconds.
[08:58] After 1000 milliseconds it will try to skip this if condition and it will move on to the other business
[09:04] logic.
[09:04] So let me show you these class and method.
[09:06] I can search for a class with the name ReentrantLock.
[09:10] Inside this class let's look for a method which is try lock.
[09:15] So there are overloaded methods.
[09:17] So if you try to open the second method which is accepting the timeout and the time unit as an input.
[09:23] So if you try to see the documentation of this method, it clearly conveys if the lock is held by another
[09:30] thread, then the current thread becomes disabled for thread scheduling purpose and lies dormant until
[09:36] one of these three things happen. The lock is acquired by the current thread or some other thread interrupts
[09:42] the current thread are the specified waiting time elapse.
[09:46] So the last point is very important.
[09:49] This means whenever you are trying to acquire a lock with the help of this method, your thread is not
[09:53] going to wait infinitely to acquire a lock.
[09:56] Instead, at a maximum time of time that we
[09:59] provided as an input to this method is going to be considered for weighting, and beyond that, the
[10:04] thread will not keep waiting.
[10:06] One more beauty of this tryLock() method is, it is going to return a boolean value as an output, indicating
[10:12] whether your thread acquired a lock on a resource or not.
[10:16] If the output from this method is true, then that indicates your thread acquired a lock and everyone
[10:23] is happy.
[10:23] If this method returns false, then that means your thread did not acquire the lock, and accordingly,
[10:29] you need to have some other business logic that needs to be executed
[10:33] in the scenarios where the lock is not acquired, you can write any business logic.
[10:38] Maybe you can go with some other business flow, or you can make your thread to sleep for 100 milliseconds
[10:43] or 200 milliseconds
[10:45] whatever works for you.
[10:46] Just like how we have this tryLock() method, which is accepting the timeout and time unit as an input.
[10:51] We also have try lock method which is not accepting any input parameters.
[10:56] So here if you try to read the documentation, it says if the lock is held by another thread, then
[11:01] this method will return immediately with the value false.
[11:04] That means your thread is not going to wait for ever, or it is not going to wait even for one millisecond.
[11:11] Immediately it is going to get a output as false and accordingly you need to execute your false related
[11:17] business logic.
[11:18] I hope you are clear on what is a deadlock and how to avoid the deadlock in multi-threading Java programs.
[11:24] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
