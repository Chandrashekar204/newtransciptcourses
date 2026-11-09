# 29.2 — [JAVA 22] Launch Multi-File Source-Code Programs

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] Java 22 version released in March 2024.
[00:05] As part of this Java 22 release, there is a new feature introduced with the name Launch Multi File
[00:11] Source-Code Programs.
[00:12] Inside this video, let's try to understand what is this new feature, why it has been introduced,
[00:17] and under which scenarios developers can leverage this new feature.
[00:21] To explain you about this new feature, first I need to go back to the flashback.
[00:26] So let's go to the Java eight version days.
[00:29] You can see this is my terminal and right now inside my system I have Java 8 setup under the Java
[00:35] Home path.
[00:35] So if I try to run java - version command, you'll be able to see that right now my system is pointing
[00:42] to the JDK 1.8 version.
[00:45] As a next step, I'm going to create a Java file inside this folder location.
[00:49] So let me type the command which is dash.
[00:52] Hello.java.
[00:55] So if I press enter there'll be a new file will be generated inside the path desktop /Java.
[01:00] So let me open this file.
[01:02] As of now this file will be an empty file.
[01:06] So inside this file I'm going to type public class
[01:10] Hello.
[01:11] And inside this class I'm going to create a main() method by typing public static void main.
[01:19] And to this main() I'm going to pass the input as string args.
[01:24] Now inside the curly braces I'm simply going to type System.out.println() and to this println()
[01:32] method I'm going to pass an input which is hello world.
[01:36] So this is just a simple Java class.
[01:39] So now if I want to execute this file without the help of Ides like IntelliJ or eclipse.
[01:45] So there is a process that you need to follow which is first you need to compile this class later on.
[01:50] Using the compiled class you can execute the main() method present inside this class.
[01:54] So let me show you that in the demo very quickly. Here what I'm going to do is first I'm going to compile
[02:00] my class with a command Java C.
[02:03] And after this java C command I'm going to mention my Java class name which is Hello.java.
[02:09] As soon as I press enter, you'll be able to see that my compilation is successfully completed.
[02:14] And if you go and check the folder location, there'll be a dot class file might have generated.
[02:19] So you can see there is a dot class file present here. As a next step,
[02:22] if I want to execute the main() method inside my Hello.java class, I need to use the Java command
[02:29] and to this Java command I need to give the class name, which is
[02:33] Hello.
[02:34] So I don't have to give any extension, I just have to give Java.
[02:37] Hello and I'm pressing enter.
[02:39] You can see we are getting the output which is hello world.
[02:43] So this is a two step process that developers they used to follow before Java 11.
[02:49] But as part of Java 11 version, there is a new feature introduced that allow developers to execute
[02:56] a Java program with a single command.
[02:58] Let me show you that demo of the same very quickly.
[03:01] Before that I'm going to delete these Hello.class file here and post that
[03:06] I'm going to switch my Java version from Java 8 to 2 Java 11.
[03:10] So here I'm going to use a command which is SDK use space Java 11 .0.22 - amzn.
[03:20] So this will set Java 11 version inside my Java home path.
[03:25] So right now if I try to execute the command which is Java hyphen version, you can see I'm getting
[03:32] the output as Java 11.
[03:34] So this gives a confirmation to me.
[03:36] Right now my system is pointing to the JDK 11.
[03:39] Like I said before from JDK 11 we don't have to manually compile and execute the program with a two
[03:44] step process.
[03:45] Instead, we can follow a single command which is Java space and what is a class name.
[03:52] So to this class name we should also give the extension which is Hello.java.
[03:56] So if I press enter you can see the beauty here I'm getting Hello World as an output now where I have
[04:03] done any compilation.
[04:04] So this is the improvement that is introduced as part of Java 11 to make developer life easy.
[04:10] So any developer who is trying to learn the basics of Java, the developer, he or she don't have to
[04:16] run the multiple commands.
[04:18] They can simply rely on the single command that we have discussed so far.
[04:22] Whereas if you try to use the same command before Java 11, you're going to get a compilation error.
[04:27] I can also show you that very quickly.
[04:29] For the same, let me point my system to the JDK 8 by using SDK use Java, and I'm trying to mention
[04:39] the Java version which is 8.0.402 - amzn.
[04:45] So this will point my system to the JDK 8.
[04:49] So right now if I try to use the same command which is Java Hello.java, you can see I'm getting
[04:55] an error because I have not compiled the class.
[04:58] So this is the beauty of
[05:00] the new feature introduced as part of JDK 11.
[05:03] This new feature we call it as launch single file Source-Code programs.
[05:08] But right now we are talking about Java 22 version feature which is Launch multi file source code program.
[05:17] So let's try to understand what is this new feature and how it is different from the single file source
[05:23] code program feature that got introduced as part of Java 11. To explain you about the Launch Multi
[05:28] File Source Code programs feature, I'm going to create one more Java class inside the same folder.
[05:35] First, let me try to clean my console post that I'm going to type the command which is touch
[05:41] Greetings.java.
[05:44] This might have created a new Java file inside my folder location.
[05:47] So here you can see I have a Greetings.java.
[05:49] Let me open the same using my text editor.
[05:53] And inside these Greetings.java
[05:55] I'm going to paste all this code post that I'll rename the class name to greetings, followed by.
[06:02] I'm going to rename these main() method to say hello and this method it is not going to accept any input
[06:10] parameter.
[06:11] And inside this static method I have the same logic which is System.out.println().
[06:15] Hello world.
[06:16] Now I'll go back to the Hello.java and here from the main() method I'm going to invoke the static
[06:23] method that I have inside my Greetings class.
[06:25] So how to do that.
[06:27] So first we need to type Greetings.
[06:30] we need to mention the method name which is sayHello().
[06:33] So here there's nothing complicated.
[06:35] I'm just trying to split my business logic into multiple files.
[06:40] It's very quite normal.
[06:42] And it's a very common scenario where a developer who is trying to learn the basics of Java, the developer
[06:48] might write the logic in multiple files like you can see here.
[06:52] So now my hello Java class
[06:55] it has a dependency on another class which is Greetings.
[06:59] So whenever you have these kind of setup where your business logic is spread into multiple files, in
[07:06] such scenarios, whatever new feature that got introduced as part of JDK 11 or Java 11 is not going
[07:13] to work.
[07:14] So let me show you that very quickly.
[07:16] For the same, first, let me try to point to the Java 11 version inside my local.
[07:23] As a next step, I'm going to execute the command which is Java.
[07:26] Hello.java.
[07:27] So you can see I'm getting a compilation error because my business logic spread in multiple files.
[07:34] Whereas if my business logic present inside the same class, then obviously I'll get an output.
[07:39] I can also show you that very quickly.
[07:41] So what I'm going to do is, I'll try to copy this class and paste it inside the same source file.
[07:47] So right now my source file has two classes.
[07:49] So with this setup we should not get any compilation error.
[07:53] So if I try to execute the same command you can see we are getting the output which is hello world.
[07:58] But like I said before there will be some scenarios where developers might have written their logic
[08:04] in multiple files.
[08:05] So to handle the scenarios where the business logic spread across multiple files, the new feature,
[08:12] which is Launch Multi File Source-Code programs, is introduced as part of Java 22.
[08:19] Now what I'm going to do is, I'll point my system to the JDK 22, which is released in March 2024.
[08:26] Once I point my system to the JDK 22, we should not get any compilation, error or business logic spread
[08:33] across multiple files.
[08:35] So here first let me remove these greetings related logic inside the Hello.java.
[08:40] Now you can see my business logic spread across multiple classes.
[08:44] As a next step, I need to point my system to JDK 22.
[08:49] For the same
[08:49] I'm using a command which is SDK use 22 - amzn.
[08:55] So now if I try to execute the command which is java - version, you can see right now my system
[09:01] is pointing to the JDK 22.
[09:03] As a next step I'm going to execute the command which is Java.
[09:07] Hello.java.
[09:09] So this time you can see we are getting a proper output.
[09:13] Hooray!
[09:14] Though our logic spread across multiple files.
[09:17] We are getting a proper output with the single command which is hello.
[09:22] Now where we are compiling the classes manually, we are straight away giving a command which is hello
[09:27] on, what is your class name
[09:28] followed by .java extension.
[09:30] And with that we are getting the output.
[09:33] I hope you are seeing the power of this new feature.
[09:35] Why it is introduced.
[09:36] So to make the developers life easy who are trying to learn the basics of Java, this new feature is
[09:43] introduced.
[09:44] Not all times developers are going to leverage the Ides like eclipse and IntelliJ to execute their programs.
[09:50] So if someone is trying to leverage their notepad or their text editors to execute the Java programs
[09:57] for them, this feature is going to be
[09:59] a life saver and it is going to improve their productivity and they don't have to execute multiple commands.
[10:05] I hope whatever we discuss is clear to you.
[10:08] For your reference, I have mentioned all the details that we have discussed.
[10:12] What is our story before Java 11 and what is the story from Java 11 and how the story changed from Java
[10:18] 22.
[10:19] So please refer to this slide for any questions.
[10:22] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
