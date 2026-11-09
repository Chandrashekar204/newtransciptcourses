# 3.7 — Introduction to Java program code structure

> Section 3: What happens behind the scenes when a Java program executes

[00:00] As of now, we are running our Java statements with the help of jshell, and these jshell behind the scenes
[00:06] is taking care of compiling and executing my Java code with the help of Java compiler and JVM.
[00:14] But jshell is not a Long-Term solution or real solution that we can use inside our real projects.
[00:21] We should learn how to write a lot of business logic with the help of Java program.
[00:26] And in the same process, we need to write all the Java code inside a file, the same file
[00:32] we need to compile it and execute it with the help of Java compiler and the JVM.
[00:37] So to demo you all this process, first I need to teach you on how to write Java code inside a file.
[00:44] For the same,
[00:45] first let's understand what is our structure that we need to follow whenever we are trying to write
[00:51] a Java program inside a file.
[00:53] Like I said before, first we need to create a Java source file, and this file should have a name and
[01:00] the extension of this file should be .java.
[01:02] Whatever name that you have given to your file, the same name you have to define as the class name.
[01:09] So we need to create a class by following the class definition.
[01:13] I'll teach you how to create a class,
[01:15] what is the definition that we need to follow in few minutes?
[01:18] Once you define a class, the very next step that you need to do is you can create any number of methods
[01:25] inside your class and inside the method
[01:29] we need to write actual business logic.
[01:31] For example, I can define two methods.
[01:34] One is to perform the sum of two numbers.
[01:37] The other one is to perform the subtraction of two numbers.
[01:40] So inside these two methods I need to write Java statements to perform these operations.
[01:46] So this is how a typical Java source file is going to look like the same Java structure we need to follow
[01:53] throughout this course whenever we are trying to develop Java program.
[01:56] Let me show you more details about this Java program code structure. Like you can see here,
[02:01] inside the very first step we need to create a class.
[02:05] And the definition of the class is going to be public class Vehicle.
[02:10] So public is a keyword that we need to define just before the class keyword.
[02:16] So this public indicates that my class can be accessed by my JVM.
[02:21] Without defining a class public
[02:24] your JVM cannot access it and it cannot execute the program inside it.
[02:29] So that's why public is mandatory.
[02:31] After public, you need to use a class.
[02:33] So these public and class these both are keywords.
[02:37] Previously we discussed there are Java keywords.
[02:40] So public has a purpose
[02:42] and a class is the keyword that we need to use whenever we are trying to create a class.
[02:47] And after the class you can give any name to your class and the case style that we need to use whenever
[02:53] we are giving a name to the Java class is Pascalcase style.
[02:57] So what is the rule that we need to follow inside Pascalcase style?
[03:01] Every word inside your name has to start with a capital letter.
[03:05] Here I have used only one word which is Vehicle.
[03:08] If I have my class name, which is a combination of multiple words, I need to make sure every word
[03:13] starts with a capital letter, and they should not be any space between the words.
[03:18] Since I have given a name as Vehicle to my class, the same name I have to use to save the file and
[03:24] the extension of the file should be .java.
[03:27] Once you have created this class, the very next question that you may have is what goes inside my class?
[03:33] Like I said before, inside class we can create variables, we can create methods.
[03:39] A lot we can do inside class.
[03:41] But for now, please note that most of the times we create methods inside classes.
[03:46] So here I have created a method.
[03:49] The method name is move() and the return type of this method is void.
[03:52] So what is the return type means,
[03:54] my method move() is not going to return anything as an output.
[03:58] That's why I have mentioned void.
[04:00] So don't worry too much about them.
[04:02] We are going to discuss in detail about methods in the coming lectures.
[04:06] So you can see
[04:07] to separate my class and methods, we need to use open braces and closing braces. For my class
[04:13] you can see there is a open brace and closing brace.
[04:15] Very similarly, inside my class I can create any number of methods.
[04:20] So for each method there should be a opening brace and closing brace.
[04:24] Once we define a method, what goes inside a method?
[04:27] Inside a method, we are going to write multiple Java statements based upon our business logic.
[04:32] And each of the Java statement is going to end with a semicolon.
[04:37] As of now, the story is going good and everyone is happy, but as a developer, we are going to build
[04:43] hundreds of Java classes.
[04:45] And inside these Java classes we may have thousands of methods.
[04:49] How my JVM knows where to start.
[04:52] You have given hundreds of Java classes thousands of Java methods.
[04:56] So my JVM is going to ask where to start.
[04:59] This is very similar to our car.
[05:01] So inside car to perform various operations like applying a brake, changing a gear, giving accelerator,
[05:08] pressing the horn, switching on the lights.
[05:11] So there are many operations inside car that you can perform.
[05:15] But in order to perform all those operations, first you need to make sure you are starting your car or
[05:22] engine.
[05:22] So just like how we have an engine start or stop button inside your vehicle, very similarly for our
[05:29] JVM
[05:29] also, we should tell what is the starting point inside our Java project.
[05:34] So to communicate the starting point for our JVM, we are going to write a main method by following
[05:40] the exact syntax recommended by the Java team.
[05:44] So what is the exact syntax?
[05:46] You can see here I need to create a method public static void main().
[05:51] The method name is main() and void indicates,
[05:54] this method is not going to return anything as an output. public
[05:58] indicates that this method can be invoked or accessed from outside of this Java class.
[06:04] Especially my JVM can access it with the help of this public keyword, and there is also a static after
[06:10] public, so static indicates that my method can be invoked without creating an object of my class.
[06:18] So there is a beautiful concept of objects inside Java,
[06:22] we are going to discuss a lot about it, but now please note that using static, my JVM can invoke this
[06:28] method without creating any object of my Java class.
[06:32] So that's the purpose of public static void main.
[06:35] And this method has to accept the input in the format of Array of String.
[06:40] We already know what is String.
[06:41] String is going to accept any amount of data.
[06:44] It can be a sentence or a word or a number or a char or a single letter.
[06:49] But what is Array of String?
[06:50] So there are two square brackets you can see after String.
[06:53] So this indicates it is an Array of String.
[06:56] So Array of String means we can pass multiple strings as an input.
[07:02] If I simply mention String without square brackets, that means my main() method can only accept one input
[07:09] like one sentence or one word, whereas with an array of strings I can pass any number of strings as
[07:16] an input.
[07:17] We're going to talk about arrays in the coming sections, and the variable name that I'm giving for
[07:21] my method input is args.
[07:23] args indicates arguments.
[07:25] After you have defined args as your variable name for your method input parameter, you need to open
[07:31] the opening curly braces and closing curly braces.
[07:35] And inside this method you can write whatever Java code you want.
[07:38] And whenever you try to run your Java code, whatever code that you have written inside this main() method
[07:44] is going to be executed.
[07:45] So from this main() method, if you want, you can invoke other methods, other classes inside your Java
[07:52] project.
[07:52] So all such techniques I'm going to teach you in the coming lectures.
[07:56] Here I also want you to observe one point which is the method names
[08:00] we are following the camel case style.
[08:03] So just like how we followed the standards for the variable names are identifier names.
[08:08] Very similarly the same standard we need to use for method names also.
[08:13] That's why the method names you can see completely in the lower case letters.
[08:17] If I have multiple words as my method names, then I need to use camel case.
[08:22] Whereas for the class name we need to use Pascal case style.
[08:26] I hope this is clear with this knowledge,
[08:28] let me show you the very first Java class that we are going to write.
[08:33] Like you can see here, the very first Java class that we are going to write is HelloWorld.java.
[08:39] So you can see hello is a word and world is a other word
[08:42] both of these words has to be combined without any space.
[08:46] But every word has to start with a capital letter.
[08:50] So this is the standard that we need to follow.
[08:53] What is this case style,
[08:54] this is a Pascal case style.
[08:56] Now let me show you what we are going to write inside this.
[08:59] HelloWorld class.
[09:00] Like you can see public class hello world opening curly brace and ending curly brace.
[09:06] This class definition you already know.
[09:08] So HelloWorld represents my class name and public and class keywords we need to use whenever we are
[09:15] trying to create a class inside Java and post that,
[09:18] I also said whenever we want to execute a Java class, there should be a starting point inside your
[09:23] class.
[09:24] So such a starting point is public static void main().
[09:28] main() is a method.
[09:29] If you follow this definition our syntax, then your JVM is going to execute whatever logic that you
[09:37] have written inside your main() method.
[09:39] So during the execution of your Java program, your JVM always look for the main() method with this syntax.
[09:46] If it finds it is going to execute your logic, otherwise it is simply going to throw an error.
[09:52] So inside this main() method I have written a simple business logic which is to print the hello world!
[09:58] On my screen.
[09:59] So what is a Java statement that we need to write System.out.println().
[10:05] And for this println() method we need to pass the String which is hello world.
[10:09] So here my main() method accepting the input parameter with the string args square brackets.
[10:15] So this square brackets we can keep after string or after args.
[10:19] So it doesn't matter where you are going to keep.
[10:21] So here, even though I'm accepting input to my method, I'm not going to send any input to my method
[10:28] and I'm not going to use that method input parameter inside my business logic.
[10:33] For now, I just want to keep my method very simple.
[10:35] I don't want to confuse you because we are ready to discuss about what are the methods, what are the
[10:41] input parameters.
[10:42] So once we are clear about all such concepts, then we can deep dive into more complex topics.
[10:48] So I hope you are clear when we define this Java class and define this main() method
[10:53] with this business logic, we are going to simply get an output hello world!
[10:57] But in order to execute this Java class, first we need to understand how to compile it and how to pass
[11:03] that
[11:03] compile the class to the JVM as an input and post that we are going to see how the JVM is going to show
[11:11] the output to us.
[11:12] I hope you are super excited for the demo.
[11:14] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
