# 7.20 — Inequality Operator in Java

> Section 7: Operators in Java

[00:00] Now inside this lecture, let's talk about the inequality operator.
[00:05] This operator is going to perform exactly opposite behavior of equality operator.
[00:12] That's why on a funny note, we can call this inequality operator as an enemy to the equality operator.
[00:19] So these operators are like siblings, but they always fight with each other.
[00:23] When the equality operator, say yes the inequality operator is always going to say as no.
[00:29] So let's try to understand how to use this inequality operator and how it is going to work.
[00:34] The syntax is going to be very similar to equality operator, where first you're going to mention what
[00:39] is your operand one, followed by what is the symbol of inequality operator.
[00:44] The symbol of inequality operator is exclamatory mark followed by equal to symbol ( != ) and post that you
[00:51] can mention
[00:52] what is your operand two on the right hand side. The behavior of this inequality operator is it is
[00:58] always going to return true if operand one and operand two, if they are not equal.
[01:04] Otherwise, if the operand one and operand two are equal, then the output from these inequality operator
[01:10] is going to be the false.
[01:11] So this is the exact opposite behavior of the equality operator.
[01:16] When we are using inequality operator, we are asking JVM whether two operands are not equal or not,
[01:24] whereas with the equality operator, the question is going to be like whether two operands are equal
[01:30] or not.
[01:31] Since the way we ask the question to the JVM changed exactly in the opposite way
[01:37] that's why the behavior
[01:38] also, we are going to see exactly opposite behavior when we use the equality and inequality operators.
[01:45] So here I have provided some examples.
[01:47] You should be able to understand these examples very easily.
[01:51] So first I have num1 and num2 variables.
[01:53] And they are holding two different values.
[01:55] So if I try to use the inequality operator on these two variables I'm going to get the output as true
[02:02] because they are not equal.
[02:04] Very similarly, I also have an expression where I have two variables of boolean like bool1 and bool2,
[02:10] and they hold two different values like true and false.
[02:14] If I try to use inequality operator on these two operands, I'm going to get the output as true because
[02:20] they hold two different values. The same behavior
[02:23] you can also observe with the double variables as well.
[02:27] Let's try to code these examples inside intelliJ and see the behavior in action.
[02:32] So here first I'm going to create two integer variables with the name num4,
[02:37] and inside the num4 I'm going to hold the value five and post that inside the num5 I'm going
[02:43] to hold the value which is 10.
[02:45] If I try to compare both of them with the help of inequality
[02:49] operator, I'm going to get the output as true because they are holding two different values for the
[02:55] same
[02:56] let me write a piece of logic here.
[02:58] First, I'll mention boolean post that I'll mention the variable name as isNotEqual, and to this
[03:06] variable I'm going to assign an expression which is num4,
[03:10] post that, I'll mention inequality operator followed by num5.
[03:15] So if I try to execute this program and see what is the value inside the isNotEqual, you can see
[03:21] we are having a value true because they are holding two different values.
[03:26] I hope this is clear.
[03:27] Now let me do the same for with the boolean variables and double variables as well.
[03:33] So first I'm going to create a boolean variable with the name bool1
[03:37] and inside this I'm going to store the value true and very
[03:40] similarly I'm going to create bool2.
[03:43] And inside this I'm going to store the value false.
[03:45] So if I try to copy the same expression here and use the variables like bool1 and bool2 here
[03:53] also I'm going to get the output as true.
[03:55] So what I can do is here I can try to remove this boolean with that
[04:00] the same variable which is is not equal to I'm going to use here as well.
[04:05] So whatever value that we have here that will be overrided at the line number 22.
[04:10] So let me try to execute this program.
[04:12] And you can see at the line number 22 the isNotEqual is having a value which is true because we are
[04:20] trying to compare two boolean operands which are holding the two different values. The same behavior
[04:26] you can also observe when you try to compare floating numbers like double numbers or float numbers.
[04:32] Let me show you the demo of the double operands as well.
[04:36] So here I'm going to paste this line of code and replace this int with double instead of num4,
[04:42] I'll mention num6 and num7 here
[04:46] and the number I'm going to assign for num6 is 3.14.
[04:51] And very similarly for num7 I'm going to assign the number which is 3.14 itself.
[04:58] Let's see what is going to happen
[05:00] if you try to compare two different operands with the help of inequality operator that are holding the
[05:06] same value.
[05:07] So here I'll remove this boolean so that the same variable is not equal to I can use here.
[05:13] So instead of num4 and num5 I'll mention num6 and num7.
[05:18] Now if I try to execute this program you'll be able to see isNotEqual at the line 26 is holding the
[05:25] value false because both my operands of double, they are holding the same value.
[05:30] And in this kind of scenarios we know inequality operator is going to return the output as false.
[05:36] I hope you are clear with these live demos.
[05:38] Now quickly let's discuss the rules that we need to be aware whenever we are trying to deal with floating
[05:45] point types with the inequality operator.
[05:48] So whatever rules that we have discussed previously for the equality operator, the same set of rules
[05:53] applicable here as well.
[05:55] But we are going to see the opposite behavior.
[05:58] The rule number one says if one of your operand is NaN, the inequality operator is always going to
[06:05] return the true.
[06:06] Even if both your operands are NaN, still, the inequality operator is going to return the output as
[06:12] true.
[06:13] Whereas with the equality operator we saw with this rule, we are always going to get the output as
[06:17] false.
[06:18] The rule number two says since the positive zero and the negitive zero considered as equal, if you try to use
[06:25] the inequality operator on top of positive zero and negitive zero, you're always going to get the output as false.
[06:32] Here also, we are seeing the opposite behavior of equality
[06:36] operator.
[06:37] Moving on to the rule number three, which is whenever you are both operands have positive infinity
[06:43] or negative infinity.
[06:45] The inequality operator is going to return the false.
[06:48] Whereas if one of the operand is positive infinity and the other is negative infinity.
[06:53] In such scenarios, the result from the inequality operator is going to be the true, and the last rule
[06:59] is,
[07:00] regarding the finite values.
[07:01] Like we discussed previously, we saw in the examples as well.
[07:05] The inequality operator checks if the values are numerically not equal or not.
[07:10] If both operands are having the same value, the result is going to be false, whereas if the values
[07:16] are different, the result is going to be true from the inequality operator.
[07:21] Apart from these rules, the special scenario that we have discussed with the equality operator, the
[07:26] same applies for the inequality operator as well.
[07:29] So you're also going to get the compilation error if you try to use the inequality operator with the
[07:36] format that we discussed previously.
[07:38] For example, here I can try to create a variable isSimilar1,
[07:42] and to this variable I can try to assign num1 != num2 !=num3.
[07:51] Here you can see we are getting a compilation error because the output from these is going to be a boolean
[07:57] operand.
[07:58] If you try to mention a boolean operand on the left hand side and the int operand on the right hand
[08:04] side, you're going to get the compilation error.
[08:06] So to resolve this we need to use the same format like we discussed previously.
[08:11] So num1 != num2 in a parenthesis
[08:15] and num2 != num3 inside another parentheses.
[08:19] And we can club both of them with the and operator.
[08:23] So from this expression you're going to get an output in an boolean format which will be stored inside
[08:30] the variable which is isSimilar1.
[08:32] You can see there are a lot of similarities between equality operator and inequality operator.
[08:38] The only important point that you need to be aware is they behave exactly in an opposite manner.
[08:45] I hope you are clear everything about the inequality
[08:48] operator.
[08:48] Thank you, and I'll catch you in the next lecture bye.

----------------------------------------
