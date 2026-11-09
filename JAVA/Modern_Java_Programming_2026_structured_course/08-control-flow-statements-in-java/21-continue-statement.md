# 8.21 — continue statement

> Section 8: Control flow statements in Java

[00:00] Inside this lecture, let's focus on the continue statement.
[00:04] With the help of the break statement, we can prematurely exit from the loops of for while or do while,
[00:11] whereas with the help of continue statement, we can only skip the current iteration.
[00:17] We can't skip or exit the entire for loop our entire while loop or do while loop.
[00:22] We can only bypass or we can only skip the current iteration.
[00:27] So let's try to understand more details about the continue statement.
[00:31] Like I said before, a continue statement can be used inside the for loop while loop and a do while
[00:36] statement.
[00:37] Whenever you are trying to use a continue statement, you have two options.
[00:40] One is with the help of labeled continue and the other one is with the help of unlabeled continue.
[00:46] First, let me show you an example of unlabeled continue.
[00:50] Like you can see here, I have written an for loop, which is going to print the numbers from 0 to 9.
[00:56] But if my requirement is to print only the odd numbers but not the even numbers, I can write a small
[01:03] logic inside my for loop.
[01:05] The logic is if i exactly divisible by two, then in such scenarios I can simply mention continue.
[01:13] So since there is a continue statement, the current iteration will be skipped.
[01:17] That means the System.out.println() is not going to be executed.
[01:21] Simply, my for loop is going to run the next iteration.
[01:26] So this is one of the way of using the continue statement with the help of unlabeled form.
[01:32] Because here we're not giving any label.
[01:34] If you have scenarios where you have written nested for loop or nested while loop or nested do while
[01:40] loops.
[01:41] In such scenarios you can use the labeled continue statement.
[01:45] Here you can see I have two for loop.
[01:48] For the outer for loop I have given the name as outer, whereas for the inner for loop I have given
[01:54] the label name as inner.
[01:56] If I simply mention continue, the continue statement is going to skip the current iteration of my inner
[02:03] for loop.
[02:03] But if I'm looking to skip the current iteration of the outer for loop, then in such scenarios I need
[02:09] to use the label statement like continue outer.
[02:13] I hope this is clear.
[02:14] Now let me show you the demo of these examples very quickly
[02:18] inside the IntelliJ, inside my intelliJ
[02:21] I'm going to create a new Java class and the class name is going to be ContinueStatementDemo here
[02:30] first I'm going to create the main() method.
[02:32] And after that I'm going to copy the for loop statement that we have from the BreakStatementDemo class.
[02:39] So let me copy this and paste it here.
[02:42] Here I'm going to make some changes whenever the I variable is exactly divisible by two.
[02:49] In such scenarios I'm going to construct that is an even number and I'll mention the continue statement.
[02:56] So with this, if I try to execute this program, you can see we are getting the output only for the
[03:02] odd numbers, but not the even numbers, because for the even numbers we are not executing the statement
[03:08] by using these continue statement.
[03:10] Whenever the continue statement executed by the JVM or Java, it is simply going to skip the current
[03:17] iteration.
[03:18] So any statements that you have after the continue, they're all going to be skipped.
[03:23] And the for loop is going to continue with the next iteration.
[03:27] Now can we see the demo of the label continue statement for the same,
[03:31] let me copy the for loop that I have here, so I can copy the same and mention inside my ContinueStatementDemo
[03:40] class.
[03:41] Here I'm going to change the label to outer.
[03:44] We can also keep the same name, but let's try giving some other name this time.
[03:49] So this is going to be inner.
[03:51] So I'll change this to five just for fun.
[03:54] And here first I'm going to mention the if statement above the System.out.println().
[04:00] So whenever the j = 2 I'm going to simply mention continue outer.
[04:07] So this is my simplest requirement that I have right now.
[04:10] So if I execute this program you will be getting the output based upon the logic that we have written.
[04:16] If you don't have this continue statement, like if I comment this one, I'll be getting a different
[04:22] output like you can see here.
[04:24] I hope you are clear.
[04:25] Let me uncomment this line of code.
[04:28] So always whenever you have some requirements to prematurely exit a loop or to skip the current iteration,
[04:35] in all such scenarios you can leverage the break statements and the continue statement.
[04:41] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
