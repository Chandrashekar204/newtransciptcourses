# 7.19 — Equality Operator in Java - Part 2

> Section 7: Operators in Java

[00:00] To share more details about how the equality operator is going to work.
[00:05] I'm going to give you a puzzle like you can see this is a piece of code.
[00:09] So here I have created three int variables like num1, num2, num3.
[00:14] And to all of them I have assigned a same value which is 9 . And inside the same code
[00:20] I also have a boolean variable with the name a.
[00:23] Now in the last expression, if you see with the equality operator, I'm trying to compare three variables
[00:30] num1 and num2, num3 if they are holding the same value, but this last line is not going to compile,
[00:36] it is going to throw an compilation error.
[00:39] Let's try to understand why the compilation is going to fail with the last line of code.
[00:45] Whenever we are trying to use the equality operator, it is always going to evaluate the expression
[00:50] from the left to right, because it is an left to associate to operator. With that information
[00:58] first, num1 will be compared with the num2.
[01:01] Since both these num1 and num2, they are holding the same value.
[01:06] The result from these num1 ==num2
[01:09] is going to give you the output as true, and with that the boolean value which is true, you are
[01:16] going to compare with the num3.
[01:18] So what is num3,
[01:19] num3 is an int data type, whereas the output from the first comparison, which is num1 and num2 you
[01:27] got a boolean value.
[01:28] So with that, what is going to happen for this second equality operator that you have inside your expression
[01:35] on the left hand side, you're going to have an operand of type boolean, whereas on the right hand
[01:40] side you're going to have an operand of type integer.
[01:43] Is this allowed inside equality operator,
[01:46] off course not.
[01:47] Whenever we are trying to use equality operator, we need to make sure both operands belong to the same
[01:52] data type.
[01:53] That's why this piece of code is going to fail at the compilation time.
[01:58] Then how to fix this issue?
[01:59] To fix this issue, we can use a parenthesis.
[02:03] So what I can do is num1, num2
[02:06] I can try to compare with the help of equality operator by keeping inside parentheses and similarly
[02:12] num2 and num3
[02:13] I will try to compare in a different parenthesis, and in between them I'm going to use an logical and
[02:21] operator where I had to discuss about this logical and operator in the coming lectures we are going
[02:26] to discuss about this, but if you try to understand this expression first, this num1, num2 is going
[02:32] to be evaluated and we are going to get the output as true. Post that here
[02:36] also, this num2 and num3 is going to be evaluated with the help of equality
[02:42] operator.
[02:42] And here also we are going to get the output as true.
[02:46] So with that, the logical and operator is going to have true on the left hand side and on the right
[02:52] hand side
[02:52] also it is going to have true.
[02:54] So if you feed two true values to the logical and you're going to get the output as true itself, that's
[03:00] what is going to be stored inside the a boolean variable.
[03:04] So this is how you can fix it.
[03:06] Can we try this very quickly inside the intelliJ.
[03:08] Let's do it.
[03:09] So here I already have num1 and num2.
[03:12] What I'm going to do is, I'm going to create one more int variable with the name num3.
[03:18] And to this also I'm going to assign 9 value.
[03:21] Now if I try to build the same expression that we discussed like boolean, and after mentioning the
[03:28] boolean I'm going to create a variable with
[03:30] the name isSimilar to
[03:33] this isSimilar variable
[03:34] first I'll try to assign an expression which is num1 == num2 ==num3
[03:43] .
[03:44] Here we are getting a compilation error because the equality operator cannot be applied to boolean and
[03:51] int.
[03:51] So first this num1, num2 is going to be evaluated since the associativity of this operator is from left
[03:59] to right.
[04:00] So the true is going to be present on the left hand side, and on the other side we are going to have
[04:05] num3 which is of type int.
[04:07] With that the compilation is going to fail.
[04:10] So how to fix this?
[04:11] First we need to make sure we are mentioning num1 and num2 inside parentheses and post that we can mention
[04:18] num2 == num3.
[04:22] In another parenthesis, and in between these two parentheses operations, we can mention logical and
[04:30] operator.
[04:31] So if I try to execute this program under isSimilar, you can see we are going to have a value which
[04:36] is true.
[04:37] I hope this is clear.
[04:38] Let me release this breakpoint.
[04:40] Now let's try to understand a few rules that my equality operator is going to follow
[04:46] whenever we are using floating point operands with the equality operator, the rule number one is if
[04:53] one of your operand is of type NaN, then the equality operator is always going to
[04:59] return the output as false, even if both operands are NaN
[05:03] also, even in such scenarios, the result is going to be false.
[05:08] So here you can see I have a num1 which is of type Double.NaN, whereas num2 is a simple double
[05:14] number which is 3.14.
[05:16] If I try to compare, I'm going to get a false value.
[05:20] The same behaviour
[05:21] you can also see, even if you try to compare two variables which are holding the values NaN.
[05:27] Even in this kind of scenario
[05:28] also we are going to get the output as false.
[05:31] But with this behaviour or limitation, you may have a question.
[05:34] What if I have a scenario inside my project where I want to check whether a given double variable or
[05:42] a given float variable contains NaN value.
[05:45] So for all these kind of scenarios, we should not use the equality operator.
[05:50] Instead, we need to use the isNaN() static method available inside the wrapper classes like Double and
[05:58] Float.
[05:58] For example, if you are looking for an option to check whether a given double variable holds a NaN
[06:05] value or not, the correct approach is to use the isNaN() static method, which is available inside the
[06:11] Double wrapper class.
[06:13] So to this isNaN() method
[06:14] you can simply pass your double variable, and if your variable is really holding the NaN value, you're
[06:21] going to get the output as true.
[06:23] The same applies for float type variables
[06:25] also inside Float wrapper class
[06:27] also we have an isNaN() method.
[06:30] Moving on to the rule two
[06:31] this is going to be super simple.
[06:33] We already discuss about this many times in the previous lectures.
[06:37] Always inside Java
[06:39] positive zero and negitive zero is always considered as equal.
[06:44] That's why if you try to compare two different variables that are holding the positive zero and negitive zero,
[06:51] you're always going to get the output as true.
[06:54] I think this should be very simple for you to understand.
[06:57] Now let me go to the rule number three.
[06:59] The rule number three says if both of your operands are positive infinity or negative infinity, the
[07:07] equality operator always going to return the true.
[07:10] Whereas if one of the operand is positive infinity and the other one is negative infinity,
[07:15] in such scenarios the output is going to be the false.
[07:18] So here you can see I have provided an example where
[07:22] inside num1 I'm trying to hold the positive infinity, whereas inside the num2 I'm trying to store
[07:28] negative infinity.
[07:30] If I try to compare both of these variables with the help of equality operator, I'm going to get the
[07:35] output as false because they are two different values.
[07:39] Whereas if my both num1 and num2, they hold the same positive infinity or the same negative infinity.
[07:46] In such scenarios the output will be true.
[07:48] And the last rule that we have around the equality operator is whenever you are trying to compare two
[07:54] finite values, the equality operator always checks whether the values are numerically equal.
[08:01] So this is very obvious.
[08:03] We are already aware about this rule.
[08:05] So here you can see I have three variables num1 and num2, num3.
[08:09] Since num1 and num2 they are holding the same double value.
[08:13] If I try to compare them, I'm going to get the true value.
[08:17] Whereas if I try to compare num1 with the num3, since they are holding two different values,
[08:22] I'm going to get the output as false.
[08:25] I hope you are clear with all these rules and the special scenario that we have discussed around the
[08:30] equality operator.
[08:31] In the next lecture, let's try to understand the enemy of this equality operator, which is inequality
[08:38] operator.
[08:39] Thank you
[08:39] and I'll catch you in the next lecture bye.

----------------------------------------
