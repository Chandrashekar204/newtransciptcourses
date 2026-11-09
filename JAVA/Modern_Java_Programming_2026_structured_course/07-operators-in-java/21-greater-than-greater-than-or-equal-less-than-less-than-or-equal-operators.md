# 7.21 — Greater than, Greater than or equal, Less than, Less than or equal operators

> Section 7: Operators in Java

[00:00] Inside this lecture, let's try to discuss the next four relational operators that we have.
[00:05] First, let's start the discussion with the greater than operator.
[00:09] So the syntax to use this greater than operator is very similar to the equal and inequality operator.
[00:16] The only difference is the symbol that you need to use
[00:20] is this greater than symbol inside your keyboard.
[00:23] You are going to see this symbol in the same key where dot is present.
[00:27] The behavior of this operator is it is going to return true value.
[00:32] If the value of operand1 is greater than value of operand2 two.
[00:37] Otherwise we are going to get the output as false.
[00:40] One important point that we need to be aware here is, this operator, along with the other operators
[00:46] that we are going to discuss inside this lecture.
[00:48] They are applicable only for the primitive numeric data types.
[00:53] We cannot use these greater than or greater than or equal less than or less than or equal on top of
[01:00] boolean variables, or on top of String objects or object reference.
[01:05] So these operators, they are strictly we can use on top of primitive numeric data types.
[01:12] And there is one rule that you need to be aware whenever you are using these operators, which is if
[01:17] one of your operand is NaN, and this NaN can be of type float or double.
[01:23] Regardless of what is the type of this NaN, we're always going to get the output as false when we use
[01:29] these greater than operator.
[01:30] So let me show you some examples here.
[01:33] So like you can see here I have declared two numbers nine and six.
[01:37] And there is a num3 double variable where I stored NaN value.
[01:41] And there is a boolean variable which is isGreater.
[01:44] So if I try to execute the expression which is num1 > num2, I'm going to first get
[01:51] the output as true because nine is greater than six.
[01:54] Whereas if one of my operand is NaN, I'm always going to get false.
[01:59] That's why this expression is going to give the output as false.
[02:03] Moving on to the next expression where I'm trying to use this operator on top of two boolean operands.
[02:10] So this expression compilation is going to fail because greater than operator are all the operators
[02:17] that we are going to discuss inside this lecture.
[02:19] They are going to be applicable for primitive numeric data types only.
[02:24] So here also you can see and at last I'm trying to compare two string objects with the help of this
[02:29] greater than operator.
[02:30] And with these expression the compilation is going to fail because like we discussed, we cannot use
[02:36] this operator for other than primitive numeric data types.
[02:40] Just like greater than operator, we also have greater than or equal to operator.
[02:45] So the symbol for this is,
[02:47] first we need to mention greater than symbol followed by equal symbol ( >= ).
[02:51] So the syntax is going to be very similar to the syntax that we have discussed for greater than and
[02:57] all the points that we discussed previously.
[02:59] They are also applicable for greater than or equal to operator.
[03:03] The output from these operator will receive true in the scenarios where operand1 is greater than
[03:10] or equal to the value of operand2.
[03:13] Otherwise, we are always going to get the output as false.
[03:17] So the same examples that we discussed previously here, I'm trying to show them with the help of these
[03:22] greater than or equal to operator for the num1 >= num2, we are going to get
[03:28] the output as true because nine is greater than six.
[03:32] But the expression where we have one of the operand as NaN, we are going to get the false.
[03:36] And if you try to compare two boolean variables with the help of these greater than or equal to, we
[03:42] are going to get the compilation error.
[03:44] And the same applies for the String objects or any other reference objects.
[03:48] So with the help of these two operators, we can only check whether the given first operand is greater
[03:54] than or equal to.
[03:55] But if you are looking for the less than operation, we have less than operator ( < ).
[04:00] Using this less than operator, we can compare if the operand one is less than operand two.
[04:06] So the syntax is going to be very similar, except the symbol we need to use less than symbol
[04:11] this less than symbol is going to present inside your keyboard in the same button where you have the
[04:17] comma.
[04:17] So the behavior whenever we use this operator is you are going to get the output as true.
[04:23] If the value of operand one is less than the value of operand two.
[04:29] Otherwise you are going to get the output as false.
[04:31] And this operator is also applicable exclusively for numeric data types and all the rules that we discussed
[04:38] previously
[04:39] they are still applicable for less than operator as well.
[04:43] So here you can see when I do num1 <num2 , I'm going to get the output as false because
[04:49] nine is not less than six.
[04:51] That's why I'm going to get the false.
[04:53] And if you have one of the operand as NaN you are going to get the output as false.
[04:58] So this behavior is
[05:00] very similar to the greater than and greater than or equal to operator.
[05:04] And this operator also, we cannot use on top of the operands other than numeric data types.
[05:09] That's why for these true less than false, I'm going to get a compilation error.
[05:13] And for the expression where I'm trying to compare two String objects with the help of this less than
[05:18] operator here
[05:19] also, I'm going to get a compilation error. After the less than operator, we have less than or equal
[05:25] to operator as well.
[05:27] And the symbol for this is
[05:29] first you need to mention the less than symbol followed by equal symbol ( <= ).
[05:33] The syntax is going to be the same like we discussed for other operators, and all the rules that we
[05:38] have discussed are also going to be the same.
[05:40] The only difference is this operator is going to return the output as true.
[05:45] If the value of operand is less than or equal to the value of operand two.
[05:51] And here also you can see some code examples that I have provided with all the previous discussions
[05:56] that we have done.
[05:57] You should be able to easily understand these code examples.
[06:00] Now inside the intelliJ, let's try to build the same code examples by using one of the operator
[06:08] maybe we can try to use greater than or equal to operator and we can see the behavior in action.
[06:14] So here first I'm going to create two into num variables.
[06:18] So the variable name is going to be num8.
[06:21] To this num8 I'm going to assign the value nine and post that I'm going to create one more variable
[06:28] which is num9.
[06:29] And to this I'm going to assign six.
[06:32] And after this int variables I'm going to create a double variable.
[06:36] And the name of this variable is going to be num10.
[06:39] To this num10 I'm going to assign the value which is NaN post that I'm going to create a boolean variable
[06:48] which is is greater than or equal.
[06:52] So this is the variable name.
[06:54] Now I'll try to write some expressions with the help of the greater than or equal to operator that we
[07:01] have discussed.
[07:02] First let me mention this boolean variable name which is isGreaterThanOrEqual to this I'm going
[07:09] to assign an expression which is num8 >= num9.
[07:17] So what is the output that you can expect here?
[07:19] We can expect the output as true here because nine is greater than six.
[07:25] Very
[07:25] similarly I can also try to write one more expression which is I will try to compare num ten with the
[07:32] double of NaN value.
[07:34] So if one of our operand is a NaN value, we are always going to get the false as an output.
[07:41] Now this time I'll try to compare two boolean values with the help of this operator.
[07:47] So I'll just mention true, which is the literal value, and post that I'll mention greater than or
[07:53] equal to followed by false.
[07:54] So if I try to compare, you can see I'm getting a compilation error saying that operator greater than
[08:00] or equal cannot be applied to boolean, boolean.
[08:03] This confirms that these operators that we have discussed inside this lecture, they are strictly applicable
[08:09] for the numeric data types.
[08:11] Even if you try to compare two different string values, like maybe I'll just try to mention hello greater
[08:18] than or equal to world in this scenario
[08:21] also you're going to get the same compilation error.
[08:23] I hope you're clear.
[08:24] Let me remove these line of code.
[08:27] Now I'll try to execute this program in a debug mode.
[08:30] Before that, let me keep a breakpoint at line number 34 and 35, so that we can see in action at runtime
[08:37] what is the output that we are going to get from these expressions.
[08:40] So let me execute this program.
[08:42] And you can see right now the execution stopped at the line number 34.
[08:46] If I try to press the shortcut which is function F8, the execution will move to the next line,
[08:53] and with that you'll be able to see what is the value inside this variable at the line number 34.
[09:00] So what is the value that we have here.
[09:02] We have the value as true.
[09:04] Now if I try to execute the next line of code, the value is going to change to false the same
[09:11] you can confirm here.
[09:12] This confirms that this greater than operator is working in a similar behavior
[09:18] like we discussed.
[09:19] My humble request here is please try to take the same piece of code and try with other operators like
[09:25] less than or equal to, less than and greater than.
[09:28] Try to provide various combinations of data and see the behavior.
[09:32] I'm not going to discuss them in detail here, because they all work in a very similar fashion.
[09:37] With this, we are done discussing about all the six operators,
[09:41] under the Relational operators, there is one more relational operator, which is instanceof which
[09:47] we are going to discuss in the coming sections.
[09:50] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
