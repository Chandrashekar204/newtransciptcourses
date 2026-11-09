# 24.8 — How Functional Interface & Lambda expressions are linked - Part 2

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] As of now, we are trying to create the lambda expression and assign the same to the variable of data
[00:06] type
[00:06] Hello.
[00:06] So this is one approach that you can follow.
[00:10] Instead of this approach we can also follow another approach which is we can directly pass the lambda
[00:16] expression as an input to these process() method.
[00:19] So here I can straight away copy these lambda expression and pass as an input to the process() method.
[00:26] This time instead of hello world I'll try to print
[00:29] Hi.
[00:29] So this is also valid.
[00:31] And this we can call it as approach too.
[00:34] So if I try to execute this method this time you'll be able to see three different type of outputs like
[00:39] Hello, Hello World and Hi.
[00:41] This way we can always pass the business logic behaviour around the methods based upon our requirements.
[00:48] So in some other scenario, if you want to pass a different business logic instead of hi, if we want
[00:53] to send something else, we can happily do that without the need of creating another subclass or overriding
[00:59] the method, or without creating any object of my subclass.
[01:03] If you still have some questions, don't worry, I'm going to show you one more example here.
[01:07] This time I'll try to create one more Functional interface with the name ArithmeticOperation.
[01:15] So this is the interface name I want to give.
[01:18] On top of this interface I'm going to mention the @FunctionalInterface annotation.
[01:22] And as soon as I mention these annotation I'm getting a compilation error because I have defined the
[01:27] interface as FunctionalInterface, but I didn't define the single abstract method.
[01:32] To resolve this compilation error, I'm going to create an abstract method with the name int peration.
[01:38] So there is a method.
[01:39] So the method name is going to be operation() and its return data type is going to be int.
[01:44] And this abstract method it is going to accept two input parameters with the name num1 and num2 of data
[01:51] type int.
[01:52] So this is my Functional interface.
[01:53] Using this Function interface I want to build the lambda expression.
[01:57] So let's try to see how to perform the same.
[01:59] To create the lambda expression based upon this ArithmeticOperation, Functional interface
[02:04] first let me create a variable of type ArithmeticOperation with the variable name
[02:09] as addition. To this variable I'm going to assign a lambda expression.
[02:14] So first we need to mention the parentheses.
[02:16] And inside the parentheses I need to mention two input parameters with the name a, b.
[02:22] So these a, b is going to be referred as into variables based upon my abstract method definition
[02:29] Post that we need to mention the lambda expression symbol followed by parentheses.
[02:35] Inside this parentheses, I can try to mention the logic which is int result = a + b,
[02:43] and the result I'm going to return from this lambda expression.
[02:47] You can see this time I'm not getting any compilation error.
[02:50] But like I said before, whenever we have a single Java statement inside our business logic, then we
[02:56] can get rid of all these curly braces and the return statement.
[02:59] That's why what I can do here is I can remove this entire logic and straight away mention a + b.
[03:06] So the outcome from these a + b operation is going to be return.
[03:10] And since it is matching with the return type here which is int I'm not getting any compilation error.
[03:16] So this is one lambda expression.
[03:19] Using this lambda expression I can invoke the operation() method.
[03:24] And to this operation() method I'm going to pass the variables like 5, 5.
[03:29] So the output from these operation I'm going to print out onto the console.
[03:33] That's why I'm trying to use this System.out.println().
[03:36] So if I execute this program this time you will be able to see inside the output we have an operation
[03:42] 10.
[03:42] So as of now you can see we are trying to perform the addition.
[03:45] So let's try to repeat the same kind of steps for similar other kind of operations.
[03:51] Like I'll try to perform the subtraction.
[03:54] That's why I'm going to mention this variable name as subtraction.
[03:58] And using the subtraction variable I'm going to invoke the operation() method to this
[04:03] also I'm going to mention five and five as an input.
[04:06] With that you know the output we are going to get is five.
[04:09] Later on, I'll just try to mention the operation name as product.
[04:13] And this time I'm going to perform the multiplication.
[04:17] And using this product I'm going to invoke the operation() method.
[04:20] And at last I'm going to perform the division operation.
[04:24] So to perform the division operation I'm going to use the operator which is /.
[04:28] And using this division operator I'm going to invoke the operation() method.
[04:32] If you closely observe all these variables, they have the business logic that needs to be executed.
[04:38] Whenever a abstract method is going to be invoked.
[04:41] Nowhere we are creating a subclass,
[04:43] nowhere we are creating an object of the class.
[04:45] With the lambda expression
[04:46] we are able to achieve all this magic with the very few lines of code.
[04:50] So if I execute this program, you'll be able to see 10, 25, 1 as the output.
[04:56] So this is working like we expect.
[04:58] I hope you are seeing the power
[04:59] of lambda expression here.
[05:01] As of now, we just saw that tip of the iceberg.
[05:04] There is more about the lambda expressions when you start using these lambda expressions inside the
[05:09] collections
[05:10] by leveraging the streams API, you are going to be mad by looking at the power of these lambda expression,
[05:16] providing to the developers. Everything that we have discussed around the relationship between the Functional
[05:21] interface and lambda expression
[05:22] I have highlighted in these two slides, along with the examples that we have discussed.
[05:28] Please refer the same for more details.
[05:30] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
