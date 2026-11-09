# 28.4 — Parallel vs Concurrent Execution

> Section 28: MultiThreading in Java

[00:00] Like I said before, all the modern computers, they are having multiple CPU cores.
[00:06] The minimum number of cores that you will be seeing inside a computer these days is four cores, and
[00:12] it can go up to 1216 cores as well.
[00:15] Right now, my system has ten different CPU cores at a time
[00:20] a single core can handle a single thread, and it can execute all the instructions associated to a thread.
[00:28] But with that you may have question, which is you have ten CPU cores, which means at a time your system
[00:35] can handle ten different threads only.
[00:38] But inside my activity monitor, you'll be able to see that most of the processors they are having multiple
[00:45] threads.
[00:46] For example, the IntelliJ Idea itself, it has 80 different threads.
[00:52] Then how come my system, which has only ten CPU cores, is handling 80 different threads and these
[01:00] 80 different threads are only from a single process, which belongs to IntelliJ Idea.
[01:05] If I try to look at the summary here in the down inside my system, as of now there are total 513 processes
[01:12] are running.
[01:13] And all these 513 processes, they are having 2582 threads running behind the scenes.
[01:22] So a computer which has just ten CPU cores, how it is able to manage thousands of threads.
[01:29] So that can be your question.
[01:30] So let's try to understand the same whenever you see an process like intelliJ
[01:35] and it can have multiple threads like 80 here
[01:39] so that doesn't mean all these 80 threads are active right now.
[01:45] So behind the scenes IntelliJ might have created all these threads for various purposes.
[01:50] For example, whenever I'm selecting file and save all behind the scenes, a thread may get activated
[01:57] to save the changes inside my file.
[01:59] So for each of the functionality, the intelliJ is going to create multiple threads and all these
[02:05] threads
[02:06] they will be only activated whenever needed and remaining all the time
[02:11] they will be in either waiting time or they will be sitting ideally. So they are not going to consume
[02:17] any of your CPU time.
[02:19] But there is a very good chance that out of these 2500 threads inside my system, at least 20 or 30
[02:27] threads may be active at a time.
[02:29] In this kind of scenario, the computer
[02:32] it is going to give you an illusion that it is processing all your threads parallely, but it is trying
[02:38] to handle all the threads concurrently.
[02:41] So here I'm trying to use various jargons like parallel execution and concurrent execution.
[02:47] Let me try to explain these very important jargons of multithreading by taking an example.
[02:53] As a software engineer, you should have a good understanding about these basics.
[02:58] First, let me try to explain you about what is parallel execution.
[03:02] For the same, let's imagine you have a computer which has only four different CPU cores.
[03:09] So with this system, which has four different CPU cores, you have a scenario where only four different
[03:16] threads are active at a time.
[03:18] So this is a very simple scenario.
[03:20] You have four cores and you have four different active threads handling four different tasks.
[03:26] So here there is no confusion for my computer.
[03:28] So all my four threads, they are going to execute the instructions on four different CPU cores
[03:35] parallely.
[03:36] So when the parallel execution is going to happen when you are active, number of threads is same as
[03:42] your number of CPU cores, then parallel execution come into picture, but most of the times parallel
[03:49] execution is not going to happen.
[03:51] Only the concurrent execution is going to happen because it is really impossible to have only four active
[03:57] threads inside a modern computer.
[04:00] So before I try to explain you how the concurrent execution is going to happen, first let me share
[04:05] you an analogy related to parallel execution.
[04:08] So whenever someone asks you what is parallel execution, you can simply give this example.
[04:14] You can take an kitchen with the four different chefs and these four different chefs
[04:19] they have received four different orders.
[04:23] Since the number of orders is equal to the number of chefs inside the kitchen, their job is very simple.
[04:30] All these chefs, they are going to independently prepare the dishes at the same time parallelly.
[04:36] So this is a perfect example of parallel execution.
[04:39] Now let's try to understand what is a concurrent execution.
[04:44] So this concurrent execution come into picture.
[04:47] If you have more number of active threads compared to your CPU core. Like you can see here, I have considered
[04:53] a example where I have a four different CPU cores, but there are 12 different
[05:00] the active threads
[05:01] they are trying to execute the task at the same time.
[05:04] So in this kind of scenario operating system, it is going to play an very important role.
[05:09] We know that about a basic rule, which is the threads themselves
[05:13] they can't execute the instructions directly on a CPU core.
[05:17] They should always approach the operating system to get a CPU time, or to get any other hardware resource
[05:24] that is required for their execution.
[05:27] So here what is going to happen behind the scenes is, the operating system
[05:31] it will assign all the active threads to multiple cores that it has.
[05:36] In this scenario it has four different cores.
[05:39] So you can see the thread nine, thread 12, 7
[05:42] these three threads, they are assigned to the core one.
[05:45] Similarly the other threads are assigned to the other course.
[05:48] But we know a CPU core can execute a thread at a time.
[05:52] So this is where the magic of concurrent come into picture.
[05:56] So behind the scenes what is operating system is going to do is, it is going to provide a very few seconds
[06:03] or a fraction of seconds of CPU time to the thread 9, and post that immediately it will jump to
[06:09] the thread 12, followed by again it will come to the thread nine, and from thread nine it can jump
[06:15] to the thread 7, and from thread 7 it can jump to the thread 12.
[06:19] So the operating system, it is going to keep on juggling the CPU core across multiple threads.
[06:26] And with that, the end user is going to get an illusion that all the processors or all the threads
[06:33] they are getting executed parallelly. Because all the threads, they are going to get some time randomly,
[06:40] and whenever they get some time from the CPU, they are going to make at least some progress.
[06:45] Since the switching from one thread to other thread, it is going to happen within a fraction of second
[06:51] or within a second.
[06:52] So always the end user will never realize that behind the scenes concurrent execution is happening.
[06:59] I hope you are clear.
[07:00] Let me give you a real time analogy for this as well
[07:04] by taking the same chef scenario. Think like inside a restaurant kitchen
[07:09] there are four different chefs with four different cooking stations.
[07:14] However, they have to prepare two different dishes.
[07:18] So in this case what the chefs are going to do, the chefs, they are going to take turns using the
[07:23] available cooking stations.
[07:25] So whenever a cooking station is not available, the chef may do some other tasks.
[07:31] Maybe behind the scenes he will be standing ideally, or the chef might be performing some other tasks,
[07:37] like cutting the vegetables or cleaning the vegetables, or bringing the plate behind the scenes
[07:42] the chef can do any kind of task till the chef gets his time onto the cooking station.
[07:48] So here also for the outsider, they will get an illusion that all the dishes are getting prepared parallelly.
[07:55] But if you closely observe at a single point of time, only the four dishes are going to be cooked on
[08:02] the cooking station.
[08:03] The same applies for the computer as well.
[08:05] I hope you are clear with the difference between the parallel and concurrent execution.
[08:09] But here you may have a question, which is, why should an operating system should try to execute more
[08:16] number of threads compared to the avail number of cores?
[08:19] Why can't computer keep the other threads wait forever till the given set of threads are getting processed?
[08:27] So you may have this kind of questions, so let's try to understand the same in the next lecture.
[08:33] Thank you,
[08:34] bye.

----------------------------------------
