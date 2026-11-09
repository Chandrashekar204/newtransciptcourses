# 7.16 — Increment and Decrement operators in Java - Part 2

> Section 7: Operators in Java

[00:00] Can we see some puzzles around increment and decrement operators?
[00:04] I know you're super excited about this.
[00:06] Let me show you the very first puzzle.
[00:08] So here I have an Java code where first I'm trying to declare a num variable of type int.
[00:15] And inside this num variable I'm going to hold the value 9.
[00:19] Later on I have written a Java expression which is num = num++.
[00:25] If I execute this Java code, what is the value that I can expect inside num?
[00:30] Do you have any guesses, with the previous concepts that we have discussed previously?
[00:34] You will tell the answer as 9 because we are using the postfix increment operator.
[00:41] That's why the num variable is going to be modified once the entire expression is evaluated, which
[00:47] is num is equal to num.
[00:48] So your guess is correct.
[00:50] We are going to get the output as 9 only.
[00:52] But there is a small twist inside this puzzle.
[00:56] Though we are going to get the output as 9,
[00:58] but we need to understand what is going to happen behind the scenes.
[01:02] So let's try to understand by looking the step by step process.
[01:05] In the very first step
[01:07] since we are using the postfix increment operator, the num value is not going to be modified.
[01:13] The current value of num, which is nine, is going to be used inside the expression.
[01:17] And with that, the expression is going to become as num = 9.
[01:21] Once this num = 9, expression is evaluated, the value of num is going to be incremented
[01:29] by one inside the memory.
[01:31] Because we have used the postfix increment operator.
[01:34] At the third step, the value of num is going to be ten inside the memory, whereas based upon the.
[01:41] Step two, we have an expression readily available which is num = 9, which is about to
[01:47] be executed.
[01:48] So once this step two and step three are completed inside the step four, whatever expression that step
[01:55] two has derived, the same is going to be executed or evaluated.
[01:59] And with that the value of 9 is assigned to the num.
[02:04] So when this assignment is going to happen, whatever value that we stored inside the memory, which
[02:10] is ten is going to be overrided with the value 9.
[02:14] This means the variable name is going to hold the value ten for a short period of time, and the ten
[02:21] value is going to be overridden.
[02:23] When the expression num = nine is going to be executed.
[02:27] That's why when we execute this code, we are going to get the output as nine but not ten.
[02:32] So what I'm trying to convey with this puzzle is before your JVM is going to modify the num variable
[02:39] by one, first it is going to prepare the expression like you can see in the step two.
[02:44] Once the expression is prepared, then the actual increment of the num variable is going to happen.
[02:51] And once this increment of the num variable is done inside the memory, the expression that is prepared
[02:57] in the step two is going to be executed as part of the step four.
[03:01] So please don't be under the assumption that inside the step two, only the expression is going to be
[03:07] evaluated.
[03:07] If that is the case, then the num value should hold the value ten.
[03:11] I hope this is clear.
[03:12] Let's try to execute this piece of code very quickly inside the jshell to validate our understanding.
[03:19] So here I'm going to create a variable which into num = 9.
[03:23] And post that I'm going to write an expression which is num = num++.
[03:29] So if I execute this line you can see the num is going to have the value 9.
[03:34] Whereas if I use the pre-increment operator the behavior is going to be different.
[03:39] We are going to get the output as ten the same
[03:42] you can confirm here.
[03:43] I hope you're clear.
[03:45] Now let me show you another puzzle.
[03:47] Here
[03:47] you can see I have some Java code in the very first line I'm trying to create a num variable and this
[03:53] num is going to hold the value 9.
[03:55] And here I have written the expression num = num++ + num.
[04:01] So what is a value that you are going to expect from this expression.
[04:05] So we are going to get the output as 19.
[04:07] Whereas for the next expression we are going to get the output as 20.
[04:11] Let me explain the steps that are going to be followed by the JVM behind the scenes to get these 19
[04:18] and 20 as an output.
[04:20] First, if you take the very first Java expression, which is num is equal to num plus plus plus num.
[04:27] In this scenario, in the very first step, the current value of num is going to be nine.
[04:31] The num plus plus uses the current value of num, which is nine inside the expression and post that
[04:38] only the increment operation is going to happen.
[04:41] So the expression is going to be changed as num = 9 + num.
[04:46] Now the value of num is going to be incremented to ten inside the memory.
[04:52] After that, once the step three is completed.
[04:54] Now my JVM will try to execute the expression that it has prepared in the step two.
[04:59] So what is the expression that it has prepared?
[05:02] num = 9 + num.
[05:04] So it will look what is the num value at this point of time.
[05:08] So inside the memory we are going to have the value ten.
[05:11] That's why the expression is going to be changed as 9 +10.
[05:15] And we are going to get the output as 19.
[05:18] Whereas if you look at the second example of code here, we are using the Pre-increment operator and
[05:25] post increment operator as well.
[05:27] So let's try to understand how this expression is going to be evaluated by JVM at runtime.
[05:33] In the very first step, we are going to have the current value of num as nine.
[05:37] Post that inside the
[05:38] step two,
[05:39] since we are using the prefix increment operator, the num value is going to be incremented by one.
[05:47] That's why the expression is going to change as 10 + num++ and after the
[05:53] step two inside step three
[05:55] since we are having the post increment operator for num, the expression is going to change to 10 + 10
[06:02] and once the expression is changed to 10 + 10 inside the memory, the value of num is going
[06:08] to be incremented by one.
[06:10] And with that inside the memory, the num value is going to hold the value 11.
[06:14] But in the last step the 10 + 10 expression is going to be evaluated, and we are going to get
[06:20] the output as 20 on the screen.
[06:23] I hope this is clear.
[06:24] Let's try to quickly validate these puzzles inside the Jshell.
[06:28] So here first I am going to create a num variable which is going to hold the value nine.
[06:33] And post that I am going to write an expression which is num = num++ num.
[06:40] So if I execute this statement like we discussed, we are going to get the output as 19.
[06:46] Whereas if I try to execute the second expression that we discussed which is
[06:53] num = ++num + num++.
[06:56] For this expression, we are going to get the output as 20.
[07:00] With these demos and puzzles that we have discussed so far, I am assuming you are clear on how the
[07:06] increment and decrement operators are going to work, so please note that the behavior is going to change
[07:13] based upon where these operators you are using.
[07:15] Whether you are using after the variable or before the variable
[07:20] accordingly, the behavior is going to change.
[07:23] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
