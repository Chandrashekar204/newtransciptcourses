# 7.7 — Introduction to Arithmetic Operators in Java

> Section 7: Operators in Java

[00:00] After the assignment
[00:01] operator,
[00:02] the mostly used operators in Java are Arithmetic operators.
[00:07] Under Arithmetic operators we have many operators
[00:10] that's why inside this lecture first I'm going to give you a very quick introduction about all these
[00:15] operators.
[00:16] Post that we can discuss each operator in detail in the coming lectures.
[00:21] So what are Arithmetic operators?
[00:23] Arithmetic operators in Java are the symbols that work with the numeric values only, like addition
[00:31] and subtraction.
[00:32] So we can perform these kind of operations to produce a new numeric result.
[00:37] Also please note that these operators we can only use with the numeric data types like byte, short,
[00:44] char, int, long, float and double.
[00:47] Here you may have a question like char is not a numeric data type, but like we discussed previously
[00:53] in the char data type lectures, behind the scenes, each char is going to have a corresponding numeric
[00:59] value that is going to be represented in the Ascii code table.
[01:03] That's why when we try to perform addition by taking two char values, the int value of those two char
[01:09] values will be considered to perform the addition.
[01:12] Apart from these numeric data types, we cannot use any other data types like boolean, primitive,
[01:18] data type or reference types as an operands whenever we are using these arithmetic operators.
[01:25] When I say reference type, these are the objects that we created with the help of a class.
[01:29] For example, if you have a Person class, you can create two objects like person1 and person2.
[01:35] You cannot apply Arithmetic operators on top of these reference types, because these Arithmetic operators
[01:41] are strictly for the numeric data types.
[01:45] Let's see what kind of operators that we have under the name Arithmetic operators in Java.
[01:51] The below table is going to give you high level summary about all the Arithmetic operators that we have
[01:56] inside Java.
[01:57] We also have more operators in the next slide.
[02:00] But before we move on to the next slide, first let me try to make you understand about these operators
[02:06] that we are seeing on this slide.
[02:07] In the very first column you will be able to see what is operator, followed by what is the description,
[02:12] followed by an example on how to use it.
[02:15] After the example, I also have a column representing what is the result value and at last what is the
[02:20] type of operator we know all these operators are Arithmetic operators, but if you want to understand
[02:26] whether a given Arithmetic operator is an binary or unary or ternary operator, you can look at the
[02:32] last column.
[02:33] So the very first famous operator, you know, it's an addition which is going to perform addition by
[02:39] taking two operands.
[02:40] The operands can be numerical values or they can be variables that are holding the numeric values.
[02:47] So 1 + 6 is going to give the result 7.
[02:50] Since these operator is going to accept two operands, we can consider this operator as an binary operator.
[02:57] Very similarly, for subtraction, we need to use minus or hyphen, followed by
[03:01] for multiplication, we should not use the x.
[03:04] Instead we should use the *, and after the multiplication we have division.
[03:08] Whenever you want to perform division inside Java, you can use two different types of operators.
[03:14] One is the /.
[03:16] So the name of these / operator is division operator.
[03:20] Whenever you are trying to use this operator you're always going to get the quotient value from your
[03:26] division.
[03:26] But if you are looking for the remainder, then you need to use the next operator which is modulus operator.
[03:33] So this modulus operator can be represented with the help of percentage symbol.
[03:38] And at last you can also see plus and minus are again repeated.
[03:42] But this time these are unary data types.
[03:45] That means whenever we are using this plus and minus on top of a single operand numeric value, then
[03:51] we can consider them as an unary plus operator and a unary minus operator.
[03:56] So these unary operators, we can use them to represent a positive number and a negative number.
[04:03] So +9 is as good as nine which is a positive number.
[04:07] So you don't have to specifically use the plus unary operator, because by default all numbers are positive
[04:14] numbers.
[04:14] But whenever you want to represent a negative number, then always use this unary minus operator by
[04:20] mentioning the hyphen or minus value just before the numeric value.
[04:25] I hope you are clear with this first set of Arithmetic operators.
[04:28] Let's try to see what more operators that we have under the Arithmetic operators.
[04:34] Here you can see we have next set of Arithmetic operators.
[04:37] When you use the plus symbol two times that indicates increment operator.
[04:42] So the increment operator we can use in two forms Post-increment or Pre-increment.
[04:47] When you mention these plus plus symbol after the variable then that is an post-increment.
[04:52] Whereas if you mention this plus plus before the variable name like ++num, then that indicates
[04:59] Pre-Increment.
[05:00] Similarly, we have Pre-decrement and Post-decrement, which we can build with the help of two minus
[05:07] symbols or two hyphen symbols.
[05:08] So don't worry about what are these operators, how to use them, what is the effect of them.
[05:14] All those details we are going to discuss in the coming lectures.
[05:17] For now, I'm just trying to give a high level summary about all the operators inside Arithmetic operators.
[05:23] After this increment and decrement operator, you can also see there are five different type of Arithmetic
[05:30] compound assignment operators.
[05:32] These compound operators, they can help us to perform arithmetic operation with a short notation.
[05:38] For example if you see here num + = 8.
[05:42] So num is a ,
[05:44] plus is equal to is a Arithmetic compound assignment operator.
[05:48] And after that I am mentioning the value eight.
[05:50] So this Java expression is same as num =num+8 .
[05:55] So whenever you have these kind of requirements where you want to perform Arithmetic operation on
[06:01] a same variable which you are trying to assign on the left hand side, then you can use these Arithmetic
[06:08] compound assignment operators.
[06:10] So we're going to discuss more details about them in the coming lectures.
[06:14] In total there are 14 different types of Arithmetic operators.
[06:18] We're going to put good amount of efforts understanding all these operators in the coming lectures.
[06:23] For now, I'm assuming you are clear about this quick summary about the Arithmetic operators.
[06:29] Whenever you have some question around the Arithmetic operators, you can always look at these tables
[06:34] to quickly understand what are all the options that you have to perform the Arithmetic operations.
[06:39] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
