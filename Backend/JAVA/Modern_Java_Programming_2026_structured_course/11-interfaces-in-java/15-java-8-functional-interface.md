# 11.15 — [JAVA 8] Functional Interface

> Section 11: Interfaces in Java

[00:00] Inside this lecture, let's try to discuss about one more special type of interface which is Functional
[00:07] Interface.
[00:07] Inside your real projects are inside Java programming, you are going to use a lot of Functional Interfaces.
[00:16] That's why understanding about these interface and the purpose of it is very important.
[00:21] So what is a Functional Interface?
[00:23] Any interface with only one abstract method is commonly referred as Functional Interface.
[00:31] You can also recall this concept using the acronym or short form which is SAM.
[00:37] Sam means Single Abstract Method.
[00:40] So whenever an interface has an SAM, we can call such interface as Functional Interface.
[00:47] Apart from having a single abstract method inside and Functional interface, we can have any number
[00:53] of static methods and default methods.
[00:56] There are no restrictions around static methods and default methods, because default and static methods,
[01:02] they are not going to play any role in determining if an interface is a Functional interface or not.
[01:08] The concept of Functional interface is introduced only from the Java 8 before Java 8,
[01:15] there is no concept of Functional interface, so inside the Java library there are some interfaces with
[01:21] the single abstract method, but still we never used to call them as Functional interface, because
[01:26] the concept of Functional interface came into picture from Java 8 only.
[01:31] Why it is introduced in Java 8.
[01:33] In Java 8 Java team, they released some major features inside Java library around the functional
[01:40] programming, Lambda expressions and method
[01:43] references.
[01:44] So from Java 8
[01:45] Java also supports functional style of programming.
[01:49] As of now, whatever we are learning, it is of imperative style of programming.
[01:55] As part of imperative style of programming, we are going to give clear and detailed instructions to
[02:01] the compiler by writing a very lengthy and detailed code.
[02:05] Whereas with the functional style of programming, we are going to write the code just like talking
[02:11] to a person or just like giving an instructions to the compiler.
[02:15] So based upon our instructions, the Java code is going to be executed behind the scenes.
[02:20] So these functional style of programming, which is supported with the help of lambda expressions and
[02:26] Functional interface, we are going to learn in the coming sections.
[02:30] But since right now we are talking about interfaces, inside this section, I want to highlight about
[02:35] these Functional interfaces. To support building Functional interfaces inside Java, there is a new annotation
[02:43] introduced as part of Java 8.
[02:45] The annotation is at symbol followed by Functional interface.
[02:49] So whenever you are mentioning these annotation on top of an interface, then your compiler will make
[02:55] sure your interface has only one abstract method.
[02:59] In case if someone is trying to add one more abstract method in future, then it is going to throw an
[03:05] compilation error.
[03:06] Though using this annotation is not mandatory.
[03:09] It is strongly recommended to use this interface whenever you have an intention to develop a Functional
[03:15] interface, and using the same to write the lambda expressions.
[03:19] When Java team released the Java 8 to enable the functional programming using lambda expressions
[03:26] and Functional interfaces, they provided lot of functional interfaces inside that Java library itself.
[03:33] For example, there is a package inside Java library which is java.util.function.
[03:40] Inside this package we have many Functional interfaces and few important functional interfaces.
[03:46] I am highlighting here like Consumer, Supplier, Predicate and Function.
[03:50] So all these Functional interfaces, they are going to have a single abstract method.
[03:55] I'm also going to show a few of these Functional interfaces from the Java library in few seconds.
[04:00] But before that let me show you the syntax that you need to follow whenever you want to create your
[04:05] own Functional interface.
[04:07] Like I said, first you need to mention @FunctionalInterface.
[04:12] So this is an annotation using which we are telling to the compiler that these interface that I'm going
[04:18] to create should accept only one abstract method.
[04:22] So please take care of the same.
[04:24] These kind of instructions we are going to give to the JVM our compiler with the help of these annotation.
[04:31] So once you have defined these annotation you can define your interface with the help of interface keyword
[04:37] followed by what is the interface name.
[04:39] And inside this interface you can define a single abstract method.
[04:44] And if needed, you can define any number of static methods and default methods.
[04:49] I hope you are clear.
[04:50] Let me show you a few examples around Functional Interface inside the Java library
[04:55] like I said, we have a Functional interface with the name Consumer and
[04:59] this is present inside that java.util.function package.
[05:04] If I can open this, you can see on top of this you're able to see an annotation which is
[05:11] FunctionalInterface and post that we have the interface definition which is public interface
[05:16] and what is the interface name.
[05:18] After the interface name we have this new syntax.
[05:21] So this syntax we call it as generics.
[05:24] We're going to talk about generics in the coming sections.
[05:27] For now don't worry about these Generics inside these interface
[05:30] if you can closely observe there are two methods.
[05:33] One is default method.
[05:34] Like I said, we can write any number of default methods and static methods.
[05:38] But coming to the abstract method, there is only one abstract method with the name accept.
[05:43] Very
[05:43] similarly, I can also open Supplier functional interface.
[05:47] So this also has a single abstract method which is get followed by I'm going to open one more function
[05:54] interface which is Predicate.
[05:55] So this also has a single abstract method followed by few default methods.
[06:01] So I have so many default and static methods inside this Predicate.
[06:05] But we have only a single abstract method like you can see here.
[06:10] Now let me show you how to create our own Functional Interface.
[06:14] For the same, I'm going to create a new interface with the name MyFunctionalInterface.
[06:21] On top of this interface I want to mention an annotation which is @FunctionalInterface.
[06:27] So as soon as I mention this annotation, you can see I'm getting a compilation error saying that no
[06:33] target method found.
[06:34] That means I don't have any abstract method defined.
[06:37] So to define an abstract method I can simply type void myMethod().
[06:43] So these are abstract method name followed by semicolon.
[06:46] With that you can see the compilation issue is resolved.
[06:50] If I try to create one more abstract method with a different method name like void myMethod1(), you're
[06:56] going to see, I'm going to get a compilation error again, multiple non overriding abstract methods
[07:03] found in interface.
[07:04] So that's why always make sure there is only a single abstract method inside your Functional interface.
[07:10] For now, please make sure you are understanding what is an Functional Interface and how to define it.
[07:15] In the coming sections,
[07:16] when we are talking about Lambda expressions and functional programming, we are going to talk in detail
[07:22] about how to use these Functional interfaces to build a lambda expressions inside our Java code.
[07:28] I hope you are clear.
[07:29] Thank you
[07:30] bye.

----------------------------------------
