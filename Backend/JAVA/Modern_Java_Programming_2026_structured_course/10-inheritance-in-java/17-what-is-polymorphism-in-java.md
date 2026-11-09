# 10.17 — What is Polymorphism in Java

> Section 10: Inheritance in Java

[00:00] As of now, we have a very clear understanding about two pillars of the object oriented programming.
[00:06] One is Encapsulation and the second one is Inheritance.
[00:11] From now onwards, for the next few lectures we are going to put focus on the Polymorphism.
[00:16] So what is a Polymorphism and how it can be achieved inside Java?
[00:21] In Java, Polymorphism refers to the ability to perform a single action in a multiple ways.
[00:28] The term Polymorphism is derived from the Greek words poly and morphs.
[00:33] What is poly?
[00:34] Poly means many in Greek language, and similarly morph means forms, hence Polymorphism
[00:40] in other words, we can call it as many forms.
[00:44] Before I try to explain about Polymorphism in Java, first let me give a real life example related to
[00:51] Polymorphism.
[00:52] On a day to day basis, we see a woman plays multiple roles, like the same woman can be a mother to
[00:59] a child, or she can be a friend,
[01:02] she can be a sister, she can be a wife, she can be an employee.
[01:06] So if you see based upon different, different scenarios, the same person is playing multiple roles.
[01:13] So we all place different, different roles based upon the relationship that we maintain with others.
[01:19] So the same person having different behavior in different situations.
[01:24] Similarly in Java also the same method are a same piece of logic, can be executed in different forms
[01:31] based upon different kinds of situations, and the input. Polymorphism is considered one of the core
[01:38] features of object oriented programming.
[01:41] Since Java is also an object oriented programming, Java also follows Polymorphism to a great extent.
[01:48] So how to achieve Polymorphism?
[01:50] First, you need to make sure you are implementing Inheritance inside your classes.
[01:55] Post that the Polymorphism can be achieved in two different forms.
[02:00] So based upon the type of binding, there are two types of Polymorphism in Java.
[02:05] The very first one is compile time or Static Polymorphism, whereas the second one is runtime or Dynamic
[02:12] Polymorphism.
[02:13] So based upon how the binding is happening, whether it is a Static Binding or Dynamic Binding.
[02:19] So accordingly the type of Polymorphism is going to be followed by the Java.
[02:24] So inside Java, whenever we are performing the method overriding we are going to implement dynamic
[02:32] Polymorphism.
[02:33] Whereas with the help of method overloading the Static Polymorphism is going to be followed.
[02:39] So what is a method overriding.
[02:41] What is a method overloading?
[02:43] We're going to talk in detail about them.
[02:45] But before I try to close this lecture, I want to show you a piece of code that is following the Polymorphism.
[02:52] Here inside my AnimalUtility class, we have written a print name static method.
[02:58] So this method is going to behave differently based upon the type of the object that we pass as an input.
[03:06] If I receive the object of Animal superclass, then it is going to invoke the eat method available inside
[03:13] the Animal superclass.
[03:15] Otherwise, if I am receiving that Dog object or cat object, the corresponding Cat methods are going
[03:22] to be invoked.
[03:23] So this is one of the classic example of Polymorphism.
[03:26] The Polymorphism is possible only when we follow inheritance.
[03:30] When we are following inheritance, we will have an option of method overriding and method overloading.
[03:36] So based upon whether we are following the method overriding or method overloading accordingly, Java
[03:43] is going to follow Dynamic Polymorphism or Static Polymorphism.
[03:48] I hope you are clear with the definition of Polymorphism inside the meme
[03:52] also, right now it is going to make sense to you.
[03:54] You can see the same spider man is performing different, different actions, or he's behaving differently
[04:01] based upon different, different situation or different kind of inputs.
[04:05] From the next lecture, let's focus on what is method overriding inside inheritance and how we can achieve
[04:13] Dynamic Polymorphism with the help of method overriding.
[04:17] Thank you,
[04:18] bye.

----------------------------------------
