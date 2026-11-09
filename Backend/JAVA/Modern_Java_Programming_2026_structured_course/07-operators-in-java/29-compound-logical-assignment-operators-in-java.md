# 7.29 — Compound Logical Assignment Operators in Java

> Section 7: Operators in Java

[00:00] Just like how we have Compound Arithmetic Assignment operators.
[00:04] Very similarly we also have Compound Logical Assignment operators.
[00:09] So let's try to understand what is a syntax that we need to use for these Compound Logical Assignment
[00:15] operators.
[00:15] Like you can see here.
[00:16] First you need to mention what is your operand1 followed by what is your Logical operator.
[00:22] So you can mention ampersand or pipe symbol or XOR symbol or caret symbol.
[00:29] After mentioning the symbol, you can mention is equal to followed by what is your operand2.
[00:34] The Java supports these kind of Compound Logical Assignment operator for three Logical operators, which
[00:41] is Logical AND, Logical OR and Logical XOR.
[00:46] The Java does not support Compound Logical Assignment operator for Logical Short-circuit AND operator
[00:53] and Logical Short-circuit OR operator you cannot use double ampersand is equal to and double pipe symbol
[01:00] is equal to inside your code because Java does not supports them.
[01:04] So when you use these Compound Logical Assignment operator behind the scenes, your expression is going
[01:11] to be converted as operand1 is equal to operand1,
[01:15] what is your operator followed by operand2.
[01:18] Can we see some examples here
[01:20] you can see I have mentioned some examples where if I use operand1 ampersand is equal to operand2
[01:26] , it is going to be converted as operand1 is equal to operand1 and operand2.
[01:32] So the overall result from operand1 and operand2 is going to be assigned to the operand1.
[01:39] I can also show you some code examples very quickly.
[01:42] So here you can see I have a boolean variable b1 which holds the value true using these variabl.
[01:48] if I use a Compound Logical Assignment with the help of logical and operator, the expression that I
[01:54] need to write is b1 ampersand is equal to true.
[01:57] So if I combine true with the true value with the help of Logical AND operator, the overall output
[02:04] I am going to get is true.
[02:05] Similarly, we can also validate these examples as well.
[02:09] If you see these example, I have mentioned the expression as b2 pipe symbol is equal to false since
[02:16] my b2 is going to hold the value true if I combine true with the false using the Logical OR operator,
[02:22] I'm going to get the overall output as true.
[02:25] The same kind of analysis you can do with the last example as well, and the output should match with
[02:31] whatever I have mentioned inside the comments.
[02:33] I hope you are clear with these explanation.
[02:35] Let's validate these examples very quickly
[02:38] inside IntelliJ. Inside IntelliJ I'm going to create quickly a boolean variable with the name b1.
[02:44] And to this first I'm going to assign a value true post that I'm going to write an expression which
[02:50] is b1 &= true.
[02:54] With this, the overall output that we are going to get will be true.
[02:57] I can also try to print out the b1 and show you the same for you inside the console.
[03:03] So if I execute this program, you can see at the end I'm getting a true value.
[03:07] Now I'll try to build the same kind of logic with the help of or operator.
[03:12] For the same
[03:13] let me rename this boolean variable to b2.
[03:16] Post that I'll mention the pipe symbol and rename this variable name to b2.
[03:21] And instead of true I can give false here.
[03:24] So with this, since we are going to feed true and false to the Logical OR operator, we are going to
[03:30] get the output as true only.
[03:32] So if I execute this program at the end, you can see we are going to get the output as true.
[03:36] If I try to copy the same code and use the Logical XOR operator with the boolean variable as b3.
[03:44] This time also we are going to get the output as true because I'm trying to feed true and false to the
[03:51] XOR operator
[03:52] since they are different values, the overall output is going to be the true only.
[03:57] That's what you can confirm here.
[03:59] I hope you are clear with these explanation and demo.
[04:02] With these we are done discussing about Logical operators in Java.
[04:07] I'm very happy that we made some progress here.
[04:10] I hope you are also happy like this girl.
[04:12] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
