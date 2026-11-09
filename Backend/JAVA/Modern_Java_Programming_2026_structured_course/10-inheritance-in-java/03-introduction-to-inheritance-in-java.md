# 10.3 — Introduction to Inheritance in Java

> Section 10: Inheritance in Java

[00:00] Let's try to understand what is an Inheritance.
[00:03] Before I try to explain you about Inheritance in Java first
[00:08] for a second, let's imagine we are all non-technical people.
[00:12] And with that assumption, let's try to answer what is an Inheritance according to a common man or a
[00:19] non-technical person. The meaning of Inheritance in a non-technical world means passing down of the
[00:26] attributes or the wealth from parents to the children.
[00:30] Like each one of us, we get our genes and DNA from our parents and similarly, children
[00:37] they will also inherit the wealth of parents if they allow.
[00:42] So this is the meaning of the Inheritance
[00:44] in a non-technical world. The same kind of definition or concept applicable inside Java as well.
[00:51] So let's try to understand what is an inheritance in Java,
[00:54] why should we care about Inheritance inside Java?
[00:58] Think like you have multiple classes and in all these multiple classes you have multiple methods and
[01:04] fields.
[01:05] Sometimes you may have a requirement to maintain a same business logic, or a same method or a same
[01:11] field across multiple classes.
[01:14] So in this kind of scenarios, what you are going to do, you are going to copy the same method or same
[01:20] code from one class to other classes where you want to maintain the same code.
[01:25] But do you think this approach is the best approach ?
[01:27] Off course not, because in future, whenever you want to make a small change or a new change inside
[01:34] this common code, then you need to change the code or the business logic in all the classes where you
[01:41] have copied the same code.
[01:42] For example, let's imagine you have three different Java classes, and inside these three different
[01:47] Java classes, you have a requirement to write a same Java method or to maintain the same Java fields.
[01:54] As a developer,
[01:55] first you are going to define the logic or the fields or the methods in one of the class and the same
[02:01] set of code you are going to copy into the two other Java classes.
[02:05] But the problem comes when you have a requirement in future to make some changes inside this common
[02:11] code.
[02:12] In such scenarios, you have to make changes in all the three places, which can be a challenging task.
[02:18] So to handle these kind of scenarios, we have an Inheritance concept inside Java or in any object oriented
[02:26] programming languages.
[02:27] So instead of you copying the same code to the different places, you can create a class with the common
[02:33] code that you want to maintain and the other classes where they want to maintain the same code
[02:39] they can inherit that code from the parent class or the class where you are maintaining all the common
[02:46] code.
[02:46] This way, all your common logic is going to be present always in the parent class, and all the child
[02:53] classes who are inheriting the parent class
[02:56] they should be able to access the methods and fields with the help of Inheritance
[03:01] concept.
[03:02] We have some jargons or terminologies that we need to aware whenever we want to implement the Inheritance
[03:08] in Java. These jargons are like superclass subclass
[03:13] so there are some good amount of jargons.
[03:15] So let's try to understand what are those.
[03:17] So the class where you are going to maintain all your common logic, whether it can be methods or fields,
[03:23] we can call that as a superclass or a base class or parent class, and all the remaining classes which
[03:30] are going to inherit from the superclass or parent class or base class, we can call such classes as
[03:37] subclass or derived class or child class.
[03:40] So this is the definition of Java Inheritance and the purpose of Inheritance in Java.
[03:47] I know you may have some questions around the Java Inheritance.
[03:50] In the next lecture, let's try to take a scenario to understand about Inheritance in a more clear manner.
[03:58] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
