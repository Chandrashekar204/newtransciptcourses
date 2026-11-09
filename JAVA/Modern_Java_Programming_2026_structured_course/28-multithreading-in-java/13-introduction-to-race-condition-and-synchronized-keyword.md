# 28.13 — Introduction to Race condition & synchronized keyword

> Section 28: MultiThreading in Java

[00:00] Building a Java program with the help of multithreading concept is somewhat complex compared to normal
[00:06] Java program.
[00:07] The reason is very obvious when multiple threads they are trying to execute your business logic parallely.
[00:13] You may need to handle lot many conditions or lot many complexities that your program may face at runtime.
[00:21] One such important complexity is race condition.
[00:25] So whenever you are dealing with the multiple threads, your program may have a race condition.
[00:32] So first let's try to understand what is this race condition.
[00:35] And later on we can try to understand how to handle these race condition.
[00:39] The race condition happens when two threads which are trying to access a shared variable at the same
[00:47] time.
[00:47] So both these threads like first thread and the second thread, they read the same value from the variable.
[00:52] But at later point of time when these threads, they want to update the same shared variable
[00:58] then a race condition will happen.
[01:01] Think like when both these threads they are trying to update the shared variable at the same time.
[01:06] They will be racing with each other to see which thread is going to write the latest value into the
[01:13] shared variable.
[01:14] So the value of the thread that writes its value at the end is going to be preserved.
[01:19] For example, think like
[01:21] initially the shared variable has a value as zero at later point of time.
[01:26] The same shared value is going to be updated by the thread one to the number ten.
[01:31] Here in the race condition, the thread one wins because it is able to first update the value inside
[01:38] the shared variable, though it wins the race, but its value is going to be overrided by the other thread,
[01:44] because thread two is going to overwrite the value present inside the shared variable with the new value
[01:51] at a later point of time.
[01:52] So this is a race condition.
[01:54] Let me give you an example so that it is going to make more sense to you.
[01:58] Like you can see here, I have a map with the name reserved tables.
[02:02] So inside this map think like we are going to store the table name as a key.
[02:08] And who reserved that table as a value.
[02:11] Think like this Java program that I'm showing right now
[02:14] it is going to be executed in some restaurant web application.
[02:18] So the restaurant has a booking functionality inside their web application.
[02:23] There is a very good chance that two multiple users may try to book the same table at the same point
[02:30] of time.
[02:31] So in these kind of scenarios, what is going to happen is thread one.
[02:35] It is going to check if these reserved table map contains the key table one.
[02:40] So indirectly it is checking if there is any one reserved that table one.
[02:44] Since these reserved table initially it is an empty map.
[02:48] So this condition inside the if condition it is going to give false.
[02:52] If we apply the Not condition on top of the false, the overall condition of this if condition is going
[02:57] to become true and the logic present inside this if block is going to be executed at the same time behind
[03:03] the scenes.
[03:04] Thread 2
[03:04] also, it is going to run the same logic.
[03:08] It is checking whether the reserved tables contains that table one as a key, since initially it read
[03:15] the reserved table which is an empty here
[03:18] also, this if condition is going to be executed and this thread 2
[03:22] also it is going to update the table one with the user two.
[03:25] So if you see here both these thread 1 and thread 2, they try to update the same shared variable
[03:31] at the same point of time with just a few fraction of seconds difference.
[03:36] In this scenario, let's assume the thread one wins the race and it wrote the value which is user one
[03:42] to this table.
[03:43] And with that the user one
[03:45] he is going to get a message inside the website saying that hey, congratulations, you reserved that
[03:49] table one.
[03:50] And with that message, the end user will be under the assumption his reservation is completed successfully.
[03:56] But behind the scenes, what happened just after few fraction of seconds?
[04:00] The thread 2 it tried to overwrite the reservation with the new user, which is user 2.
[04:06] So with this logic, if both these user one and user two go to the restaurant at the given time, only
[04:13] the user two will be able to get the table 1 because the user one data is overriding by the thread 2
[04:19] .
[04:20] So this is one of the serious problem that you may face while you are trying to implement a logic with
[04:25] the help of multi-threading environment.
[04:27] The problem here we have is, there is a shared variable which is the reserved tables HashMap.
[04:33] Both these threads are trying to update these reserved table at the same time.
[04:37] When they are trying to update the variable at the same time, obviously they both will not be able
[04:42] to write at the same time, just with a fraction of seconds difference.
[04:46] Both of these threads, they are going to write their values and whatever thread committed the value
[04:51] at the end, its value is going to be maintained inside the shared variable.
[04:56] So how to resolve this race condition?
[04:58] It's very simple
[04:59] we
[05:00] need to take the help of synchronized keyword like we discussed briefly in the previous lecture.
[05:05] Synchronized keyword is used to control the access of multiple threads to the shared resources.
[05:12] So whenever we are using this keyword, it is going to ensure that only one thread can execute a synchronized
[05:19] block or a method at a time.
[05:21] So the synchronized keyword can be used in two forms.
[05:24] You can use the synchronized keyword along with the block of code.
[05:28] Whenever you have some complex logic which needs to be executed by only one thread at a time.
[05:34] In such scenarios, you are going to keep all such complex logic inside the curly braces.
[05:39] And just before this curly braces, you're going to mention the synchronized keyword along with the
[05:44] shared object that you're trying to write.
[05:47] So with that, this synchronized block ensures that only one thread at a time can execute the code within
[05:53] the block.
[05:53] So if you try to apply the same synchronized keyword logic with the previous example, what we have
[05:59] to do is we need to keep these shared variable logic inside the synchronized block.
[06:05] And with that, only a one thread will be able to read and overwrite at a time while the thread1
[06:11] is doing the reading and writing operation on the shared object, the thread2
[06:16] it is going to keep waiting as soon as the thread1 completes the execution of this synchronized block,
[06:22] then thread2 will enter into the synchronized block.
[06:25] So this is how it is going to work.
[06:27] So we need to use the synchronized block.
[06:29] Whenever you have some piece of code which needs to be executed by one thread at a time.
[06:34] In the similar lines, you can also apply the synchronized keyword on top of a method itself.
[06:40] If you want your entire method to be executed only one thread at a time, then you can mention the synchronized
[06:47] keyword
[06:47] just before the return type of your method.
[06:50] You can use the synchronized keyword on top of the static methods and on top of instance methods.
[06:54] So whenever a method is declared as synchronized, it implicitly uses the Object instance at the class
[07:01] object as a monitor.
[07:02] I hope you are clear with this.
[07:04] I also mentioned a picture here, saying that threads are going to wait for their chance to execute
[07:09] this method, or to execute these block.
[07:12] This way we can avoid the conditions like race conditions.
[07:16] Inside the next lecture, we can see that demo of the synchronized block by taking an example so that
[07:22] it is going to be super clear for you.
[07:24] Thank you,
[07:25] and I'll catch you in the next lecture, bye.

----------------------------------------
