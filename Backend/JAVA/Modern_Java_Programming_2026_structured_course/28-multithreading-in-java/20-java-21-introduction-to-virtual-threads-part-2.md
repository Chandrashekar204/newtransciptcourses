# 28.20 — [JAVA 21] Introduction to Virtual Threads - Part 2

> Section 28: MultiThreading in Java

[00:00] In the previous lecture, we discussed all these three models, and I also told you that any software
[00:06] or any programming language, they have an option to choose one of these three models while creating
[00:12] the user level threads.
[00:14] Let's try to understand what is the model that Java uses behind the scenes when we start creating the
[00:20] threads?
[00:21] Many years back in 1990s when Java released the very first version inside Java programming language,
[00:28] the threads are used to create and mapped with the kernel threads by following the many to one thread
[00:35] model.
[00:36] So these kind of threads inside Java, they used to call them as green thread.
[00:41] I also highlighted here that these green thread concept is available only in the Java version, which
[00:47] is less than 1.2.
[00:48] That means only in the initial version of Java, like one and 1.1 only in those versions, green threads
[00:56] are available later on from 1.2.
[00:58] A new type of threads came into picture.
[01:01] But before we try to understand the new thread that came into picture from 1.2, first let's try to
[01:06] understand what the disadvantage that these green thread has. Whenever a thread is created by Java in
[01:13] the initial versions of Java version, all the user threads which are created from a Java program,
[01:19] they used to be directly overseen and scheduled by the Java virtual machine.
[01:24] So think like one of the Java program
[01:27] it created three different user threads.
[01:29] Since these green thread model leverages these M to One thread model, obviously all these three threads,
[01:36] they have to be mapped to one of the kernel thread or OS thread.
[01:40] So these mapping responsibility and scheduling used to be taken care by the JVM itself.
[01:46] So these green threads are there very fast in terms of execution or in terms of creation.
[01:53] The only drawback with these green thread model are with these Many To One thread model is with these
[02:00] green threads, Java could not effectively scale across multiple processors, limiting its ability to
[02:08] leverage multiple cores. Long back,
[02:11] when Java released its initial version in 1990s, during the same time CPUs, they used to have only
[02:18] a single core.
[02:19] But over the decades, a lot of advancements happened inside hardware.
[02:23] And with that, nowadays, every system and every CPU, they are having at least four cores and it may
[02:30] reach to 20 cores as well.
[02:32] But with this green thread model, regardless of how many cores your CPU has, since all these user
[02:38] threads are mapped to a single kernel thread which is available in one of the CPU core, the other CPU
[02:45] cores can be leveraged by these green threads to execute their business logic, so this is one of the
[02:50] drawback.
[02:51] The other drawback of this green thread is, if you see the responsibility of mapping and scheduling these
[02:58] user threads onto a kernel, thread is completely with that JVM.
[03:02] So any library or any program that needs to be built on top of Java or JVM, they need to know all the
[03:10] low level details of JVM, which requires a lot of learning curve, and this may not be not feasible
[03:16] for everyone.
[03:17] So with these two disadvantages, right from Java 1.2, these green threads are removed.
[03:25] And from Java 1.2 a new thread model came into picture.
[03:29] So let's try to understand the same.
[03:31] So from Java 1.2 JVM is going to follow the 1 to 1 thread model, which means each user thread is going
[03:40] to be available to the kernel thread or OS thread.
[03:43] So these kind of threads we can call them as native thread or platform threads.
[03:49] So these native threads are platform threads.
[03:51] They can be managed by the JVM with the assistance of the underlying operating system.
[03:58] These native threads, they exhibit high efficiency during execution but incur notable cost when starting
[04:06] and stopping.
[04:07] So whenever a thread is being created from Java 1.2, it is going to take some milliseconds of time.
[04:13] It can be one millisecond, or it can be ten millisecond.
[04:16] And the same kind of time is also going to cost during the stopping of the thread.
[04:21] Though this time is very negligible.
[04:23] But still these native are platform threads.
[04:26] They have certain limitations which I'm going to discuss in few seconds.
[04:31] So whatever threads that we have created so far inside this section with the help of Thread class.
[04:36] So all those threads we can call them as native or platform threads.
[04:40] So these option of native or platform threads is available for many years to the developers.
[04:47] So right from 1.2, version two Java 20 version, every developer they have to create these platform
[04:54] threads or native threads only.
[04:55] But from Java 21, like I said, we have an option of either
[04:59] creating a virtual thread or a platform thread.
[05:02] With these you may have a question which is these native are platform threads
[05:06] they are with the Java from more than two decades.
[05:10] Then why suddenly Java team they are trying to move to the virtual threads.
[05:15] So this can be your question.
[05:16] So let's try to understand the same here.
[05:18] What's wrong with the native threads and how virtual threads they are going to solve this problem?
[05:23] The problem with the native threads is, these native threads or platform threads
[05:28] they are initially created in the early versions of Java like 1.2, 1.3.
[05:33] So they kind of pretty outdated because when these threads are initially developed, obviously the developers
[05:41] might have not considered lot many advancements that are going to happen inside the hardware.
[05:46] So this is one of the drawback of these threads.
[05:48] The next important drawback is, these native threads or platform threads
[05:53] they are going to be expensive to create and maintain and destroy.
[05:57] They need a good amount of memory to store their call stack to store their local memory.
[06:02] So these memory can range from 1MB to 20MB, depending on the JVM and the platform that you are
[06:09] using.
[06:10] And depending on the business logic that you are trying to create.
[06:13] So these memory will be assigned to a thread from your Ram, not from the hard disk, because threads
[06:21] they need a memory location inside the Ram.
[06:24] So what is a Ram memory?
[06:25] It is a temporary memory that can be used by the threads, or by the processors, or by the softwares
[06:32] to store some information, which can be retrieved very fastly.
[06:37] So if you consider a system which has 8GB of Ram, it can only accommodate 800 platform or native
[06:45] threads if each thread consumes 10MB of Ram memory.
[06:50] So with that, it's pretty clear that these threads they have some restrictions based upon your Ram
[06:56] capacity, the number of threads.
[06:58] They are also going to be limited.
[07:00] On top of these, launching a new native thread or a platform thread takes approximately one milliseconds,
[07:07] and when our operating system try to context switch from one thread to another thread, the context
[07:12] switching operation is also expensive because it involves a system called to the kernel.
[07:17] So with all these limitations, whenever you use native threads or platform threads, they are going
[07:23] to impact the performance and scalability of your applications.
[07:27] For example, with just 8GB Ram or with just a 16GB Ram, you can't create 1 million native threads
[07:34] or platform threads, because each of your native or platform thread they need some amount of Ram memory.
[07:41] So that's why creating unlimited native threads is never an option due to these limitations.
[07:48] Let me try to explain about all these limitations by taking an example.
[07:52] Think like a company has a web server, and this web server has a Ram of 16GB.
[07:59] Inside these web server
[08:00] think like the company deployed a web application.
[08:03] So this web application has both UI and backend logic.
[08:07] So basically you can think this web application as a website.
[08:11] So websites can be accessed by any number of people through the web or through the browser.
[08:17] So whenever a user initiate a request to the website behind the scenes, a new separate thread will
[08:24] be created for each request that is coming from each end user.
[08:28] So the website can be accessed by any number of people throughout the world.
[08:32] Suppose if 1000 different people, they are trying to access this website at the same time 1000 different
[08:37] threads, they are going to be created.
[08:39] So with the assumption of that, each thread requires at least 10MB of Ram memory.
[08:44] This web server, it can only capable of creating 1600 threads at a given time.
[08:51] This also means that at a time, your website can be accessed by only 1600 different people, beyond
[08:59] the capacity of 1600.
[09:01] If someone is trying to access your website, they may not get the response immediately
[09:05] they may see some slow response on the browser, but most of the times, what is going to happen if
[09:10] someone is sending a request to the web server?
[09:13] As soon as the request reaches to the web server internally inside the backend logic, we will be doing
[09:19] a lot of interaction with the databases, or we might be making remote calls to the other web servers
[09:25] using Rest.
[09:26] So if you see most of our business logic, they are predominantly IO-bound rather than CPU-bound.
[09:34] So if you try to visualize a request that comes to the web server, think like the request to preparation
[09:41] is going to take 0.1 millisecond.
[09:44] So during these request preparation, only the CPU time is needed based upon these requests inside the
[09:52] backend
[09:53] think like some IO operations are happening.
[09:55] Like like storing the data into the DB or reading the data from the DB or.
[09:59] You might be invoking another rest API and usually these IO operations
[10:03] they are going to take some amount of time because the data has to travel to the server location where
[10:09] the DB is deployed, or where the other remote server is deployed.
[10:12] That's why typically these IO operations, they will take at least 100 milliseconds to complete.
[10:18] So once these IO operations are completed at the end, we need to send the response back to the end
[10:24] user which can be displayed on the browser.
[10:26] So these response processing and response building also requires CPU time.
[10:33] Since this is a very small task, usually it will take only point to one millisecond or a 0.5 millisecond.
[10:39] So with this assumption, let's try to understand what is going to happen behind the scenes with these
[10:45] 1600 requests that are coming towards these web server.
[10:48] I hope you are clear with this picture.
[10:50] So this picture represent what is the time taken by each request coming from the end user.
[10:56] So most of the time the request goes through the IO operations where the CPU time is not required.
[11:02] So with this assumption, if you try to perform some calculations, the total CPU time required for
[11:08] a single request is 0.1 plus 0.11 is request preparation time and the other one is response preparation
[11:15] time.
[11:16] So if you add both of them it will be 0.2 milliseconds.
[11:19] So this is the total CPU time required for each incoming request.
[11:24] But if you try to understand what is the total time for 1600 requests, it will be three 20 milliseconds
[11:31] because I'm trying to multiply 1600 with 0.2 milliseconds.
[11:35] So the total CPU time required by all the 1600 requests that are coming towards your web server is only
[11:42] three 20 milliseconds.
[11:44] Now, with an assumption that in a second, our server can handle only 1600 requests because we can
[11:50] only create only a maximum of 1600 threads with a factor of one second is equal to 1000 milliseconds.
[11:56] If you try to understand in a second how much of your CPU is getting utilized, it will be only that
[12:03] 32%.
[12:05] That means we are wasting around the 68% of the CPU capacity in a single second.
[12:11] Whenever we are using the native or platform threads.
[12:15] How this wastage is happening.
[12:17] If you see here during these IO operations, the thread which is handling this entire request, it is
[12:23] going to sit idle during these IO operation.
[12:26] Here you may have question which is why the thread has to sit idle.
[12:30] The operating system can perform the context switch and it can make the thread busy with some other
[12:35] CPU tasks.
[12:36] So this can be a question.
[12:37] But the problem with the context switch while using the need two threads or platform threads is context
[12:43] switching is also going to be expensive operation.
[12:46] On top of that, since native threads approach is using one is to one thread model.
[12:51] Again, once these IO operation is completed, the operating system has to find one of the kernel thread
[12:57] to prepare these response processing.
[13:00] Since all these are expensive operations, it is not going to make sense to perform context switching
[13:06] whenever we are using the native threads.
[13:09] On top of that, we also have a limitation, which is we can only create up to a maximum of 1600 threads
[13:16] in the example that we have considered.
[13:18] So let's try to understand how all these complexities and limitations are overcome by the virtual threads.
[13:26] Let's continue this discussion in the next lecture as well.
[13:29] Thank you,
[13:30] bye.

----------------------------------------
