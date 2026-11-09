# 3.10 — [JAVA 25] Compact Source Files and Instance Main Methods

> Section 3: What happens behind the scenes when a Java program executes

[00:00] As part of Java 25 version.
[00:02] A new feature with the name compact to source files and instance main methods is introduced by the Java
[00:09] team in order to make the Java language more beginner friendly.
[00:12] This feature is introduced to make the Java language more beginner friendly.
[00:17] As of now, whenever we want to get started with Java, we have to create a Java class, and inside
[00:22] the Java class, we need to write an main method by following this exact syntax.
[00:28] Public static void main string array with args.
[00:33] But with this syntax the beginners.
[00:35] They will have very hard time in understanding all these concepts, like what is the purpose of this
[00:40] static?
[00:41] What is the purpose of this public?
[00:42] What is the purpose of this void and what is the string array?
[00:46] All these kind of questions will be running behind for the beginners.
[00:50] That's why to make their life easy Java team, they gave a flexibility from Java 25 version that they
[00:58] can try to execute some Java code by following a compact source file.
[01:04] By using this compact source file and instance main method feature.
[01:08] You don't have to create any Java class.
[01:10] You can directly write a method inside your Java file.
[01:14] What is the method?
[01:15] It should be main and since it is not going to return anything as an output, the return type should
[01:20] be void.
[01:21] So void main and inside the curly brackets we can write statements like System.out.println.
[01:28] Hello world!
[01:29] Even for the beginners to understand, the System.out.println is very hard for them because there is
[01:35] a brief history around the syntax which we are going to discuss in the coming lectures.
[01:40] Since the beginners, they are going to have hard time in remembering these syntax.
[01:45] They gave another option for beginners, which is we can invoke the same println method from an Evo
[01:51] class.
[01:52] Evo is a Java class which is available inside the Java library.
[01:56] Inside this class there is a println method which is same as this method.
[02:00] To this method, we can pass whatever we want to display onto the console.
[02:04] The same is going to be displayed since we are going to write very compact code inside the Java file.
[02:10] This name came which is compact source file and coming to the instance method, whatever main method
[02:15] that we have written here.
[02:17] This is an instance method.
[02:19] So we are going to talk about what are these instance methods in the coming lectures.
[02:23] Whereas the previous main method that we have written it is a static method.
[02:27] So there is a very big difference between an instance method and static method.
[02:32] Since Java team is looking to make beginner life easy, they try to get rid of most of the code from
[02:38] these beginner Java class.
[02:40] So you don't have to write this code.
[02:42] You don't have to type public static, and you don't have to write this one.
[02:46] And even instead of writing system dot out, you can simply use your class.
[02:50] And from that you can invoke the println method.
[02:54] Let me show you a demo of this very quickly.
[02:57] If you recall, this is the Java code that we have written previously and we compiled it and executed
[03:02] as well.
[03:03] So here we have created a Java class, which we don't have to do if we are using Java 25 version.
[03:10] So let me delete the same and the last curly brace.
[03:13] Also I have to delete.
[03:14] Now coming to the main method, I can make it further simple by removing public static.
[03:20] And I can simply have void main and I don't even have to pass any input as well.
[03:26] Next, instead of the system dot out, I'm going to mention Ivo, which is the class name.
[03:33] Ivo means input and output.
[03:35] Inside this class we're going to have a method with the name println and to the same.
[03:39] I'm trying to pass the input as Hello world.
[03:42] Maybe instead of Hello world.
[03:43] This time I'll just mention Hi world so that you can see the difference in the output.
[03:48] So right now, by adopting the compact source files and instance main method new feature from Java 25.
[03:55] My first Java program is ready.
[03:57] So let me save this and go to the terminal.
[03:59] From the terminal I'm going to execute the command Java hello world dot Java.
[04:04] With the single command, I should be able to compile and execute both at a time.
[04:09] As soon as I press enter I am going to get the output.
[04:13] Hi world, I hope you are clear on how to develop and execute Java code by using compact source files,
[04:20] but this feature you should use only when you are learning the Java program.
[04:25] You should not use these feature, or you should not try to develop your Java code by using these feature.
[04:31] When you are developing real applications or when you are working in a real organization.
[04:37] When you are writing real Java code for real requirements, you should definitely use the older syntax
[04:43] that we have discussed previously.
[04:44] That's why throughout this course I'm going to use the same public static void main syntax so that you
[04:50] will get familiarized with that complex syntax.
[04:53] But as we start discussing more advanced concepts like what is public, what is static, what is void,
[05:00] what is an array as we are progressing inside this course, you should be able to easily understand
[05:05] and remember the older syntax as well, but feel free to use these compact syntax as well whenever you
[05:12] want to quickly execute some Java code.
[05:14] Even the experienced Java developers, they are going to leverage this new feature because whenever
[05:19] they want to quickly test some business logic, or whenever they want to quickly test some prototype,
[05:24] they don't have to create a class and they don't have to type that lengthy syntax.
[05:29] Instead, they are going to leverage these new compact code.
[05:32] But please note that these compact source code is going to work only from the Java 25 version.
[05:39] When you are using these compact source file feature, you should be able to write main method by following
[05:45] any of these variations.
[05:47] Instead of just mentioning void main, you can also mention public void main or static void main args.
[05:53] Public static void main are public void main string args are public static void main string.
[06:00] So whatever I have mentioned towards the end that is the correct and full syntax that we need to follow
[06:05] inside production or real applications.
[06:08] But the Java team from Java 25, they gave a flexibility to the beginners to use any of these main method
[06:15] flavors.
[06:16] In case if a developer has both a main method with a string array args and another main method without
[06:22] any input parameters, then JVM, it is going to give preference to the main method, which is having
[06:27] the string array args as an input.
[06:30] I can show you a quick demo around this as well.
[06:32] So let me first show you various main method variations that you can use.
[06:36] Instead of simply using void main, you can also use public void main.
[06:41] So if I save this and execute the program, I'm still getting the same output.
[06:46] Next, instead of mentioning public void main, we can also mention static void main this time.
[06:51] Also, if I execute the program I'm going to get the same output.
[06:54] You can also mention both of them like public static void main.
[07:00] This time also I'm going to get the same output in case if a developer is mentioned two main methods.
[07:07] For example, if I mention the another main method which is the simpler one like void main.
[07:14] In this scenario we are going to get a compilation error.
[07:17] If I execute this program, I'm getting an error saying that main method is already defined in the class.
[07:22] Hello world!
[07:23] You should not have two main methods which are not accepting any input parameters.
[07:29] Instead, if you want, you can have another main method which is accepting string array as an input.
[07:37] So the first main method I have updated that to public static void main string array args, which is
[07:43] a full syntax that we usually follow inside this method.
[07:47] What I'll do is I'll just mention system dot out dot println.
[07:53] And here I'm going to mention Hello world.
[07:56] So as I said before, when you have these kind of two different methods, one is not accepting any input
[08:01] and the other one is accepting.

----------------------------------------
