# 7.13 — Unary plus and minus operators

> Section 7: Operators in Java

[00:00] Now inside this lecture, let's try to talk about unary plus operator and unary minus operator that
[00:07] we have under Arithmetic operators.
[00:09] The simplest definition about the unary plus operator is,
[00:13] you can use this operator just before any numerical values to represent a positive number.
[00:19] Most of the times, using this operator is not going to change anything, because +9 is same
[00:26] as 9 itself.
[00:27] But there are some rules that you need to be aware.
[00:30] The very first rule is we can use this unary plus operator only on top of primitive numeric type values.
[00:38] That means I can only use these on top of the numerical values, but not other values like boolean or
[00:44] String values.
[00:45] And whenever you are using these operator on top of a byte, short or char, this operator is going to
[00:53] promote your operands to an int.
[00:56] So this is one of the special rule that you need to be aware.
[00:59] Otherwise, if your operand is of type int, double or float, then using these operator is not going
[01:06] to have any effect.
[01:07] For example, think like there is an int variable num and this num variable holding a value 9.
[01:13] If I try to apply these operator by mentioning plus num, the result is going to be the same.
[01:19] You will be seeing the same 9 value on your console, but we need to be very careful while using
[01:26] these operator on top of an byte, short or char operand.
[01:31] I can give an example here.
[01:32] Think like I have num1 and num2, byte variables, and inside these variables I'm trying to store values
[01:39] like 9 and 3.
[01:40] Here you can see I have an expression which is num1 is equal to num2.
[01:44] So with this there won't be any compilation errors, whatever value that you have inside num2 variable,
[01:49] the same is going to be assigned to the num1.
[01:52] But if you try to change the same expression by using the plus operator like you can see here,
[01:58] num1 = num2.
[02:00] I'm trying to mention based upon the rule that we have discussed this num2, which is a byte.
[02:05] when we mention these unary plus operator, this byte is going to be converted as an int value.
[02:12] And if you try to assign these into value to the byte num1 , you're going to get compilation error
[02:18] because you're trying to downcast from int to byte.
[02:22] So how to fix this issue?
[02:24] To fix this issue you need to do the typecasting.
[02:28] So here you can see I changed the expression to num1 is equal to byte of +2.
[02:34] So I'm trying to do the typecasting here with the help of casting operator.
[02:39] Most of the times, using unary plus operator is going to be very easy, but we need to be very careful
[02:46] while using with byte, short or char operands.
[02:49] Let's see a demo of this very quickly.
[02:51] So here I'm going to create a byte variable with the name num7.
[02:57] And to this I'm going to assign 9.
[03:00] Very similarly I'm going to create one more byte variable which is num8.
[03:04] And to this num8 I'm going to assign a value 3.
[03:08] So if I try to execute an expression which is num7 = num8, I'm not going to get
[03:15] any compilation error because I'm trying to assign a byte value to another byte variable.
[03:20] But as soon as I try to mention the unary plus operator, I'm going to get a compilation error, because
[03:26] this expression, which is +num8 will convert my num8 into a int data type variable.
[03:33] That's why you can see I'm going to get an error which which is related to casting.
[03:37] So to fix this issue I need to mention byte just before the unary plus operator.
[03:44] I hope you are clear.
[03:45] So whatever we discussed for the unary plus operator, the same concepts are applicable for the unary
[03:52] minus operator
[03:53] also, even when we use this unary minus operator on top of a byte, short or char operands, it is going
[04:00] to promote them as an int.
[04:02] On top of that, whenever we are using this minus operator on any numerical values, it is going to
[04:09] convert that numerical value into an negative value.
[04:13] For example, think like
[04:14] initially I have a variable num, and inside this I'm trying to store a positive number which is 9.
[04:19] If I try to use this unary minus operator just before my num variable like minus num, then the positive
[04:27] nine is going to be converted as minus nine.
[04:30] And whatever special scenario that we discussed previously by taking byte variables.
[04:35] The same applies for unary minus operator as well.
[04:38] So that's why I have mentioned all those details here as well.
[04:41] And the last point that you need to be aware whenever you are using the unary minus operator is if you
[04:47] try to use this unary minus operator two times, then you're going to convert your number to a positive
[04:54] number.
[04:54] So here you can see I have an expression which is num is equal to minus and
[04:59] post that I have mentioned parentheses, and inside the parentheses I have mentioned minus 9.
[05:04] So the product of minus and minus is going to be the positive.
[05:08] That's why you're going to get the output as 9.
[05:11] So let's see the demo of this unary minus operator
[05:14] also very quickly here I'm going to copy these lines of code and paste them here and post that.
[05:20] I'm going to change the variable names to num9, num10.
[05:24] And here if I try to use this minus operator, you can see since we have this byte casting conversion
[05:31] there is no compilation error.
[05:33] But if I try to remove these you're going to get the compilation error.
[05:37] So whatever we discussed for the unary plus operator the same applies for the unary minus operator.
[05:44] Now let me show you an expression where I'm going to use this unary minus operator two times.
[05:50] So let me create a variable which is num11.
[05:54] And to this num11 I'm going to assign the expression - (-9).
[05:59] We should not use like minus minus nine because this is a different operator which we are going to discuss
[06:06] in the coming lectures.
[06:06] So whenever you want to use a unary minus operator two times, please make sure you are mentioning parentheses
[06:13] around your operand like you can see here.
[06:16] So this will make your num 11 as a positive number.
[06:20] So if I try to execute this program under the num 11 you can see we have a value which is nine.
[06:25] With this I'm assuming you're clear about unary plus operator and unary minus operator.
[06:31] Thank you
[06:32] and I'll catch you in the next lecture bye.

----------------------------------------
