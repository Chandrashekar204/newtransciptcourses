# 2.15 — Demo of Overflow and Underflow

> Section 2: Primitive data types in Java

[00:00] Now, inside this lecture, let me try to explain you the concepts of overflow and underflow that may
[00:06] happen whenever you are trying to deal with a primitive data types that involves numbers.
[00:12] So what are these overflow and underflow.
[00:14] So these overflow and underflow refers to the situations where the result of an arithmetic operation
[00:22] exceeds the range of data type being used.
[00:25] Think like you are trying to add two different int numbers
[00:28] or two different short numbers are two different byte numbers or long numbers.
[00:33] So whenever you are trying to perform some arithmetic operation like addition, multiplication, in such
[00:39] scenarios, if the result is exceeding the range of your data type that you have assigned on the left
[00:46] hand side, then overflow or underflow may happen.
[00:50] I know you may have some questions here, so let's try to deep dive into these overflow and underflow.
[00:55] In the previous lectures, we saw that while we were trying to declare variables with the help of primitive
[01:01] data types like int, if you try to assign a number which is not in the range of data type, then we
[01:07] are getting immediately a compilation error saying that the number is not in the range.
[01:12] If you see here I'm trying to create a overflow number variable, and for this I'm trying to assign
[01:18] a number which is one value greater than the Integer.MAX_VALUE.
[01:23] In such scenarios, I will get an compilation error because the number that we assigned is in the outside
[01:31] range.
[01:31] So these kind of overflows the compiler can detect immediately
[01:35] and it can stop us by throwing a compilation error.
[01:39] Very similarly, if you see for next variable where I named it as underflow number, here I'm trying
[01:45] to provide a negative number which is less than minimum value by one number.
[01:50] In this scenario the underflow is happening,
[01:52] that's why my compiler is going to throw an error.
[01:56] So it is pretty clear if you are only doing the variable initialization and declaration, the Java compiler
[02:03] is smart enough to detect them and throw compilation error.
[02:06] But if you try to perform some arithmetic operations, your compiler cannot detect these situations.
[02:12] So let's try to understand more details about it.
[02:15] So here you can see I'm trying to give an overflow scenario.
[02:19] Think like I have built a Java statement where I'm trying to add two numbers and assign that to the
[02:25] variable on the left hand side.
[02:27] So here the very first number that I'm trying to use is what is the maximum number supported by the
[02:34] integer.
[02:34] So this is the maximum number which is ending with 647. With this maximum number,
[02:40] I'm trying to add one more number.
[02:42] In this kind of scenario, my Java compiler cannot detect this overflow scenario because during the
[02:48] compilation time, my Java is not going to evaluate all my expressions like additions, subtractions.
[02:55] That's why it is simply going to accept this code and execute the same.
[02:59] So what is going to happen if you try to execute this code?
[03:02] The overflow will happen and with the overflow, the output that you are going to get will be not like
[03:09] you expect.
[03:10] The output that you are going to get from this expression is,
[03:12] this is the negative number that you are going to get, because with the overflow, the output is going
[03:17] to be derived by wrapping around to the minimum value.
[03:21] So it is going to be a circle.
[03:23] Think like all your numbers are marked on a circle. At some point of time
[03:27] if you are trying to overflow from the positive numbers, then immediately you will go to the negative
[03:33] numbers because it is like a circle.
[03:36] Very similarly, let's try to understand underflow scenario.
[03:39] In the underflow scenario, I'm trying to do subtraction by taking a minimum value supported by the
[03:47] integer.
[03:47] So this is the minimum value supported by the integer.
[03:50] From this number I'm trying to subtract one, and since this is a expression, my compiler cannot detect
[03:57] the underflow scenario and this statement is going to be compiled successfully and it will result in
[04:03] the underflow.
[04:04] So whenever the underflow is happening, the output you are going to get from the positive number.
[04:10] So this is the output that you are going to receive from your Java code.
[04:13] So the outputs were not getting like we expect.
[04:16] So that's why since these kind of scenarios cannot be detected by the compiler, it is the responsibility
[04:23] of the developer to always use the correct data types.
[04:27] So if you see this kind of scenarios may happen inside your code based upon the arithmetic expressions,
[04:32] then it is always a wise decision to use long in the place of int.
[04:37] Otherwise, from your Java code you are always going to get unexpected output.
[04:42] So let's try to see these overflow and underflow demo inside the jshell. In order to show you the demo
[04:48] of underflow and overflow, first I need to understand what are the minimum and maximum values of integer.
[04:55] Using the Integer class name, I'm going to get what is the
[04:59] MIN_VALUE and what is the MAX_VALUE supported by the integer?
[05:05] As a next step, I will try to create a variable of type int.
[05:10] So the variable name I'm going to give as overFlowNum. Because I want to show you the demo of overflow.
[05:17] So in order to see the overflow scenario, what I can do is I can take the maximum value.
[05:23] And to this I'm going to add one number
[05:26] and with this the overflow will happen.
[05:29] And you can see there is no compilation error happening, but we are getting an unexpected output.
[05:35] Similarly, if we try to add 2 the negative number is going to be changed.
[05:40] So let's see what is the output we are going to get.
[05:43] You can see we are getting 647.
[05:45] That means the position of the number is acting like a circle where whenever the overflow is happening,
[05:52] it is moving on the negative side based upon how many numbers it is overflow.
[05:58] Now can we see the demo of underflow for the same
[06:01] I am going to create a variable of data type int and the variable name is going to be underFlowNum.
[06:08] For the underflow scenario, I need to take the minimum value.
[06:12] From this minimum value I am going to subtract one and with this the underflow will happen and you can
[06:19] see we are getting an unexpected output.
[06:23] That's why always be cautious while you are trying to perform arithmetic operations and the internal
[06:28] numbers.
[06:29] If you have some doubt that some point of time, the number may become outside the range of int, then
[06:35] my recommendation is always to declare your variables as long so that the overflow and the underflow
[06:43] is never going to happen.
[06:44] With this, I'm assuming your super clear about the concepts of underflow and overflow.
[06:49] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
