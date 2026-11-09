# 9.3 — Introduction to packages & benefits of them

> Section 9: packages in Java

[00:00] What is a package in Java?
[00:03] With the help of packages, we can organize the Java code like Classes, Interfaces, Enums and Annotations
[00:12] into namespaces.
[00:14] In other words, a package is a collection of related Classes, Interfaces, Annotations, and Enums
[00:21] grouped together in a single unit.
[00:24] Why should we group our Java code with the help of packages?
[00:29] Because we do have certain advantages when we use packages inside Java projects.
[00:36] So let's try to understand what are those advantages.
[00:38] The very first advantage is with the help of packages, we can organize large code bases into logical
[00:46] units, making it easier to manage and maintain code.
[00:51] In the previous lecture, I showed you some videos where the fruits and plants they are organized into
[00:57] logical units or logical groups.
[01:00] Very similarly, inside real projects.
[01:02] We have thousands of Java classes.
[01:04] Since we are going to have lots and lots of classes inside real projects, it is always advisable to
[01:10] organize them into logical units.
[01:13] For example, think like you are working in an application related to a bank inside this bank
[01:19] related projects.
[01:20] You may build a business logic to handle functionality related to saving account, current account,
[01:26] credit card, debit card,
[01:28] home loan, personal loan, vehicle loan.
[01:30] So there are lot many functionalities that you are going to build inside your Java project.
[01:35] So when you are creating a Java class or an interface, Annotation or Enum, it is always advisable
[01:42] to create them in the package associated to their business logic.
[01:47] Maybe you're trying to build a business logic inside a Java class which is related to a credit card.
[01:52] So all credit card related business functionality.
[01:56] You should try to group together in a separate package so that it is going to make your life easy in
[02:02] future,
[02:02] whenever you want to manage and maintain your code, the next advantage that we have is Encapsulation.
[02:10] Packages provide a way to encapsulate the classes and interfaces.
[02:15] When I say encapsulate with the help of packages, we can hide the business logic or implementation
[02:21] details from other packages or from other parts of the Java application.
[02:26] So encapsulation is a mechanism to hide the business logic from other packages or from other modules
[02:33] or other Java projects.
[02:35] The same we are going to achieve with the help of packages.
[02:38] Apart from Encapsulation,
[02:40] with the help of packages, we can also control the access to our Classes, Interfaces, fields, methods
[02:47] by using access modifiers like public, private, protected and default.
[02:52] As of now, we are only using the public access modifier inside our methods for our fields and classes.
[03:00] But when we start using the packages and organizing the code with the help of packages in Java, we
[03:06] can use the other access modifiers like private, protected and default using which we can control who
[03:14] can access our Java methods, Java classes, Java fields.
[03:17] So these kind of access control we can do with the help of packages.
[03:22] So once we discuss everything about the packages inside this section, we're going to talk in detail
[03:27] about all the access modifiers and how to control the access inside Java.
[03:32] And the last advantage that we have when we use packages is packages provide a way to avoid naming conflicts
[03:40] between the Classes and Interfaces by giving them unique names within a package.
[03:46] Like I said before, there is a good chance that two developers they may create a Java class with the
[03:52] same name like Person, User, Document.
[03:55] So these are very commonly used names and multiple developers
[03:59] they may end up using the same Java class name.
[04:02] To avoid these kind of name conflicts we can leverage packages.
[04:06] The developer one he can create his own package, whereas developer two also he can create his own package.
[04:13] Inside these two different packages, they can have a Java class with the same name.
[04:18] Since they are present in different packages.
[04:21] The Java compiler is not going to complain anything about it.
[04:24] So we're talking a lot about packages, but you may have a question here
[04:29] as of now, throughout the course we have created so many classes inside Java projects and nowhere we
[04:35] have created a package.
[04:37] Does that mean we can build a Java projects without packages?
[04:40] Off course we can build a Java projects without packages.
[04:44] Technically it is possible.
[04:46] So whenever you try to create Java classes without any package, all your Java Classes or Interfaces
[04:53] or any other data types, they will end up in an unnamed or default package that
[04:59] is going to be maintained by the JVM behind the scenes, but generally speaking, an unnamed or default
[05:06] package is only for small or temporary applications, or when you are just starting the development
[05:12] process.
[05:12] Otherwise, when you are trying to build a real or bigger Java applications, always we need to keep
[05:18] our Classes, Interfaces, Annotations and Enums inside the named packages.
[05:24] I hope you are clear with these basic details of packages.
[05:27] Let me show you some live example of these packages and how they are being used inside the JDK library.
[05:35] To see the demo of Java packages, you can open any of the Java projects that we have built so far inside
[05:42] IntelliJ.
[05:43] As of now, you can see I have opened the section8 Java project that we have built in the previous
[05:49] section, inside the same window of IntelliJ, you should be able to see an option external libraries.
[05:56] Please click on this arrow button here and add this external libraries,
[06:00] you will be able to see what is the JDK that you are using.
[06:04] As of now, I'm using the JDK from Amazon Corretto, and the version of JDK that I am trying to use here
[06:10] is JDK 21.
[06:11] That's why I'm able to see the folder name as Corretto - 21.
[06:16] As part of JDK, we have thousands and thousands of Java Classes, Interfaces built which developers can
[06:24] use on their day to day development activities.
[06:27] One such class is String.
[06:29] We are using String class to a great extent throughout this course, since JDK also have thousands and
[06:36] thousands of Java classes and other data types.
[06:39] The JDK team or the Java team
[06:41] they have grouped or segregated or organized the entire code into multiple modules, and inside the
[06:49] modules we are going to have multiple packages.
[06:52] Here you can see all these are the Java modules.
[06:55] There is a module with the name java.base
[06:58] very similarly java.compiler.
[07:00] This way there are many modules.
[07:02] If you open any of the module like java.base, you should be able to see many packages.
[07:08] For example, there is a package with the name java.lang, and inside this package only we have
[07:17] a class with the name String.
[07:19] Apart from String, there are many other Java classes like you can see here.
[07:23] So inside these package let me look for the String class.
[07:27] So if I can scroll down, scroll down, scroll down,
[07:30] here there is a class with the name String.
[07:33] Very similarly
[07:33] we also have other kind of classes like StringBuffer, StringBuilder which we discussed in the previous
[07:39] section.
[07:40] Let me open String class and you should be able to see all the source code of the String class.
[07:46] Here you can see the very first Java statement inside the String.java is package java.lang.
[07:54] So this is the statement that you need to define inside your own Java classes as well.
[08:01] Whenever you want to assign your Java class to a particular package.
[08:06] Since String class is going to present inside a package java.lang, the same needs to be defined
[08:14] here as a very first Java statement inside your Java class.
[08:18] So what is the statement?
[08:20] First, we need to mention the package keyword followed by space, followed by java.lang.
[08:27] And after that semicolon.
[08:29] So the lang
[08:30] here is a short notation for the language.
[08:33] So this is how you should also define your own packages inside your Java classes.
[08:38] If you try to open any other classes outside of java.lang package, you will be able to see similar
[08:45] kind of syntax.
[08:46] For example, I can open java.math and inside this math I have a class with the name BigDecimal.
[08:54] If I open this BigDecimal, you can see the very first Java statement I'm going to have is package
[09:01] java.math.
[09:02] With this, I'm assuming it is pretty clear for you that Java team
[09:06] also, officially they have grouped their source code into modules and inside the modules they also
[09:13] have multiple packages, the same set of standards we need to follow inside our real projects as well.
[09:19] First, inside this section let's focus on the packages because modules are optional inside Java projects.
[09:25] Once we clear about all the basics of Java, we are going to talk about modules as well
[09:31] towards the end of this course.
[09:33] I hope you are clear about the purpose of packages with this quick demo.
[09:37] In the next lecture, let's try to create our own packages and inside these packages we can create our
[09:44] own Java classes.
[09:45] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
