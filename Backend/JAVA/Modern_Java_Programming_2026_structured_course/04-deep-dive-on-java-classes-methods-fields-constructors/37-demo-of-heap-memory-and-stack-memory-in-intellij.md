# 4.37 — Demo of Heap memory and stack memory in IntelliJ

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] In this lecture, I want to show you a demo of Heap memory and Stack memory with the help of intelliJ.
[00:07] For the same, I came to the class CarMain.
[00:09] Inside this CarMain class, we're trying to create two objects like car1 and car2.
[00:15] Let me try to keep a breakpoint at the line number one inside the method
[00:19] and at the last line after putting these breakpoint, I'm going to click on this debug option.
[00:25] And the breakpoint is going to stop at the very first line, because I have put a breakpoint at line
[00:31] number eight. To see the Heap memory inside your debug window,
[00:35] so this is a debug window.
[00:36] If you're not able to see this debug window you can click on this debug icon.
[00:41] You will be able to see this if you try to click on this.
[00:44] If you're not able to see this debug icon you can go to View, Tool Windows and there is a Debug option
[00:50] please select that.
[00:51] And with that you should be able to see this icon. Inside this debug window on the right hand side you
[00:57] can see there is a layout settings.
[00:59] You can click on this layout settings inside the layout settings,
[01:03] as of now you can see the memory related option is not selected.
[01:07] Let me select that and post that
[01:10] you'll be able to see a tick mark against that
[01:13] and along with that, you'll be able to see a new menu here.
[01:16] As of now, you can see there is no class loaded because by default the memory details will not be loaded.
[01:23] As a developer, I need to click on these load classes.
[01:27] This will load the classes based upon the execution right now happening inside my Java program.
[01:34] And you can see these are all the objects right now created inside my memory.
[01:39] So behind the scenes when we try to run a main() method, there are a lot of libraries and Java classes,
[01:45] java methods and variables, objects.
[01:48] They are going to play various roles to initiate the program execution, but we are more interested
[01:55] about the object which is created with the help of Car class.
[01:58] That's why I'm going to search here with the name Car.
[02:01] And you can see there are no objects right now which are created with the help of Car class, because
[02:07] right now we are at the line number one only.
[02:10] At this point of time we have not created any object.
[02:14] Let me try to click on this step over, which will take me to the next line.
[02:18] And I'm going to click on Load Classes one more time
[02:21] this time you can see the object is not at created because this line 9 is yet to execute.
[02:27] If I try to click on this step over this time, if you click on this Load classes, you will be able
[02:33] to see a Car class and the count as one.
[02:37] That means one object is created which is related to this class, and under the difference you will
[02:43] be able to see plus one.
[02:45] This means compared to the previous line of code, one object is created which is related to the Car
[02:52] class.
[02:53] Let me try to execute the next line as well by clicking on this step over.
[02:57] Right now my breakpoint is at the last line.
[03:00] If I try to click on this Load classes this time, you should be able to see there are two objects and
[03:07] compared to the last line, one more object of Car class is created.
[03:11] So if you try to click on these, you can see a new window which will show you all the objects related
[03:17] to a particular class.
[03:18] You can also see at which line this object is created inside the main() method, which is present inside
[03:24] the CarMain
[03:25] class
[03:26] it is created at the line number ten.
[03:28] This way we can also see that details where the particular object is created.
[03:32] You can also open these objects and see what kind of data is available inside these objects, which
[03:39] are present inside the Heap memory.
[03:41] I hope you are clear.
[03:42] Most of the times you don't have to deep dive into the Heap memory, but if you are receiving some memory
[03:47] related errors like memory leak or out of memory in such scenarios, you will be advised to debug your
[03:54] code to understand where the more number of objects are getting created.
[03:59] So in such scenarios, you need to come to this memory window and you need to debug to understand where
[04:05] the unnecessary objects are getting created.
[04:08] And accordingly you need to fix your program.
[04:10] So this is the demo of Heap memory. Coming to the stack memory,
[04:15] it is very simple.
[04:16] We already saw the Stack memory demo previously.
[04:18] Before I show you the Stack memory demo, let me go to the layout settings and uncheck this memory because
[04:25] I no more wanted that.
[04:27] If you see under the debugger window, you will be able to see all the methods that are executed inside
[04:33] your Java class.
[04:34] As of now, we have only main() method inside the Java class.
[04:37] That's why we're able to see a single entry inside the method stack and the stack reference
[04:44] you should be able to see what are all the objects and variables that are going to be tracked by your
[04:50] Stack memory.
[04:51] So here we have only one method.
[04:53] That's why it might be not super clear for you.
[04:56] Let me resume this program and let me go to the method invocation
[05:00] demo.
[05:00] Here we have many methods.
[05:01] If I try to run this class by keeping a breakpoint inside, the method4(), you will be able to see
[05:07] the Stack memory very clearly.
[05:10] So right now the debug point stopped inside the main() method.
[05:13] Let me release this by clicking on this resume program.
[05:16] And with that the execution is going to stop inside the method4() where we have the next breakpoint.
[05:22] This time you can see you will be able to see all the stack entries.
[05:25] So is the Stack memory.
[05:27] We have an entry for main() method,
[05:29] method1(),
[05:29] method2().
[05:30] method3(),
[05:31] method4().
[05:31] When I tried to select a particular method on the right hand side window, the variable details and
[05:37] the object details are getting changed.
[05:39] That means whatever we are able to see on the right hand side that is specific to a particular stack
[05:45] inside the Stack memory.
[05:46] When a particular method execution is completed, then the stack entry for that method is going to be
[05:51] removed from the Stack memory.
[05:53] With this, I'm assuming you are super clear about the Stack memory and the Heap memory in Java.
[06:00] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
