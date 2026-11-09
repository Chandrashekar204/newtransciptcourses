# 7.11 — Division Operator in Java

> Section 7: Operators in Java

[00:00] Inside Arithmetic operators as of now
[00:02] we discussed in detail about addition operator. Whatever we discuss
[00:07] for addition operator, the same set of rules and concepts are applicable for subtraction and multiplication
[00:16] operators as well.
[00:17] That's why I'm not going to discuss in detail about subtraction and multiplication.
[00:22] With that, let's try to discuss the next set of operators that we have inside Arithmetic operators,
[00:28] which are division and modulus.
[00:31] If you can recall our school days we used to have mathematic exam
[00:35] and inside these mathematic exam, maybe when you're studying third or fourth class your teacher might
[00:42] have given a question like perform the division on top of these two numbers and tell me what is a quotient.
[00:48] And very similarly, the teacher can also ask you the same question in another flavor.
[00:53] By providing two numbers, the teacher is going to ask you to perform the division operation and give
[00:59] me what is the remainder as an answer.
[01:02] With this, it should be pretty clear for you.
[01:04] Like whenever we try to perform the division, we get two types of results.
[01:09] One is quotient and the other one is remainder.
[01:12] So to accommodate these two different types of results, we have two different Arithmetic operators.
[01:18] The very first one is division.
[01:20] Using these operator, whenever we try to perform division operation on top of two numbers, by using
[01:26] a symbol forward slash (/) , we're always going to get the quotient value as an output, whereas if you
[01:33] are interested more about the remainder, then you can go for the another operator, which is modulus (%).
[01:38] If you try to apply this modulus operator on top of two numbers, by using the symbol percentage, you
[01:45] are going to get the remainder as an output value.
[01:48] So this is a very quick introduction about these division and modulus operators.
[01:53] But let's try to understand in detail about these operators for the same
[01:58] first I'm going to focus on division operator.
[02:01] Whenever we are trying to perform the division operation with the help of this forward slash (/), the division
[02:07] can happen in two different flavors.
[02:09] The very first flavor is integer division.
[02:12] If you are both, operands of the division operator are integers like byte, short, char, int, or
[02:19] long.
[02:19] The division operation is going to perform in an usual way, and the result is going to be truncated
[02:26] towards zero to represent an integer.
[02:29] That means if you try to give two different values for numerator and denominator of your integer division,
[02:36] you're always going to get an output in an integer format.
[02:40] For example, if you try to perform the division 9 / 2 two internally, the division
[02:47] result is going to be 4.5.
[02:49] But since we are trying to perform the division operation on top of integers, the decimal part or the
[02:56] fractional part is going to be disregarded or truncated, and the final result we are going to get is
[03:03] four.
[03:03] So instead of 4.5 you're going to get four.
[03:06] This type of division where the fraction part is going to be ignored is known as integer division.
[03:12] And when this integer division is going to happen only in the scenarios where you are both operands
[03:17] are numeric integer values.
[03:19] But if one of your operand is a float or double number, then a float point division is going to happen
[03:27] and the result that you are going to get will be in float or double format, which means the decimal
[03:33] precision value is going to be retained without truncation.
[03:38] For example, if you try to perform this division with the help of 27 / 2.0f, in this
[03:45] scenario, the output you are going to get is 13.5.
[03:48] So with this, it should be pretty clear for you the type of division that is going to be carried out
[03:54] by the JVM is going to depend on your type of operands that you are going to use.
[04:00] Let's see the demo of this very quickly
[04:02] inside IntelliJ.
[04:03] Inside my Arithmetic operators demo, I'm going to write a simple division expression.
[04:09] So let me write int result1 = 9/2.
[04:16] So there are two operands
[04:18] here you have nine and two.
[04:20] Both of them are of type int format.
[04:22] With this the integer division is going to happen.
[04:26] But if you try to perform the same division by using a decimal operand, then the floating point division
[04:33] is going to happen.
[04:34] So let me change this values to 27 by 2.0 f in the denominator
[04:41] I'm using the float.
[04:43] Since one of the operand is of type float, I'm going to get the result also in an float format.
[04:49] So that's why I'm getting a compilation error here.
[04:52] So instead of int I need to use float with this
[04:56] If you try to execute this program in debug mode will be
[04:59] able to see what are the values that we have under result1 and result2 and the result1
[05:04] you can see we are having the quotient value in the integer format.
[05:10] So we have only 4 but not 4.5,
[05:13] whereas in the next expression the result2 is going to have the exact quotient value by including
[05:20] the decimal values as well.
[05:21] So that's why here the output is going to be 13.5.
[05:25] I hope you're clear.
[05:26] Now let me discuss about few special scenarios.
[05:30] Whenever you're performing these division operation,
[05:33] with these division operator, you need to be aware about few special scenarios.
[05:38] The very first scenario is, in the numerator if you have an integer number, and in the denominator if
[05:44] you try to use zero, then you're always going to get an Arithmetic exception during the runtime.
[05:50] So there won't be any compilation issues, but at runtime you're going to get these exception.
[05:55] But if your numerator operand is an float or decimal number, then dividing by zero will not result
[06:03] into an any exception.
[06:04] Instead, you're going to get positive infinity or negative infinity based upon the numerator value
[06:11] that you are trying to use.
[06:13] We can validate all these points very quickly inside the jshell.
[06:16] We don't have to explore them inside IntelliJ, because when we get runtime exceptions, you may not
[06:21] be able to run the complete program successfully.
[06:23] That's why let's try to evaluate these points very quickly inside jshell itself.
[06:28] So inside jshell I'm going to first mention a numeric integer value.
[06:33] So I'll just mention 24.
[06:35] And I'm trying to divide this with zero.
[06:37] And with this we are going to get an RuntimeException.
[06:41] And the Runtime Exception that we are going to get is of type Arithmetic exception.
[06:45] Whereas if I try to perform the same operation with a decimal number like 24.0, I'm not going to get
[06:53] Airthametic exception,
[06:55] Instead I'm going to get an positive infinity, because in the numerator I'm using the positive number.
[07:02] This time let me try to use a negative number.
[07:05] The negative number is -24.0 / 0.
[07:10] So here I'm going to get minus infinity as an output.
[07:14] The behavior is going to be the same even if you try to use 0.0 in the denominator.
[07:21] So regardless whether you are using 0 or 0.0 the behavior is going to be the same.
[07:27] Now let's try to discuss the last important point.
[07:30] What will be the output if you try to divide 0.0 and 0.0?
[07:35] If you're trying to use float representation of 0.0, you're going to get NaN as an output.
[07:41] So what is NaN?
[07:42] Nan indicates not a number.
[07:45] Very similarly, if you try to use the double representation of 0.0, you are going to get NaN value
[07:52] from that Double class.
[07:53] So inside the Double class we have a static variable constant with the name NaN.
[07:58] So the same NaN you are going to get as an output.
[08:01] So let's validate this point also very quickly inside this jshell.
[08:04] So here first I'm going to mention 0.0f / 0.0 f.
[08:11] For this the output is going to be NaN.
[08:14] And what is this type of NaN.
[08:16] It will be equal to the same NaN static variable that is available inside the float wrapper class.
[08:22] If you try to perform the same operation with the 0.0, which is in the format of double number, you're
[08:30] going to get the same NaN as an output.
[08:33] But this time this NaN represents the static variable constant available inside the Double wrapper class.
[08:40] With this, I'm assuming your super clear about how to use the division operator inside your Java statements.
[08:47] In the next lecture, let's try to understand how to use the modulus operator.
[08:52] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
