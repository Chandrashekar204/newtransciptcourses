# 24.4 — What are lambda expressions and their syntax

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] In the previous lecture, when we were discussing about the functional style of programming, I showed
[00:04] you this example on how to filter the even numbers from a list, post filtering the even numbers, how
[00:12] to calculate the square of the even number, and how to sum it with just a single line of code.
[00:17] We are able to implement this solution.
[00:19] In the same process, we invoke the existing methods available inside the Java library like filter(), sum(),
[00:26] mapToInt(), stream().
[00:28] We are going to discuss about these methods in the coming lectures.
[00:31] For now, let's focus on lambda expression that we are trying to pass to this method, to this filter()
[00:38] method, or to this mapToInt() method
[00:40] we are trying to pass the lambda expression.
[00:43] Using this lambda expression, we are trying to convey our business logic on how to perform the filtering,
[00:50] or on how to map the each of the even numbers to its square value.
[00:55] So that's why whenever you are trying to implement a functional style of programming inside your Java
[01:01] program, the very first basic requirement is you should know how to express your business logic using
[01:08] the lambda expression.
[01:10] Inside this lecture, let's try to understand what is a lambda expression.
[01:14] Lambda expressions
[01:15] like we discussed, it is introduced from Java 8 as part of the functional programming introduction.
[01:22] If you ask me, what is the definition of a lambda expression?
[01:25] I would say lambda expression is like a compact representation of an anonymous function that can be
[01:33] easily passed around.
[01:35] So whenever I'm trying to refer to a jargon called function, please consider it as a Java method.
[01:40] Unlike our regular named methods that we are going to write inside the Java class, these lambda expressions
[01:47] they are not going to have any explicit name which make them simple to write.
[01:52] And these lambda expressions, they also share common characteristics with a normal Java methods such
[01:57] as they are going to accept input parameters, they are going to have a body, they are going to have
[02:02] a return type, and they also support handling and throwing the list of exceptions.
[02:07] With this definition, you may feel overwhelmed and you may feel it is a very big definition.
[02:11] Let's try to break it down and try to understand in small pieces.
[02:16] The very first important information about lambda expression is it is going to be a Anonymous function.
[02:21] So whenever we are trying to write a lambda code with our business logic, we can call it as a Function.
[02:27] Whereas if we are trying to define the business logic with the imperative approach, in such scenarios,
[02:33] we can call it as a Java method.
[02:35] So the functions that we are going to define with the help of lambda expressions, they are going to
[02:40] be anonymous.
[02:41] Unlike the Java methods, these lambda functions are lambda expressions
[02:45] they are not going to have any name.
[02:48] This means you are less to worry about what name you need to give.
[02:52] Giving a name to a method is such a complex process where you have to imagine what is the best name
[02:58] that you can give.
[02:59] So all these background steps that you are going to follow
[03:01] whenever you are trying to create the Java method, you you can avoid when you are dealing with the
[03:06] lambda expression because they don't have any name.
[03:08] And the second important information about the lambda expression is, Function.
[03:13] So what is a Function?
[03:14] Like I said, this is just like a normal Java method.
[03:17] But whenever we are trying to define a functional style of programming with the help of lambda expressions
[03:22] in such scenarios, instead of calling the method, we can call them as function.
[03:27] So these anonymous functions, they are capable of having a body.
[03:32] Inside this body we can write our business logic.
[03:34] They can have a return type.
[03:36] And optionally they also allow you to define the exceptions.
[03:40] However, these anonymous functions that we are going to define with the help of lambda expressions,
[03:46] they are not going to be tied to any particular class. In imperative approach
[03:51] whenever you want to define a Java method, definitely you need to write them inside a Java class or
[03:57] inside an interface, or inside an abstract class.
[04:00] But coming to these Lambda functions, they don't have to be tied to any particular class.
[04:06] We can simply assign these lambda expressions, or the business logic that we have written with the
[04:10] help of lambda functions to a variable.
[04:13] When we are going to discuss about lambda expressions in the coming lectures in detail, then this statement
[04:18] is going to make more sense to you.
[04:20] But now let's move on to the next important point, which is Passed Around a lambda expression
[04:26] once it is defined, it can be conveniently passed as an argument to a method or stored in a variable,
[04:33] which means when you define a piece of logic with the help of lambda expression, you can send that
[04:38] business logic, which is in the form of lambda expression, as an input to the some other methods.
[04:44] So just like how you are throwing data with the help of input parameters and input objects to the methods,
[04:51] very similarly, with the help of lambda functions, you can throw the behavior as an input to the other
[04:58] methods in the coming lectures.
[04:59] I'm going to show you how to pass the lambda expression as an input to other methods.
[05:04] With that, you're going to throw the business logic that you have written as an input to other methods
[05:09] and the receiving methods
[05:10] they can use your business logic as per their requirements.
[05:14] And at last, whenever we are defining the lambda functions or lambda expressions, we don't have to
[05:19] write extensive low level boilerplate code.
[05:22] Instead, we are going to provide high level instructions, which is going to make your code compact
[05:28] and concise.
[05:29] I hope you are clear with these
[05:30] lambda expression definition.
[05:32] If something is not clear, don't worry.
[05:33] When we start exploring the examples of lambda expressions, you're going to become the master of these
[05:39] functional programming.
[05:41] Believe me, I'm there for you.
[05:42] Just bear with me a couple of more lectures where I'm going to focus a lot about theory.
[05:46] Later on we can discuss more examples.
[05:49] Now, coming to the interesting part, which is what is the syntax that we need to follow while we are
[05:55] trying to define a lambda expression or a lambda function like you can see here, there are two types
[06:01] of syntaxes.
[06:02] The very first syntax you can follow if your business logic has only one Java expression.
[06:09] In this kind of scenarios, first you need to mention the parentheses, and inside these parentheses
[06:15] you can accept parameters that your lambda function is going to accept.
[06:19] If your lambda function is not going to accept any input parameters, then you can have empty parentheses.
[06:26] After these parameter-list parentheses, you need to mention the symbol which is hyphen followed by
[06:32] greater than symbol.
[06:34] So inside Java, in future, whenever you see the symbol inside any code, you can safely assume that
[06:41] it has an lambda expression.
[06:43] So after this symbol, you can define your single Java expression followed by semicolon.
[06:49] So this is one basic style of writing lambda expression.
[06:52] Whereas coming to the scenario where your lambda expression may have more than one Java statement as
[06:58] a business logic, in such scenarios, you need to mention all your Java statements inside the curly
[07:03] braces, so you can assume all the code that you are going to write inside these curly braces.
[07:08] It is the body of your lambda expression.
[07:11] Whereas if you have only a single Java expression, then there is no need of mentioning these curly
[07:17] braces.
[07:17] They are going to be optional.
[07:19] I hope you are clear with these lambda expression syntax.
[07:21] In the next lecture, I'll show you a few examples on how to build the lambda expressions by taking
[07:28] normal methods as an reference.
[07:30] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
