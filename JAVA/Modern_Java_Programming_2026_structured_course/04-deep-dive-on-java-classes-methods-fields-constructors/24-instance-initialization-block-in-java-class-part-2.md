# 4.24 — Instance Initialization Block in Java class - Part 2

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] In this lecture, let me answer your burning question, which is why Java provides two approaches to
[00:07] write the initialization logic for the Java objects.
[00:11] There are two reasons why Java provides two options.
[00:14] The reason why we need these instance initialization block is, inside Java
[00:19] not all Java classes are going to have constructors, and this may be surprise for you like i said.
[00:24] Let's try to understand what type of classes will not have constructors.
[00:29] The constructors will not be available for the anonymous classes that we are going to create inside
[00:36] the Java.
[00:37] Yes, you heard me correct.
[00:39] Inside Java we can create anonymous classes without any name.
[00:43] So these are very advanced and complex topic we are going to discuss in the upcoming sections.
[00:49] But for now, please note that we can create anonymous classes inside Java.
[00:53] If your class itself is not going to have any name, then how your constructor will be created because
[01:00] your constructor need the name of the class to define the definition of itself.
[01:05] That's why inside anonymous classes we can't have constructors.
[01:09] In such scenarios, we can leverage the instance initialization block to define some initialization
[01:16] logic for the objects that we are going to create for the anonymous classes.
[01:21] So these are very first reason why Java provides this option when we already have constructors
[01:27] to write the initialization logic of the objects, we are going to discuss more about anonymous classes
[01:33] in the upcoming sections, but I'm assuming this is clear to you.
[01:36] Moving on to the reason two sometimes when you try to define multiple constructors inside your Java
[01:43] class, you may have some duplicate code. Few lines of code
[01:47] you may end up writing in all the constructors.
[01:50] So instead of repeating all the code in all the constructors.
[01:54] So instead of repeating that common code inside all the constructors, you can move that duplicate code
[02:00] inside the instance block and post that
[02:03] you can delete that duplicate code inside your constructors.
[02:06] And this is one of the best practice that you can follow to avoid the unnecessary duplicate code inside
[02:13] your Java classes.
[02:15] For example, here you can see in the screenshot I have two constructors.
[02:18] One is default constructor and the second one is overloaded constructor, which accepts three parameters
[02:25] like model, color and horsePower.
[02:27] Think of a scenario
[02:28] I have a requirement to print a statement saying that Car object is being created whenever an object
[02:35] of Car is getting created.
[02:37] If I don't have this instance initialization block, I need to write this System.out.println()
[02:42] in both the constructors
[02:44] Whereas with the help of instance initialization block, I can write the System.out.println()
[02:50] only once.
[02:51] Anyway, during the object creation, my instance initialization block is going to be executed regardless
[02:58] of which constructor I am going to use to create the object.
[03:00] That's why the output should be same and the behavior should be same.
[03:05] Even if you move that duplicate code to the instance initialization block, I can show you this with
[03:10] the help of a demo.
[03:11] For example, inside the Car.java.
[03:13] As of now we have only the instance initialization block.
[03:17] So let me create an default constructor.
[03:20] The default constructor is going to be public Car, and it is not going to accept any input parameters
[03:27] inside these public Car
[03:29] I'm going to define the statement which is System.out.println().
[03:33] After this default constructor, I'm going to create one more constructor, which is going to accept
[03:40] three input parameters.
[03:41] The very first one is going to be the model.
[03:44] And after the model I'm going to mention color.
[03:48] And after the color I'm going to mention horsePower.
[03:51] Inside this constructor body I'm going to define this.model = model, which I have received
[03:59] as part of these input parameters.
[04:01] And after the model I can do similar assignment for color and horsePower.
[04:06] So here I will do the horsePower first, because I want to show you that the order of variable assignment
[04:14] does not matter.
[04:15] You don't have to follow the same order like model, color horsePower.
[04:19] You can move these horsePower first and you can bring the model to the end.
[04:23] It's perfectly fine as long as you are assigning the correct input to arguments to the correct object
[04:29] to fields, you should be fine.
[04:31] This time
[04:31] let me try to do the assignment for color.
[04:34] After this color you can see I have an System.out.println().
[04:38] So as of now I have two constructors and this is the duplicate code which I have inside both of the
[04:44] constructors.
[04:44] Now first let me remove my instance initialization block and show me what is going to happen.
[04:49] I'll go to the CarMain and here I'm trying to create two objects.
[04:54] First one I'll try to create with the help of default constructor, whereas the second object I will
[04:59] try to create with
[05:00] the help of overloaded constructor that we have created.
[05:03] The first argument I need to mention the Camry, which is a model of the class, followed by black,
[05:09] which is the color of the Car, followed by 200, which is the horsePower.
[05:13] If I try to execute this, we are going to get this output, which is car object is being created two
[05:19] times because we are creating two different objects with two different types of constructors.
[05:25] Now let's see what is the advantage that we are going to get with the instance initialization block.
[05:30] For the same, let me create an instance initialization block.
[05:33] I'll try to move the System.out.println() statement from the constructors to the instance initialization
[05:41] block.
[05:41] And with that I can delete these duplicate code that we have inside the constructors.
[05:47] Here I'm just trying to show you with a simple System.out.println().
[05:51] In real projects you may have lots of duplicate code which may get repeated inside your constructors.
[05:57] So in such scenarios this instance initialization block is going to be a savior for you.
[06:03] Now let me try to execute this car main program using this run button.
[06:08] And you can see we are getting the same output and the behavior is also going to be the same.
[06:13] I hope you are clear.
[06:14] What is the purpose of instance initialization block?
[06:17] But in real projects you will see this instance initialization block very rarely because most of the
[06:24] times we create normal classes, but not the anonymous classes.
[06:29] Developers will use these instance initialization block only in the scenarios where the anonymous class
[06:35] is being created or in the scenarios where a particular duplicate code is being repeated across all
[06:42] constructors.
[06:43] I hope this makes sense to you.
[06:45] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
