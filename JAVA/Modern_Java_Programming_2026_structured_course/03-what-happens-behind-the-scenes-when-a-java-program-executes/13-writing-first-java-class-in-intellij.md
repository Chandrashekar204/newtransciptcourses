# 3.13 — Writing first Java class in IntelliJ

> Section 3: What happens behind the scenes when a Java program executes

[00:00] I hope you are excited to create First Java class inside IntelliJ.
[00:05] In the same process, we are going to explore the advantages provided by Ides like IntelliJ under the
[00:11] Hello world project.
[00:13] We have various folders like dot, idea, src and there are some files like dot git, ignore hello world
[00:20] ml.
[00:20] So these dot git ignore hello world email and dot idea.
[00:24] Those are the folders and files created by IntelliJ IDE to maintain your Java project.
[00:31] Don't ever try to delete them or change them.
[00:34] The important folder that we need to look is src folder.
[00:39] By selecting this folder you can right click and go to the new option.
[00:43] So here you have an option of creating a Java class or Java Compact file.
[00:50] As we discussed previously as part of Java 25, a new feature of compact to file is introduced.
[00:56] By using any of these approaches, you should be able to write your Java program.
[01:01] If you are not seeing these Java Compact File option, please make sure to update your IntelliJ Idea
[01:08] to the latest version.
[01:09] First, I'll show you on how to write a Java code by using Compact File.
[01:13] Later, I'll also show you the traditional approach by using a normal Java class.
[01:19] So here you can select the Java Compact file.
[01:22] And by default it is going to recommend you some name like main.
[01:26] If it is not giving you any name, try to give some name like main.
[01:30] I'm fine with this recommended name.
[01:31] Let me press enter and with that we are going to get a main dot Java file.
[01:37] And inside that file the shorter main method is already provided by IntelliJ.
[01:42] Even if it is not providing, you can type it manually.
[01:45] Let me type void followed by space followed by main.
[01:49] After the main, I'm going to type opening and closing bracket followed by curly braces.
[01:54] Now inside this method we can write our Java logic.
[01:58] For example, I can write Ivo.
[02:01] Ivo is a Java class.
[02:03] As soon as I type dot.
[02:05] The IntelliJ, it is going to show me all the options that I have.
[02:09] I'm more interested in invoking the println method which is going to accept object as an input.
[02:15] So let me select the same and to this I'll try to provide that text data as.
[02:21] Hello mother.
[02:23] In the similar lines, I'll try to write one more Java statement by using System.out.println.
[02:29] So first I'll try to type system.
[02:31] So inside the system make sure you are typing first S as capital followed by.
[02:36] As soon as you type dot.
[02:38] You don't have to remember any code, you just have to look.
[02:41] What are the options that you have?
[02:42] Since we are looking to invoke the out as soon as you type O, it is going to show you that out.
[02:49] You can select the same and press enter followed by.
[02:53] If you type dot, it is going to show you the next set of recommendations that you have.
[02:58] So these are all the possible options that the developer has to invoke as an extra code.
[03:03] So here I'm looking for the method println which is going to accept a string as an input.
[03:09] So please make sure you are selecting this method.
[03:11] I know most of these concepts.
[03:13] They're not going to make sense to you.
[03:14] We are definitely going to discuss about them in the coming sections.
[03:17] Meanwhile, I am getting you comfortable with the simple Java classes.
[03:22] So here I am going to press enter and to this I will try to provide input like hi Java, if you see
[03:29] the IDE, it is making my job very easy.
[03:32] Even if I make any mistakes, it is going to highlight and help me in resolving the issue.
[03:36] For example, if I forget to mention the semicolon, it is going to show me a compilation error saying
[03:42] that semicolon is expected.
[03:44] By looking at that, I can mention and resolve the problem.
[03:47] Unless there are no errors inside my code, the IDE, it is not going to allow me to execute this program.
[03:53] Similarly, if I forget to mention some double quote here, Here also it is going to throw me some compilation
[04:00] error.
[04:01] So these are all going to give me some clues to the developer about what is the mistake has been done
[04:07] and how to resolve the same.
[04:08] Before we try to execute this program, I want to change the default font provided by the IntelliJ.
[04:13] So this looks very boring to me.
[04:15] What I can do is I can go to settings and under this appearance I can select these use custom font option.
[04:24] And here I can select any of these font.
[04:27] So feel free to select any of the font that excites you.
[04:31] I will go with a font with the name Comic Sans Ms..
[04:36] If you have this font in your operating system, you can select the same.
[04:40] Otherwise you can go with your favorite font coming to the size of the font.
[04:43] Also, I'm going to increase this to 18 so that you can see the code that I'm writing clearly.
[04:48] But for your local development, you should be fine with the 13 or 14 size.
[04:53] Let me apply and okay the font on the left hand side menu is changed, but the font inside the Java
[05:00] class, it didn't change anything.
[05:02] So what I can do is I can open the settings and search for font.
[05:07] So here there is a font option under the editor menu.
[05:11] Let me select the same.
[05:12] And this is the font that is going to be used inside the Java files.
[05:17] So here I'm going to select the same option of Comic Sans Ms..
[05:23] And I'll go with the size as 18 and apply okay.
[05:29] This time as you can see the font inside that Java file also changed.
[05:33] Now to execute this program we can use this button.
[05:36] So as soon as I click on this I'm going to have two options like run and debug.
[05:41] So run is an option which is going to execute your program without stopping at the breakpoints.
[05:46] Whereas with the debug option your code execution is going to stop at the breakpoints.
[05:51] I'm going to teach you what are breakpoints and how to debug your code in the coming lectures.
[05:56] For now, let's go with this run option.
[05:58] As soon as I click on this option, I'm going to get an output inside the console.
[06:03] Inside the console, you'll be able to see Hello Maiden, which is the output from the first statement,
[06:08] followed by hi Java, which is coming from the second statement.
[06:12] On top of this output, you can also see what is the JDK version right now you are using.
[06:17] In case if you are not seeing the expected JDK version, you can always right click on the project and
[06:25] select Open Module Settings.
[06:27] Inside this project settings you can select this project and here also you can select the SDK version
[06:34] or JDK version that you want to use.
[06:36] Once you select SDK here, you need to go to the modules and under the sources, you need to either
[06:42] use the project default or you need to select 25 hyphen compact source files comma module imports.
[06:50] So under that 25 version.
[06:52] So these are the major features that got introduced the same you need to select.
[06:56] Once you make sure all these are fine, you can click on apply and okay.
[07:01] So this is how you can select a specific JDK version for your Java project.
[07:06] Before we try to write another Java class by using traditional main method, let me show you some of
[07:12] the advantages provided by IDE.
[07:14] So as soon as I created a Java class, you will be able to see.
[07:18] Next to this file there is a C icon.
[07:20] And here also you will be able to see there is a C icon.
[07:23] So that indicates this is a Java class.
[07:25] And along with the C icon you also see some run icon.
[07:29] So since this class has a main method this run icon also is being shown in the IDE.
[07:35] So this way when your project has hundreds of files, you can easily understand what is the type of
[07:41] a file inside Java.
[07:42] Apart from Java class, we should be able to create Java interfaces, abstract classes for all those
[07:48] different Java files that we can create the icons that you will be seeing inside the IDE will be different.
[07:55] Next I want to talk about these out folder.
[07:57] So previously we don't have this folder.
[07:59] But right now once we execute our Java program we are seeing these out folder.
[08:04] So when we are not using IDE and when we want to execute our Java program through a terminal, it is
[08:11] our responsibility to execute some commands by using Java, C or Java.
[08:16] But when you are using IDE, you don't have to execute all those commands manually.
[08:21] You just have to click on these icons.
[08:22] And behind the scenes, the compilation and the execution of the file is going to happen.
[08:28] So the compiled files you will be able to see under these out folder.
[08:32] So there is a main file.
[08:34] If I open the same you'll be able to see this is a dot class file.
[08:37] That means this is a compiled Java class but not a Java source file.
[08:42] Usually inside dot class file we are going to have the bytecode.
[08:46] If you open the same main dot class by using some text editor, for example, I can go to these open
[08:53] in finder, which is going to show me the folder where this main dot class is present.
[08:58] And here I'm going to open this with a text editor like Sublime Text.
[09:03] So this is how the dot class file is going to look like with the bytecode.
[09:07] But inside IntelliJ we are able to see some Java source code itself.
[09:12] So how this is happening is the IDE.
[09:15] It is doing that decompilation process.
[09:17] What is the Decompilation process?
[09:18] It is the process where you convert a bytecode into a normal Java code, the IDE, it is doing this
[09:25] decompilation process for the convenience of the developers.
[09:29] So we have not created any Java class inside the source code.
[09:33] Behind the scenes.
[09:33] The compiler.
[09:35] It is going to add these Java class with the name main.
[09:38] At the end of the day, every code that we write it should be present under a Java class.
[09:43] So we have not mentioned a Java class here.
[09:45] The same is created behind the scenes by the compiler.
[09:49] This is the beauty of the feature that got introduced inside Java 25, whereby, writing some compact
[09:55] code, we should be able to execute any Java code.
[09:58] This way, Ides like IntelliJ.
[10:00] Or NetBeans or any other Ides, they're going to make that developer life easy.
[10:04] Throughout this course, I'm going to teach you various features from these Ides and how to use them,
[10:10] and how to make your life easy, regardless of which IDE you are using.
[10:14] The overall features that they provide, and the overall look and feel of these Ides should be very
[10:20] similar, with some minor changes from now onwards.
[10:23] We are going to use IDE to a great extent.
[10:26] Occasionally we are going to use Jshell.
[10:28] So compared to IDE, Jshell has its own advantage.
[10:31] By using Jshell, we should be able to execute a single statement like System.out.println or any other
[10:39] Java statement.
[10:40] Whereas if you want to execute a code by using IDE or by using a terminal, you need to make sure you
[10:46] have created a Java file.
[10:48] You need to make sure to create a Java method, especially with the name main.
[10:52] All these steps you need to follow just to test a single Java statement.
[10:56] Whereas with the Jshell it's going to work out of the box.
[10:59] It is going to accept your single Java statement, execute it, and it is going to show you the output.
[11:04] So for the beginner, Jshell is going to be super helpful once you are confident with the basics of
[11:09] Java.
[11:09] Obviously the next upgrade that you are going to follow is using and proper Ides like IntelliJ.
[11:16] So we're going to switch between Jshell and IDE from now onwards.
[11:20] But majority of the times we are going to use IntelliJ and in real projects also the developers, they
[11:25] are going to use products like IntelliJ to a great extent.
[11:28] As a next step, let me show you on how to create a normal Java class with a traditional main method.
[11:35] So here I'm going to right click and select New Java class.
[11:39] This time it is asking me to provide a Java class name.
[11:43] Let me mention the class name as Hello World!
[11:47] While creating a new Java class, I have various options like interface record, enum annotation, exception,
[11:52] compact source file.
[11:54] We're going to discuss all these options throughout this course.
[11:56] So we already explored about what is a compact source file.
[11:59] But right now we are looking to create a normal Java class.
[12:03] So as soon as I select the class and press enter, a new Java class is going to be created.
[12:09] And inside this I can create a main method with the syntax public static void main.
[12:15] Instead of typing that public static void main every time, I can follow a shortcut inside IntelliJ,
[12:22] the shortcut is p SVM.
[12:26] So SVM is shortcut for public static void main.
[12:30] And since we are also looking to provide input arguments we need to type a as well.
[12:36] So p SVM.
[12:38] As soon as I press enter I'm going to get a main method.
[12:42] So here mentioning public is optional.
[12:45] But still I'm going to mention the same for your understanding.
[12:49] So next I'm going to type System.out.println.
[12:52] So even for System.out.println we have a shortcut which is S for you.
[12:58] If I press enter I'm going to get the System.out.println complete statement.
[13:03] And to this I will try to provide something like hello world.
[13:07] Next I'm also going to use io dot println.
[13:12] Here I'm going to type something like Hi world.
[13:16] Once the code changes are completed, we can try to execute this program by using this icon and selecting
[13:22] the run option.
[13:24] So this time we are going to get the expected output inside the compact file.
[13:28] If you are looking for a shortcut to create the main method, you just have to type PS VM.
[13:35] As soon as you type PS vm and select and press enter, you're going to get the void main, which is
[13:41] the same as the upper method.
[13:43] Since right now we have two main methods of same type, we are getting this compilation error.
[13:49] Let me delete the same.
[13:50] And with that the compilation error is going to be solved.
[13:54] I hope you are clear on how to create Java files and Java code using IntelliJ.
[13:59] I know this is the initial baby step that we are taking, but I would recommend you to pause this course
[14:05] and try to practice what I have showed you inside IntelliJ.
[14:09] Please create the same Java files and try to write some Java code inside main methods and try to execute
[14:15] those programs.
[14:16] So please be comfortable with IntelliJ because this is very important for a Java developer.
[14:21] If you are feeling exhausted with all this information, don't worry, that is perfectly fine for the
[14:26] beginners.
[14:27] I would recommend you to take a break and do practice.
[14:30] Once you are comfortable with all the concepts that we have discussed so far, then you can come back
[14:35] and continue with the course at any point of time.
[14:38] If you need any help, feel free to post your question inside the Q&amp;A.
[14:42] I hope you are enjoying the course.
[14:43] If yes, please provide your valuable feedback to the course.


########################################
