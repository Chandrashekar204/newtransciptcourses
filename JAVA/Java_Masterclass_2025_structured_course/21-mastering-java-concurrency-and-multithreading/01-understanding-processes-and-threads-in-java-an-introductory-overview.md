# 21.1 — Understanding Processes and Threads in Java: An Introductory Overview

> Section 21: Mastering Java Concurrency and Multithreading

Kind: captions Language: en I want to start this section, on concurrency and multi threading, by defining a few key terms that you need to know, as they relate to this topic in Java. I'll start with the term, Process , which is a unit of execution, that has its own memory space. Now most instances of a java virtual machine, the JVM, run as a process. When we run a java console application, what we're doing is, we're kicking off a process. The terms process and application are often used interchangeably, and I've done that myself, and will again in this section.

If one java application is running, and we start up another one, Each application has its own memory space, also known as the heap. The first application can't access the heap that belongs to the second java application. In other words, The heap isn't shared between two applications or two processes, they each have their own. Next, Let's talk about a thread. A thread is a single unit of execution, within a process. Each process can have multiple threads.

In Java, Every process or application has at least one thread, and that's the main thread for most programs. In fact, just about every Java process also has multiple system threads, that handle every day tasks, like memory management, and input output. We don't have to explicitly create, and code these kinds of threads, the JVM does this work. Our code will run on the main thread, which is created automatically by your Java program. We can also have our code run in other threads, which we can explicitly create and start.

In this section of the course, you're going to be learning different ways to create threads, execute them, and manage them. Creating a thread doesn't require as many resources as creating a process does. It's important to understand that Every thread created by a process, shares that process's memory space, the heap. This can cause big problems with your applications, and you'll find out about that, in a later lecture. In addition to the processâ€™s memory, or heap, Each thread's got what's called a thread stack.

This is memory, that only a single thread, will have access to. I'll be comparing the heap, versus the thread stack, in a later lecture in this section as well. Every Java application runs as a single process, and each process can then have multiple threads within it. Every process has a heap, and every thread has a thread stack. I guess at this point you might be asking, why would we want to use multiple threads in our application? Why not just stick with the main thread?

What are some of the advantages, to creating a multi-threaded application? Well, there are several reasons why you'd want to do this. One of the most common reasons, is to offload long running tasks. Now, for example, we might want to query a database, or we might want to fetch some data, from a website on the internet. Since code executes linearly, if we performed this task in the main thread, we'd be stuck waiting until this operation completed, before the main thread could do anything else.

To the user, this could appear as if the application has died, or is locked up, especially when we're dealing with a user interface application. Instead of tying up the main thread, we can create additional threads, to execute tasks that might take a long time. This frees up the main thread so that it can continue working, and executing, and being responsive to the user. You can report progress, or accept user input, and perform other tasks on the screen, or in other parts of the program, while that long-running task, continues to execute, in the background.

You also might use multiple threads to process large amounts of data, which can improve performance, of data intensive operations. A web server, is another use case for many threads, allowing multiple connections and requests to be handled, simultaneously. That now brings us to the concept of Concurrency, which refers to an application doing more than one thing at a time. Concurrency allows different parts of a program to make progress independently, often leading to better resource utilization, and improved performance.

Underneath the covers, there's a lot of thread management tasks that occur, which give the impression that progress is being made on multiple fronts, even in a single C P U environment. Let's say that an application wants to download data, and separately, draw a shape on the screen. If it's a concurrent application, what it can do is, it can download a bit of data, then switch to drawing part of the shape. It can then switchback to downloading some more data, then back again to drawing more of the shape, and so on.

Each task is done a bit at a time, and can report on its progress, to the user. What concurrency really means is, that One task doesn't have to complete, before another one can start, and multiple threads can make incremental progress. Concurrency is something that's best learnt by example, so let's move on to the next video. I'll be examining the main thread a little bit, to explain some key Thread concepts, and then I'll create and kick off, a concurrent thread.

I'll see you in that next video.

----------------------------------------
