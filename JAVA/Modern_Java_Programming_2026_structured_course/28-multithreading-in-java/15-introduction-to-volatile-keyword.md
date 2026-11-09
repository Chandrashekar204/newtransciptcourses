# 28.15 — Introduction to volatile keyword

> Section 28: MultiThreading in Java

[00:00] In theory, multithreading program may look very simple, but when you start implementing multithreading
[00:05] program inside a real Java application, it is going to become super complex because at runtime we need
[00:13] to handle so many conditions.
[00:15] One such condition is race condition, which we discussed in the previous lectures.
[00:20] In the similar way there are many other conditions also which we need to understand.
[00:24] As a Java developer, you can see this meme perfectly conveys the same.
[00:28] In theory, multithreading is going to be very simple, like like feeding these puppies in a line,
[00:34] but in reality, all these puppies, they are not going to be so disciplined.
[00:38] And the person who is trying to feed them, you need to struggle a lot, because the puppies are going
[00:43] to move from one location to other location.
[00:46] Even the life of the Java developer is going to be like this
[00:49] only when the developer started implementing multithreading inside Java program.
[00:54] Inside this lecture, I am going to discuss one runtime issue that you may face while implementing the
[01:00] multithreading program.
[01:01] And I'm also going to teach you how to overcome the same.
[01:04] Let's consider FIFA game that we can play inside the play station.
[01:08] Many of you might be playing FIFA game inside the play station, so let's consider the same to understand
[01:14] a scenario inside this FIFA game.
[01:17] Think like the developers are trying to use multi-threading program.
[01:20] So there is a thread, one which is going to track the goals made by the players inside this thread.
[01:27] Think like we have a logic which is to update the goal boolean variable to true whenever a goal is made
[01:33] by a player.
[01:34] So initially this variable is going to hold the boolean value false.
[01:39] As soon as a player made a goal, the boolean variable is going to be updated to true value and think
[01:45] like this
[01:46] updation is happened exactly at the time nine hours, 32 minutes 18 seconds, 346 milliseconds.
[01:55] I'll also try to mention Am or PM.
[01:57] So for now let's try to consider am time.
[02:00] I hope you are clear with the job of this thread one.
[02:02] Now let's try to understand the job of another thread which is running inside this program, which is
[02:07] thread two.
[02:08] So this thread two responsibility is to update the score by incrementing the goals value by one inside
[02:14] the thread2
[02:14] there might be some logic with the help of while loop.
[02:18] So this while loop it is going to keep on monitor the variable which is isGoal
[02:24] whenever this variable become true.
[02:26] Inside this while loop, we are trying to increment the goals value by one and after the increment happened,
[02:33] the isGoal variable is going to be reset to false.
[02:36] So this way these two threads are trying to coordinate with each other based upon the shared variable
[02:42] which which is isGoal.
[02:44] So as soon as our goal has been incremented by this thread two, the same is going to be visible to
[02:49] the end user, whoever is trying to play the game.
[02:52] So think like this
[02:53] updation of the goals happened exactly at this point of time.
[02:56] Maybe after delay of ten milliseconds this update happened.
[03:00] So we as a humans, we can't recognize if there is a delay in fraction of seconds or if there is a delay
[03:06] in milliseconds.
[03:08] So this is an ideal scenario which we are trying to discuss in a multithreading environment.
[03:13] But in reality the update is not going to happen so fastly.
[03:18] Sometimes you may have a delay of one second, three seconds, five seconds based upon how busy your
[03:24] system is.
[03:25] So think like there is a three seconds delay in updating the goal.
[03:28] With that, the end user who is trying to play the game, he or she will be easily able to recognize
[03:34] that the score is not getting updated immediately as soon as the goal happened.
[03:40] So this gives some bad experience to the persons who is trying to play this game.
[03:45] But here you may have a question, which is why there will be a delay as soon as this thread update
[03:51] this boolean variable.
[03:52] My while loop can easily recognize it, right?
[03:54] What is the problem here which may result into 3 seconds or 5 seconds or one second delay.
[04:00] So this can be your question.
[04:02] So let me try to explain the same inside multi threading environment
[04:06] whenever we are dealing with the instance variables or any other variables, what is going to happen
[04:11] behind the scenes is all the threads
[04:13] they are going to cache the variables.
[04:16] So what is a cache?
[04:17] Cache is a mechanism using which threads they are going to store the variable values in a nearest local
[04:24] memory location, instead of reading them every time from the main memory location, like CPU heap memory.
[04:30] So what are the threads that are trying to achieve with these caching mechanism?
[04:34] They are trying to achieve some performance improvements by caching the variable values inside the local
[04:41] memory.
[04:41] You might be hearing this caching also very first time.
[04:45] Let me try to explain the same by taking a real life example.
[04:48] Let's go back into 1990s.
[04:51] During 1990s, no one has mobile numbers.
[04:55] Everyone used to use a landline telephone to make a call and not all homes
[04:59] they not have landline phones, only inside few rich peoples house
[05:04] these land phones used to be available. For a common person
[05:08] if he or she wants to make a call to someone else, the person have to walk in into one of the locations
[05:14] where they can make a phone call by paying some money.
[05:18] So in this kind of setup, think like there is a student with the name Adam.
[05:23] So he is studying somewhere in a different country and he will try to talk with his parents regularly.
[05:31] So here, whenever he want to call his parents landline number, he will walk into the nearest shop
[05:36] where he can make a call, and he's going to look for what is the landline number of his parents.
[05:42] So there are two approaches for him to look for the landline number.
[05:45] The very first approach is, he can write it on a piece of paper, and he can carry the same piece of
[05:51] paper every time he's trying to make a call to his parents.
[05:54] So this is one approach.
[05:55] And the second approach is, he can memorize that number inside his mind.
[06:01] So these are the two different approaches.
[06:03] So which approach do you think is faster and efficient.
[06:06] Off course the approach2 itself is efficient because if he memorize them number, he will be able to
[06:13] easily recollect whenever he wants very quickly.
[06:17] And he will not have any dependency on the paper and he don't have to carry it as well.
[06:21] So the caching also is going to work very similarly.
[06:25] If a thread stores a variable inside the local memory, it is like its brain, where it can read the
[06:30] variable very quickly without relying on the CPU main memory.
[06:35] But here you may have a question which is, when this thread2
[06:38] to initially try to execute this logic, it is going to read the isGoal variable from the main memory,
[06:44] and the main memory is going to have the value as false and this false value
[06:49] my thread2
[06:50] it is going to cache it inside its local memory. With this local cached value
[06:54] this while loop is never going to be executed.
[06:57] And with that there is no meaning for my thread2 to continuously run behind the scenes with a local
[07:03] cached value.
[07:04] So this can be your question.
[07:05] So it's a great question.
[07:06] Let me try to answer the same.
[07:08] Whenever a thread is trying to cache a value, it is not going to retain it forever.
[07:13] Instead, at a regular intervals of time, it is going to recheck the variable and its value inside
[07:20] the main memory location.
[07:22] If there is a change inside the value, then obviously it is going to copy the same into the local cache
[07:27] value.
[07:28] So, based upon how frequently a thread is trying to read the value from the main memory location accordingly,
[07:34] there can be a delay between this thread1 and thread2 output.
[07:39] So if there is a delay of five seconds by this thread2 to read this variable value from the main
[07:45] memory location, then obviously the five seconds delay will happen in incrementing this goal.
[07:52] And the same delay is also going to happen in displaying the latest goal value onto the screen.
[07:56] So think like this thread one
[07:58] also cached.
[07:59] This is goal value into the local memory location.
[08:02] If it is trying to update these variable to true in its local memory location at this point of time,
[08:10] and maybe after three seconds if it is trying to write the same into the main memory location, then
[08:16] obviously the time at which the latest value is going to be available will be plus three seconds to
[08:22] these initial time.
[08:24] It will be 9 hours, 32 minutes, 21 seconds and 346 milliseconds.
[08:30] So this is the time at which the main memory location variable value is going to be updated.
[08:36] Now think like my thread2
[08:38] it is taking five seconds regular interval of time to read the value from the main memory location and
[08:44] update the same into the local memory.
[08:46] So with that there will be five more seconds
[08:49] delay will be added in reading this variable inside the thread2 and to this, if you try to add
[08:55] five seconds, it will be 9hours, 32 minutes, 26 seconds, 346 milliseconds is going to be
[09:04] the time, and if it is taking ten more milliseconds to update this counter, then obviously the time
[09:10] at which this counter is going to be updated is 9hours, 32 minutes, 26 seconds, 356 milliseconds.
[09:18] So if you see here the actual goal happened at this point of time, but due to the fact that all these
[09:24] threads, they are trying to cache the variable value inside the local memory, this delay happened.
[09:30] So total there is a delay of around eight seconds here.
[09:34] So this is some scenario that I'm trying to mention here.
[09:37] But in reality the delay can be one second or two seconds or point five seconds, regardless of whatever
[09:43] is the delay
[09:44] the problem that we have right now here is the threads
[09:48] whenever they are dealing with the variables which are stored inside the local memory location, there
[09:53] is a very good chance that the outputs may get delayed by some seconds.
[09:58] So if you have these kind of
[09:59] there were multiple threads that are trying to use a common shared variable.
[10:04] In all such scenarios, you can use the volatile keyword.
[10:08] So whenever you're trying to declare an instance variable that can be leveraged by multiple threads
[10:12] instead of defining it normally you can mention the volatile keyword inside the variable declaration
[10:19] code.
[10:20] So with that, what is going to happen whenever a variable is marked as volatile, then the threads,
[10:26] they are never going to cache that variable.
[10:29] They always going to read the variable value from the main memory location only.
[10:34] Even the visibility of the thread is going to be immediately, because there is no caching involved.
[10:40] When it is trying to update the boolean variable immediately, it is going to overwrite the value inside
[10:45] the main memory location and post that immediately the thread2
[10:49] since it is reading the value from the main memory itself, there won't be any delay, and with that,
[10:55] the output is going to be visible to the end user immediately.
[10:59] So please use this volatile keyword in the scenarios where an instance variable is being shared across
[11:05] multiple threads.
[11:06] But don't try to over use it because you know, the drawback of using the volatile keyword is the threads
[11:12] are not going to cache the variable inside their local memory, and with that you may see some fraction
[11:17] of seconds performance issues.
[11:19] I hope you are clear with the scenario and the purpose of volatile keyword.
[11:23] In the next lecture, let's try to understand how to define a volatile keyword, and we can also see
[11:28] the demo of the volatile keyword.
[11:30] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
