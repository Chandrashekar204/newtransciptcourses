# 4.33 — Static Initialization Block in Java class - Part 2

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture,
[00:01] let's see the demo of static initialization block to demo you the same
[00:05] first I'm going to create a static variable for the same
[00:09] first we need to mention static followed by byte and I'll keep the variable name as numberOfEngines.
[00:17] I want to store
[00:18] number of engines an car can hold.
[00:21] We know regardless of what are the type of car, a car is always going to have a single engine.
[00:26] That's why I'm trying to create this variable as static, because regardless of how many objects we
[00:33] can create with the help of this Car class, the number of engines is going to be same for all the objects.
[00:38] But I'm not going to initialize here.
[00:41] I just want to declare here the initialization part
[00:44] I want to take care with the help of static initialization block.
[00:48] And since this is not a constant field and I did not use a final keyword, I have used the normal camel
[00:55] case style to name the variable.
[00:57] Now let me define a static initialization block for the same
[01:01] first I need to mention static and post that opening and closing curly braces.
[01:07] Inside the static initialization block, I can access the static variables like numberOfEngines,
[01:14] and I'm going to mention the value which is 1.
[01:18] And after that I'm also going to mention System.out.println(), and to this println() method
[01:24] I'm going to mention a statement saying that static block is being executed.
[01:30] So whenever this block is executed we're going to get this output.
[01:34] Now let me show you some negative scenarios like we discussed previously inside the static block
[01:39] we cannot use the ' this ' keyword.
[01:41] This is completely invalid.
[01:43] And very similarly we cannot access the instance fields like I cannot access the color variable.
[01:51] You can see I'm getting a compilation error.
[01:54] And apart from this limitations return statement is also not allowed inside the static block.
[01:59] So these are the limitations.
[02:01] I hope you are clear about these limitations.
[02:03] Now as a next step, I'll go to the CarMain class.
[02:07] As of now, you can see we're trying to create a two objects of the Car class.
[02:11] That means whatever statement that we have inside the instance block, this is going to be printed two
[02:16] times.
[02:17] But this statement which you have mentioned inside the static block, is going to be executed only once.
[02:23] That will give a confirmation to us all.
[02:25] This static variable is going to be executed only once.
[02:29] So let me go to the CarMain and here, instead of the numberOfWheels, I'm going to access the field,
[02:34] which is numberOfEngines, to make sure whether the initialization is completed or not inside the
[02:40] static block.
[02:41] And just before this objects creation, I want to mention a System.out.println() with a statement
[02:47] saying that main() method invocation started.
[02:52] There is a reason why I'm trying to print this statement.
[02:54] I'm going to explain you what is the reason while I'm trying to run this Java class.
[02:59] So I think I have made all the required changes.
[03:02] Let me save this changes and run the Java class.
[03:05] So the very first statement that I'm seeing here is main() method invocation started.
[03:10] But previously I said the static block is going to be executed before the main() method.
[03:15] Then in that case, why we are seeing the static block is being executed after the main() method invocation
[03:22] started.
[03:22] This is because the static block is present in a different class, which is Car.
[03:27] So when these Car class is being loaded in that scenario, only the static block is going to be executed.
[03:34] So when this class is going to be loaded in the scenarios when we try to create the object of the class,
[03:40] what I can do here is I can try to create a static block inside the same class.
[03:45] And inside this static block I can mention System.out.println() with the statement saying that
[03:52] static block from the same class.
[03:55] This statement is going to be executed just before this statement.
[04:00] Let me show you that in the demo as well.
[04:02] For the same, let me run this program.
[04:04] You can see this time
[04:05] first I'm getting the output which is static block from the same class followed by main() method invocation
[04:11] started.
[04:12] So this confirms always your static block, which is present in the same class is going to be executed
[04:18] just before the main() method.
[04:20] So if someone asks you in the interview, can I execute a piece of code before the main() method?
[04:26] In such scenarios you can tell yes, we can do that with the help of static block.
[04:30] And after these two statements, we are trying to create the object of the Car class.
[04:35] At this point of time, the Car class will be loaded into the JVM memory.
[04:40] That's why we're able to see these static block is being executed and post that
[04:45] we are seeing the two statements from the instance block, which is Car object is being created two
[04:51] times, so the object is getting created two times.
[04:54] We are seeing the statement from the static block is being displayed only once.
[04:58] This confirms,
[04:59] regardless of how many objects you're trying to create, your static block is going to be executed only
[05:05] once during the loading of the class into the JVM memory, and at last we can also see the numberOfEngines
[05:11] value, which is one.
[05:13] This confirms whatever code we have written here
[05:16] to assign the value, one is executed and it is working fine.
[05:20] Now let me show you a tricky question that you may face inside the interviews.
[05:23] Some people, they may give a Java program with a static block and the main block, inside the static
[05:29] block, they're going to mention a Java statement, which is System.exit().
[05:35] And to this exit they're going to mention some int value like 0 or -1, regardless of whatever value
[05:42] that they're trying to mention
[05:44] for the exit method, they're going to ask you what will happen in this scenario, will the main() method
[05:49] will be executed or not?
[05:51] So the answer for this question is the main() method will never be invoked.
[05:55] Because when we try to run this program first the static block is going to be executed. In the static
[06:02] block,
[06:02] we are trying to terminate the program with the help of System.exit().
[06:07] So System is a class inside the Java library.
[06:10] And there is an exit() method inside this class.
[06:14] To open this exit() method you can press command button inside mac or control button inside Windows post
[06:22] that you'll be able to see a hyperlink.
[06:24] Please click on this and you'll be taken to the exit() method available inside the System.java.
[06:30] So this is a Java class available inside the Java library.
[06:34] So this is a static method
[06:35] that's why we're able to invoke the static method with the help of Java class name.
[06:40] The logic that we have inside this method is, we're simply trying to get the runtime, and we're trying
[06:45] to kill it with the help of this exit() method.
[06:48] Let me close this class
[06:49] I can also show you this in the demo.
[06:51] So let me try to execute this program.
[06:54] And if I keep a breakpoint here, the breakpoint will never stop because always the program is going
[07:00] to be killed at this point.
[07:02] That's why we were able to see only this statement, which is static block from the same class.
[07:06] Always zero indicates we are trying to terminate the program gracefully, but if you want to terminate
[07:12] the program indicating an error, then you can always use -1.
[07:17] So let's see what is going to happen.
[07:19] If we use -1 this time you can see we are getting a different exit code.
[07:24] This represents that we are trying to terminate our program due to some error.
[07:29] So if you want to terminate your program gracefully or peacefully, you should use zero
[07:35] otherwise -1 you can use.
[07:37] I hope you are clear about this tricky scenario.
[07:40] I'm going to remove this code so that it is not going to create any issues when you try to run this
[07:46] program.
[07:46] I just wanted to give a quick information about that tricky scenario, which we talked about with this
[07:52] I'm assuming your super clear about static block.
[07:55] Always please make a note that whenever we say static that is applicable for the class level but not
[08:03] the object level, it can be a static variable,
[08:06] it can be a static block,
[08:07] it can be a static method, regardless of whether it is a field or method or a block,
[08:12] static means it always applicable to class level but not the object, whereas non-static fields,
[08:19] non-static methods, non-static blocks.
[08:21] They are always applicable for the objects that we are going to create.
[08:25] I hope this makes sense to you.
[08:27] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
