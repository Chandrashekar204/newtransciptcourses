# 7.26 — Logical Short-Circuit OR, Logical OR operators in Java - Theory

> Section 7: Operators in Java

[00:00] Inside this lecture, let's try to discuss about the Logical Short-circuit OR operator and the Logical OR
[00:07] operator.
[00:08] The syntax to use the Logical Short-circuit OR operator is,
[00:12] first you need to mention what is your operand1 on the left hand side followed by
[00:17] you need to mention pipe symbol or vertical bar symbol two times.
[00:22] Once you have mentioned this symbol, you can mention what is your operand2 on the right hand side.
[00:27] These OR operators
[00:28] they are also work very similarly like AND operator, except with the rules that they follow.
[00:34] The rule that these Logical Short-circuit OR operator is going to follow is if one of your operand is
[00:42] true, then the output from these operator is going to be true.
[00:47] You're only going to get false if both of your operands is false.
[00:52] I have mentioned a table also for your reference.
[00:54] You can see we are going to get output as true in the very first to three combinations because we have
[01:00] at least one operand as true in the very first three combinations, whereas in the last combination
[01:07] we have both operands as false.
[01:09] That's why we are going to get the overall output as false when we are using these Logical Short-circuit OR
[01:15] operator.
[01:16] If you are very first operand is evaluated as true, then these operator immediately it is going to
[01:23] return the overall output as true without evaluating or validating the right hand operand or right
[01:31] hand expression.
[01:32] That's why you can see I have also highlighted in the very first two combinations, where the left hand
[01:38] side operand is true,
[01:39] in this kind of scenarios, this operator does not care about what is their present on the right hand
[01:46] side.
[01:46] The way this operator works is very similar to the Logical Short-circuit AND operator, but you need
[01:53] to be aware about the rules that I have highlighted in the table.
[01:57] Now, if you try to see a few examples around this operator, you can see I'm trying to create two into
[02:02] variables like num1 and num2.
[02:04] Using these two variables only, I have built an expression with the help of these Logical Short-circuit OR
[02:11] operator.
[02:12] So on the left hand side I have mentioned num1 < 5.
[02:17] This is going to be evaluated as false because num1 holds nine, so nine less than five is going to
[02:24] be false.
[02:25] That's why this operator is going to look at what is present on the right hand side.
[02:31] So since on the right hand side this expression is going to be evaluated as true, the overall output
[02:37] we are going to get as true.
[02:38] Whereas if you change the same example to num1 greater than five on the left hand side, since this
[02:45] left hand side operand or expression is going to result into true, my Logical Short-circuit OR operator
[02:51] is not going to evaluate what is present on the right hand side, it is simply going to give the overall
[02:58] output as true.
[02:59] But I have mentioned this as false,
[03:01] it's my mistake.
[03:02] I'm going to correct these after recording this video on the very similar lines.
[03:06] We also have another operator which is logical or operator.
[03:10] So the syntax to use this operator is to use only a single pipe symbol or a single vertical bar between
[03:17] your two operands.
[03:19] And the rules that these operator is going to follow is very similar to the Logical Short-circuit OR
[03:25] operator.
[03:26] You can see the same table I have mentioned.
[03:28] The only difference is this Logical OR operator is going to evaluate your operand two expression as
[03:36] well, regardless of whatever the value present on the operand1 even in the scenarios where you are
[03:42] operand1 resulted into true,
[03:44] even in such scenarios, this operator is going to evaluate what is there on the right hand side, operand
[03:51] or on the operand2 two.
[03:52] Now, very quickly, let's try to understand examples on how to use these
[03:57] OR operator.
[03:58] You can see we just have to use a single vertical bar or a single pipe symbol whenever you want to use
[04:05] these Logical OR operator.
[04:08] In this example, if you look at the line number three on the left hand side, we have mentioned an
[04:13] expression which is num1 > 5.
[04:16] So this is going to give the output as true.
[04:19] But still this operator is going to evaluate what is present on the right hand side as well.
[04:24] So on the right hand side we have an expression 6 < 2.
[04:28] So this is also true since we have true on both sides of this
[04:32] operator we're going to get the output as true.
[04:34] This operator needs only a single operand to be true.
[04:38] Otherwise it is going to give the false the same
[04:40] you can see in the next line of code.
[04:42] In the next line of code
[04:44] first, the left operand is going to give the output as false, followed by on the right hand side
[04:49] also, we are going to get the output as false.
[04:52] That's why the overall output we are getting is false.
[04:55] I have given an example to prove you that that this operator is always
[05:00] is going to evaluate the right hand side operand.
[05:02] So here you can see inside this example this num1 less than ten is going to result into true.
[05:08] But still my Logical operator is going to evaluate the right hand expression.
[05:12] That's why we are going to get the output as 16 when we try to print these num2 value.
[05:17] So all these examples are very similar to what we have discussed as part of and operators, the same
[05:24] kind of examples and combinations I have considered for the our operators as well.
[05:28] I hope you are clear with these theory discussion.
[05:31] In the next lecture, let's try to build some code examples inside IntelliJ to clear our understanding
[05:38] further about the OR operators.
[05:40] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
