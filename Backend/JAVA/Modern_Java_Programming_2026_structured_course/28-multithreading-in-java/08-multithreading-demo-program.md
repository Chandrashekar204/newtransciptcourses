# 28.8 — MultiThreading Demo Program

> Section 28: MultiThreading in Java

[00:00] As of now we are simply trying to execute System.out.println() statements as a business logic with the
[00:07] help of Thread.
[00:09] But with these simple logic, we cannot really see the demo of the benefits provided by the Thread
[00:15] inside Java.
[00:16] In order to see the benefits of multi-threading environment inside Java, we need to take some complex
[00:22] business logic.
[00:23] That's why inside this lecture I'm going to show you an example which is complex in nature compared
[00:29] to the System.out.println() statements.
[00:32] So first let me build the business logic without the threads and we are going to calculate how much
[00:38] time the business logic is taking without two threads.
[00:42] Post that we are going to implement the same business logic with the multiple threads.
[00:46] We are going to again see what is the total time it took.
[00:49] And when we try to compare both the times, we will be able to see the benefits of multi-threading inside
[00:56] Java.
[00:56] The business logic that I want to write as part of these lecture is I want to add all the positive integer
[01:04] numbers.
[01:05] So inside Java we have int.
[01:08] Using these int we will be able to represent all the int numbers up to a certain maximum value.
[01:14] So right from zero to the maximum value supported by the int I want to add all of them and the output
[01:22] I want to print them onto the console.
[01:23] So first let's try to build this logic with the help of normal Java method without using threads.
[01:29] So I'll try to create a Java class which is SumOfIntsDemo.
[01:35] So here I'm not using any threads.
[01:37] That's why I'm not mentioning any thread inside the class name. Post that I'm going to create the main()
[01:43] method.
[01:43] Inside this main() method I want to write a for loop and this for loop.
[01:49] It is going to start the index from zero, followed by
[01:53] it has to run this for loop.
[01:55] If the I is less than or equal to the maximum value supported by the integer, and at last I want to
[02:02] increment the index value by one during each iteration.
[02:06] So inside this for loop, I want to perform the addition with the help of these index value.
[02:12] So outside of this for loop I can try to create a variable long with the value as result and zero.
[02:19] We need to make sure the result is of type long, because when we try to add all the positive integer
[02:24] values, definitely the outcome is going to be of type long.
[02:28] That's why in order to accommodate the complete result, I'm trying to create the result variable
[02:33] as long.
[02:34] Now inside this for loop I'm going to write a logic.
[02:37] So during each iteration I will check what is the current result value to the same
[02:42] I'll try to add the index number and the output from this sum I'm trying to assign back to the same
[02:47] variable, which is result.
[02:48] And at last I'll try to print out what is the result onto the console.
[02:54] Inside this for loop there is a bug, which is
[02:56] we're trying to define the i as int, but during the last iteration what is going to happen is, the i
[03:03] is going to be incremented by one.
[03:05] So the max value when we try to increment by one, it may result into the overflow.
[03:10] That's why to avoid that overflow of the int value, we need to declare the i as long.
[03:16] So that's what I'm trying to do here.
[03:17] So now with this we should be good.
[03:20] If I try to execute this program, you will be able to see this is the total result that we are going
[03:25] to get when we add all the positive integer numbers.
[03:29] Now I want to identify what is the total time this program is taking to print the result.
[03:36] So it is very simple.
[03:37] First we need to invoke the System.currentTimeMillis() to know what is the current time in milliseconds.
[03:44] So that's what I'm trying to catch on the left hand side with the variable name as start time of type
[03:50] Long.
[03:50] The same I can try to mention towards the end, but this time I'll mention the variable name as end
[03:57] time, and at last I'll try to have a System.out.println() which is going to print
[04:02] total time taken by normal Java class is colon space.
[04:10] And to this I'm going to append the difference of endTime - startTime.
[04:17] So here I'm getting an error because I need to mention these endTime - startTime inside the parenthesis.
[04:24] So the output from this expression it is going to be added to the String with the help of these String
[04:30] concatenation symbol.
[04:31] So now we are going to execute this program.
[04:33] And we'll be able to see what is the total time it is trying to take.
[04:37] So you can see the total time it took is 692 milliseconds.
[04:42] Let me try to run one more time.
[04:44] This time you'll be able to see 690.
[04:47] If I try to execute one more time.
[04:50] This time you should be able to see 689.
[04:52] So overall we are getting the output around 690 milliseconds.
[04:58] So let's
[04:59] a make a note of this.
[05:00] Now, the same business logic I'm going to build with the help of multiple threads to implement these
[05:07] business logic with the help of multi-threading.
[05:09] First I'm going to create a Java class with the name SumThread.
[05:14] Inside this class I'm going to extend Thread superclass followed by
[05:19] I'm going to override the run() method.
[05:22] So first I need to mention override and below this I'll try to mention public Void run().
[05:30] And inside this run() I'm going to write my for block.
[05:34] So let me copy these four block and paste it here.
[05:39] With this we can't leverage the multithreading because if you see, whenever I try to create an object
[05:45] of this SumThread class, it is always going to perform the addition operation right from zero to
[05:52] the max value.
[05:53] Instead, I want this SumThread class to accept what is the start index and end index to perform the
[05:59] addition, so that I can split this task of adding of all into numbers to multiple threads.
[06:06] So to achieve the same, what I'm going to do is, I'm going to create a couple of instance variables
[06:11] inside the SumThread class.
[06:13] So these variables are private int,
[06:16] what is the startIndex.
[06:18] Followed by I'm going to create one more variable with the name endIndex.
[06:23] And at last we also want to store the result into an instance variable so that when multiple threads
[06:30] are trying to perform the sum operation, we can get the output from each thread and the output from
[06:36] all the threads.
[06:37] We can try to perform addition one more time towards the end, so that we can display the overall output
[06:43] onto the console.
[06:44] So that's why I need to create one more instance variable with the name, result and post that I need
[06:50] to create a constructor of SumThread, which is going to accept to these two variables as an input.
[06:56] So let me create a constructor of SumThread which accept two input parameters, which are
[07:04] int startIndex, int endIndex and
[07:08] inside this constructor I can mention this.startIndex = startIndex followed by
[07:14] this.endIndex = endIndex.
[07:19] Now, instead of hard coding these values inside the for loop, what I'm going to do is I'll try to
[07:24] initialize the I variable with the startIndex.
[07:27] And similarly I will check if i < = endIndex.
[07:32] And similarly I don't need to declare the result as zero every time.
[07:36] Instead I'll just mention result = result + i.
[07:40] But here I'm getting a compilation error because I declared the result data type as int.
[07:45] So let me correct this to long.
[07:46] And with that the compilation error is going to be resolved.
[07:50] So as a next step, whenever we want to create a Thread using this class, we just need to provide what
[07:55] is a startIndex and the endIndex.
[07:57] And it is going to perform the calculations behind the scenes based upon the for loop.
[08:02] So to get these results as an output from our Thread object, we need to define a getter method for
[08:09] the result variable.
[08:10] So I'll just create a getter method which is public log getResult().
[08:15] And inside this method we're simply going to return the result instance variable.
[08:21] I hope this makes sense.
[08:22] Now let me create a class with the name SumOfIntsThreadDemo.
[08:29] So inside these class first I need to create the main() method followed by.
[08:34] I'll try to copy all this code so that we can save some time inside this main() method, let me paste
[08:41] and delete all the unnecessary logic.
[08:44] So I'm trying to delete this for loop.
[08:46] So first what I'm going to do is, I'll try to create an object of SumThread with the variable name
[08:52] as Thread1.
[08:54] So to the constructor of SumThread we need to pass what is the startIndex and what is the endIndex.
[09:00] So I'll just pass startIndex as zero, followed by endIndex as Integer.MAX_VALUE / 2.
[09:10] Similarly, I can also create one more object of SumThread with the variable name as Thread2,
[09:16] and this time I'll just mention the startIndex as Integer.MAX_VALUE/ 2 to the output
[09:26] of this division, I'm going to add the plus one and the endIndex I want to consider as Integer.MAX_VALUE.
[09:34] .
[09:35] So basically what I'm trying to do here with these two thread objects is I try to divide the task between
[09:41] these two threads by giving the first half of the int numbers to the first thread, and the second of
[09:47] the int numbers to the Thread2 object.
[09:50] So when both of them they are going to execute, they're going to perform the arithmetic operation Parallely.
[09:57] And with that we should be able to.
[09:58] See some improvement.
[10:00] So let me invoke the start() method using the Thread1, followed by
[10:04] I'll also going to invoke the start() method using the Thread2, and at last I'll try to get the overall
[10:10] result by invoking the getResult() method using two Thread objects.
[10:16] So that's what I'm trying to do here.
[10:18] And the same will try to print it onto the console.
[10:21] And here let me update the System.out.println()
[10:24] total time taken by multiple Thread Java class.
[10:29] Now if I execute this program you'll be surprised.
[10:33] You can see I'm getting the total time taken by multiple thread.
[10:37] Java class is one millisecond and the result also I'm getting zero.
[10:41] If I execute one more time,
[10:42] this time you can see the result I'm getting one and the total time I'm getting as one millisecond.
[10:48] So there is a problem inside our Java program.
[10:50] So basically what is happening is we are just invoking the threads with the help of the start() method.
[10:57] But we are never waiting for these threads to complete their business logic.
[11:01] Without waiting for these threads to complete their business logic, we're trying to get the result
[11:06] and print the output onto the console.
[11:08] So basically all these four lines of code, they are getting executed before these threads.
[11:14] They completed their business logic.
[11:16] So to fix this issue we need to tell to the main method() or main Thread
[11:21] Please wait for these Thread objects to complete their business logic.
[11:25] So how to communicate that.
[11:27] So there is a method called join() which we need to invoke to let the main() Thread to wait for the Thread
[11:34] objects to complete its business logic.
[11:36] So using both of these Thread objects we just have to invoke the join() method.
[11:41] So let me invoke the join() method
[11:43] similarly, let me do the same for Thread2.
[11:46] I'm getting a compilation error because whenever we are invoking the join method behind the scenes,
[11:50] it is going to throw and checked
[11:52] exception which is java.lang.InterruptedException.
[11:56] For now, let's not worry about handling this exception.
[11:58] Let's simply add this to the main() method signature by just mentioning these throws
[12:04] InterruptedException.
[12:06] After seeing these two lines of code, the main() method, it is going to wait for the threads to complete
[12:12] their business logic and terminate themselves.
[12:15] Post that only the code from line number 14 is going to be executed.
[12:20] So let me execute this program.
[12:21] And this time you can see we got the same output, but the output is completed within three 69 milliseconds.
[12:31] Let me copy these output into a text editor post that let me try to execute one more time.
[12:37] This time you can see around 371 we got.
[12:39] So we can assume a average number which is 370.
[12:42] But if you execute the same with the help of SumOfIntsDemo, where we have not used the multithreading,
[12:49] you'll be able to see the total program.
[12:51] It is taking six 90 milliseconds.
[12:54] So let me copy this output also into the text editor.
[12:58] If you see from both the Java classes we are getting the same output.
[13:02] But the magic is here.
[13:04] The normal Java class
[13:06] it is taking six 90 milliseconds, whereas the multithreading class it is taking almost half of the
[13:13] time only because I used two threads.
[13:16] If I use three threads, the performance is going to be improved further.
[13:20] I hope you are now convinced with the power of multi-threading environment.
[13:25] So inside your projects, whenever you have a scenario where you can leverage threads to perform the
[13:31] business logic, then you can happily create the Thread objects and with the help of Thread objects,
[13:36] you should be able to execute the program with a better performance.
[13:41] I hope this is clear,
[13:42] thank you and I'll catch you in the next lecture, bye.

----------------------------------------
