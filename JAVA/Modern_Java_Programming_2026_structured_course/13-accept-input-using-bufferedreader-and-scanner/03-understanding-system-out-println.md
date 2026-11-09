# 13.3 — Understanding System.out.println

> Section 13: Accept input using BufferedReader and Scanner

[00:00] I know you are super excited to learn on how to make your programs to ask the input data from an end
[00:07] user, but before we try to understand the concept of accepting the input data from an end user, first
[00:13] let's try to understand how we are displaying the output data from our Java programs.
[00:19] You already know about this, and we use these approach hundreds of times throughout this course.
[00:25] Can you tell me what is the approach that we are using to display the output from a Java program?
[00:29] Yes, you are correct.
[00:31] We are using System.out.print() or println() or printf() methods.
[00:37] For example, think like you have a requirement to display an output which is hello world from your
[00:44] Java program.
[00:45] In this kind of scenarios you can achieve the same with the help of three most commonly used different
[00:51] approaches.
[00:52] The very first one is System.out.print() method.
[00:56] So this is going to print the given input data.
[01:00] And after printing that data it is not going to move your cursor into the next line.
[01:05] The cursor is going to stay at the same place where your output data is displayed.
[01:11] The second approach is println() method.
[01:13] This works very similar to the print() method, except with a difference which is the cursor is going
[01:19] to be moved to the beginning of the next line as soon as the output is printed onto the console.
[01:26] And at last we also discussed about the printf() method, which is going to support the formatting of
[01:32] the given input.
[01:33] You can have some placeholders inside your output data and these placeholders
[01:38] you can replace them with some dynamic data based upon the variables that you are providing to the printf()
[01:44] method.
[01:44] I know it might be annoying for you to repeat this concept one more time, and you may have a question.
[01:50] I know all these concepts.
[01:51] Just tell me how to accept the input data.
[01:54] I'm already aware about how to display the output data and I'm perfect at it, but please be patient.
[02:00] I want to share a very important update around the System.out.print() method or println() method
[02:07] or printf() method.
[02:09] If you closely observe these three different approaches, we are invoking the methods like print(), println()
[02:15] and printf() with the help of code like System.out.
[02:19] So with this you might be thinking that these print(), println() or printf() method
[02:24] they are present in the class which is System.
[02:27] So system is a class and out
[02:29] it should be a static variable because we are trying to invoke this variable by using the class name,
[02:36] and after the variable name, we are trying to invoke the method name.
[02:40] So this code looks very unique.
[02:43] And this is very different compared to the other kinds of method invocations that we have done throughout
[02:48] the course.
[02:49] Usually how we do the method invocations, if it is a static method, we are going to invoke with the
[02:54] help of class name, whereas if it is an instance method, we are going to invoke it with the help of
[03:00] object of a class.
[03:01] But here, if you see we are not invoking these methods either with the class name or with the object
[03:07] of the System, we are doing something different.
[03:09] We are invoking with a different syntax, which is System.out.
[03:13] So this can be a tricky question inside your interviews.
[03:17] So people may ask you explain me what is happening whenever I write System.out.print() or System.out.println()
[03:25] or printf() method.
[03:26] That's why let's try to spend few minutes on this and try to understand what is happening here.
[03:31] Once we understand about these Java basic output concept, then we can focus on the accepting the input
[03:38] data.
[03:38] I'm promising you both this output and input are related to each other.
[03:43] That's why first I'm trying to explain you everything about the output scenario.
[03:48] So here you can see I have a System.out.println().
[03:51] So System is a Java class which is present inside the Java dot lang package.
[03:57] If you can go to the top of the class.
[03:59] So this class belongs to the java.lang package.
[04:03] That's why we don't have to add any explicit import statement whenever we are using these System class.
[04:09] And inside the System class, we have a static variable with the name out.
[04:14] So let me open this.
[04:16] You can see this output static variable is of type PrintStream.
[04:21] So what is this static final out variable is doing inside the System class.
[04:26] So let's try to understand the same by reading the documentation.
[04:30] So if you read the documentation it says the standard output stream.
[04:34] This stream is already open and ready to accept the output data.
[04:39] Typically the stream corresponds to display output or another output destination specified by the host
[04:46] environment or the user.
[04:48] So what do they mean from these documentation is, whenever you want to print your output data onto a
[04:54] console.
[04:55] If we invoke these out to static variable, it is going to give you an object
[05:00] to PrintStream.
[05:01] So what is this PrintStream?
[05:03] PrintStream is an another class which is available inside the java.io package.
[05:09] So the purpose of this class is it is going to provide lot many utility methods to print the given data
[05:17] onto the output stream.
[05:19] For example we are trying to use print(), println().
[05:23] So all these methods are available inside this class.
[05:27] Since printing the data onto the output is very common scenario Java team
[05:32] they have provided a shortcut to create the object of PrintStream, which is by invoking the
[05:39] System.out.
[05:40] As a developer, we just have to invoke the static variable out which is present inside the System.
[05:45] So the combination of System and out it is going to give an object of PrintStream.
[05:51] When the object of PrintStream is created, it is also going to open the connection and ready to accept
[05:57] the output data.
[05:58] Which means when you start executing the program, since you are running inside an intelliJ idea,
[06:04] the PrintStream object, by the time it is trying to get created, it is going to open the connection
[06:10] with your console.
[06:11] Post that when you invoke this println() method based upon the object of PrintStream whatever data
[06:17] you are trying to provide as an input to this method, the same is going to be displayed onto the console.
[06:22] For example, if I try to execute this program, you can see I'm getting the output as 25.
[06:28] So how this is possible behind the scenes.
[06:31] When I execute this System.out, an object of PrintStream is going to be created, and during the
[06:37] same process it is going to open a connection with this console.
[06:41] And since I'm trying to invoke the println() method on top of object of PrintStream by providing an input,
[06:48] the same is going to be displayed on the output console.
[06:51] I hope you are clear about the history of System.out.println().
[06:55] So people can always try to confuse you.
[06:58] Why this System.out.println() is looking something different.
[07:01] For example, they can ask you to which class this println() method belongs to.
[07:06] You should not say it belongs to System.
[07:08] You should say it belongs to the PrintStream.
[07:10] But nowhere you are creating an object of PrintStream.
[07:13] That can be the immediate question.
[07:15] So to answer this question you should tell them System is a class and inside the System class we have
[07:21] an out static final variable of type PrintStream.
[07:25] Whenever we invoke this code, which is System.out behind the scenes, it is going to create the
[07:31] object of PrintStream and using the same object of PrintStream and going to invoke the println() method.
[07:37] If you don't have this System.out inside the Java library, every time the Java developer, they
[07:43] have to create the object of PrintStream and behind the scenes, a connection to the console has
[07:48] to be created.
[07:49] So it is going to be an expensive operation if you try to do manually.
[07:54] That's why behind the scenes Java is going to do that for you and make your life super easy.
[07:59] I hope you are clear.
[08:00] Whatever we have discussed for your quick reference, I have mentioned all the points that we have discussed
[08:06] in this slide as well.
[08:07] So whenever you have some confusion about the statement System.out.println().
[08:12] Please read this slide.
[08:13] Thank you,
[08:14] I'll catch you in the next lecture bye.

----------------------------------------
