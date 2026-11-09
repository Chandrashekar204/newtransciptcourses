# 24.18 — Deep dive on BiFunctional Interfaces - Part 2

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Inside this lecture
[00:01] let's see the demo of BinaryOperator interface.
[00:04] So if you can search for binary operator interface you can see it is extending the BiFunction interface,
[00:12] which is capable of processing the same data type as an input and output.
[00:18] So when we should use this BinaryOperator, when you are input data type and the output data type,
[00:24] they are going to be same in all such scenarios.
[00:26] Instead of mentioning three different data types, you can happily use the BinaryOperator.
[00:31] So this interface, it is going to inherit all the methods from this BiFunction.
[00:35] On top of that, like we discussed, it has two static methods like minBy() and maxBy() which we can use
[00:41] to identify the maximum value or a minimum value based upon the comparison logic that we are going to
[00:47] provide.
[00:48] I'll show you the demo in few minutes.
[00:50] Before that, let's try to define a lambda expression with the help of BinaryOperator. For the same,
[00:55] here you can see as of now we are trying to write this logic with the help of BiFunction, but the
[01:01] same can be achieved with the help of BinaryOperator as well.
[01:05] The reason is it's very simple.
[01:06] The input data type and the output data type is double, which is same in all the places.
[01:12] So that's why I can copy this piece of code and paste it here instead of BiFunction.
[01:18] I'll mention BinaryOperator that you need to mention double only once, and I'll rename this variable
[01:25] name to calculate power with vivo.
[01:29] Vivo means BinaryOperator.
[01:31] So using these variable name this time I'm going to invoke apply() method with the input five and two.
[01:38] So if I execute this program I should get the output which is 25.0 like we expect.
[01:44] As a next step, let me show you the demo of the static methods available inside these BinaryOperators.
[01:50] Since they are new to you, it would be a wise addition to see a demo around them.
[01:54] So to invoke the static methods, first I need to type BinaryOperator followed by
[01:59] I need to invoke the method which is maxBy().
[02:02] Think like I have a requirement where I'm going to pass two different int values, and from these two into values,
[02:08] my maxBy() lambda expression should return one of the int value, which is a maximum value.
[02:14] So if you see here the input and output everything is integer.
[02:18] That's why on the left hand side I'm going to mention BinaryOperator in the angle brackets integer
[02:25] followed by I'll give a variable name to my lambda expression, which is maxOperation.
[02:31] Now on the right hand side to this maxBy() method, I need to pass a lambda expression along with the
[02:37] comparison logic.
[02:38] So first I'll try to mention the input parentheses.
[02:41] Inside this input parentheses, I'll mention the parameter names as a, b.
[02:46] So these a, b represent two different int numbers.
[02:49] So now I want to provide a comparison logic on how to compare these two integer values.
[02:55] To derive the maximum number.
[02:57] We already have such logic inside the compare static method available inside the Integer class.
[03:04] So to this Compare class, I'm going to pass the input a, b.
[03:08] So with this now we have the maxOperation ready.
[03:11] So using these maxOperation I'm going to invoke the apply() method.
[03:16] To this apply() method I'll pass two different int values like 16, 30.
[03:21] So when we execute this line of code we are going to get a number which is a maximum number.
[03:26] I can also confirm that by printing the output onto the console with the help of System.out.println().
[03:33] So if I execute this program, you can see I'm going to get the output 30.
[03:37] In the similar lines, we can also use minBy() static method available inside the BinaryOperator.
[03:43] Here instead of maxBy(), I'm going to invoke the minBy() method and the variable name
[03:48] also, I'll just mention as minOperation.
[03:51] Using the same minOperation, I can invoke the apply() method.
[03:55] So if I execute the program this time, I'm going to get the output as 16 because this is a minimum
[04:00] number.
[04:00] So if you see the beauty here, I didn't change anything on the comparison logic side, since I'm using
[04:06] the minBy() behind the scenes, the comparison logic is getting reversed to derive the minimum number.
[04:12] I hope this is clear to you all this code
[04:15] I'm going to push into the GitHub repo for your reference.
[04:17] If you have any questions, feel free to refer the same and develop these kind of programs inside your
[04:23] local system as well.
[04:24] With that, you're going to get enough practice.
[04:26] You will face enough errors if you try to solve them
[04:29] you will learn new things.
[04:30] I hope you are clear about the BiFunction interfaces purpose.
[04:34] Whenever you are dealing with the two input parameters of any data type, feel free to use any of the
[04:41] BiFunctional interfaces based upon your business scenario.
[04:44] With that you may have a question which is do we have TriFunctions which are capable of accepting three
[04:51] different input parameters?
[04:52] The answer is no.
[04:54] So if you start implementing three, four, five the Java team will end up creating and
[04:59] maintaining lot of functional interfaces.
[05:01] That's why they stop these functional interfaces at the binary function interfaces itself.
[05:07] In fact, in the real projects, most of the times you will develop methods which are going to accept
[05:12] a single parameter or a two parameters at max.
[05:15] If you have a special scenario where you're going to accept more than two input parameter, then you
[05:20] can happily define your own Functional interface.
[05:24] I hope this makes sense to you.
[05:25] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
