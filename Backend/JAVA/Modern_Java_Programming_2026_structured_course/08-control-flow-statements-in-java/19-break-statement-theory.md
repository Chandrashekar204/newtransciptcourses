# 8.19 — break statement - Theory

> Section 8: Control flow statements in Java

[00:00] Branching statements inside Java helps to jump the flow of the execution from one part of a program
[00:08] to another part. Inside Java
[00:10] there are three branching statements.
[00:12] One is the break statement and the second one is continue, and the last one we have is return statement.
[00:20] So for the next few lectures we are going to focus on these branching statements.
[00:24] And we are going to learn in detail about these branch statements when to use them, what are the rules
[00:30] that we need to follow.
[00:31] So all these kind of discussion we are going to do for the next few lectures. Inside this lecture, first
[00:37] let's try to focus on the break statement.
[00:40] We already saw how the break is going to help to terminate the flow of the execution inside the switch
[00:48] case statements.
[00:49] Very similarly, if you use these break statements inside a loop that you have developed with the help
[00:54] of for loop or while loop or do while loop, this break statement is going to help you to prematurely
[01:01] exit a loop based upon the condition that you have defined.
[01:04] So there are two types of break statements that we can define.
[01:08] The very first one is labeled break statement and the second one is unlabeled break statement.
[01:14] So let's try to understand more details about the break statement by looking at few examples.
[01:20] Here I have a simple example.
[01:22] I have written a for loop.
[01:23] If I don't have break statement inside this for loop
[01:26] this for loop is going to run total ten number of times.
[01:31] It is going to print all the numbers right from 0 to 9.
[01:35] But if you closely observe my for loop inside my for loop business logic, I have written an if condition.
[01:41] Whenever the I value become five
[01:43] I'm trying to use the break statement, and with that, my entire for loop execution is going to be
[01:50] stopped, and any other further iterations that is supposed to run will not be executed.
[01:55] Because with the help of this break statement, we are coming out of the for loop execution,
[02:01] regardless of how many more iterations it's supposed to run.
[02:05] Here, you may have a question,
[02:07] we are trying to break the for loop as soon as the I value become five.
[02:12] Why can't we control the same inside the for loop definition?
[02:16] Maybe instead of i < 10, I can define i less than five so that whenever the i value become
[02:22] five, the System.out.println() is never going to execute.
[02:26] I agree with you to make you understand.
[02:29] I have given this small example, but in real projects you will face more complex problems.
[02:34] For example, your method may receive 100 different numbers as an array.
[02:40] So from these array of numbers, maybe you are looking to find a specific number.
[02:45] So you will keep looping all the elements of the array one by one.
[02:49] At certain point of time
[02:51] whenever you identify the given searching number inside the array, you don't want to continue the for
[02:57] loop iteration because you already found the result that you are looking in such scenarios, you can
[03:02] simply break out of the for loop.
[03:04] I'm also going to show you a demo of these example in few minutes.
[03:09] So whatever break we are using right now here it is an unlabeled break.
[03:14] So whenever we use a break statement inside a for loop, when the given condition is met, it is going
[03:20] to break the execution of the for loop.
[03:23] And the execution will be continued with the statements that we have outside of the for loop.
[03:29] Now let me show you an another example where we are trying to use the labelled break statement.
[03:35] Here you can see I have two for loops, one is outer for loop and the second one is a nested for loop.
[03:41] For both these for loops I have given a label.
[03:44] So for the first outer for loop I have given a label as outerForLoop.
[03:49] So after mentioning this label you can give the colon.
[03:52] And with that this entire outer for loop is going to have a label or a name which is outerForLoop.
[03:59] Very similarly for the inner for loop also I have given an label which is innerForLoop.
[04:05] So I have a logic here inside my inner for loop and whenever a condition is met like i == 3
[04:13] ,
[04:14] I'm trying to mention the break.
[04:16] If I simply mention the break, the inner for loop only is going to be stop.
[04:21] The outer for loop is not going to be impacted.
[04:24] So from my inner for loop, if I want to stop the outer for loop also, then in such scenarios I can
[04:30] use this label.
[04:31] After the break, I am mentioning the label which is outerForLoop.
[04:35] So whenever I mention this break with the label, my JVM is going to look for the for loop with a given
[04:42] label.
[04:43] So the label that we have given is outer for loop.
[04:46] And with this label we have an for loop which is outside of my inner for loop.
[04:51] So with this, my JVM is going to stop the iteration of the outer for loop.
[04:56] And whenever the execution of the outer for loop is stopped, obviously the
[05:00] inner for loop execution is also going to be stopped.
[05:03] So this is how we can use the labeled break statements as well based upon our own requirements.
[05:10] I hope you are clear with these quick introduction about the break statement.
[05:14] If something is not clear, don't worry.
[05:17] In the next lecture, I'm going to show you a few examples on how to use these break statement.
[05:23] As of now, I'm trying to explain everything with the help of for loop, the same kind of behavior you
[05:28] can also achieve inside the while loop or do while loop as well.
[05:32] So any loops where you are trying to use the break statement, the syntax is going to be the same and
[05:37] the behavior also is going to be the same.
[05:40] The break is going to help you to prematurely exit the loop based upon the condition that you have defined.
[05:47] Let's see the demo of this break statement in the next lecture.
[05:50] Thank you,
[05:51] bye.

----------------------------------------
