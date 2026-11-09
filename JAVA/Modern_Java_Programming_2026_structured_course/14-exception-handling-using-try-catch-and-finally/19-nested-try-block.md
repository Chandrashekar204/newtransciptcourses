# 14.19 — Nested try block

> Section 14: Exception handling using try, catch and finally

[00:00] Just like how we can write a nested if block nested for loop nested while loops.
[00:06] Very similarly, inside Java we can define nested try blocks as well.
[00:11] For example, here you can see a sample code that I have written.
[00:15] So there is a main try block which is trying to execute a piece of code.
[00:20] And to this main try block we have a catch block which is handling the exception with the object reference
[00:27] name as Ee3.
[00:28] Inside this main try block we have statement one and statement two.
[00:32] But when we are trying to execute this statement three and statement four, we have another nested try
[00:39] block.
[00:39] The reason why we will develop these kind of nested try blocks is,
[00:43] imagine if there is an exception happens inside this statement three or statement 4.
[00:48] In such scenarios, we don't want to affect the execution of our try block.
[00:53] Maybe after these second try block at the end, I may have other statements like statement 7, statement 8.
[01:00] .
[01:01] So if I want to make sure that the statements that I'm trying to execute as part of this second try
[01:07] block should not affect the execution of the statements that I have inside the outer try block.
[01:11] In such scenarios, we can use this nested try block concept.
[01:16] So inside the second try block I'm trying to execute statement 3 and statement 4.
[01:20] If there is an exception happen at this point of time, the catch block with the object reference e1
[01:27] is going to handle the same.
[01:28] And inside the second try block I have another nested third try block.
[01:33] So it is going to execute the statements with the number statement 5 and statement 6.
[01:38] If there is some issue happen at this point of time, the innermost catch block with the object reference
[01:45] e2, it is going to handle the exception.
[01:47] So this way we can always write any levels of nested try blocks.
[01:53] The purpose of nested try block is we don't want to propagate the exception to the outer try block,
[01:59] or to the method.
[02:00] For example
[02:01] here, if there is something happening in the third nested try block, the exception is not going to
[02:07] be propagated to the second try block or to the top try block or to the method.
[02:12] The reason is we are handling the exception with the help of this catch block.
[02:17] Let me show you the demo of nested try block very quickly.
[02:20] For the same, I'm going to create a new Java class with the name NestedTryDemo.
[02:25] Inside this class I'm going to paste a few lines of code just to save some time.
[02:29] You can find this class inside the GitHub repo as well, but don't worry, I'm going to discuss line
[02:35] by line.
[02:36] You can see from the main() static method
[02:38] I'm trying to invoke another static method inside the same class with the name nestedTryBlock().
[02:43] Inside the nestedTryBlock() I have two different try block
[02:46] this is the outer try block, whereas it has its own catch and finally block.
[02:51] Now inside the inner try block or in the nested try block, I have a code which may throw
[02:57] ArithmeticException because I'm trying to do that division with zero.
[03:01] With this the inner try block it is going to have the exception.
[03:05] And since we have its own catch block, this catch block and finally block is going to be executed.
[03:11] And this statement is not going to be executed because we are getting the exception at this point of
[03:17] time.
[03:17] So once this exception is handled as part of the nested try block, the outer try block execution is
[03:24] going to complete as usual.
[03:26] That means this statement is not going to be affected in any manner, even though there is an exception
[03:32] happened inside the inner or inside the nested try block.
[03:36] Let me execute this program by debugging line by line.
[03:40] First, I'm going to keep a breakpoint inside my nested try block.
[03:43] Now I'm trying to execute this program.
[03:45] You can see right now this statement is going to be printed post that we are going to enter into the
[03:52] next try block.
[03:53] And here we are going to print the statement which is inner try block start.
[03:57] Next I'm going to execute the statement which may result into the ArithmeticException.
[04:02] That's why the next System.out.println() we have
[04:05] it is not going to be printed.
[04:06] So let me move my debug point to the next line.
[04:10] And you can see now the catch block is going to be executed followed by finally block.
[04:16] And after the finally block, the next statement that we have inside the outer try block is going to
[04:22] be executed.
[04:23] The catch block of the outer try block is not going to be executed because we didn't receive any exception.
[04:28] And at last the finally of the outer try block is going to be executed, followed by the main() method
[04:35] will be executed.
[04:36] Now I can try to release the breakpoint so that entire program execution is going to complete.
[04:42] If you go and check the console, you can see first we have the statement followed by inner try block
[04:47] statement followed by catch block statement,
[04:50] finally block statement from the inner try block and at last we have outer try block and statement followed
[04:57] by outer try block finally
[04:59] block statement.
[05:00] So this confirms always we can use the nested try blocks whenever we don't want to propagate the exception
[05:06] to the outer try block, or whenever we want to make sure that the further execution of the program
[05:11] should not be impacted.
[05:12] In all such scenarios, we can safely use nested try blocks.
[05:17] I hope you are clear.
[05:18] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
