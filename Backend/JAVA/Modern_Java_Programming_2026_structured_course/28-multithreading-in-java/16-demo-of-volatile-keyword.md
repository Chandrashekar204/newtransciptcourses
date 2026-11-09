# 28.16 — Demo of volatile keyword

> Section 28: MultiThreading in Java

[00:00] To show you the demo of Volatile keyword
[00:03] first, let me create a Java class with the name SharedBooleanResource.
[00:09] So this is a class name.
[00:10] Seems I have a spelling mistake.
[00:12] Let me correct this and post that
[00:15] rename the file also with that
[00:17] now my class name looks good.
[00:19] Now inside this class I'm going to create a boolean variable that is going to be shared by multiple
[00:24] threads.
[00:25] So let me type private boolean and the boolean variable name is going to be stop flag.
[00:31] So initially I'll set the value as false.
[00:34] After creating this variable I'm going to define a method which is public void setStopFlag().
[00:42] And this method it is not going to accept anything, it is simply going to update the stopFlag variable
[00:48] to true.
[00:49] So whenever a thread it is trying to invoke this method, the boolean variable is going to be changed
[00:54] from false to true.
[00:56] After this method, let me create one more method.
[00:58] This time I'm going to mention the method name as public void doWork().
[01:04] So this method it is going to simply do some work.
[01:07] So inside this doWork() method I'm going to write a while loop which is going to keep on monitoring the
[01:14] stopFlag.
[01:15] So whenever the stopFlag is false, since I'm mentioning the Not condition, this while loop is going
[01:21] to be executed.
[01:22] So inside this while loop, I'll just create a System.out.println() with the statement working
[01:28] and outside this while loop I'll also have a System.out.println() saying that work stopped.
[01:35] So if you see here initially whenever a thread invokes this method, it will keep on executing the System.out.println()
[01:44] with the statement working, working, working.
[01:46] And if some other thread update the stopFlag to true.
[01:50] And with that this while condition is not going to be satisfied.
[01:54] And the other thread which is working continuously, it is going to execute this statement which is
[01:59] working
[02:00] stop and it will come out of that execution.
[02:02] I hope you are understanding the purpose of these two methods and these Boolean variable.
[02:07] Since these Boolean variable is going to be shared by the multiple threads, it will be a good position
[02:13] to mark this variable as volatile.
[02:16] So how to do that just after the access modifier and before that data type of the variable.
[02:22] We just need to type volatile.
[02:25] So this is the approach to define a variable as volatile.
[02:28] And with this this variable always going to be written and read from the main memory location by all
[02:35] the threads inside your Java program.
[02:37] So now let me create one more Java class where I can create multiple threads.
[02:43] So the Java class name I'll just mention volatile example.
[02:47] And inside this class first let me create the main() method followed by
[02:52] I'll first create a thread with the variable name as worker thread, and on the right hand side to the
[02:59] constructor of Thread() class.
[03:02] I can pass the lambda expression, but before I try to do that, first let me create the object of
[03:09] SharedBooleanResource.
[03:10] So I'm trying to create the same with the help of default constructor.
[03:13] Now using this SharedBooleanResource, I'll try to write a lambda expression.
[03:19] And inside this lambda expression I'm simply going to invoke the method which is doWork().
[03:24] So you can see this Thread
[03:25] when it is started, it is going to execute the doWork().
[03:28] And inside this doWork() method we have a while loop which is going to be executed continuously when
[03:34] the boolean is false.
[03:35] So here using this Worker thread, I can try to invoke the start() method followed by
[03:40] I can also try to invoke the join() method.
[03:43] So since we are invoking the join() method, we need to make sure we are handling that checked exception.
[03:48] So here I'm trying to add these throw statement to the main() method.
[03:52] So if I execute this method you will be able to see that I keep on getting working because there is
[03:58] no other thread which is going to update the shared boolean variable to true.
[04:03] So that's why let me create one more thread which is going to update the shared variable to true after
[04:10] some time.
[04:10] So here I'm going to create a thread with the variable name as stopThread
[04:17] or maybe I can mention stopperThread.
[04:20] So this name is going to look more better.
[04:22] Now on the right hand side, as usual to the Thread() constructor, we need to pass a lambda expression.
[04:28] So here inside the lambda expression what I'm going to do is first I'll try to make my thread to sleep
[04:35] so that we're not updating the boolean variable immediately.
[04:38] So since we are invoking the sleep() method, we need to make sure we are handling the exception
[04:45] InterruptedException.
[04:45] So that's what I'm trying to handle it with these try and catch.
[04:48] Now what I can do is, after the sleep statement with the help of SharedBooleanResource object, I can
[04:55] invoke the set stopFlag.
[04:57] So this Stopper thread what it is going
[04:59] to do is, initially it is going to sleep, and after that it is going to invoke the set stopFlag.
[05:05] And whenever it is invoking the setStopFlag, this boolean is going to be updated to true inside the
[05:11] main memory location, but not inside the local memory location, because we mark this variable as volatile.
[05:16] And with that, immediately the other thread which is doing this work, it can immediately recognize
[05:23] the latest value from the main memory location and it will stop executing these while statement followed
[05:29] by is going to print this statement and it is going to terminate the execution.
[05:33] So that's what it is going to happen.
[05:34] So let me use the Stopper thread and invoke the start() method followed by I can also invoke the join()
[05:43] method.
[05:44] So now let me execute this program.
[05:46] And ideally the working statement should stop after the three seconds.
[05:50] But still it is running continuously.
[05:52] I know the reason.
[05:53] The reason is we invoked this join() method here and with that this Stopper thread
[05:59] it is always going to wait for this other thread to complete its execution.
[06:03] And since the Worker thread is never going to stop its execution, we are seeing the infinite output.
[06:09] So what I can do is, I can try to bring these statements towards the end.
[06:15] And here also after the start, I'm not going to invoke the join() method.
[06:20] Simply I will start the Stopper thread and after the StopperThread.start() I can mention the join
[06:26] statement related to the Worker thread.
[06:27] So with this we are going to start both the threads at the same time and the main thread where this
[06:32] main program is running is going to wait for these two threads to complete their execution.
[06:37] This time, if I try to execute this program, you'll be able to see within three seconds you'll be
[06:43] able to see that we are getting the output work stopped.
[06:46] So do you see the beauty of volatile?
[06:48] So please always make sure you are using the volatile keyword.
[06:51] If multiple threads, they are trying to leverage the same variable inside their business logic.
[06:57] If you don't use that, you are going to get the same output, but there can be some fractions of seconds
[07:02] delay and sometimes there can be seconds of delay as well.
[07:06] Whatever example that we have discussed so far inside this lecture, I have mentioned the same in this
[07:10] slide for your reference, so feel free to refer the same or GitHub repo for any questions.
[07:15] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
