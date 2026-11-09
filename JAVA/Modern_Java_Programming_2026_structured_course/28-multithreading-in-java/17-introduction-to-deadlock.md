# 28.17 — Introduction to Deadlock

> Section 28: MultiThreading in Java

[00:00] Inside this lecture
[00:01] let's talk about deadlock scenario that may happen in multi-threading Java programs.
[00:07] So what is a deadlock?
[00:09] Before I try to explain you about what is a deadlock, first let me provide you some basics on how threads
[00:14] they are going to work behind the scenes.
[00:16] Whenever a thread want to execute some business logic, or whenever a thread wants to leverage the instance
[00:22] variable available in a object first, the thread will try to get a lock on the object so that no other
[00:28] threads there will be able to modify the same object.
[00:31] So this is what we discussed and implemented with the help of synchronized block or synchronized methods.
[00:37] This deadlock whatever we are going to discuss inside this lecture, it is going to happen in the scenarios
[00:42] when threads they are trying to acquire the lock of a object.
[00:46] So let's try to understand in detail about this
[00:48] Deadlock.
[00:48] Deadlock is a scenario where one of the thread is waiting to acquire the lock of an object currently
[00:55] held by another thread.
[00:57] That means a thread which is t1,
[00:59] it is waiting for a object which is already locked by another thread, which is t2.
[01:05] So the fun is not going to stop there.
[01:07] The actual fun start now.
[01:09] Now the second thread is waiting to obtain the lock of a different object held by the first thread.
[01:17] So consequently, both these threads find themselves in a state of mutual waiting.
[01:23] Expecting each other will release the lock and this will result into a deadlock situation.
[01:28] Let me show you this with the help of an image, so that it is going to be super clear for you.
[01:33] So here I have a thread which is t one and I also have thread t2.
[01:38] So initially t1 locked on a object which is r1.
[01:43] You can think r1 is a resource, it can be an object or it can be any other resource that t1 right
[01:49] now have a lock.
[01:50] And similarly t2 is having a lock on top of r2 object
[01:55] or resource 2 object.
[01:57] As a next business logic, my t one thread it want to get the lock on the r2 resource.
[02:03] So that's why t1.
[02:05] What it is going to do is, it is going to request CPU to provide me the lock onto this resource r2,
[02:12] and it is going to wait for the r2.
[02:15] So during this wait period it is not going to release the lock on r1.
[02:19] The same applies for t2.
[02:21] So t2 right now have a lock on r2.
[02:24] But it is waiting for the new object lock which is on the r1.
[02:28] So in this scenario t2 will go and ask operating system that I want to obtain a lock on r1.
[02:35] And I'm going to wait for the same once I got a lock on r1
[02:38] obviously the lock on r2 is going to be released.
[02:43] So whenever a thread gets a lock on a new object, the old lock will automatically released.
[02:48] But the problem here is t1 has a lock on r1 and it is expecting the lock on r2 until the lock
[02:55] of r2 is achieved by t1, it is not going to release the r1 object, whereas on the t2 the
[03:01] story is different.
[03:02] The t2 it is having a lock on r2, but it is waiting for a lock on r1.
[03:08] So if you see they are waiting forever like t1 is never going to release the lock on r1 until
[03:15] it receives the lock on r2.
[03:17] And similarly r2 is never going to release the lock on r2 until it receives a lock on r1.
[03:23] So this is a deadlock scenario in multi-threading environment.
[03:27] In the next lecture, I'll show you a program where a deadlock will happen and whenever a deadlock will
[03:32] happen, there won't be any progress inside the Java program.
[03:36] So once we saw the demo of deadlock, I'll also show you how to fix a deadlock.
[03:41] And what are the possible options that we have to avoid the deadlock inside multi threading program.
[03:47] Deadlock can be one of the toughest question that you may face in Java interviews.
[03:51] So having a good understanding around these is going to help you to clear your Java interviews.
[03:57] I hope you are clear with what is a deadlock.
[03:59] And I'm assuming you will be able to answer a definition of deadlock to anyone.
[04:04] Before I try to close this lecture, let me show you a couple of memes around deadlock so that it is
[04:09] going to be super clear for you.
[04:11] So this is one of the real life deadlock that may happen in some interviews.
[04:16] So if you see the interviewer, she is trying to ask the candidate saying that, explain me the deadlock
[04:22] and I will hire you.
[04:23] The programmer who attended the interview.
[04:26] This fellow is saying you first hire me, then I'll explain deadlock to you.
[04:31] So this is one of the perfect example that you can say around deadlock scenario, but don't do this
[04:37] inside interview.
[04:37] I'm just trying to shed this on a fun note.
[04:40] Let me show you next deadlock meme.
[04:42] So this you might be seeing lot many times in US city as well.
[04:46] If you see there is a signal and all the roads inside the signal, they are completely blocked and there
[04:52] is no way for the cars to move back.
[04:55] So this is kind of deadlock scenario.
[04:58] In the similar lines we also have
[05:00] another deadlock meme.
[05:01] So this is my favorite one.
[05:03] And in fact it happens many times to me as well.
[05:05] So think like you went to some supermarket to buy some groceries.
[05:10] So here, this woman, she's looking at these fish and she's trying to buy these fish.
[05:16] The catch woman, she's thinking, I need that thing which is sold by her.
[05:21] So she's thinking that in the meantime, she's also telling to her, I'll pretend to look at these until
[05:26] she moves.
[05:27] She don't need these bananas, but she's trying to pretend as if she's looking at them.
[05:31] And she's continuously waiting for this lady to leave from these fish section.
[05:36] But in the third picture, if you see, there is one guy who is waiting for this cat lady to leave because
[05:42] this guy, he wants to buy these bananas.
[05:45] Now, coming to the first lady who is standing at the fish grocery section, she is waiting on this
[05:52] guy.
[05:53] So if you see all three of them, they are waiting for others to move.
[05:57] So this is a funny example of deadlock.
[06:00] Off course, there won't be waiting infinitely in this scenario, but in real multithreading Java programs,
[06:05] the objects that are going to wait infinitely in deadlock scenario and that will result your program
[06:10] to run infinitely.
[06:12] I hope you're clear with the definition of deadlock in the next lecture
[06:15] let's see the demo of deadlock.
[06:17] Thank you,
[06:18] and I'll catch you in the next lecture, bye.

----------------------------------------
