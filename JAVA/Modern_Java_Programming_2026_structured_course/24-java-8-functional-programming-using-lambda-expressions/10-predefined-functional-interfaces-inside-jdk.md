# 24.10 — Predefined Functional interfaces inside JDK

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] With the initial introduction and demos that I have provided around the lambda expression.
[00:05] You may have a feeling, which is I like them to some extent, but still I'm not convinced to use them
[00:12] in the place of traditional imperative style.
[00:15] I'm with you here because your head to see the power of lambda expressions.
[00:19] When we start discussing more and more concepts around the Functional programming, you're going to
[00:23] realize the benefits of Lambda programming.
[00:26] But right now you may have $1 million question, which is, hey man, I like the lambda expressions.
[00:32] I'm planning to use them as well.
[00:34] But I see a drawback here with the lambda expressions, which is every time I want to create a lambda
[00:40] expression, first I need to create a Functional interface.
[00:44] Without creating the Functional interface, I'm not able to write the lambda expression.
[00:48] Don't you think this is a disadvantage for lambda expression?
[00:51] This can be your question.
[00:53] Let me clarify your question, my friend
[00:55] we are talking about the most commonly used programming language in the IT industry, which is Java.
[01:02] Do you think Java is going to have such a huge drawback?
[01:05] Off course not,
[01:06] let's try to understand how Java libraries are going to help us in writing the lambda expressions without
[01:13] creating our own Functional interfaces.
[01:16] When Java team planned to introduce the Lambda style of programming inside Java 8 to make the developer
[01:22] life easy, they have created good amount of Functional interfaces that we can use on our day to day
[01:30] basis
[01:31] to write the lambda expressions.
[01:32] All such Functional interfaces they arranged inside a package with the name java.util.function.
[01:39] You can see here I have highlighted most commonly used Functional interfaces.
[01:44] The name of this function interfaces are like Predicate, Function, Consumer, Supplier by Predicate,
[01:50] by function by consumer, unary operator, binary operator and primitive Functional interfaces.
[01:56] In real projects, we may have thousands of scenarios for which we may have to develop lambda expressions.
[02:03] By assuming all those thousands or millions of scenarios
[02:06] java team
[02:07] they did a very clever job by introducing the predefined function interfaces inside that Java library.
[02:13] As a Java developer, you just have to learn about these Functional interfaces and you should gain a
[02:19] knowledge under which scenarios you need to use, which function interface to write your lambda expression.
[02:24] So once you acquire this knowledge, you are good to go and write any kind of lambda expression without
[02:31] creating your own Functional interface.
[02:33] Believe me, 99% of the scenarios that you may have inside your real projects.
[02:39] They can be handled with the predefined function interfaces available inside the java.util.function
[02:45] package.
[02:46] Under some rare scenarios, you may have to define your own function interface, and defining your own
[02:52] function interface is not a complex task.
[02:55] It is such a simple task where you can create a Functional interface within seconds.
[02:59] Let's explore these package java.util.function inside IntelliJ Idea.
[03:04] So here I'll try to open one of the existing Functional interface with the name Predicate.
[03:10] I'm going to discuss in detail about this function interface in the next lecture.
[03:15] But for now you can see this is marked as a function interface with the help of this annotation.
[03:19] And it also present inside this package which is java.uti.function.
[03:23] So let me click on this project icon.
[03:26] Post that I'm going to click on this select to open the file which is going to help me opening the file
[03:33] like you can see here.
[03:34] This Predicate is a file which I have opened.
[03:37] If I can scroll up here you'll be able to see a package which is java.util.function.
[03:43] And at this we have so many functional interfaces that we can use on our day to day work.
[03:49] I'm going to discuss about most of these interfaces, so that you are going to have a good knowledge
[03:55] around them.
[03:55] And with that, you're also going to be become expert on creating the lambda expressions by using all
[04:01] these Functional interfaces.
[04:03] From the next lecture, let's try to explore all these Functional interface one by one along with that
[04:09] demo of them.
[04:10] Thank you
[04:10] and I'll catch you in the next lecture, bye.

----------------------------------------
