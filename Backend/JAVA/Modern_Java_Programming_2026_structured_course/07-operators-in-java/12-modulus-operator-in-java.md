# 7.12 — Modulus Operator in Java

> Section 7: Operators in Java

[00:00] In this lecture, let's talk in detail about the modulus operator.
[00:04] We know the modulus operator will always give the remainder from the division operation.
[00:10] Let me show you a small demo very quickly inside IntelliJ.
[00:14] Here I'm going to write an expression using the modulus operator.
[00:18] So I'll rename this variable to result3
[00:21] and instead of 9 I'll just mention 21.
[00:24] And instead of forward slash (/) I'll mention the modulus operator which is percentage and the denominator
[00:31] at the right hand side operand I'll mention the value two.
[00:34] So with this the division will happen internally.
[00:37] And what will be the remainder that we are going to get.
[00:40] We are going to get the remainder as one because 2 * 10 = 20.
[00:45] And with that we left with a remainder value one.
[00:48] That's why if you try to run this program at runtime inside the result three, you're going to see the
[00:54] value one.
[00:55] So this confirms that modulus operator always provide you the remain value.
[01:01] But don't be fooled by these simple expression modulus operators also has some special scenarios which
[01:07] we need to discuss in real projects
[01:09] we'll never have this kind of happy path operations.
[01:13] We will end up with varieties of data.
[01:16] That's why let's try to focus on the special scenarios as well.
[01:19] There are certain rules that you need to be aware whenever you are using the modulus operator. Behind
[01:25] the scenes, it is also going to perform the division operation, but it always going to give the remainder
[01:30] as an output.
[01:31] So let's try to understand what are these rules in this operator
[01:35] also, the rules are broadly categorized based upon the types of operands that you are using inside
[01:41] your modulus expression.
[01:43] First, let's try to discuss about the scenario where both of your operands are of type integers or
[01:50] int values.
[01:50] There are no decimal values involved in such cases
[01:54] the rule number one is very similar to the division operator.
[01:58] If your right hand operand is zero, that means if your denominator is zero, then you're always going
[02:04] to get an runtime exception, which is Arithmetic exception.
[02:08] And the rule number two is if the right hand operand is not a zero, the sign of the result is going
[02:15] to be aligned with the sign of the left hand upper end.
[02:18] We know when we use both operands as an integer values, we are going to get an output which is of type
[02:25] integer only.
[02:26] But how about the sign?
[02:27] The sign of the result is going to be determined by your sign of the left operand or the numerator.
[02:35] So here you can see I have given some examples.
[02:38] If you try to perform 21 % 2, you're going to get the positive number one as an output.
[02:44] Whereas inside the numerator, if you keep the -21 you're going to get the output as -1.
[02:51] But whatever sign is mentioned on the right hand side operand or on the denominator operand is always
[02:57] going to be ignored by this % operator.
[03:00] It is strictly going to consider whatever sign is present on the numerator or on the left hand side
[03:08] operand.
[03:08] Let's try to quickly validate these rules inside jshell.
[03:11] So inside my jshell first I'm going to run an modulus expression which is 21 % 0.
[03:19] So here both operands are of type int.
[03:21] And on the right hand side we have an zero as an value.
[03:25] With that you're going to get an exception which is Aritomatic exception.
[03:30] Now let me try to run a expression which is 21 % 2.
[03:36] And with this we are going to get the output as one.
[03:39] But this time if I try to use -21 %2, I'm going to get the output as -1 because
[03:47] the numerator sign is going to be retained by the result.
[03:51] But if you try to mention the same minus symbol on the right hand side operand or on the denominator
[03:57] side, the result is not going to be negative value.
[04:01] You can see we are still going to get the plus one as an output.
[04:04] So let me also try to run a expression which is -21 % -2.
[04:11] With this we are going to get the output which is -1.
[04:14] So whatever -2 here is present.
[04:17] It is not going to cancel the minus present inside the numerator, because the modulus operator is always
[04:23] going to retain the sign by blindly looking at the left hand side operand are at the numerator upper
[04:30] end.
[04:30] So these are the rules that we need to be aware whenever we have the
[04:34] both operands are of type integers.
[04:36] But how about if we have one of the operand as an float or double value.
[04:41] So let's try to understand those rules as well.
[04:44] Whenever you are having one of the operand as an float pointing number or a double number, there are
[04:50] good amount of rules that are going to be applicable.
[04:52] Let's try to understand one by one.
[04:54] The very first rule is, if the right hand operand or if your denominator
[04:59] is 0 or 0.0 or 0.0f.
[05:02] You're always going to get the output as an NaN if you try to execute the expression which is 2.0 f
[05:09] modulus 0.0 f, you're going to get the output as an NaN.
[05:14] Here since we are using the float number, the NaN is going to be from the Float of wrapper class.
[05:20] This rule behavior is different from the division operator in the division operator.
[05:25] In this kind of scenarios, we are going to get a positive infinity or a negative infinity.
[05:31] But with the modulus operator you're always going to get NaN as an output.
[05:36] If you use 0 or 0.0 or 0.0F in the denominator while you are having a float pointing number on
[05:44] the numerator.
[05:45] So I hope you are clear with this difference, so don't get confused.
[05:48] Moving on to the rule two,
[05:50] If we either of your operand is a NaN, the result of the operation will be NaN always
[05:57] for example, in the numerator or denominator, wherever you want, you can take a NaN.
[06:03] It can be a Float.NaN or Double.nan.
[06:05] In all these kind of scenarios where if one of your operand is of type NaN, the output is always going
[06:12] to be NaN.
[06:13] I hope you are clear with the rule number two.
[06:15] Now moving on to the rule number three.
[06:17] If the left operand is an infinity, the result will be always NaN.
[06:22] That means if you have an positive infinity or a negative infinity inside your numerator, you're always
[06:30] going to get a NaN as an output, whereas you have the same infinity value on the denominator or on
[06:38] the right hand upper end.
[06:39] The result will be always same as your left operand.
[06:43] For example, if you try to use the expression 6.3 % Float.POSITIVE_INFINITY, the output
[06:51] is always going to be 6.3.
[06:53] So please make a note about this
[06:55] rule three and rule four.
[06:56] They are looking very similar, but the output is going to be the different based upon where you are
[07:01] keeping your positive infinity.
[07:03] If you are keeping the positive infinity and the left hand side or on the numerator, the result is
[07:09] always going to be NaN.
[07:11] Whereas if you are keeping the positive infinity on the denominator or on the right hand side, the
[07:16] output is always going to be 6.3.
[07:18] Moving on to the next rule, which is if none of the previous rules applies, the modulus operator returns
[07:26] the remainder of the division between your left hand operand and the right hand upper end.
[07:32] For example, here I have given a few examples.
[07:35] So all of them
[07:36] they are going to give a valid remainder value as an output based upon your operand values.
[07:42] So here I want to share a shortcut for you.
[07:45] If your denominator or your right hand operand is greater than compared to your left hand operand,
[07:53] then you're always going to get the remainder as on your left hand operand.
[07:58] So here 25 is greater than 7.5.
[08:01] That's why I'm getting the output as 7.5.
[08:03] And very similarly here
[08:04] also 4.4f is > 4.3.
[08:08] That's why I'm going to get the value which is on the left hand side as an output.
[08:13] So what do we have on the left hand side we have 4.3 f the same
[08:17] we are going to get as an output from this expression.
[08:20] So let's try to validate all these rules very quickly inside the jshell.
[08:24] So the very first rule says whenever you are trying to use the modulus operator with 0 or 0.0f, in
[08:32] all these scenarios you are going to get NaN as an output, even if you try to perform 0.0 % 0.0.
[08:41] In this kind of scenario
[08:42] also, you are going to get the NaN as an output.
[08:45] The second rule says if one of your operand is an NaN, then you're going to get an output also as NaN.
[08:53] So here on the numerator side I'm using the NaN as an operand.
[08:58] Whereas on the denominator or on the right hand side operand I'm going to use a valid float pointing
[09:04] number like 1.5 f.
[09:06] So with this you can see I'm going to get the output as NaN based upon our rule number two.
[09:11] Now let's try to evaluate the rule number three.
[09:14] The rule number three says if you are trying to use positive infinity or negative infinity on the left
[09:22] hand side, then you're always going to get the output as an NaN here by mistake, I'm using the division
[09:29] operator instead
[09:30] I should use the modulus operator.
[09:33] So let me correct this expression.
[09:35] And if I try to execute this expression I'm going to get the output which is NaN.
[09:40] But if I use a same positive infinity on the right hand side or on the denominator, then I'm going
[09:47] to get the same value like in the left upper end.
[09:50] So let me execute 6.3 f %
[09:55] and on the right hand side I'm going to mention
[09:58] Float.POSITIVE_INFINITY.
[10:00] So with this the output you can expect it is going to be 6.3.
[10:05] This behavior conforms with our discussions around rule number three and rule number four.
[10:10] Now moving on to the rule number five.
[10:12] If both of you are operands are a proper normal values like they are not a zero values, they are not
[10:18] a NaN values or POSITIVE_INFINITY or NEGITIVE_INFENITY values.
[10:22] Then in this kind of scenarios, a proper division will happen behind the scenes and you are going to
[10:28] get the remainder as an output.
[10:30] So let me write an expression which is 13.5 % 2.5.
[10:36] So if I try to execute this expression I am going to get the remainder which is 1.0 as an output.
[10:42] Now let me show you one more example where I'm trying to use a left hand operand value, which is less
[10:48] than compared to the right hand side operand value.
[10:51] So here I'm going to mention 4.3 f as the left hand operand value.
[10:56] Whereas on the right hand side I am going to use a value which is 4.4f, which is greater than the
[11:03] left hand operand value.
[11:04] So in this kind of scenarios, we are going to get the left hand operand value as an output.
[11:10] So let me try to execute this,
[11:12] you can see we are getting the 4.3 as an output.
[11:15] With this
[11:16] I'm assuming your super clear about all the rules around the modulus operator.
[11:20] I hope you are understanding the complexity.
[11:22] I can simply teach you that it is going to give you a remainder, and I can show you happy path scenarios
[11:28] and with that I can close the lecture.
[11:29] But I'm trying to share the special scenarios here because I want you to become master of Java so that
[11:36] any kind of tricky questions that you may face inside your interviews or inside your real projects,
[11:42] you will be able to face them with all the concepts that we are discussing inside this course.
[11:48] I hope you are enjoying the course.
[11:50] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
