# 28.14 — Demo of synchronized methods and blocks

> Section 28: MultiThreading in Java

[00:00] Inside this lecture, I'm going to show you how to solve the race conditions with the help of synchronized
[00:06] keyword.
[00:06] Before I try to show you the demo of synchronize, first let me build a multithreading program without
[00:13] using synchronized.
[00:14] And in the same process I'll be showing you an output which occurred due to race condition.
[00:19] Post that we'll try to fix it with the help of synchronized keyword.
[00:22] Inside my package, I'm going to create a Java class with the name Counter.
[00:28] So inside this Counter I'm going to create a private integer variable with the name count.
[00:36] Maybe what I can do is, I'll try to assign an initial value zero post.
[00:40] Creating this count variable
[00:41] let me create an getter method for my count variable.
[00:46] So here let me select the getter option and generate the getter method.
[00:50] After the getter method, I'll try to write a method which is public void with the name as
[00:59] incrementUnSynchronized()
[01:00] So to this method it is not going to accept anything as an input parameter.
[01:05] What this method is going to do is, it is simply going to increment the Counter by one.
[01:10] So this is a simple class which has a instance method which is going to increment the counter value
[01:16] by one.
[01:17] Now using this Counter class let me build some multi-threading program for the same.
[01:22] Let me try to create another Java class with the name UnSynchronizationExample.
[01:30] Seems I have a spelling mistake inside my class.
[01:32] Let me correct this s y n c h r o n i z a t i o n.
[01:39] So UnSynchronizationExample.
[01:41] So let me rename the file as well.
[01:43] Now the class name looks good.
[01:45] Let me create the main() method.
[01:46] And inside the main() method first I'm going to create an Runnable object with the variable name as
[01:54] unSynchronizedTask.
[01:56] So to this Runnable object I'm going to assign a lambda expression.
[02:00] Inside this lambda expression I'm going to simply invoke the method of counter().
[02:05] So to invoke the counter() method first we need to create the object of Counter with the help of default
[02:11] constructor of Counter().
[02:12] So inside my lambda expression,
[02:15] first I'll try to define the for block with the int I is equal to zero, followed by i < 1000,
[02:23] followed by i++.
[02:25] And inside this for block I'm going to invoke the incrementUnSynchronized() method.
[02:31] So basically what is going to happen is, whenever a thread is using this business logic, it is going
[02:35] to iterate these for loop 1000 different times, and it is going to increment the counter by 1000 times.
[02:41] So with that we should get the counter value from thread as 1000.
[02:46] Now using these UnSynchronizedTask object, let me create multiple threads like
[02:51] first I'll try to create a thread one and to the constructor of Thread() I'll try to pass the object which
[02:57] is UnSynchronizedTask.
[02:58] Similarly, let me create one more thread with the variable name as thread 2 post that
[03:03] I'll try to start both of these threads by invoking the start() method.
[03:08] So let me repeat the same code and replace this variable.
[03:11] Name two thread 2 and after this I want to invoke the join() methods using both of these thread objects,
[03:17] because I want my main() method to wait for the complete execution of thread one and thread 2.
[03:24] So that's why let me invoke thread1.join().
[03:28] Similarly, I'll try to invoke the same join() method with the help of thread2.
[03:32] So since we are invoking the join() method, we need to make sure we are handling this exception or we
[03:37] are adding this to the method signature.
[03:39] So let me click on this solution.
[03:42] And with that this throws will be added to the method signature.
[03:46] Post that I'll try to print out the counter value with a statement UnSynchronized Count Value.
[03:56] After that colon followed by I'm going to invoke the getCounter() method available inside the Counter
[04:04] object.
[04:04] So basically what is happening here is, both these threads.
[04:08] they'll try to update the same count variable with the help of these increment unsynchronized.
[04:14] So since I'm not using any synchronized keyword inside this method signature.
[04:19] So there is a good chance that my threads might be updating this count variable at the same time.
[04:26] with that, we should get an unexpected output.
[04:29] Ideally, if both of these threads they execute this method only at once.
[04:34] We should get the count value as 2000, because thread one is going to execute this first block 1000
[04:40] times and thread two also, it is going to execute this third block for 1000 times, but we're not
[04:44] going to get 2000.
[04:45] Let me confirm that by executing this program, you can see we are lucky we are getting count as 2000.
[04:52] Let me re-execute one more time.
[04:54] This time you can see 1634 we are getting.
[04:57] Let me execute one more time.
[04:58] This time I'm getting
[05:00] 1883.
[05:01] If I execute one more time, I'm getting 2000.
[05:03] So sometimes the race condition is happening and due to that we are getting incorrect value.
[05:10] Ideally we should get always 2000 as an output.
[05:13] So let me spend a few minutes explaining you what is happening behind the scenes.
[05:17] Think like
[05:17] initially the count value is zero and thread one will try to increment this two one.
[05:23] This way the thread one might have made a good progress, and it might have reached to a level where
[05:30] like for 450 is a counter. But at some point of time
[05:33] thread two also will try to execute the same logic, and thread 2 might have fall behind the thread 1
[05:40] and it might have the counter value as 435.
[05:44] So whenever it is trying to increment these 435 value the previous value, which is 450, it is going
[05:50] to be overwrite it with 435.
[05:52] And with that even the thread 2 also is going to use the value which is 435.
[05:58] So this kind of race condition is happening right now because this method, which is increment unsynchronized
[06:05] sometimes it is getting executed by both the threads at the same point of time due to the race condition.
[06:12] So let me execute this example one more time.
[06:14] You can see we are getting 1348
[06:16] sometimes we are getting 1922 and sometimes we are also getting 1808.
[06:21] So the output is not like we are expecting.
[06:24] So to resolve this issue it is very simple.
[06:27] We just have to mention the synchronize keyword just before this return type.
[06:31] Maybe what I can do is, I'll try to copy this method and mention synchronized just before the void,
[06:39] and rename this method to increment synchronized.
[06:42] Now I will try to copy this class, which is UnSynchronizedExample, and paste it inside the same package.
[06:50] And this time I'll mention the class name as
[06:53] SynchronizationExample.
[06:54] Now inside this class I'm going to rename this variable name to SynchronizedTask and at the same time
[07:01] I'll also try to invoke the incrementSynchronized() method.
[07:06] So let me mention the synchronized task variable for both of the threads.
[07:10] So this time if I try to execute this class every time I should get the output as 2000.
[07:17] So let me confirm that here you can see I'm getting 2000.
[07:20] I'm trying to execute one more time 2000.
[07:22] and I'm trying to execute one more time.
[07:24] So always I'm getting 2000, 2000, 2000.
[07:27] So this is because due to the beauty of these synchronized keyword that we are using inside the method
[07:35] signature
[07:35] So this is the demo of synchronized keyword as part of the method signature.
[07:40] But instead of mentioning the synchronized keyword inside the method signature, we can also mention
[07:44] as part of a block.
[07:46] So what is a block?
[07:47] A block is a code which is present inside a method.
[07:49] It can have any number of instructions.
[07:52] So just before this block you need to type synchronized followed by
[07:56] inside the parentheses
[07:57] you need to mention your class name which is Counter.class.
[08:02] So if needed you can mention this count+++ inside the synchronized block.
[08:08] So with this you don't need to use the synchronized keyword inside your method signature.
[08:13] Now if I try to execute the synchronized example I'm going to get the same kind of output.
[08:18] You can see every time I'm getting that 2000 as an output.
[08:22] So with that you may have a question which is under which scenarios I need to use synchronized block
[08:27] and under which scenarios I need to use the synchronized () method.
[08:30] The answer is very simple if you want to make sure only if you set off lines to be executed by one thread
[08:37] at a time, then you can always use the block.
[08:40] And inside this block you can mention one line, two lines or five lines.
[08:44] It's up to you anything outside the synchronized block.
[08:47] It is going to be executed by multiple threads at a time.
[08:50] But if you are looking for an entire business logic which is present inside, a method needs to be executed
[08:56] by one thread at once, then obviously you can mark that entire method as synchronized by mentioning
[09:03] the synchronized keyword just before that return type.
[09:06] I hope you are clear.
[09:07] Let me revert back to the synchronized() method, and I'll try to mention these synchronized block for
[09:14] your reference by commenting it, and post that inside the method
[09:18] I'll try to mention count++. So please refer them for any questions.
[09:23] And I'm assuming you are clear how synchronization is going to help us to avoid the race conditions.
[09:30] Whatever examples that we have discussed so far inside this lecture, one with the help of unSynchronized
[09:34] method and the other one with the help of synchronized method.
[09:37] Both of them I have mentioned in these two slides for your reference.
[09:41] You can also find the code inside the GitHub repo as well.
[09:45] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
