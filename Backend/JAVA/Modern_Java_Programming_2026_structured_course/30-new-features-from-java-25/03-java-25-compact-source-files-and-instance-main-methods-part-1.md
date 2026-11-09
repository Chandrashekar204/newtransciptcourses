# 30.3 — [JAVA 25] Compact Source Files and Instance Main Methods - Part 1

> Section 30: New features from Java 25

[00:00] Compact to source files and instance main methods.
[00:04] This is another feature introduced as part of Java 25 release.
[00:08] With the help of these new features, the Java team, they're trying to make the Java language more
[00:13] beginner friendly anytime.
[00:15] If you want to teach a new beginner on how to get started with a Hello World program inside Java, all
[00:22] these days we are writing these kind of programs.
[00:25] First, we are going to create a class followed by a main method by mentioning public static void and
[00:32] this main method, it is going to accept the input by using an array of string with the parameter name
[00:38] args, and inside the main method we are going to write system dot out dot println to print hello world!
[00:45] So for experienced developers this may look very simple, but for beginners it may be very complex for
[00:51] them to understand around the purpose of class.
[00:55] What is this public static and what are the string args?
[00:58] And they may also face some problems in understanding the this syntax System.out.println.
[01:04] So to make the beginner's life easy, a new feature with the name Compact Source files and instance
[01:10] main method is introduced by using this new feature.
[01:13] Right now the beginners.
[01:14] Whenever they are getting started with the Java language, they can simply write a void main, and inside
[01:21] this main method they can use io dot println method to print the content onto the console.
[01:27] Here the beginner.
[01:28] They don't have to create any class on top of that.
[01:32] This is an instance method, which means they don't have to mention the static or public, and it is
[01:37] also not going to accept any input parameter.
[01:40] So by writing these minimal code where there will be a main method which is not going to return anything,
[01:47] and inside this main method they're simply invoking a method with the name println, which is present
[01:52] inside an IO class.
[01:53] And to this method, they just have to pass the content that they want to display on the console.
[01:58] This is a very compact to code, and inside this compact code we have an instance main method.
[02:05] So that's why they have given this name to this new feature, this new feature.
[02:10] It is also going to help the experienced developers as well, because they can quickly prototype their
[02:16] ideas with less boilerplate code.
[02:19] This compact code can grow and evolve as developers started gaining skills and applications are getting
[02:26] expanded with this new feature.
[02:28] I'm assuming the beginners.
[02:29] They are going to love the Java language because we're not throwing at them too many jargons.
[02:34] Explaining this code is very simple compared to this code.
[02:38] So by using this compact code, they can start learning all the basics like variables, declaration,
[02:44] creating the methods, learning the operators like arithmetic operators so all the basics of the language.
[02:50] They can start learning by using this compact code.
[02:53] When they are comfortable with the basics of Java, then the tutor or the experienced programmer, they
[02:59] can slowly introduce them to the class concept.
[03:02] What is a static?
[03:04] What is this public and why we should send some input to the methods.
[03:08] So all these advanced concepts can come later.
[03:10] All these days, the experienced programmers, they are telling to the junior developers while explaining
[03:14] these hello world program, they just say, for now, let's forget about the static public string args.
[03:21] We'll always start with this statement and we'll simply ask them to focus on these System.out.println
[03:28] statement.
[03:29] But this also is a complicated statement.
[03:32] Instead, if we start the explanation by using these compact source code, it is going to make the beginners
[03:37] life very easy.
[03:38] Let's see the demo of this new feature very quickly.
[03:42] I'm going to create a new sub package with the name com dot dot Java 25 dot compact.
[03:51] Inside this package I'll try to create a new Java class.
[03:56] Let me right click on this package and select this new and Java class.
[04:01] If you are using the latest version of IntelliJ inside this pop up, you're going to have an option
[04:07] of compact source file, you can select the same and you can give the file name as Hello World.
[04:15] As soon as I press enter, if you see the compact source file, it is going to be created under the
[04:22] default package, which is directly under the src.
[04:26] So I have selected the compact to package, but it is not getting created there.
[04:30] This is done intentionally.
[04:31] So the always the compact source file.
[04:34] It is going to be created in the default package.
[04:36] So if you see for this class the file name is helloworld.java.
[04:41] But there is no classes created inside this class by the IDE.
[04:45] I can try to create this main method manually by typing main inside IntelliJ.
[04:51] If you type the shortcut and press enter, you're going to have a instance main method inside this method.
[04:58] Let me try to print the content by using println method present in the Ivo.
[05:04] So Ivo is a new class introduced as part of this new feature under the package Java dot lang.
[05:10] Since Java dot lang package is by default imported the beginner, they don't have to worry about the
[05:16] import statement of this class as well.
[05:18] They can simply look for a class with the name Ivo, dot and println to this println method.
[05:24] They can pass any content like Hello World with this compact code.
[05:29] Right now, if I try to execute this program, I'm going to get the expected output with the statement
[05:37] hello world!
[05:38] Are you seeing the power of this new feature?
[05:40] It is very easy for beginners to get started with this compact source code and instance method, and
[05:47] in fact it is going to help the experienced developers as well.
[05:50] They don't have to create a class, they don't have to create a public static void main method.
[05:56] They can simply type void main and they can start typing their business logic for quick prototypes.
[06:02] I hope you got some good introduction about this new feature.
[06:05] I want to explain more details about this new feature.
[06:08] Let's try to understand the same in the next lecture.

----------------------------------------
