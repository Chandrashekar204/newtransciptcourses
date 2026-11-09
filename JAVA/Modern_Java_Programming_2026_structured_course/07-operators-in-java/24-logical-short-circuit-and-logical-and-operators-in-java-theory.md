# 7.24 — Logical Short-Circuit AND, Logical AND operators in Java - Theory

> Section 7: Operators in Java

[00:00] Inside this lecture, let's try to discuss about the Logical Short-circuit AND operator and Logical
[00:06] AND operator.
[00:08] The syntax to use the Logical circuit operator is,
[00:11] It's very simple.
[00:12] First you need to mention what is your operand1 followed by you need to mention two ampersand symbols,
[00:19] and after these symbols you need to mention your operand2.
[00:22] So both operand1 and operand2 they have to be of type boolean.
[00:27] You have various options to mention the operand values.
[00:30] You can directly mention the literal values, or you can mention the variable values, or you can mention
[00:35] the Java expressions.
[00:37] Or if needed, you can invoke a Java method as an operand, but your Java method has to return a boolean
[00:44] value, otherwise you're going to get a compilation error.
[00:48] So let's try to understand how these Logical Short-circuit AND operator is going to work.
[00:53] This operator in Java returns true value only if both operands are true.
[00:59] If any one of your operand is false, it is going to result in false.
[01:04] The reason why it is referred as Short-circuit AND operator is, if the left operand, which is the operand1,
[01:11] evaluates to false, then this operator simply ignore operand2 or the expression inside the
[01:18] operand2, because anyway, even if it evaluates the operand2, the output is going to be false
[01:24] only.
[01:24] That's why to achieve some performance, this operator is always going to ignore the operand2 if
[01:31] your operand1 is giving the output as false, I have a table showing you the combinations of operand1
[01:37] and operand2, and what will be the result when we use this Logical Short-circuit AND operator.
[01:44] So you can see if both of your operands are true, then you're going to get the output as true.
[01:49] If one of your operand is false, then you're always going to get the output as false.
[01:55] In the third scenario and the fourth scenario, since the very first operand, which you are going to
[02:00] use on the left hand side is false, then the operand2 is not going to be evaluated.
[02:06] My Logical Short-circuit AND operator simply going to give the output as false and false without looking
[02:12] at the operand2 values.
[02:14] I hope this clear.
[02:15] Now let's see some code examples.
[02:17] Here you can see I have declared a num1, num2 and num1 holds nine and num2 hold six.
[02:24] Once these variables declared along with their values, I built a Java expression with the help of Logical
[02:31] Short-circuit AND operator.
[02:33] So here I have a expression on the left hand side.
[02:37] This expression is num1 > 5.
[02:40] So since the 9 > 5, this entire expression on the left hand side it is going to
[02:46] give an output as true, since the very first operand resulted into the true.
[02:51] Then this operator is going to evaluated what is present on the right hand side.
[02:55] So on the right hand side we have another Java expression where I have defined num2 < 10.
[03:02] And with this expression, since my num2 < 10 , I'm also going to get the output as true
[03:07] on the right hand side.
[03:09] So with that the expression will change to true ampersand,
[03:12] ampersand true.
[03:13] That's why we are going to get the output as true.
[03:16] And the same is going to be assigned to
[03:18] this variable is true.
[03:20] Now if you see another example where I have taken the same kind of input like num1 and num2 here, the
[03:27] very first expression which is on the left hand side of my operator, is going to be evaluated to false.
[03:33] The reason is nine is not greater than ten.
[03:36] That's why this expression is going to give you output as false.
[03:40] And with that my Logical Short-circuit AND
[03:42] operator, it is not even going to look at what is present on the right hand side.
[03:47] It simply going to give the output as false.
[03:50] And here I know you may have a question you are going to ask me to prove it
[03:55] I'm telling that my operator is not going to evaluate the expression on the right hand side.
[04:00] So your question obviously is can you prove it?
[04:03] Show me a demo then
[04:05] only I'm going to believe you.
[04:06] So this is your concern.
[04:08] I can understand your concern.
[04:09] Let me show you an example using which I can prove this concept.
[04:14] Here I have taken an example and this example is some what complicated compared to the previous examples.
[04:20] Let's see what do I have here.
[04:22] As usual, I have created two num variables num1 and num2 with the values nine and six.
[04:28] Now to the left hand side of my operator, I have an expression which is num1 > 5.
[04:34] So since my num1 which is 9 > 5 , this is going to evaluate it to true.
[04:40] That's why my operator is going to look what is present on the right hand side.
[04:45] And the same it is going to be evaluated. On the right hand side
[04:49] I have written an expression where first I'm trying to assign a value 16 to the num2,
[04:55] once these expression is executed, suppose that I'm trying to come
[05:00] num2 > 15.
[05:02] If this expression on the right hand side is going to be evaluated, then num2 is going to become 16
[05:09] and 16 greater than 15 is going to give the output as true.
[05:14] If this operator has true on both sides, you're going to get the output as true.
[05:18] And at the same time, if you try to print the num2 with the help of System.out.println(), you're going
[05:25] to get the output as 16.
[05:26] Initially the value is six.
[05:28] If I try to change the same example into an expression where the left hand side operand is going to
[05:34] give a output as false.
[05:36] In such scenarios, this right hand side expression is not going to be evaluated.
[05:41] If you see
[05:41] first, I'm trying to check if 9 > 10, and since this is false, my operator is not
[05:47] going to look at these right hand side expression.
[05:50] And with that, the num2 is not going to be assigned to 16.
[05:54] The same initial value is going to be present inside the num2.
[05:58] That's why if I try to print the num2 with the System.out.println().
[06:02] With this sample code, I'm going to get the output as six.
[06:05] And this also gives a confirmation to us that these Logical Short-circuit AND operator are never going
[06:12] to execute the right hand side operand or right hand side expression if the left hand operand, or if
[06:19] the left hand expression is evaluated to false.
[06:22] We are going to see the demo of these code in few minutes.
[06:25] But before that, I want to discuss very quickly about the Logical AND operator.
[06:30] So the syntax to use this operator is you just need to mention a single ampersand compared to the Logical
[06:37] Short-circuit AND operator.
[06:39] This operator is going to have a single ampersand value.
[06:42] The only difference between this operator and the previous operator that we have discussed is this Logical
[06:49] AND operator is always going to execute the right hand side expression or right hand side operand,
[06:56] regardless of the output from the left hand side upper end.
[07:00] So that's the only difference.
[07:01] Other than that, the output you are going to get is always going to be the same, like the
[07:07] Logical Short-circuit AND
[07:08] operator.
[07:08] You can see this also going to give true as an output only if the two operands are true.
[07:14] Otherwise it is always going to give the false.
[07:17] But like we discussed the second operand is always going to be executed even if the operand1 evaluated
[07:24] to false.
[07:25] So if you are into the scenarios where you are looking for and performance where you don't want to execute
[07:31] the expression on the right hand side unnecessarily, then you can always go for the Logical Short-circuit AND
[07:38] operator.
[07:39] Most of the times developers they also use the same.
[07:42] But if there are some peculiar scenarios where you want to evaluate both operands for whatever reasons,
[07:49] regardless of what is the value present inside the operand1 in such scenarios you can use these Logical AND
[07:56] operator.
[07:57] Can we see some code examples here you can see I have an code example where I have declared same variables
[08:03] like num1 and num2 with the values nine and six.
[08:06] For the statement inside the third line, we are going to get the output as true because num1 which
[08:11] is 9 > 5, which is true, and num2 < 10 is also true.
[08:16] So the true on both sides for this operator is going to give the output as true.
[08:21] Whereas for the last line, if you try to execute the left hand side expression, which is num1 > 10,
[08:27] it is going to become false because we have nine under num1 and the right hand expression,
[08:33] which is num2 < 10 is going to become true.
[08:37] So false on the left hand side and the true on the right hand side to this operator will give an result
[08:43] which is false.
[08:44] Now let me show you another example to prove you that that this operator is always going to evaluate
[08:51] the right hand side expression or right hand side operand, regardless of what is the value present
[08:56] on the left hand side.
[08:58] So here you can see I have taken an expression which is num1 > 10.
[09:02] Since nine cannot be greater than ten.
[09:05] This left hand expression, you're going to get the output as false.
[09:09] And since we are using the Logical AND operator here, the right hand expression at the right hand upper
[09:16] end is still is going to be evaluated, even though my left hand operand is false.
[09:20] So that's why this num2 is going to be assigned to 16.
[09:25] And when we print the same with the help of System.out.println(), we are going to get the output as 16.
[09:31] With this, I'm assuming you are clear about the what is the Logical AND operator, and what is the
[09:36] Logical Short-circuit AND operator.
[09:39] So please be aware about the differences between them. Inside your interviews or inside your Java related
[09:45] exams
[09:45] people can trick you by using single ampersand or double ampersand.
[09:50] So regardless of what operator they are using, if you are clear with the basics of these operators,
[09:55] you should be able to answer those questions very easily.
[09:59] In the next lecture,
[10:00] let's see the demo of these operators by writing some code inside IntelliJ.
[10:05] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
