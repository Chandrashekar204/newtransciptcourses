# 4.23 — Instance Initialization Block in Java class - Part 1

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Few lectures back when we were discussing about what is a Java class, I said Java will contain components
[00:06] like fields, methods, constructors, instance initializers, and static initializers.
[00:13] As of now, we discussed about what are Java methods?
[00:16] What are constructors?
[00:17] As a next step, we need to understand what are these instance initializers and static initializers
[00:23] that we can define inside a Java class.
[00:27] Inside this lecture, let's focus on instance initializers.
[00:31] In Java instance initialization block is a block of code which we can write within a Java class that
[00:38] is going to be executed each time an instance of the class or
[00:43] the object of the class is getting created.
[00:45] The primary purpose of the instance initialization block is to initialize the instance variables of
[00:51] an object, and this block is particularly useful when we want to perform some initialization logic
[00:57] for each object of a class.
[00:59] And here you have a burning question we discussed just now about constructor.
[01:04] Constructor also is playing the same role.
[01:06] With the help of constructor, we can define some initialization logic for the objects.
[01:11] Then why
[01:12] java is given another approach to initialize my Java variables and to initialize some tasks during the
[01:19] object creation.
[01:20] I'll answer that question in few minutes.
[01:22] For now, let's focus on how to define these instance initialization block.
[01:27] We can define this block within a class, but outside of the methods or constructor.
[01:32] We should not write this instance initialization block inside Java methods or inside the constructor.
[01:38] We should develop these blocks inside the Java class.
[01:41] But outside of that Java methods and Java constructor.
[01:44] And the very important point that you need to be aware about this instance initialization block
[01:50] is there not going to have any name.
[01:52] We just have to mention the open curly brace and closing curly brace.
[01:56] And within the braces we need to write the logic that we want to be executed as part of this instance
[02:03] initialization block.
[02:05] Let me show you a sample.
[02:06] This time I have taken the car class that we have.
[02:09] Inside the Car class we have three Java fields with the name, model, color and horsePower.
[02:14] Just before the Java fields you can see I have defined an instance initialization block with the help
[02:21] of opening and closing curly braces, and my block does not have any name. Inside these curly braces
[02:27] I have written some code to initialize the fields of my object during the object creation, so I'm going
[02:34] to populate the value of model, color and horsepower values with the help of these instance initialization
[02:41] block.
[02:41] So whatever we have written inside this block, it is going to be executed whenever an object or whenever
[02:47] an instance of the class is getting created.
[02:50] If needed, you can define multiple instance initialization blocks within the same class, and these
[02:58] multiple initialization blocks are going to be executed in the same order in which they appear in the
[03:05] class definition.
[03:06] For example, I can define the two initialization blocks like you can see on the right hand side.
[03:12] So in the very first initialization block I'm trying to define the values for the fields of model and
[03:18] color.
[03:18] Whereas in the second initialization block I'm trying to assign a value for the Java field horsePower.
[03:25] And just like how inside constructors return statement is not allowed very similarly inside the instance
[03:32] initializers also the return statement is not allowed.
[03:36] Can we see this instance initialization block in the demo for the same
[03:40] let's go to the intelliJ and open the Car class inside my IntelliJ
[03:44] I'm going to close my existing classes related to Employee and EmployeeMain, and this time I'm going
[03:51] to open the Car class that we have defined previously.
[03:54] Inside these Car class I'm going to create an instance initialization block for the same
[04:01] I'm going to mention open curly brace and closing curly brace.
[04:05] And inside this block I'm going to define the logic which is this.model is equal to camry is the
[04:12] model that I want to define.
[04:14] After the model I'm going to assign the value for the Java field, which is color.
[04:19] The color that I want to assign here is black.
[04:22] After the color I'm going to mention horsePower value with the help of this.horsepower is equal
[04:29] to, and I'll mention the horsepower value as 200.
[04:32] With this, every time I try to create an object of Car class, this instance initialization block is
[04:39] going to be executed.
[04:40] I can also keep a breakpoint so that we can see this in action.
[04:44] As of now, you can see my Car class does not have any constructors defined behind the scenes
[04:50] my Java compiler will create that default constructor, but let's not focus on the constructors right
[04:56] now.
[04:57] We can simply focus on these instance
[04:59] initialization block.
[05:00] So to create the object of this Car class, I'm going to create a another Java class.
[05:07] The Java class name is going to be CarMain.
[05:11] Once this class is created inside this class, I'm going to first define the main() method with the shortcut
[05:17] psvm.
[05:18] So here I'll try to create two objects of Car to create the Car object
[05:23] first I need to mention the class name which is Car and post that I will mention the variable as car1
[05:29] is equal to new keyword, followed by
[05:32] I'm going to invoke the default constructor because we don't have any other overloaded constructor.
[05:39] After this, I'm going to create one more object with the name car2.
[05:43] When I try to create these two objects, my instance block will be executed, and for the both objects,
[05:49] we are going to assign the same values like Camry, black and 200.
[05:54] Let me save this file and run this program in a debug mode.
[05:58] As soon as I click on this debug option, you can see the breakpoint stopped inside my instance initialization
[06:07] block.
[06:07] And the breakpoint is going to stop two times because we are trying to create two different objects.
[06:12] So let me release this breakpoint and this time you can see the breakpoint stopped again.
[06:18] Let me release this breakpoint and you can see that the program execution is completed.
[06:23] We're not getting any output because we didn't print anything here.
[06:27] Maybe what I can do is I can try to mention System.out.println() l and inside the
[06:34] System.out.println().
[06:36] I will try to print a statement which is Car object is being created.
[06:43] This time we should be able to see the statement in the output console two times.
[06:48] So let me go to CarMain.java and execute this program in the debug mode and release the breakpoints
[06:55] two times.
[06:56] And you can see the statement is getting displayed two times.
[06:59] So this confirms our instance initialization block is being executed
[07:05] every time we try to create the object of the given class.
[07:09] I hope you are clear about the purpose of instance initialization block and how to define it.
[07:14] But you may have a burning question, which is why Java provides two options to initialize the objects
[07:21] one with the help of constructors, and the other one with the help of instance initialization block.
[07:27] Let's try to understand more about this in the next lecture.
[07:31] Thank you.
[07:32] Bye.

----------------------------------------
