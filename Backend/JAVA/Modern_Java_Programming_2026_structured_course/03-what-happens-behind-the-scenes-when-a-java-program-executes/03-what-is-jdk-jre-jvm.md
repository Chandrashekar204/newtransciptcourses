# 3.3 — What is JDK, JRE, JVM

> Section 3: What happens behind the scenes when a Java program executes

[00:00] In the previous lecture I introduced lot many jargons like JDK, JRE, JVM.
[00:06] In this lecture let's try to understand what are these jargons and what is the role that they play
[00:11] whenever I try to execute my Java program. The very first jargon that I want to talk here is, JDK.
[00:17] So what is the full expansion of JDK?
[00:20] Java Development Kit. JDK is nothing but your Java installation folder.
[00:26] Whenever we install Java inside a system as part of the installation, we are going to get a collection
[00:32] of tools and utilities.
[00:33] And inside these tools and utilities will have various components like Java Runtime Environment which
[00:40] is JRE and interpreter or loader, a compiler and archiver, a documentation generator.
[00:47] This way there are many other tools will be available inside your installation folder.
[00:52] Since these installation folder has lot many utilities and tools, that is going to help the developers
[00:58] while developing Java programs.
[01:00] We call these installation folder as Java Development Kit.
[01:05] Let's see the installation folder inside our system to better understand what are going to present inside
[01:11] the JDK folder.
[01:12] For the same, I came to my terminal using my terminal,
[01:15] first, I want to understand where I have installed my Java.
[01:19] So to understand that I need to run a command using my operating system terminal.
[01:23] That's why I need to come out of my jshell session.
[01:26] So let me execute the command /ex or /exit.
[01:31] So this will come out of my jshell session.
[01:34] So now the command that I want to run here is, echo $JAVA_HOME.
[01:41] So whenever we install Java inside our local system and environment variable is going to be set up.
[01:48] And this environmental variable name is going to be JAVA_HOME.
[01:51] So inside this environment variable we are going to maintain the Java installation folder
[01:57] details.
[01:58] So let me execute this.
[01:59] So since I have install Java with the help of sdkman inside my local system I'm getting this path.
[02:06] So this is the path where I have installed my Java inside windows operating system.
[02:12] The same commands may not work.
[02:14] The command that you need to execute is echo % after percentile,
[02:19] you need to mention JAVA_HOME and at the end you should mention the % again.
[02:25] So these are the command that you need to run inside your windows operating system.
[02:30] So this will give you the Java installation folder.
[02:34] Whereas inside mac operating system or Unix or Linux based operating system.
[02:39] You need to run the command which is echo $JAVA_HOME.
[02:43] I hope this is clear.
[02:44] Now let me go to the installation folder location.
[02:47] So I'll go to my user's folder.
[02:50] Inside my users folder there is a user with the name eazybytes and inside eazybytes
[02:55] I have a folder with the name .sdkman, so let me look for the same.
[03:00] So here is the folder.
[03:01] Let me go inside this and inside this, I need to look for candidates folder.
[03:06] So these are folder and inside candidates I have java folder under a java folder,
[03:11] I need to open the current.
[03:12] And you can see this is the folder where my Java has been installed.
[03:17] We can go and open the bin folder.
[03:20] Inside the bin folder we have all the executable files that are provided by the JDK.
[03:26] So all these executable files are going to help Java developer for various operations.
[03:31] For example we are using jshell.
[03:33] So whenever I try to run the command jshell from my terminal it is going to invoke this executable
[03:40] file which will give me a jshell session using which I can execute Java commands. Very similarly,
[03:46] like I said before, we have a javac command to initiate the compilation process.
[03:51] Very similarly, using this Java command I can execute my compiled Java code.
[03:56] So behind the scenes, whenever I'm trying to run my bytecode with the help of Java command, JVM will
[04:02] take care of converting that bytecode into the machine code.
[04:05] And I'm going to get an output.
[04:07] So this way there are many executable files.
[04:10] Let me show you the list of files.
[04:11] You can see here
[04:12] the kind of these files are Unix executable files.
[04:16] So this is inside my mac operating system.
[04:18] It is showing like this.
[04:19] But if you are using windows operating system or other operating system, it may show you the different
[04:25] format based upon your operating system.
[04:27] I hope this is clear.
[04:28] Now let's try to understand what exactly is JRE and JVM.
[04:33] So inside JDK we are going to have JRE and some dev tools.
[04:38] So these dev tools are going to help the developers to run their Java program to compile their Java
[04:44] program.
[04:45] So inside dev tools only we're going to have Java compiler, a tool like document generator, a tool
[04:51] like jar Generator.
[04:52] So there are many dev tools are going to be available as part of your JDK.
[04:56] Apart from these dev tools your JDK is also going to
[05:00] have JRE.
[05:01] So what is JRE, Java runtime environment.
[05:05] If you ask me, what is the difference between JDK and JRE?
[05:07] JDK is going to have both JRE and dev tools.
[05:12] That means whoever going to develop the Java programs they need to install the JDK, because if they
[05:18] install JDK then only they are going to have tools like Java compiler using which they can compile their
[05:24] Java source code.
[05:25] Whereas for the people who are looking to simply execute the compiled Java code, they can use JRE.
[05:32] For example, think like I have developed a Java program.
[05:35] I compiled it with the help of dev tools and JDK, and I also validated if it is working properly or
[05:41] not by using the JRE.
[05:43] So once I satisfied with all the outputs, I can give the .class file that is generated during the
[05:49] compilation process to one of my friend.
[05:52] Now my friend want to simply see the output.
[05:54] He don't want to do the compilation because compilation
[05:57] I already taken care and since he's not a Java programmer, he don't care
[06:02] also to compile it, he simply want to see the output from my program.
[06:06] So he's going to take that .class file and he's going to use the JRE
[06:12] and with the JRE he can simply execute my compiled Java code.
[06:16] And he can see the
[06:17] what is the output.
[06:18] So in simple words JDK is going to be needed for all the developers, whereas JRE is going to be needed
[06:26] for people who want to simply execute a compiled Java code.
[06:30] So instead, JRE, what do we have?
[06:32] We have JVM and other set of libraries.
[06:35] So what is the role of JVM?
[06:36] JVM is going to accept the byte code or the .class file that is generated during the compilation
[06:43] process.
[06:44] And this JVM is going to convert your byte code to an operating system specific format.
[06:50] So what is the full expansion of JVM, Java Virtual Machine.
[06:54] So I have mentioned all the details about these jargons,
[06:56] like what is a Java compiler, what is Java Runtime Environment and what is a Java Virtual Machine,
[07:02] what is the role that they play.
[07:04] So all the details that we have discussed, I have mentioned here, in simple words if anyone asks you
[07:09] what is JDK and what is the JRE and what is Java Virtual Machine, you can always say that JDK is equal
[07:16] to JRE and inside JRE
[07:18] we are going to have JVM and libraries and apart from JRE, we are also going to have dev tools inside
[07:24] JDK.
[07:25] So these JDK is needed for the developers.
[07:27] But coming to the JRE, it is going to simply have the JVM and the supporting libraries.
[07:32] That's why using the JRE we can simply execute the Java program, but we can't compile it,
[07:38] we can't write the Java code with the help of JRE alone.
[07:41] So I hope you understand,
[07:43] but here I have a surprise for you from JAVA 9.
[07:47] The JRE is no longer officially provided, only the JDK is offered.
[07:52] This is because to reduce the Java installation size by removing the duplicate files.
[07:58] So let's try to understand more details about this.
[08:01] Why JRE is no longer offered from JAVA 9.
[08:04] Like I said before, before JDK 9, the Java build system, they used to generate two distinct types
[08:10] of Runtime images.
[08:11] One is Java Runtime Environment and other one is a Java Development Kit.
[08:16] So people have an option whether they want to install JDK, which is going to have JRE inside that,
[08:22] or they can simply go with the Java installation.
[08:26] That means if someone don't want the all the development tools, they can simply go with the JRE installation.
[08:32] So they used to have an option of JDK or JRE, but from JAVA 9, a good amount of changes happened
[08:38] in the directory structure of the JDK.
[08:40] One such important change is JRE was completely eliminated.
[08:45] The entire folder structure of JDK has been flattened to save some space, and to avoid the confusion
[08:52] for the people who want to use Java.
[08:55] So before JAVA 9, they used to have confusion whether they should install JDK or whether they should
[09:00] install JRE.
[09:01] So to avoid such confusions, the option of installing only JRE is completely eliminated.
[09:07] Now everyone has to install JDK, but for some reason, if an organization is looking to generate their
[09:13] own standalone JRE, then they can simply generate their own custom JRE with the help of jlink option
[09:20] introduced in JAVA 9.
[09:22] But people rarely use this jlink option.
[09:25] Now, as a next step, let me show you how the Java installation folder is going to look like before
[09:31] JAVA 9 and after JAVA 9, like you can see here before JAVA 9, whenever someone installed
[09:37] JDK, inside JDK, they used to have Java folder, and inside this folder they used to be bin and lib.
[09:44] So here it is very clear,
[09:46] there are some files are some utilities.
[09:48] They are duplicated both in JRE and the parent JDK folder.
[09:52] So to avoid such scenarios now from JAVA 9 version, the JDK installation folder is not going to
[09:59] have
[10:00] any folder with the name JRE.
[10:02] I hope you are able to see the difference, but here you may have a question for me if from JAVA 9.
[10:07] If there is no JRE option available, then why the hell are you explaining as what is JRE,
[10:13] what is JDK,
[10:14] you should have explained simply JDK.
[10:16] I understand your frustration, but like I said, there are good amount of people and organizations
[10:21] who are still using JAVA 8.
[10:24] So if you go for an interview inside an organization who are using JAVA 8, then they may ask you
[10:30] what is JDK,
[10:31] what is the JRE,
[10:32] I want you to be prepared for all such scenarios and some organizations who are using the latest versions
[10:38] of Java like Java 17, Java 21, even
[10:41] they may also ask you why we don't have Java option right now,
[10:45] if I want to generate my own JRE, what is the option that I have?
[10:48] So for all such questions, you should be well prepared.
[10:51] That's why I have provided all this data.
[10:54] I hope this is all clear to you.
[10:55] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
