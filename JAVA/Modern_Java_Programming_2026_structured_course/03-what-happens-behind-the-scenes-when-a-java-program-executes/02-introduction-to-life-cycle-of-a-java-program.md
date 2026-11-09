# 3.2 — Introduction to life cycle of a Java program

> Section 3: What happens behind the scenes when a Java program executes

[00:00] As of now we are typing our Java code inside jshell, and jshell is processing our Java code and based
[00:07] upon the Java instructions that we have given, it is giving an output.
[00:11] For example, if you try to give an Java instruction which is System.out.println() and to this
[00:18] println() method, if we pass your name, you are going to get an output, which is whatever name you
[00:24] have provided to the println() method.
[00:27] As a developer, we are getting the output from our Java instructions very easily.
[00:32] But do you know there is a lot of process that happens behind the scenes whenever we try to execute
[00:37] a Java code. Because whatever Java code that we have written is not going to be understand by your
[00:44] operating system.
[00:45] At the end of the day, all the instructions inside a computer has to be executed by a operating system.
[00:51] So if I feed this System.out.println() along with the name to the operating system, my operating
[00:58] system will throw an error.
[01:00] You can try typing the same command in a computer where you have not installed Java.
[01:05] Since we have installed Java inside our local system, and since we are using the jshell to execute
[01:12] our Java code, we are getting a proper output.
[01:15] So whatever Java installation that we have done, it is helping to execute the process behind the scenes
[01:22] to convert my Java source code into a format that can be understand by my operating system, regardless
[01:29] of which operating system you are using, whether it can be a mac operating system, windows operating
[01:34] system, Unix or Linux operating system.
[01:37] In all these operating systems, the same process is going to happen behind the scenes,
[01:43] whenever we try to execute a Java code. Throughout this section, we are going to put very good amount
[01:48] of efforts to understand the process that will happen in the background whenever we try to execute a
[01:54] Java code, because as a developer, you should know all these basics and these are the favorite topics
[02:00] for all the interviewers.
[02:02] There is a very good chance that you may face questions around this topic whenever you try to attend
[02:08] an Java based interview.
[02:09] So that's why let's try to put good amount of efforts to understand what happens behind the scenes
[02:15] whenever we try to execute a Java code.
[02:17] Inside this lecture, I'm going to do a very quick introduction about the life cycle of a Java program.
[02:23] As a developer, the very first step that we follow is, we will write a Java code with the help of classes,
[02:31] methods that are available inside the Java programming language.
[02:35] As of now, I know we are ready to discuss what is a class, what is a method inside Java, but for
[02:41] now, please note that inside Java, whenever we want to write a business logic with the help of Java
[02:46] programming language, we need to write all our business logic inside a class.
[02:52] And inside this class we can write any number of methods.
[02:55] I can create a class which will help me to perform the arithmetic operations. Inside my Java class,
[03:02] I can create multiple methods one method to perform addition,
[03:06] the second method to perform subtraction.
[03:08] Very similarly, for multiplication, division I can create more methods.
[03:13] So once a Java developer written all his Java code inside a Java class with the help of Java methods,
[03:19] he need to save that file with that .java extension.
[03:23] So whatever I'm discussing right now, we have not followed all these steps because we are using the
[03:29] jshell.
[03:30] with the help of jshell, we can quickly test our Java code by giving some simple instructions.
[03:36] But in the real projects, jshell is of no use because we are going to write thousands of lines of
[03:42] code inside real projects.
[03:44] That's why we need to always write our Java code inside files that should be saved with an extension
[03:51] of .java.
[03:52] So whatever code that we have written inside that .java file, we are going to call that as a source
[03:58] code.
[03:59] Now as a next step we are going to feed the source code to the Java compiler.
[04:04] That's why the second stage we call it as compilation stage.
[04:08] So what is the purpose of compilation process inside the Java?
[04:11] Inside this compilation stage only your source code will be validated against the syntax or against
[04:18] the rules of Java programming language.
[04:21] Maybe think of a scenario you forget to terminate a Java statement with the help of semicolon.
[04:26] If you forget that, then your compilation is going to throw an error.
[04:30] And very similarly, think of a scenario where you might have created a variable or identifier without
[04:36] following the variable naming convention rules that we have discussed previously.
[04:41] So in all these kind of scenarios, whenever your source code is not following the syntax of Java programming
[04:47] language, your compilation will throw an error along with the details of the errors, like at which
[04:54] line, what error is there?
[04:55] So all such details will be thrown by your Java compiler.
[05:00] So where is this Java compiler present, when we install Java inside your JDK folder
[05:05] there are files that will be installed to help you with the compilation process.
[05:10] So how to process this compilation process you need to use the javac command.
[05:15] The c indicates compile to this javac command.
[05:18] You need to pass your Java class name.
[05:21] So whenever you are using this javac command along with your Java class name behind the scenes, the
[05:27] utilities present inside the JDK folder or inside your Java installation.
[05:31] They're going to take care of compilation process.
[05:34] If your Java source code is looking good without any syntax errors, then your compilation process is
[05:40] going to generate a .class file in the third step.
[05:45] So this .class file that is generated by your compilation process is going to have bytecode.
[05:51] This bytecode we cannot understand as humans, we can only understand the source code that we have written
[05:56] in the very first step.
[05:58] This bytecode format is always going to be the same regardless of what type of machine it was created
[06:05] on.
[06:05] That means if you try to compile the Java source code inside a macOS or windows operating system,
[06:12] or Unix or Linux two based operating systems, you're always going to get the same bytecode.
[06:18] The .class files are always going to be the same.
[06:21] We're going to talk more about what is this bytecode, what is the role that it is playing in the coming
[06:27] lectures.
[06:27] But for now let's go to the next step which is in the final step, the JVM, which is available inside
[06:34] your JDK installation.
[06:36] It is going to convert your bytecode into the format that your operating system can understand.
[06:43] So what is a JVM, Java Virtual Machine like?
[06:47] The name itself is very clear virtual machine.
[06:50] Virtual machine means it is some kind of machine that is not physically available, but it is going
[06:56] to be available virtually inside your Java installation folder.
[07:00] This JVM is responsible to convert your bytecode into the format that your operating system can understand.
[07:09] Here you may have a question like why can't we feed these bytecode directly to the operating system?
[07:15] It's a very valid question.
[07:17] Like I said before, every operating system is going to have its own style of understanding the instructions
[07:24] and executing the instructions.
[07:26] That's why this bytecode, we cannot directly feed to the operating system.
[07:30] There is also a reason why we can't directly generate the OS specific instructions in the compilation
[07:36] stage itself.
[07:36] I'm going to explain all of them in the coming lectures, but for now, please note that since you are
[07:41] operating systems cannot understand your bytecode, your JVM is going to convert your bytecode into
[07:48] the instructions that your particular operating system is going to be
[07:52] understand.
[07:53] These operating specific instructions can be different for different operating systems.
[07:57] The instructions for windows operating system may not make any sense to the Mac operating system, and
[08:04] very similarly for other operating systems as well.
[08:07] So these are very high level life cycle of a Java program.
[08:10] Whenever you try to run your Java code, all these four steps will be executed behind the scenes.
[08:15] I hope this is clear.
[08:16] In this process,
[08:17] I also used a lot many jargons like JDK, Java JVM.
[08:23] So let's try to understand what are these JDK, JRE JVM in the next lecture and post that, we'll try
[08:30] to deep dive into the life cycle of Java program, so that it will be super clear for you.
[08:35] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
