# 10.31 — abstract methods and classes - Part 1

> Section 10: Inheritance in Java

[00:00] As of now, we discussed about the three pillars of object oriented programming, which are Encapsulation,
[00:07] Polymorphism, and Inheritance.
[00:09] As a next step, let's try to understand what is an Abstraction and how to implement it
[00:15] inside the Java programs. Both the Polymorphism and Abstraction, they are tightly coupled with the
[00:21] Inheritance like we saw in the previous lectures,
[00:24] Polymorphism can be easily achieved with the help of Inheritance.
[00:29] Very similarly Abstraction
[00:31] also we can only implement along with the Inheritance.
[00:35] That's why whenever you are trying to implement Inheritance inside your Java project, you should also
[00:40] try to take care of implementing and balancing other pillars of object oriented programming, which
[00:47] are Polymorphism and Abstraction.
[00:49] With that, now let's try to understand what is an Abstraction.
[00:53] As of now, all the super classes that we have created, they have the methods along with the business
[00:59] logic.
[01:00] That means the super classes, they are giving an option to the subclass
[01:04] you can inherit my business logic which is present inside my methods.
[01:09] If you want, you can change that business logic by overriding the methods defined inside the superclass.
[01:15] So this is what happening right now.
[01:17] But with Abstraction, the developers, they are going to have an option to have some methods inside
[01:24] their classes without any business logic.
[01:27] That means a super class can simply define a method without any business logic, and it will be the
[01:33] responsibility of the subclass to define the actual business logic based upon the subclass requirements.
[01:41] I know this might be a super confusing.
[01:43] Let me show you an example.
[01:45] First, I'm going to create a class inside the base package.
[01:49] The class name is going to be Subject.
[01:52] So this Subject is going to act as a superclass for many other subjects.
[01:57] Inside this superclass of Subject, I can create normal methods with the business logic, or I can also
[02:04] try to create methods without any business logic.
[02:07] Let me show you how to do that.
[02:08] First I'm going to create a new method which is public int totalMarks().
[02:14] So this is the method name.
[02:16] And the logic that I want to write inside this method is return 100, because we know each and every
[02:23] subject that we are going to study, it is always going to hold the maximum 100 marks.
[02:29] As a next step, I want to create another method which is teach() method.
[02:34] For the same
[02:35] let me type public void teach() and inside this teach() method, I can write a business logic that all my
[02:43] subclasses that they can inherit.
[02:45] But do you think the teaching logic is going to be same for all the subjects ?
[02:49] off course not.
[02:50] Mathematics will have its own teaching style, Science will have its own teaching style, English will
[02:56] have its own teaching style.
[02:57] Since each of my actual subjects, they are going to have different, different teaching style.
[03:03] I don't want to define any business logic inside the superclass.
[03:07] I simply want to define a method without any business logic, and I want the subclasses of this class
[03:15] to take care of implementing the actual business logic.
[03:18] So how to define an method without any business logic?
[03:22] It is going to be super simple.
[03:23] You should not construct these kind of methods as an method without any business logic.
[03:29] These kinds of methods, we can call them as empty methods because they have a business logic which
[03:34] is empty.
[03:34] So this is not the actual correct way of creating the methods without any business logic.
[03:40] Instead, we should remove the curly braces and we should simply mention the semicolon.
[03:46] Apart from mentioning the semicolon after the method signature, you should also mention a keyword which
[03:52] is abstract inside your method signature.
[03:55] So these kind of methods, we can call them as abstract methods because they're not going to hold any
[04:01] business logic.
[04:01] They are simply going to give you the method signature that the subclasses they have to follow.
[04:07] And here you can see I'm getting a compilation error because we are trying to write an abstract method
[04:13] in a normal class, this is not allowed.
[04:16] We can only write the abstract methods inside abstract classes.
[04:20] So how to define the abstract classes?
[04:23] We need to mention the same abstract keyword just before the class keyword.
[04:29] With that you can see the compilation error is resolved.
[04:32] I hope you are clear on how to create the abstract classes and the abstract methods.
[04:37] Using the abstract keyword inside the class definition and the method definition, we can create the
[04:44] abstract class and the abstract methods.
[04:46] Once you have defined the abstract keyword inside your method definition, if you try to provide the
[04:52] business logic within the curly braces, you're going to get an error saying that abstract methods cannot
[04:58] have a body.
[04:59] That's why
[05:00] always make sure when you are defining the abstract methods, you are not mentioning any class party
[05:05] and you are simply terminating the method signature or a definition by using the semicolon.
[05:12] When we create an abstract class, you should be able to see a different icon inside your IntelliJ
[05:18] as well.
[05:19] For this class, the icon is different compared to other class.
[05:23] There is some gaps because with the help of abstract class, we are not going to provide 100% of the
[05:29] business logic or 100% of the implementation.
[05:32] So that's the beauty of abstract class.
[05:35] It is going to mandate your subclasses to take care of implementing the abstract methods by following
[05:42] the standards that you are setting inside your abstract class.
[05:46] So the normal methods that we are writing as of now throughout the course.
[05:50] So these methods, we are going to call them as concrete methods because they are going to hold the
[05:56] complete business logic.
[05:58] And similarly all the classes as of now that we are creating throughout the course, we call such classes
[06:05] as concrete classes.
[06:06] So anytime someone says a Java class, they are going to refer to a concrete class only if they want
[06:13] to highlight about an abstract class, they are going to specifically highlight you that that a given
[06:18] class is an abstract class.
[06:20] I hope you're clear on how to create an abstract class abstract method,
[06:24] with this quick introduction, you should have got a basic understanding about the Abstraction.
[06:29] But let's try to continue to discuss more details about Abstraction in the next lecture as well.
[06:36] Thank you,
[06:36] bye.

----------------------------------------
