# 28.19 — [JAVA 21] Introduction to Virtual Threads - Part 1

> Section 28: MultiThreading in Java

[00:00] The latest buzzword in Java multithreading concept is virtual threads.
[00:05] So what are these virtual threads?
[00:07] Virtual threads are the new feature introduced as part of Java 21.
[00:13] They are introduced very recently.
[00:15] These virtual threads are going to be a game changer for all the applications where they are using lot
[00:23] many threads as part of their business logic.
[00:26] As of now, we're just trying to create an object of Thread class and using the same.
[00:30] We are trying to invoke the start() method join() method.
[00:32] Everyone is happy with the thread, but it has some drawbacks which we are going to discuss in the coming
[00:39] lectures.
[00:40] But if you ask me on a high level, what is the difference between a normal thread and a virtual thread?
[00:45] The answer is very simple.
[00:46] Virtual threads are lightweight in nature.
[00:49] With that, you can create millions of virtual threads inside your Java program.
[00:56] There won't be any restriction, whereas with a normal thread, since they are not lightweight like
[01:01] virtual threads, you will be limited with how many threads you can create inside your application based
[01:07] upon your Ram, memory and CPU cores.
[01:10] Oracle team
[01:11] they are working on these virtual threads from many years under the project name Loom.
[01:16] So Loom is a Oracle's initiative aimed at tackling the complexities associated with the developing,
[01:23] maintaining and monitoring high throughput concurrent applications.
[01:28] Finally, after doing a lot of research and testing, virtual threads are introduced in Java 21.
[01:35] So to understand in detail about what is a virtual thread and how it is different from a normal thread,
[01:40] first we need to understand some basics of operating system and threads.
[01:44] So let's try to understand the same. Inside operating system
[01:48] there are two types of threads that you can create.
[01:52] The very first type is kernel threads.
[01:55] So these threads in other words we can call them as operating system threads.
[02:00] These kernel threads are OS threads
[02:02] they are going to be overseen and scheduled by the operating system kernel.
[02:06] These threads are relatively heavyweight in terms of resources and requires system calls for their creation,
[02:14] scheduling and synchronization.
[02:16] So these kernel threads, they are going to be created strictly for the operating system purpose.
[02:21] That's why whenever you try to start your operating system like Windows or Mac, it is going to take
[02:27] some 30s or one minute based upon your computer and operating system.
[02:32] So during all these 30s or one minute behind the scenes, your operating system taking enough time to
[02:38] boot up and create all these kernel threads.
[02:41] The other type of threads are user level threads.
[02:45] So what are user level threads?
[02:46] If you try to run any software, or if you try to execute any program like Java
[02:51] so these softwares are Java programs
[02:53] they can be able to create the threads.
[02:56] All such threads we can call them as user threads.
[02:59] Throughout this section we are able to create the threads inside a Java program with the help of Thread
[03:04] class.
[03:04] So all these threads, we can call them as user threads, because a particular library or a particular
[03:10] software is trying to create these threads, but not the operating system.
[03:14] Compared to the kernel threads, the user threads are lightweight in nature, and creating and destroying
[03:20] these user threads is faster compared to the OS threads.
[03:24] So when we are creating a thread inside Java program, we never side delay.
[03:28] The threads are getting created instantly, but OS threads are kernel threads
[03:32] they are not going to be created instantly.
[03:34] That's why during the startup of the operating system, they are going to take few seconds of time.
[03:40] In simple words, whenever a program or a software want to create the threads first, it is going to
[03:46] start the process with a default thread to run the applications entry point.
[03:51] In the case of Java, the applications entry point is main() method.
[03:55] That's why behind the scenes it default thread is going to be created by the Java libraries.
[04:01] Following these main() thread
[04:02] java are any other program
[04:05] they have the flexibility to generate the extra user threads as per their requirement.
[04:10] So all these user threads, they are going to be executed indirectly by the operating system threads
[04:18] or kernel threads, which means each of the user threads that we are trying to create with the help
[04:24] of a Java or any other program, they need to be mapped to some kernel thread so that the kernel thread
[04:30] is going to take care of executing the user thread by getting the CPU time from the operating system.
[04:36] So basically, whenever you have many number of user threads and kernel threads, the mapping has to
[04:42] be done between user threads and kernel threads.
[04:45] And there are multiple approaches to perform these mapping.
[04:49] So let's try to understand those approaches.
[04:51] In the same process we can try to evaluate the evolution of threads inside Java the association between
[04:59] user.
[04:59] And kernel threads can be done in three approaches.
[05:03] The very first one is, M : 1 model, which means all user threads
[05:09] they are going to be linked to a single kernel thread.
[05:13] So here you can see U indicates user threads and K indicates kernel threads.
[05:18] So in these many to one thread model all the user threads
[05:22] they are going to be mapped to a single kernel thread.
[05:25] The next model is, one is to one model
[05:28] in this model each user thread is going to be mapped to one of the kernel thread, and at last M is to M
[05:34] model, and inside this model, all user threads are mapped to a pool of Kernal threads.
[05:43] That means a user thread can be mapped to a many kernel thread, and similarly a kernel thread can be
[05:50] mapped to many user threads.
[05:52] So these are the three models that are available inside operating system based upon which mapping a
[05:59] particular program or a particular library is leveraging
[06:02] accordingly, the performance is going to be impacted inside multi-threading program.
[06:08] Since we are talking from Java perspective from the next lecture, let's try to understand how these
[06:13] three models are going to affect the multi-threading Java program execution.
[06:17] I hope you are clear
[06:18] with all the discussion that we have done so far, we simply discussed there are two types of threads
[06:23] which are kernel threads and user threads.
[06:26] The mapping between these two types of threads can be done by using all these three models.
[06:31] The mapping has to be done because at the end of the day, a user thread has to coordinate with the
[06:36] kernel thread to get some CPU time and to execute its instructions.
[06:41] I hope you are with me.
[06:42] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
