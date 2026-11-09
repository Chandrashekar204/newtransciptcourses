# 7.14 — Compound Arithmetic Assignment Operators in Java

> Section 7: Operators in Java

[00:00] There are five fundamental Arithmetic operators, and these five are addition, subtraction, multiplication,
[00:08] division, and modulus.
[00:09] For all these five fundamental Arithmetic operators, we have an associated compound Arithmetic assignment
[00:18] operator.
[00:19] The syntax on how to use these Compound Arithmetic Assignment Operator is,
[00:24] first you need to mention what is your operand one.
[00:27] So on the left hand side you are going to have one operand.
[00:30] And very similarly on the right hand side also you're going to have another operand in between your
[00:35] operand1 and operand2.
[00:38] First you need to mention what is your operator.
[00:40] So op here indicates what is your operator.
[00:43] Whether you want to use plus, minus, asterisk or forward slash or modulus.
[00:48] So you need to mention what is your operator followed by is equal to symbol.
[00:53] When you combine your Arithmetic operator with is equal to symbol, it is going to become Compound Arithmetic
[01:01] Assignment Operator.
[01:02] So when you use the short form of syntax behind the scenes, the JVM or Java, it is going to convert
[01:09] this simple expression into the following expression.
[01:12] First, on the left hand side you're going to have operand1, followed by is equal to and after the
[01:17] is equal to symbol, you're going to have the casting operator based upon the type of your operand1.
[01:23] After the casting operator, you're going to have an expression which is operand1 op and operand2
[01:30] .
[01:30] For example, think like I have an int variable num which is storing a value 42.
[01:36] If I try to use my Compound Arithmetic Assignment Operator with the plus symbol, I need to use this
[01:43] expression which is num plus is equal to and on the right hand side I'm mentioning 3.3 as an value.
[01:51] So this is my second operand.
[01:53] So if you see here on the right hand side I'm using the double operand,
[01:57] whereas on the left hand side I'm using the int operand.
[02:01] So this short expression is going to be converted into this format.
[02:05] So how it is going to look like it is going to look like like this
[02:09] you can see num is equal to typecasting to int y int typecasting is happening because your left operand
[02:16] is an int value.
[02:17] That's why the casting is happening with the help of this int, post thta we are going to have an expression
[02:24] num + 3.3.
[02:26] When the addition happened like 42 + 3.3, the output is going to be 45.3.
[02:32] But since we have a casting here, the overall output we are going to get is 45.
[02:38] I hope you are clear.
[02:39] This Compound Arithmetic Assignment Operator we can also use on top of String as well.
[02:45] But there is a rule that we need to follow your operand1
[02:48] must be of type String and the operand2 can be of any type, including the boolean.
[02:54] For example, here you can see
[02:55] first I have an str variable which is going to hold the String value
[03:00] Hello and post that you can see I have an expression which is str = str + 9.
[03:06] So the output from this expression is going to be hello9.
[03:10] So the same kind of behavior I can also achieve by using the Compound Assignment Operator which is
[03:18] str += nine.
[03:19] But please note that we can only use plus is equal to Compound Arithmetic Assignment Operator with the
[03:26] Strings.
[03:26] I hope you are clear with this theory discussion.
[03:28] Let's see the demo of these examples inside our IntelliJ inside the Arithmetic Operators demo class.
[03:34] First, I'm going to create an integer variable with the name num12.
[03:40] And to this variable I'm going to assign a value which is 42.
[03:44] Now here I'm going to write an expression by using the Compound Arithmetic Assignment Operator.
[03:50] So first I'll mention what is my left hand operand which is num2.
[03:55] I'll post that I'll mention plus immediately followed by is equal to and on the right hand side I'm
[04:02] going to mention a value which is 3.3.
[04:06] So this short expression is going to be converted into num12,
[04:11] is equal to casting to int, and after the casting the actual addition will happen which is num12 + 3.3
[04:19] .
[04:21] So this is how the internal calculation is going to happen.
[04:24] And since we are doing the casting here, the output is going to be the 45.
[04:29] So if I try to execute this program under the num12, you can see we have a value 45.
[04:34] I hope you're clear.
[04:35] Very similarly we can use other type of operators, like if I can take the same code and I can change
[04:41] the variable name to num13.
[04:43] And here instead of plus this time I'm going to use minus.
[04:47] So with this the expression is going to change like num13 = (int) num13 - 3.3.
[04:56] So what is the value that you are expecting under num13?
[05:00] It is going to be 38.
[05:03] If you try to do the subtraction of 42 from 3.3, the value is going to be 38.7.
[05:10] And since we are trying to do the type casting into the int variable, the decimal value will be ignored
[05:16] and we are going to get the output as 38.
[05:18] So let's see the same by running this program.
[05:21] Before that, let me try to correct my expression by correcting this variable
[05:25] name two num13.
[05:27] Now if I try to execute this program, you can see under num13 we are going to get an output value
[05:33] which is 38.
[05:34] This way you can use other type of operators also like asterisk, division operator and a modulus operator.
[05:42] Now let me show you a demo of on how to use Compound Arithmetic Assignment Operator on top of a String
[05:49] object.
[05:50] For the same first I'm going to create a String variable.
[05:52] So the variable name is going to be str
[05:54] and to this I'm going to assign a value which is hello post that I'm going to write an expression which
[06:01] is str plus is equal to
[06:04] and on the right hand side I can use any value like I can use a normal int value or I can use a boolean
[06:11] value.
[06:11] It's up to me.
[06:12] So with this my String object is going to have the data which is Hello9.
[06:17] You can also see here.
[06:19] So this confirms whenever we use this plus is equal to on top of an String operand.
[06:25] Behind the scenes it is going to perform the String concatenation.
[06:29] But please note that your left operand should be always String object if you try to write the same expression
[06:35] by using 9 += str, you're going to get a compilation error because the thumb rule
[06:43] is always the left operand should be a String object.
[06:47] That's why don't try to use this kind of syntax.
[06:49] And one more important point that you need to be aware here is we can only use up plus is equal to with
[06:55] the string operand we cannot use minus is equal to or asterisk is equal to or forward slash is equal
[07:03] to
[07:03] or modulus is equal to,
[07:05] because these operators are not allowed, only the plus operator is allowed with the String operand.
[07:12] I hope you are clear with these discussions.
[07:14] Now let me answer your burning question.
[07:16] Why should I use these short notation?
[07:19] Can't I write these complete expression?
[07:21] Off course you can write.
[07:22] There are few advantages that you are going to get whenever you are going to use Compound Assignment
[07:28] Operator.
[07:28] So let's try to understand what are those advantages.
[07:31] There are two advantages that we may get whenever we are using Compound Arithmetic
[07:36] Assignment Operator.
[07:38] The very first advantage is the performance.
[07:40] Why performance means you are operand1 is always going to be evaluated only once.
[07:47] If you try to use a short notation of Compound Arithmetic Assignment Operator.
[07:53] For example, inside the expression num+= 3.3.
[07:57] The operand1, which is num variable is going to be evaluated only once, whereas if you try to write
[08:04] this detail expression, the num is going to be evaluated twice.
[08:09] That's why when we use these Compound Arithmetic Assignment operator you are going to have better performance.
[08:15] And the second advantage is automatic casting.
[08:18] Whenever we are using this Compound Assignment Operator, the casting will happens automatically behind
[08:23] the scenes.
[08:24] You don't have to do manually.
[08:25] The casting may result in either a narrow conversion or an identity conversion.
[08:30] So what is a narrow conversion?
[08:32] If you are trying to downgrade a float to int or double to int, this kind of conversion or casting
[08:39] is narrowing conversion, whereas identity conversion means if the casting is happening from int to
[08:45] int, float to float, double to double.
[08:48] Such casting, we call it as identity conversion.
[08:51] So these narrowing conversion or identity conversion is always going to happen automatically.
[08:57] And here you may have a question,
[08:59] how about the scenario where we're trying to upgrade int to float or int to double, int to long.
[09:06] So these kind of upgrade scenarios like we discussed previously, the casting is always going to be
[09:11] automatic because the implicit casting inside Java is always automatic.
[09:16] We don't have to do the casting manually.
[09:19] That's why here I have highlighted about narrowing conversion and identity conversion because for broader
[09:27] conversion or implicit conversion, there is no need of automatic.
[09:30] We already have such behavior inside Java.
[09:33] I hope you are clear with these two advantages.
[09:35] Always
[09:36] if possible, please use the Compound Arithmetic Assignment Operator because they have these advantages.
[09:44] I hope you are clear with the syntax and how to use the Compound Arithmetic Assignment Operators in
[09:49] Java.
[09:50] Thank you
[09:50] and I'll catch you in the next lecture bye.

----------------------------------------
