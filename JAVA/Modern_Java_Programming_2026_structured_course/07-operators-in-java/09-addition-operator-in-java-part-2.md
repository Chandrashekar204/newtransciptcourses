# 7.9 — Addition Operator in Java - Part 2

> Section 7: Operators in Java

[00:00] In the previous lecture, we explored this scenario and we discuss everything about the special scenario.
[00:06] Now, inside this lecture, let me show you a few more examples.
[00:10] This time, let me use some double variable along with the int variable for the same
[00:15] I'm going to copy this entire content and paste it here, and I'll rename this to num4, num5,
[00:23] num6.
[00:24] And instead of byte I'm going to make it as double followed by num5
[00:29] also I'm going to make it as double.
[00:30] And the value I'm going to assign here is 3.14, whereas num6 I'll keep it as byte only.
[00:37] Now if I try to assign the num5 + num6 to the num4, let's see what is going to happen.
[00:44] So I'll just remove this typecasting and all these parentheses.
[00:48] I'll straight away try to add these num5 with the num6 content.
[00:54] So in this scenario I'm not getting any compilation error because think about the rules that we have
[01:00] discussed.
[01:01] If one of the operand is of type double, then the second operand is also going to be converted as a
[01:07] double.
[01:07] And when we add them the resultant you are going to get as double only.
[01:12] With that rule, we are trying to assign a double value to the num4, which is of type double only.
[01:18] But instead of double
[01:19] if I make my num four as an int, then you'll end up with a casting problem where you're trying to downgrade
[01:27] double to the int.
[01:28] That's why you're getting an compilation error.
[01:30] So if I revert back to the double, you can see the error is resolved.
[01:34] I can try to print what we have inside these num4.
[01:37] So let me try to print that with the help of this System.out.println().
[01:42] If I try to execute this program, you'll be able to see 6.14 followed by many zeros and one.
[01:49] Because double is capable of storing the decimal values up to 15 precision values.
[01:56] So with this, I'm assuming you're clear about the other three rules that we have discussed.
[02:00] Now moving on to the rule number four again,
[02:03] this time just after this num1 expression, I'm going to do the addition one more time with the Java
[02:12] expression, as num1 = 5 + 3.
[02:16] So this time you can see I'm not getting any compilation error.
[02:20] Why can't the same rule number four applies again here?
[02:23] Off course it applies.
[02:25] But here we're not sending the variables.
[02:27] We are directly sending the literal values like 5 + 3.
[02:31] So whenever you define constant values inside your expressions like 5 + 3, your Java compiler
[02:39] is going to compile and execute your expression at the compilation time itself, like 5 + 3
[02:46] it is going to execute and it knows the resultant value
[02:49] eight we can easily store inside the byte because byte range falls from -128 to 127, whereas with the
[02:58] above expression, my Java compiler is not going to evaluate and execute this expression at the compilation time,
[03:04] because it never know what value it is going to come inside num2 and num3.
[03:09] With that reason, it is going to be super strict around the casting, whereas here with the 5 + 3,
[03:15] we are going to get an output as eight, and with the eight value, my compiler is going to
[03:20] be super happy because it can easily accommodate inside the byte num1.
[03:26] Since it knows about these evaluation and output at the compilation time, it is not going to throw
[03:32] any compilation errors.
[03:34] For example, if I try to change this to 127 + 3, which is outside the range of byte, you can
[03:41] see I'm getting a casting error or a compilation error.
[03:45] I hope you are clear with this scenario.
[03:47] Java is very easy if you learn the rules.
[03:50] So inside interviews people can confuse you by giving this expression and this expression.
[03:57] They will ask you why I need to do that
[03:59] casting
[04:00] in the first statement where I don't have to do in the second statement.
[04:04] Since you are aware about all our discussions, you should be able to answer these questions very easily.
[04:10] For your reference
[04:11] all the points that we have discussed around the scenario of 5 + 3,
[04:15] I have mentioned all of them inside this slide
[04:17] for your quick reference in future, please refer to these slides to brush up all the scenarios that
[04:23] we have discussed.
[04:24] Now, before I try to close this addition operator lecture, I want to share an important update.
[04:31] So whatever four rules that we have discussed for addition operator, the same set of rules is also
[04:37] going to be applicable for other Arithmetic operators like subtraction, multiplication, division and
[04:44] modulus.
[04:45] So I'm not going to discuss about these scenarios one more time in detail when we are talking about
[04:51] these operators.
[04:52] The reason is we already discussed about them here.
[04:54] And the same rules applies for other operators as well.
[04:58] I hope you are clear.
[04:59] Thank you.
[04:59] And I'll catch you in the next lecture bye.

----------------------------------------
