# 28.5 — How multiple threads improve performance

> Section 28: MultiThreading in Java

[00:00] Inside this lecture, let's try to understand how multiple threads they are going to improve the performance
[00:07] and under which scenarios
[00:08] we should not go for the multithreading. Like we discussed in the previous lecture, if you consider
[00:14] a computer which just has four CPU cores at most, these computer can execute four parallel threads
[00:21] simultaneously.
[00:23] However, you may have a question which is then why do applications often create hundreds of threads?
[00:31] What are the applications that are going to achieve by creating hundreds of threads?
[00:34] Why not limit the number of threads to match the CPU core count?
[00:38] So you may have all these questions.
[00:40] So let's try to answer all of your questions by trying to discuss in detail about threads.
[00:46] So whenever a thread want to execute a task, the task can be categorized into two categories.
[00:53] The very first one is CPU-bound and the other category is IO-bound.
[00:59] IO means input and output, so all the tasks that requires computational power from the CPU, such as
[01:08] Arithmetic operations, logical processing operations, and relational calculations.
[01:13] So all these kind of calculations and operations, since they need CPU power, we can call these kind
[01:20] of tasks as CPU-bound task.
[01:23] On the other hand, we also have IO-bound tasks which are highly dependent on input output operations.
[01:31] For example, if you're trying to play a YouTube video inside your Chrome browser, it is not a CPU-bound
[01:36] task,
[01:37] it is a IO-bound task because the browser in this scenario it does not require the CPU time
[01:43] instead, it is going to rely on the network of your system to load the video from a remote server.
[01:50] So any task which which involves communication over a network, or reading or writing operations onto
[01:56] a file or onto a remote server.
[01:58] So all these kind of tasks we can consider them as IO-bound task.
[02:03] So basically whenever a thread is executing a CPU-bound task only in such scenarios, only the thread
[02:12] needed a CPU time or a CPU core time.
[02:15] And while IO task is being executed, the thread is not going to do any job.
[02:21] It is going to sit ideally behind the scenes because IO-bound tasks, they are going to be executed
[02:27] based upon the network of your system.
[02:30] So let's try to understand more details about the CPU-bound and IO-bound task.
[02:34] So first I'm going to take a scenario where it involves only CPU-bound tasks.
[02:40] Think like I have a scenario where I want to perform some mathematical calculations.
[02:46] Maybe to my program, I might have given a larger data set as an input, and based upon this large data
[02:53] set, the program has to generate some complex statistical models, all without engaging in any input
[03:02] or output operations.
[03:03] So this is a scenario where it requires only the CPU-bound to task.
[03:08] And the similar lines
[03:09] I'm also going to give one more example.
[03:11] So this time consider a scenario where I have a combination of both the CPU and IO operations.
[03:18] For example, think of a program where it is going to fetch the data from a remote database.
[03:24] So fetching the data from a remote database involves IO-bound tasks because the data has to be transmitted
[03:32] over the network.
[03:33] So once that data is received by my thread, it has to perform some complex calculations.
[03:39] So since calculations requires a CPU time, we can consider the second step, which is the complex calculations
[03:45] as a CPU-bound task.
[03:48] And after the calculations are completed, we have the final step, which is the results that are derived
[03:53] from the second step.
[03:54] They need to be sent to the other remote server.
[03:57] So when we want to send the results to another remote server, it again involves IO-bound tasks.
[04:04] So this example, it is a combination of both the CPU-bound task and the IO-bound task.
[04:09] Similarly, you may also have a scenario where you are performing only the IO-bound related tasks.
[04:16] I'm not considering that example, because if you are performing only the IO-bound tasks, your software
[04:21] or your program is never going to create the threads because threads are only required whenever we are
[04:26] trying to execute the CPU-bound task.
[04:30] I hope it is clear.
[04:31] Now let's try to discuss more details by taking these two examples.
[04:35] In the very first example where we are trying to perform only the CPU-bound task.
[04:40] So to handle this scenario, since I have a large data set and since I need to perform lot many calculations
[04:46] think like 12 different threads are created to execute all my CPU-bound tasks.
[04:52] Since all these 12 threads can't be executed at the same time behind the scenes, the operating system
[04:59] it is going give me
[05:00] the CPU time randomly
[05:02] So here under the CPU core one you can see we have threads like nine, 12, seven.
[05:07] So randomly my operating system, what it is doing is first it is giving some time to the thread nine
[05:12] to perform some calculations, post that immediately it is trying to switch to the other thread.
[05:18] So the switching from one thread to other thread by the operating system we call that as context switch.
[05:25] So in this example we have purely CPU tasks.
[05:29] And that's why my threads are always busy.
[05:32] But the problem right now I have is my operating system is keep on switching from one thread to other
[05:38] threads so that it can achieve the concurrency, and nowhere it is giving a specific dedicated time
[05:45] to a given thread.
[05:46] It is keep on context switching, and since the operating system is doing lot of context switching,
[05:52] obviously in this scenario, creating 12 different threads may not be super efficient because the more
[05:59] number of threads you are trying to create, if you have only CPU-bound tasks, then the more number
[06:05] of context switches is going to happen by the operating system.
[06:08] And whenever the context switch is happening from one thread to other thread behind the scenes, it
[06:13] is going to take some milliseconds of time.
[06:16] It can be 1 millisecond or 2 millisecond, so that kind of unnecessary switching is going to happen.
[06:22] That's why whenever you have purely CPU-bound tasks, don't try to create too many threads.
[06:29] We should go with a limited number of threads.
[06:32] Maybe in this scenario, having the four threads only is sufficient with the four threads, the context
[06:39] which is not going to happen, and all the course they are going to give a dedicated time.
[06:43] And with that the data is going to be processed fastly.
[06:47] Now with this discussion, you might be under the assumption always we should try to create the threads
[06:53] which are same to the number of cores available.
[06:56] But this is not going to be true always.
[06:58] Let me share more details around this.
[07:00] So with the discussion that we have done, you might be under the impression for the example two that
[07:05] we have where we are trying to read the data from database post, that we are trying to perform the
[07:10] complex calculations, and after the complex calculations, we are trying to send the results to a remote
[07:15] server.
[07:16] So in this example, think like you are only using the four threads which are matching to the four CPU
[07:23] cores.
[07:23] With this, let's try to understand what is going to happen.
[07:26] So first we are going to perform the IO operation to read the data from the DB.
[07:30] So since this is a IO operation during the IO operation, the CPU core is going to be free because
[07:38] no other thread is right now assigned to this core.
[07:41] So once this reading of the data from the database is completed immediately, I have a calculation task
[07:48] which requires a CPU time.
[07:49] So this is the place where the thread will be assigned with a CPU time.
[07:54] And at this point of time, which is highlighted in green color, the CPU is going to be utilized properly.
[08:02] Again, after this calculation, my thread is going to enter into the idle state, or it is going to
[08:07] enter into the waiting state because the next operation is IO operation.
[08:12] So during this I o operation also where we are trying to send the data to the remote server.
[08:16] Since this is a I o operation, again CPU is going to be free.
[08:20] So if you try to create only four different threads for four different cores for this example, then
[08:27] you are wasting a lot of CPU core time.
[08:30] Most of the time you are keeping your CPU core free.
[08:34] So that's why in this kind of scenarios where you have a mix of CPU and IO, it is always recommended
[08:42] to create more number of threads.
[08:44] So let's try to understand by taking the same example, this time with the 12 different threads.
[08:50] So this time you can see all the IO operations
[08:53] they are going to happen behind the scenes.
[08:56] I have not mentioned them in this diagram. So think like
[09:00] initially thread nine is performed some CPU operation like calculation post that it is trying to send
[09:06] the results to some other remote server, which is a IO operation.
[09:10] So during the IO operation, obviously thread nine is going to be idle and it is not going to require
[09:16] any CPU time.
[09:17] And with that the operating system immediately it can switch to the other waiting thread like thread
[09:24] 12 with the help of this context switch concept.
[09:27] And similarly, when our thread two done with its calculations and it is waiting for some IO operation
[09:32] to complete, the next thread is going to get the CPU time.
[09:36] So with this, whenever a thread is waiting for an I o operation to complete behind the scenes, my
[09:42] operating system is not wasting the CPU time.
[09:45] Immediately it is trying to switch to the other thread.
[09:48] It is trying to provide that CPU time to another thread.
[09:51] So this way we are going to use the CPU time efficiently.
[09:56] Nowhere we are going to waste the CPU time.
[09:59] So if you see here, based upon the scenario that you are into, you need to choose the number of threads
[10:05] that you want to create.
[10:06] For example, in the initial arithmetic calculation task where we have only the CPU-bound tasks, having
[10:13] the four threads only will improve the performance instead of 12 threads.
[10:17] But if you follow the same strategy for this example where you have a lot of I o operations, you are
[10:23] going to have some performance issues.
[10:25] That's why in this example two, we need to create a more number of threads so that your CPU time is
[10:31] not going to be wasted.
[10:32] Whenever a thread is waiting for some I o operation to complete.
[10:35] So the thumb rule is always if you have higher IO-bound tasks, try to create more number of threads
[10:42] to achieve the efficiency.
[10:43] With this discussion, I am assuming you are clear about when to use higher number of threads and when
[10:50] to use lesser number of threads.
[10:52] Always whenever into a scenario where you need to build a program that leverages multiple threads,
[10:58] you don't have to worry much.
[11:00] First, start with the two threads, or three threads or four threads.
[11:03] If you are satisfied with the results, then you should be good.
[11:07] But if you received a feedback for better performance, then obviously you need to increase the number
[11:13] of threads.
[11:14] So this way you can always go with that trial and error approach.
[11:18] I hope this makes sense to you.
[11:20] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
