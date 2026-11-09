# 15.11 — Deep dive on finalize() in Object class

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] We talked briefly about the finalized() method in the previous section when we were trying to compare
[00:05] with the final keyword and the finally block.
[00:08] But now let's try to discuss in detail about the purpose of this finalized() method.
[00:14] In Java, it is very normal that an Java object.
[00:17] Sometimes it may consume some resources, or it may open some connection with resources like files or
[00:24] a database.
[00:24] So in all these kind of scenarios, whenever an object is trying to consume a resource, it is always
[00:30] a good practice to release these resources whenever it is no longer needed by your object to achieve
[00:36] the same.
[00:37] The Java language offers a mechanism to perform the cleanup or resource releasing just before the object
[00:44] is destroyed or discarded by the garbage collector.
[00:48] We know inside Java, we as a Java developers, we are only allowed to create the objects and there
[00:54] is no need of manually destroying the objects or destructing the objects inside the heap
[00:59] memory.
[00:59] We are not allowed to do that because behind the scenes, the Java virtual machine, it is going to
[01:04] employ a low priority process known as garbage collector to identify and eliminate all the objects that
[01:12] are no longer needed.
[01:14] So whenever an object is being destroyed or removed by your garbage collector, it is going to give
[01:20] an opportunity to execute some cleanup code in the form of finalize() method.
[01:26] The purpose of the finalize() method is whatever logic that you are going to write
[01:30] Inside these finalize() method, the same is going to be executed by the garbage collector.
[01:36] Just before your current object is going to be destroyed.
[01:39] You can see by default the finalize() method in the object class does not going to do anything, it is
[01:45] an empty method.
[01:47] If needed, we can override this method based upon our business logic inside our class.
[01:52] But there is a caveat or important note that you need to be aware, which is the garbage collector does
[01:57] not guarantee that it is going to invoke the finalize() method.
[02:01] Whenever the object destroying is going to happen, it is going to invoke your finalize() method randomly
[02:07] based upon its own calculations.
[02:09] That means this makes using this approach as undependable or unpredictable for programmers to write
[02:17] cleanup logic.
[02:18] That's why since this method has all these limitations, and it is also not advisable to use this method
[02:25] to clean up the resource due to security reasons.
[02:27] With all these reasons and limitations, this finalize() method is deprecated from Java 9.
[02:34] That means the Java team itself is encouraging not to use this method to clean up the object related
[02:41] resources.
[02:42] Instead, there are better alternatives or better approaches that we have.
[02:47] Like we discussed previously, there is a try with resource or you can write a try with the finally
[02:52] block, which is going to automatically close the resources or the connections that a specific object
[02:59] has opened.
[03:00] I hope you are clear with these initial theory discussion around the finalize() method.
[03:04] Now let me show you a small demo around this method.
[03:08] First, inside the object superclass you can see by default the finalize() method
[03:13] it is going to have empty logic.
[03:15] That's why we are seeing the empty curly braces without any method body.
[03:20] On top of that you can see there is an annotation on top of this method which is at symbol followed
[03:25] by deprecated.
[03:26] So whenever someone is mentioning this annotation on top of a method, or on top of field, or on top
[03:32] of a class that conveys that these method is not recommended to use and it is going to be removed in
[03:40] the future
[03:41] releases.
[03:41] To this deprecated annotation.
[03:43] We also have other kind of details, like from which version.
[03:46] This method is deprecated, so it is deprecated from that Java 9 version.
[03:51] That's why we have this since as nine.
[03:53] And at the same time we also have other information which is for removal is equal to true.
[03:58] That means in future this method is going to be removed by the Java team.
[04:04] That's why it is not recommended to use these inside your Java program.
[04:08] On top of that, we also have a limitation which is garbage
[04:11] collector is not going to guarantee you that it is going to invoke this method all the times, whenever
[04:18] it is trying to destroy a given object.
[04:20] I can also show you a quick demo around this.
[04:23] For the same, I'm going to create a new Java class.
[04:26] The class name is FinalizeDemo inside this class
[04:31] first, let me try to create the main() method.
[04:34] Post that
[04:35] inside this main() method I'm going to write a for loop, which is going to be executed 10,000 times because
[04:42] I'm trying to mention I < 10,000 was that I'm going to increment i++ inside this
[04:50] for loop, I'm simply going to create the object of Person with the help of new operator.
[04:57] So as soon as the current iteration completes.
[05:00] Whatever object is created within the current iteration, it is going to be eligible for destroying
[05:07] by the garbage collector.
[05:08] So whenever the destoying is happening, my garbage collector is supposed to invoke the finalize() method
[05:13] that I'm going to override.
[05:15] But like I said, it is not going to do all the times randomly.
[05:19] It is going to do that.
[05:20] As a next step, I can go to the Person class and inside this Person class, I can try to override these
[05:26] finalize() method by copying the same code.
[05:29] But on top of that I can mention the override annotation, and inside this finalize() method I am going
[05:36] to simply have a System.out.println() which is object is being destroyed.
[05:44] So whenever my garbage collector is invoking this method to clean up the resources, I am going to have
[05:50] this statement to be printed on the console.
[05:52] We are getting a error here because this is marked as deprecated, but still we are trying to use it.
[05:58] That's why IntelliJ is trying to throw an error here.
[06:02] But this is a error which is reported by the intelliJ.
[06:06] But still we should be able to run our programs because inside Java language using the deprecated methods
[06:13] is not going to halt your program.
[06:15] According to Java programming language, it is a warning, but IntelliJ is trying to make it more severe
[06:21] by showing it as an error.
[06:23] Before I try to run this FinalizedDemo method, I'm going to have a System.out.println() statement,
[06:29] which is going to print the current index value of the for loop.
[06:33] So if I try to execute this program, let's see if we are going to get at least one time the statement
[06:39] that we have written inside the finalize() method, you can see we have not received even one time the
[06:46] output that we have written inside the finalize() method.
[06:49] This is because my system has enough memory to create 10,000 objects.
[06:54] That's why Garbage Collector might have not destroyed my objects immediately, or it might have destroyed,
[07:00] but it didn't bother to invoke the finalize() method.
[07:04] Maybe what we can do is we can put a breakpoint here and try to increase this number to one lakh.
[07:10] So I'm trying to make this as 100 k this time
[07:13] also, my breakpoint didn't stop.
[07:15] That means my finalize ()method never invoked.
[07:18] Let's try to increase this number to 1 million or 10 lakhs.
[07:22] Let's hope this time at least finalize() method is going to be invoked.
[07:26] Hurray!
[07:27] The finalize() method is invoked.
[07:28] That's why the breakpoint stopped here.
[07:30] So let me remove this breakpoint and release my program.
[07:34] You can see my for loop executed total 1 million times, but it is invoke the finalize() method randomly
[07:42] at only few places.
[07:44] Maybe I can show you where it has invoked.
[07:46] You can see at this point of time it has invoked.
[07:50] So this confirms the finalize() is going to be invoked randomly for only for few objects.
[07:57] And due to this unpredictable behavior of the garbage collector, it is not recommended to use this
[08:05] finalize() method to clean up the resources of your object.
[08:09] Instead, always use try with resources and try finally block.
[08:14] I hope you are clear.
[08:15] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
