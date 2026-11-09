# 7.25 — Logical Short-Circuit AND, Logical AND operators in Java - Demo

> Section 7: Operators in Java

[00:00] Let's write some Java logic to evaluate our understanding around the Logical Short- circuit AND operator,
[00:07] and Logical AND operator.
[00:09] Inside my LogicalOperatorsDemo class, I already have two int variables with the name num1 and num2,
[00:16] and inside these variables we have values like nine and six.
[00:20] That's why I'm not going to create these variables one more time.
[00:23] I'm going to straight away write an expression which is boolean a,
[00:27] a is a variable name is equal to
[00:30] first I'm going to write the expression related to the left operand.
[00:34] Inside this expression I'm going to mention num1 > 5.
[00:39] Post this expression I'm going to mention the ampersand symbol two times ( && ), followed by I'm going to
[00:45] write the right hand operand expression.
[00:48] First, let me mention parentheses, and inside this parentheses I'm going to mention one more pair
[00:53] of parentheses.
[00:54] Inside the inner parentheses I'm going to write an expression which is num2 = 16.
[01:00] With this inner expression I'm trying to assign a value 16 to the num2 post that I'm going to mention
[01:06] greater than operator, followed by 15.
[01:10] With this
[01:10] when my right side operand expression is executed, the num2 value is going to be 16.
[01:16] But do you think these right hand side expression is going to be executed in this overall expression?
[01:22] Off course it is going to execute because the left hand side operand it is going to evaluate as true.
[01:27] That's why my Logical Short-circuit AND operator, it is also going to evaluate the right hand side
[01:33] expression.
[01:34] To evaluate the same.
[01:35] We can try to print few variables here.
[01:37] The very first one I want to print is a boolean variable followed by I want to display the num2 variable.
[01:44] So if I try to execute this program, you can expect a value true inside a and under the num2 we can
[01:51] expect a value 16.
[01:52] So let me try to execute this program.
[01:54] You can see we have an output which is true and 16.
[01:58] Whereas if I try to change this 5 to 10, with that my left hand side operand expression is going
[02:05] to give a result as false.
[02:06] And my Logical Short-circuit AND operator is not going to evaluate this expression.
[02:11] In this scenario, the output we are going to get is false, and under the num2 we are going to have
[02:17] the initial value, which is six.
[02:18] So let me try to execute this program.
[02:20] And you can see we have an output which is false and six.
[02:24] But here instead of these Logical Short-circuit AND operator, if I use logical and operator by simply
[02:31] mention a single ampersand ( & ).
[02:33] In this scenario, even though my left hand side operand is going to be evaluated as false.
[02:39] Still, my Logical AND operator is going to be
[02:42] evaluate this right hand operand expression.
[02:45] We can also confirm this by executing this program.
[02:49] You can see under the num2 you will be able to see a value.
[02:52] This gave a confidence to us.
[02:54] Whatever concepts that we have discussed about the Logical Short- circuit AND operator and Logical AND
[03:00] operator in the previous section, they are working in very similar manner.
[03:04] But like I said in real project, always try to prefer using the Logical Short-circuit AND operator
[03:12] because it is going to provide some performance improvements in the scenarios where if your left hand
[03:17] operand is going to result in false, then your JVM or Java is not going to execute what we have on
[03:24] the right hand side, and this gives some performance improvement for your code.
[03:28] I hope you are clear.
[03:29] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
