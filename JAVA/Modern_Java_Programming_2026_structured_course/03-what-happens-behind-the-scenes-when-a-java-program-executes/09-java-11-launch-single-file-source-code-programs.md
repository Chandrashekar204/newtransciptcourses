# 3.9 — [JAVA 11] Launch Single-File Source-Code Programs

> Section 3: What happens behind the scenes when a Java program executes

[00:00] Our team regularly, they are going to introduce new features inside Java.
[00:05] Few of these new features are going to help the Java language in adopting the latest trends, and few
[00:11] of the features.
[00:12] They are going to help the developers in improving their productivity.
[00:15] Inside this lecture, I'm going to introduce you one such feature, which is going to help the developers.
[00:21] So far, whenever we want to execute a Java program, we are following two step process.
[00:27] The first one is a compilation followed by the Java code execution.
[00:30] As you can see, this is the first Java class that we have written.
[00:34] So whatever code that we write inside that Java files, we call this code as source code.
[00:39] Once the source code is ready, we are going to compile the source code by using Java C command.
[00:45] So how to do that we have to type Java C followed by what is the file name.
[00:50] It is hello world dot Java.
[00:54] As soon as we press enter the compilation is going to complete and we are going to get a dot class file
[01:00] which is going to have bytecode.
[01:02] We all know all this story.
[01:03] Next, in order to validate our program and see the output, we are going to execute the next command
[01:09] which is Java, followed by hello world.
[01:12] When we are providing a name to the Java command, we should not provide any extension.
[01:16] We just have to mention Hello world and press enter.
[01:20] And with that we are going to get the expected output.
[01:22] As you can see, this is a two step process where we are first doing the compilation, followed by the
[01:28] execution of the Java code.
[01:29] Instead of executing these two commands.
[01:31] Now developers from Java 11 version, they should be able to achieve the same result by executing a
[01:38] single command.
[01:40] Let me show you the demo of the same.
[01:42] First I'm going to clear my terminal, followed by.
[01:45] I'm going to delete these dot class file.
[01:47] This time the command that I'm going to type is Java, which is the same one that we have used before
[01:52] to this Java.
[01:53] If you provide the file name along with the extension which is Dot Java, this time when we execute
[02:00] this command, the compilation and the program execution is going to happen simultaneously and we are
[02:06] going to get the output this time, as you saw with a single command, we are able to get the same result.
[02:11] And behind the scenes, I'm not going to have any dot class file generated because the Java is going
[02:17] to take care of compiling my source code and executing in a single step.
[02:22] That's why we are not going to see any intermediate dot class file, even when we are executing the
[02:27] single command Java Helloworld.java.
[02:29] Behind the scenes, the Java is going to take care of compiling your file and executing it by using
[02:36] that two commands that we have discussed before.
[02:38] The purpose of introducing this new feature as part of Java 11 version is to help the developers to
[02:44] improve their productivity.
[02:46] When the developers, they quickly want to see the output of their Java code, they don't have to go
[02:51] with the lengthy process.
[02:52] Instead, they can follow this shortcut inside Java Interviews.
[02:55] If someone asks you on how to compile a Java code, you should always explain the two step process that
[03:01] we have discussed previously.
[03:03] On top of that, you can mention them from Java 11 version.
[03:07] The developers has the flexibility to compile and execute the code with a single command for your reference.
[03:13] I have prepared this slide as part of Java 11 version.
[03:16] A new feature with the name launch Single File Source code program is introduced.
[03:22] Usually Java team.
[03:23] For every new feature that they are going to introduce, they are going to provide a name like this.
[03:27] So here I have given a brief history before Java 11.
[03:30] When you want to compile and execute a Java code, you have to follow a two step process Java C followed
[03:38] by file name dot Java.
[03:40] And as part of the second step you need to execute Java and hello without extension.
[03:45] Whereas from Java 11, by using these launch single file source code program feature, you should be
[03:51] able to complete both compilation and execution by using a single command.
[03:56] The command is Java and this time, along with the file name, you need to give the Dot Java extension.
[04:02] But whatever.
[04:03] This feature which got introduced as part of Java 11, this is going to work when your entire Java code
[04:09] is present in a single source file, but in real applications or for a complex examples developers,
[04:16] they are going to split their Java code into multiple files.
[04:19] For example, here I have a file with the name hello and greetings from the hello main method.
[04:25] I'm trying to invoke the method present inside the greetings class.
[04:29] The method name is Say Hello which is present here.
[04:32] So I'm trying to invoke the same from the hello class.
[04:34] So this way the developers, they're going to develop their code across multiple files.
[04:39] I know where to discuss about these complex topics, but I'm trying to give a quick introduction about
[04:44] another feature that got introduced as part of Java 22.
[04:48] So when you have these kind of Java code, whatever Java single command that we are using from Java
[04:55] 11, it is not going to work.
[04:57] The developers has to go through the normal process of executing both these two commands, but this
[05:02] limitation is also addressed by the Java team from the Java 22 version.
[05:08] Inside Java 22, the Java team, they introduce a new feature with the name Launch Multi File Source
[05:14] Code program.
[05:15] So from Java 22, even though if your Java code is spread across multiple Java files, you should be
[05:21] able to compile and execute the code by using this single command.
[05:25] So always to the Java command, you need to give the class name where the main method is present.
[05:31] So I have hello and greetings class names.
[05:34] Since the main method is present inside hello Java file the same I have to provide here.
[05:40] I hope you are clear before Java 11.
[05:42] This is how the process from Java 11.
[05:45] We should be able to compile and execute single file source code programs.
[05:50] Whereas from Java 22 we should be able to compile and execute even multi file source code programs as
[05:57] well.

----------------------------------------
