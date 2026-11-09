# 7.18 — Equality Operator in Java - Part 1

> Section 7: Operators in Java

[00:00] The very first operator that we have under the relational operators is equality operator.
[00:06] So what is a symbol of equality operator we need to use equal to symbol two times continuously (==).
[00:13] If you ask me, what is the syntax that we need to follow whenever we are using this equality operator.
[00:18] The syntax is going to be very simple.
[00:21] First you need to mention what is your operand one followed by the equality operator symbol which is
[00:28] = = and after the symbol you need to mention what is your operand two.
[00:35] Like we discussed previously, all relational operators are binary operators.
[00:39] That means they are going to always operate on two operands.
[00:43] So whenever we use these kind of syntax to compare two different operands, this operator is going to
[00:50] follow certain rules behind the scenes.
[00:52] So let's try to understand what are those rules.
[00:55] The rule number one is both operands that you are trying to use with the equality operator
[01:00] they should be of same type.
[01:02] Your operands can be primitive data types or reference data types, regardless of whatever data type
[01:08] that they represent.
[01:09] We need to make sure both operands belongs to the same type
[01:14] combining different types of operands is not permitted.
[01:17] That means on the left hand side, if you try to keep int operand and on the right hand side if you
[01:22] try to keep String operand, it is not going to work.
[01:26] The compilation is going to fail.
[01:27] And the rule number two is whenever you are using primitive data type operands, this equality operator
[01:34] is going to evaluate to true if both operands represents the same value
[01:39] otherwise the result is going to be the false.
[01:42] So this should be clear for you.
[01:44] Whenever you are using primitive operands, the equality operator is going to look for the values that
[01:49] we store inside the operands.
[01:51] If the values are same, then it is going to return the true, otherwise false.
[01:55] But coming to the reference operands,
[01:57] when I say reference operands, this can be a String
[02:00] objects or these can be objects of Person class.
[02:03] So if you try to use this equality operator on top of reference operands, the operator is going to
[02:09] return true if both operands refer to the same object inside the heap memory.
[02:16] Otherwise it is always going to return the false.
[02:19] And the last rule that we have is we should not get confused with these operator with the equals() method
[02:25] inside the String.
[02:26] When you are looking for an option to compare the contents of two String objects, then you should use
[02:32] the equals() method.
[02:34] Otherwise, if you are trying to understand if two String objects are pointing to the same memory location,
[02:40] then you can use these equality operator.
[02:44] This rule number four is very, very important.
[02:47] Many times developers confused between these equality operator and equals() method.
[02:52] So please make sure you are clear about this
[02:54] rule number four.
[02:55] Now let me show you a few examples on how to use these equality operator.
[03:01] Like you can see here, the equality operator we can use on top of variables or on top of literal values,
[03:08] or with a combination of a variable and a literal value.
[03:12] But we need to make sure both operands belong to the same data type.
[03:16] In the very first example, I have num1 and num2 of type int.
[03:20] They hold the same number nine.
[03:22] So that's why if I try to compare these num1 == num2.
[03:27] I'm going to get the output as true inside a variable isSame.
[03:32] Very
[03:32] similarly, if I try to change the expression to compare num1 with the literal value nine in this
[03:38] scenario
[03:38] also, I am going to get the output as true and the last line like you can see here, I'm trying to
[03:43] compare two literal values like 9 with 9 itself.
[03:47] So that's why I'm going to get the output as true.
[03:49] So in this very first example I have taken the int operands very similarly
[03:54] we can also take boolean operands or any kind of operands.
[03:59] So in the second example I have two boolean operands like a and b.
[04:03] They are holding the value true.
[04:05] So if I try to compare a and b with the equality operator, I'm going to get the output as true.
[04:12] Instead of variables comparison
[04:14] we can also compare a with the literal value true or if needed, we can also compare two literal values
[04:20] like true with true itself
[04:22] with this equality operator.
[04:24] In all these scenarios, we are going to get the output as true.
[04:28] I hope you are clear.
[04:29] Now let me try to show you a very quick demo by coding these examples inside the IntelliJ.
[04:34] So inside my IntelliJ
[04:36] as of now I have my class open which is ArithmeticOperatorsDemo.
[04:40] I don't want to make changes related to the relational operators inside this class.
[04:45] That's why I'm going to create a new class
[04:48] and the class name is going to be RelationalOperatorsDemo.
[04:54] So this is the class name
[04:55] and regarding class name you may have a question which is can I
[04:59] have a class name which is of type any length.
[05:02] Off course, there is no such restriction.
[05:04] We can have a class name with any length, but it is always good to maintain a decent length as your
[05:12] java class name.
[05:13] Don't try to create a Java class name with the 40 characters or 50 characters length.
[05:18] That is going to be considered as a bad practice.
[05:20] There is also a funny image around super lengthy class names, so let me show you that funny image.
[05:26] Before that, let me create this Java class.
[05:29] So this is a funny image.
[05:30] Someone in the Twitter or in the X platform, they posted this image.
[05:34] They bought a new monitor which is of type 16in or 17in I believe, but still they are not able to fit
[05:42] their Java class names in it because someone created a Java class name with more than 50 or 100 characters.
[05:49] This kind of funny things always happens inside your career as well, so please enjoy this kind of funny
[05:55] moments inside your career.
[05:57] But my humble request is don't create such mistakes because other developers, they are going to laugh
[06:03] by looking at your code.
[06:05] I hope you like this image.
[06:07] Now let's go to our IntelliJ,
[06:09] here inside this class, I'm going to first create the main() method and post that
[06:13] I'm going to create two int variables with the name num1
[06:17] and inside this I'm going to store the value 9.
[06:21] And similarly I'm going to create one more variable which is num2.
[06:25] And inside that also I'm going to store 9 value.
[06:28] Now if I try to write a boolean expression by creating a boolean variable which is isSame, to this isSame
[06:35] variable I'm going to assign an expression that I'm going to build with the help of equality
[06:41] operator.
[06:42] So here I'll try to compare two integer variables.
[06:46] The variables that we have right now is num1 == num2.
[06:53] So this expression which is num1 i== num2 is going to return a boolean value
[06:59] and the same we are trying to store inside this isSame variable if needed inside of these variables
[07:05] comparision.
[07:05] You can also try to use literal values.
[07:09] But here let me go with the variables comparison.
[07:12] So if I try to execute this program, I'm going to get that true value
[07:16] under the is the isSame variable.
[07:18] That's what you can confirm here.
[07:20] So let me release this
[07:21] this time I'll try to compare two boolean variables.
[07:25] So the boolean variables that I'm going to create here is boolean a = true and boolean b =
[07:32] ,
[07:33] maybe I can give false so that we can try to validate false output as well.
[07:38] Now I'll try to create a boolean variable with the name isEqual.
[07:44] And to this isEqual I'm going to assign an expression that I'm going to build with the help of equality
[07:51] operator.
[07:52] Since a and b are holding two different boolean values, I can expect false as an output value
[07:59] inside my isEqual variable.
[08:01] So let me execute this program and you can see we have false inside is equal to variable.
[08:07] I hope you are clear with these examples.
[08:09] But there are some special scenarios also outside of these simple scenarios.
[08:14] So let's try to discuss about them as well in the next lecture.
[08:18] Thank you,
[08:19] bye.

----------------------------------------
