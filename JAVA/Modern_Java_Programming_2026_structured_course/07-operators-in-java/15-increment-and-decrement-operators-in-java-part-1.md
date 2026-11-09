# 7.15 — Increment and Decrement operators in Java - Part 1

> Section 7: Operators in Java

[00:00] Inside this lecture, let's try to discuss about the last set of operators that we have under Arithmetic
[00:07] operators.
[00:07] So what are these operators?
[00:09] Increment and decrement operators.
[00:12] Whenever you are using plus symbol two times continuously without any space,
[00:17] we can call such operator as an Increment operator.
[00:21] And similarly if you are using minus symbol or hyphen symbol continuously two times, it indicates decrement
[00:29] operator.
[00:30] With that quick introduction, now let's try to understand what are the action or the operation that
[00:35] they are going to perform
[00:36] whenever we are using these operators on top of a operand, whenever we are using increment operator
[00:44] on top of a variable of numeric data, it is going to increase the variable's value by one.
[00:51] Whereas if you use a decrement operator, you're going to see the opposite behavior, which is the value
[00:57] inside the variable is going to be decrease by one.
[01:01] And here you may have a question like why do we need separate increment and decrement operators.
[01:06] If I can add one or subtract one with the help of addition and subtraction operators that we have discussed
[01:12] previously?
[01:13] I agree with you.
[01:14] That's a very valid question.
[01:15] But these increment and decrement operators, they are going to be super helpful when we write our Java
[01:21] logic with the help of loops, like for loop, while loop.
[01:25] So in all such looping scenarios, these operators are going to be severe.
[01:29] When we discuss about the for loops and while loops that we have inside Java at that time, it is going
[01:35] to make more sense to you.
[01:36] For now let's try to learn on how to use these operators and what is the operation that they are going
[01:42] to perform
[01:42] whenever we are using these variables on top of a operand, I'm going to focus a lot about the increment
[01:49] operator.
[01:50] But whatever I'm discussing about the increment operator, the same concept, the same examples, they
[01:55] are also going to be applicable for that decrement operator, except with a single difference, which
[02:02] is,
[02:02] the decrement operator is always going to decrease the value by one, whereas increment operator is
[02:08] always going to increase the value by one.
[02:10] I hope it is clear whenever we want to use these operators, we need to make sure we are using these
[02:16] operators on top of a variable operand.
[02:20] We cannot use these operators on top of literal values or hard coded values like I cannot write
[02:27] 2++ or 4--.
[02:29] So this is completely invalid
[02:31] in Java.
[02:32] Whenever you want to apply this operator, first you need to store your numerical value inside a variable.
[02:38] Using that variable, you need to perform this increment and decrement operation.
[02:43] And when we want to use these operators, we have two options on how to use these operators.
[02:49] We can use these increment and decrement operators in the format of postfix or in the format of prefix.
[02:57] Postfix means if I mention this plus, plus or minus minus after the variable name, then such operator
[03:04] we can call it as postfix increment operator or postfix decrement operator because I'm mentioning this
[03:11] operator post variable name.
[03:13] Whereas if I mention these operators before the variable name, then in such scenarios these operators,
[03:20] we can call them as prefix increment operator or prefix decrement operator.
[03:25] And the behavior is also not going to be the same.
[03:28] If you try to apply postfix and prefix on the same variable, you're going to get different outputs.
[03:34] So the difference is whenever we are using the prefix increment operator or prefix decrement operator
[03:42] just before the variable name.
[03:44] In such scenarios, the variable value first will be modified.
[03:48] If you are using an increment operator, the variable value will be increased by one.
[03:54] Otherwise, with the decrement operator, the variable value is going to be decreased by one.
[03:59] Once the variable value is modified, then only the rest of the expression is going to be evaluated.
[04:07] Inside your Java expression
[04:08] you might be using other operators like assignment operator, addition operator, subtraction operator.
[04:14] So your whole expression is only going to be evaluated once the variable is modified, either by increasing
[04:22] or decreasing by one, whereas if you use these increment or decrement operator in the format of postfix,
[04:30] in such scenarios, the values of the variables is going to be modified only after the expression is
[04:37] completely evaluated.
[04:39] I know it might be confusing for you.
[04:41] Let me try to show you some examples
[04:43] to clear your confusion. Let's consider an example
[04:47] like you can see.
[04:47] First, I'm trying to declare an integer variable num1 and inside this num1 variable I'm storing a value
[04:54] 45, whereas inside the num2 variable I'm storing the value 4 after
[04:59] these first two lines of declaration and initialization.
[05:03] I'm trying to write a Java expression, which is num2 = num++ +5.
[05:10] So here I'm trying to use the increment operator on top of the variable num1.
[05:15] After mentioning these operator, I'm also trying to use another operator which is plus
[05:21] and with this plus I'm trying to add a value five.
[05:24] So this is complete Java expression.
[05:26] So here we are using a postfix increment operator.
[05:31] That's why we are going to get the output as 50.
[05:34] Like 45 is the num1 value to this 45 we are trying to add the value five.
[05:40] So 45 + 5 = 50.
[05:43] The same is going to be assigned to the num2.
[05:45] But here you may have a question,
[05:47] we are trying to increment the num1 value by one.
[05:50] Why I'm not getting the output as 51 instead
[05:54] why I'm getting the output as 50.
[05:56] So you may have this question.
[05:58] So let's try to understand the same by discussing the steps that your compiler is going to follow.
[06:03] So whenever your compiler sees this expression, since we are using the postfix increment operator,
[06:10] the num1 variable is not going to be incremented by one immediately.
[06:15] It is going to be modified only once the entire expression is evaluated.
[06:20] With that assumption,
[06:21] what is our current value that we have under num1,
[06:24] it is 45, so the expression is going to become as 45 + 5.
[06:29] Post that the value of num1 inside the memory is going to be incremented by one.
[06:35] So that's why the variable value of num1 inside the memory is going to become 46.
[06:41] But these 46 is not going to be used inside this 45 + 5 expression, because by the time the num1
[06:48] variable is incremented by one, this expression is already evaluated in the previous step.
[06:54] So that's why the output we are going to get as 50 under the num2, and the value that we are going
[07:00] to store inside the num1 by the end of this entire expression is 46.
[07:05] Now let's try to see the same kind of code by using the prefix increment operator.
[07:10] So here you can see this time I'm trying to mention the prefix increment operator just before the num1.
[07:16] .
[07:17] Like you can expect.
[07:18] This time we are going to get the output as 51.
[07:21] The reason is whenever we are using the prefix increment operator or prefix decrement operator, first
[07:28] the variable value is going to be modified post that only the remaining expression is going to be evaluated.
[07:34] So if you see the list of steps that are going to happen first the num1 value is going to be incremented
[07:41] by one.
[07:41] So the num1 value inside the memory is going to become 46.
[07:45] With that inside the step two, the expression will become 46 + 5.
[07:51] That's why the value of 51 is going to be assigned to the num2.
[07:55] I hope you are clear.
[07:56] Let me show you that demo of this very quickly
[07:59] inside the IntelliJ, inside IntelliJ, I'm going to create a num variable which is num14.
[08:06] To this num14, I'm going to assign a value 45.
[08:10] Post that
[08:10] I'm also going to create one more int variable with the name num15
[08:15] and to this I'm going to assign a variable value 4.
[08:19] This value can be anything,
[08:21] it doesn't matter.
[08:22] Now I'm going to write an expression which is num15 is equal to num14++.
[08:30] After mentioning this post increment operator, I'm going to give some space and mention plus, which
[08:36] is an addition operator to the right hand side of this addition operator,
[08:40] I'm going to give a value which is five.
[08:42] So what is the output we are going to get.
[08:44] So let's see the output by running this program in a debug mode, you can see the num15 is going to
[08:52] have the value 50.
[08:53] And the num14 is going to have the value 46.
[08:57] So this is the value inside the memory which is modified after this expression is evaluated.
[09:04] That's why though you are able to see the 46 value here inside the memory, the num15 is holding the
[09:11] value 50.
[09:12] The reason is first, the expression is evaluated post that only the num14 variable is incremented.
[09:19] I hope you are clear.
[09:20] Let me release this breakpoint and this time I'm going to use the prefix increment operator for the
[09:27] same
[09:27] let me copy the same lines of code and rename this variables to num16 and num17.
[09:34] This time, instead of postfix increment operator, I'm going to use the prefix increment operator.
[09:42] After that, I'm also going to change this variable names to num17, and this one I'll change to num16.
[09:48] .
[09:48] So if I try to execute this program this time, you're going to get the output as 51 and the num16 : 46.
[09:56] This confirms first that num16 variable
[09:59] is modified post that only the expression is calculated.
[10:03] That's why we are getting the output as 51 here.
[10:06] I hope you are clear the same kind of behavior
[10:09] you can also see whenever you are using post decrement and pre decrement operator inside the next lecture.
[10:16] Let's try to discuss few more puzzles around this increment and decrement operators.
[10:22] And these puzzles are going to be super interesting for you.
[10:25] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
