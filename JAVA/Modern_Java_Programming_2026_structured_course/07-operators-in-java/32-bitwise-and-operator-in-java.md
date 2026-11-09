# 7.32 — Bitwise AND operator in Java

> Section 7: Operators in Java

[00:00] What is a Bitwise AND operator we know its symbol is ampersand.
[00:04] Using the ampersand, we can apply Bitwise AND operation on two operands of type int.
[00:12] Now let's try to understand in detail how this operator is going to work.
[00:16] The Bitwise AND operator is a binary operator, and it expects two operand values as an input, and
[00:23] both of them should be of type int.
[00:26] This operator is going to perform bitwise and operation and the binary representation of its operands.
[00:33] So what is a bitwise and operation logic?
[00:35] I have given a table here.
[00:37] If you closely look at this table, there is a pattern that we can identify when we compare this table
[00:43] with the Logical AND operator that we have discussed previously.
[00:47] So what is the pattern.
[00:48] Think like one represents two and zero represents false.
[00:52] So inside Logical AND operator and Logical Short-circuit AND operator we know when we are going to get
[00:58] the output as true.
[00:59] We are going to get the output as true only if both operands are holding the true value.
[01:05] The same applies here.
[01:06] If the both of the operand bits they are holding a value one, then the output is going to be one,
[01:12] otherwise the output is going to be zero.
[01:14] Let's try to take an example.
[01:16] Here you can see I have two int operands x and y.
[01:20] And inside them I stored the decimal numbers like ten and six.
[01:23] If I apply these Bitwise AND operator on top of these two operands, I am going to get the output as
[01:30] two the same.
[01:31] I am going to store inside the variable z.
[01:34] Let's try to understand how we are going to get the output as two in this scenario.
[01:38] First, we need to make sure we are representing the both the decimal numbers ten and six, in their
[01:44] own binary representation values.
[01:46] So here ten I can write it as eight plus two.
[01:50] That's why I have mentioned one and one at the position, two to the power of three and two to the power
[01:55] of one.
[01:56] Whereas coming to the six, six we can write it as four plus two.
[02:00] That's why I have mentioned the bits one at two to the power of two and two to the power of one.
[02:05] Once we derived these binary format for the two operands, we need to apply these Bitwise AND operator
[02:11] logic that have defined inside this table.
[02:14] So zero and zero is going to be zero one and one is going to be one, which means only in the positions
[02:21] where the both operands holding the bit value as one.
[02:24] In such positions only you are going to have the output as one.
[02:28] Otherwise, in all the remaining positions you are going to have the bit value as zero.
[02:32] So once you calculated your binary number of your output, this binary number is going to be converted
[02:39] into a normal decimal number.
[02:41] So we have only one bit at the position two to the power of one.
[02:45] That's why the output we are going to get is two.
[02:48] Can we quickly validate these example inside intelliJ for the same.
[02:52] Let's go to the IntelliJ.
[02:53] Here I'm going to create a variable with the name x one.
[02:57] And to this I'm going to assign a value ten.
[03:00] Post that I'm going to create one more variable which is int y1 is equal to six.
[03:06] And after creating these variables I'm going to create one more variable which is into z1.
[03:11] And to this I'm going to assign an expression which is x1 ampersand y1.
[03:17] So with this we are going to get the output as two.
[03:20] Let me try to print the z1 onto the console.
[03:23] So if I try to execute this program I'm going to get the output as two.
[03:27] So here you may have a question.
[03:29] The same symbol we need to use for logical and operator as well.
[03:33] Then how my Java compiler knows whether I have intentions to use Bitwise AND operator or Logical AND
[03:40] operator.
[03:41] So the answer is very simple based upon the type of your operands that you have provided, the compiler
[03:47] is going to decide which operator it has to use.
[03:50] So since here I have provided the int type operands for the ampersand.
[03:56] That's why here the Bitwise AND operator is going to be considered by my JVM
[04:01] our compiler.
[04:02] Whereas if I try to provide the boolean operands as an input to my ampersand symbol, then in that case,
[04:08] obviously the compiler at JVM will consider Logical AND operator.
[04:14] I hope you are clear, and instead of these variables, we can also directly mention the literal values
[04:20] like I can mention ten, ampersand y1 or 10 & 6.
[04:24] So it's up to me whether I want to use a literal value or a variable.
[04:28] It's always recommended to use the variables as an input to any operator.
[04:33] I hope you are clear with the Logical AND operator.
[04:36] Did you see how easy it is?
[04:38] If we don't know the basics of these operators, you may be very clueless, like in an interview or
[04:44] inside a Java exam, they can give ten ampersand six and you'll have some four.
[04:49] Options are two options or three options.
[04:52] And if you don't know the steps that you need to follow, you will be scratching your head inside your
[04:56] interview or inside your exam.
[04:58] But with the steps that we have discussed.
[05:00] You should be able to easily identify the answer, which is to thank you, and I'll catch you in the
[05:04] next lecture bye.

----------------------------------------
