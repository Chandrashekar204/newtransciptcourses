# 4.39 — Object Destruction and Garbage collection in Java

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now, we discussed about how to create the objects inside Java.
[00:05] So what is the approach to create objects inside Java?
[00:08] With the help of the new operator and the constructor of the Java classes, we can create any number
[00:14] of objects.
[00:15] So creating of the objects with the help of Java class,
[00:18] in other words, we can call it as object construction.
[00:21] Inside this lecture let's try to discuss about object destruction.
[00:25] Because inside interviews, people may ask you how to destroy an object or how to remove an object inside
[00:32] Java.
[00:33] In Java, there is no need of destroying the object or removing the object.
[00:38] People can try to confuse you by asking questions like how can I destroy or remove or destruct the object
[00:45] inside Java?
[00:46] So please let them know that there is no such concept, and there is no need for the Java developers
[00:51] to manually delete or remove the objects.
[00:54] If you worked on the languages like C or C++, inside these languages, it is the developer responsibility
[01:00] to destroy the object to clean up the memory.
[01:03] Otherwise, the program which is written with the help of C or C++ it is going to have some
[01:09] memory leaks and eventually the memory execution will fail.
[01:12] But Java is different.
[01:14] You don't have to stress about manually getting rid of things that you have created like objects, because
[01:20] inside Java we have Garbage collector.
[01:23] So behind the scenes there is a process that is going to run continuously, which is going to keep an
[01:29] eye on all the objects and things that you are trying to create.
[01:32] If this Garbage collector identifies that a particular object is no more going to be used in such scenarios,
[01:39] the Garbage collection is going to free up the memory that is occupied by the particular object by deleting
[01:45] it.
[01:45] So with the help of Garbage collection in Java, the developers, they never have to worry about destroying
[01:50] the objects.
[01:51] They can always focus on the creating the objects and building the business logic.
[01:56] The memory management inside Java is going to be taken care by the JVM automatically, with the components
[02:03] like Garbage collection. Behind the scenes, this Garbage collection, they are going to follow some
[02:08] algorithms to identify the unused objects.
[02:12] If we talk about the old JVM's, which Java used to use a decade back, they used to follow an algorithm
[02:19] with the name mark and sweep.
[02:21] By using these algorithm, the Garbage collector process which is going to run behind the scenes, it
[02:27] is going to mark all the objects that were still being used by the JVM.
[02:32] With that, whatever objects which are not marked, the JVM is going to sweep them away and free up
[02:39] the space.
[02:40] But this approach has some issues, like JVM used to take some passes in between the cleanup of the
[02:47] objects.
[02:47] That's why sometimes the cleaning up the objects is going to take more time, because regularly JVM
[02:53] is taking a pass to overcome this disadvantage
[02:56] in the latest JVM's that are introduced in the latest versions of the Java new Kind of Modern Garbage
[03:03] collectors are introduced, which are smarter, and they can work continuously without causing any delays.
[03:10] These modern Garbage collectors, they are going to divide the memory into multiple sections.
[03:16] For example, they can keep all short lived objects separately in a quicker cleanup area compared to
[03:23] long lived objects.
[03:25] So these are with the help of modern Garbage collectors
[03:28] nowadays, Java and JVM is doing a great job in terms of object destruction and the memory management
[03:35] at runtime.
[03:36] Sometimes you may end up in a scenario where you want to manually tell to the Garbage collection process
[03:43] to initiate the cleanup as soon as possible.
[03:46] In such scenarios, you can manually initiate this process of cleanup or tell to your JVM to speed up
[03:53] this process by invoking a static method available inside the System class.
[03:58] So what is this method?
[04:00] GC means Garbage Collector.
[04:02] If you try to invoke this gc() method inside System class, it is going to give a nudge to your Java JVM
[04:08] to clean up the Garbage collection process.
[04:11] But please note that it is not a guarantee that your JVM or Java are your Garbage collection always
[04:18] going to listen for you?
[04:19] It is going to be completely random.
[04:21] Sometimes it is going to simply ignore it if it has some other priorities.
[04:25] Let me show you this Garbage collection invocation manually in the inter-league as well.
[04:30] You can go to any of the classes that we have created, and inside any of the methods, you can simply
[04:36] invoke the class with the name System.
[04:39] After this class name you can mention dot operator followed by gc().
[04:45] gc means Garbage Collector.
[04:47] This is a static method.
[04:48] That's why I'm able to invoke it without creating the object of System class.
[04:53] If I go inside the documentation of this GC method by hovering on this method, you can see I'm getting
[04:59] a hyper
[04:59] link because I'm holding the command button inside my mac system.
[05:04] Whereas inside the windows operating system, you need to hold the control button and hover your mouse
[05:10] onto this gc() method.
[05:11] And with that, you'll be able to see a hyperlink.
[05:14] If I click on this hyperlink, I'll be taken to the System.java class, which is available inside
[05:20] the libraries of the Java.
[05:22] You can also see that documentation of this method which is mentioned
[05:26] on top of this method.
[05:28] There are details about this method.
[05:30] What is going to happen when we call this method?
[05:33] Inside these commands, they clearly highlighted.
[05:35] There is no guarantee that this effort will recycle any particular number of unused objects.
[05:41] That's why
[05:42] please make a note that System.gc() always will not trigger the Garbage collection process.
[05:49] Sometimes if your JVM has other priorities, it can simply ignore your request.
[05:55] This point is going to be a very important question for the interviews inside the interviews, they
[06:00] can ask you about what is Garbage collection, and once you answer about the Garbage collection, they
[06:05] can also ask you how to invoke the Garbage collection process manually.
[06:10] But this question you can answer by simply saying that with the help of System.gc()method, I can
[06:17] invoke the process of Garbage collection manually, but there is no guarantee that my JVM or Java is
[06:23] going to accept my request.
[06:26] I hope you are clear about object destruction in Java.
[06:29] In simple words, there is no need of object destruction inside Java, and the Garbage collector is
[06:35] going to take care of it.
[06:37] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
