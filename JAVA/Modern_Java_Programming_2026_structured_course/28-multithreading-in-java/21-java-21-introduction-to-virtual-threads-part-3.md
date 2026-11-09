# 28.21 — [JAVA 21] Introduction to Virtual Threads - Part 3

> Section 28: MultiThreading in Java

[00:00] We know from Java 21 version, virtual threads are introduced to replace platform or native threads.
[00:07] Virtual threads have some clear advantages.
[00:10] Let's try to understand what are those.
[00:11] The very first advantage is these virtual threads are notably lightweight.
[00:16] They are going to be super, super lightweight because they require only a small memory inside your
[00:22] Ram.
[00:23] Typically, each virtual thread consumes only a few bytes of memory.
[00:28] We're talking about bytes, but not the megabytes.
[00:31] We know 1MB is equal to 1024 bytes.
[00:35] If your virtual thread requires only few bytes, like two bytes or eight bytes, it's going to be a
[00:41] game changer.
[00:41] Because a normal platform thread or a native thread, it requires a Ram memory in the range of 1MB
[00:48] to 20MB, and sometimes it may even higher as well.
[00:52] Since the memory footprint is reduced from megabytes to bytes, we will be able to create any number
[01:00] of virtual threads.
[01:01] That's why if you see the next advantage of virtual threads is their scalability.
[01:06] So there is no limit on how many number of virtual threads that you can create.
[01:10] In fact, you can create millions of virtual threads as well because all these million virtual threads,
[01:16] they require only a less memory inside your Ram.
[01:19] On top of that, whenever you are creating a virtual thread, they are not going to require any system
[01:24] call to the kernel, because the mapping between a virtual thread and the kernel thread is not going
[01:30] to happen directly.
[01:32] I'll come to that point in very few seconds, since the memory footprint is very less for the virtual
[01:37] thread, and also they don't require system calls to the kernel to get them created.
[01:42] With all these advantages, creating and destroying the virtual threads will be like a super quick.
[01:49] They don't even require milliseconds.
[01:51] They may require nanoseconds time.
[01:53] So these virtual threads, they are going to leverage the M is to N thread model.
[01:59] That means a large number of virtual threads can be scheduled or mapped to run on a small number of
[02:07] OS threads.
[02:08] So let's try to understand how this is going to happen behind the scenes.
[02:11] So if you see here, whenever that JVM is getting started behind the scenes, what it is going to do
[02:17] is it will try to create some platform threads.
[02:20] For example, here it's trying to create eight different platform threads or native threads.
[02:26] And for all these threads it also have a equivalent mapping with the operating system.
[02:32] So this is what happened behind the scenes by the JVM.
[02:35] But when a Java program or when a developer try to start creating the virtual threads, all these virtual
[02:42] threads, they are going to be created inside the Java heap memory because they require only a minimum
[02:48] amount of memory.
[02:49] So your Java program can create any number of virtual threads.
[02:53] And all these virtual threads.
[02:55] Mapping to the platform threads is going to be maintained by the JVM.
[03:00] And since the platform thread and OS threads mapping already happened as soon as the virtual thread
[03:06] assigned to your platform thread the instructions, they are going to be executed super quickly, and
[03:12] once the instructions executed by the virtual thread, it is going to be destroyed, or it is going
[03:18] to be kept in a waiting state by the JVM, and immediately the JVM will try to assign this platform
[03:24] thread to some other virtual thread.
[03:26] So with this, what advantages we are getting, we are getting a better or enhanced CPU utilization.
[03:32] When we are discussing about the platform threads
[03:35] in the previous lecture, we saw that in an example, only 32% of the CPU utilization is happening because
[03:41] during the IO operation the platform thread or native thread, it is sitting idle without using any
[03:48] CPU time.
[03:49] And the operating system also didn't try to perform the context switching because context switching
[03:54] is expensive whenever we are dealing with the native threads or platform threads.
[03:58] But with the introduction of virtual threads, all these issues are resolved because since virtual threads,
[04:04] context switching does not require system call and they can be created and destroyed any number of times
[04:10] very easily.
[04:12] Behind the scenes, what JVM is going to do is, during the 100 milliseconds of IO waiting period time,
[04:18] the virtual thread which is handling the request, it is going to be destroyed, or it is going to kept
[04:24] in a wait status, and immediately the JVM is going to assign the platform thread to some other virtual
[04:31] thread, which requires a CPU time.
[04:33] So in simple words, we can say a virtual thread while waiting for an IO operation to complete will
[04:39] detach from the platform thread so that platform threads can be used by other virtual threads which
[04:45] need CPU time.
[04:47] I hope you are clear.
[04:48] With the help of virtual threads, we will be able to create any number of threads if needed
[04:53] an application can create millions of threads as well.
[04:56] The other advantage that we are getting is during the IO
[04:59] operations, the virtual threads, they are going to be detached from the platform thread, so that
[05:04] platform threads can be leveraged by the other threads, and this will eventually result into the enhanced
[05:11] CPU utilization.
[05:12] In the next lecture, I'll be showing you a demo with the normal platform threads and with the virtual
[05:17] thread in the same process.
[05:19] You'll be surprised by the improvements provided by the virtual thread.
[05:23] I hope you are clear with the virtual thread.
[05:25] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
