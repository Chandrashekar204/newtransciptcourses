# 14.22 — final, finally and finalize

> Section 14: Exception handling using try, catch and finally

[00:00] Inside Java, there are three different similar jargons that you may hear a lot
[00:05] many times these are final,
[00:08] finally, finalize.
[00:09] Though they are looking very similar, but there is a lot of difference between them and the scenarios where
[00:15] we are going to use them also vary a lot.
[00:18] Since this is a topic where students can easily get confused, I want to spend a few minutes explaining
[00:24] you about the differences between final, finally and finalize, and this is also a favorite question
[00:31] for the most of the interviewers.
[00:33] That's why
[00:34] please be attentive to this lecture, and with that, any confusions that you may have around these
[00:39] jargons will get cleared.
[00:41] The very first jargon or
[00:43] the keyword that you can see here is final.
[00:45] So what is the purpose of final inside Java?
[00:47] Using final we can declare final constant values or final methods under final Java class.
[00:56] Whenever we are using this final keyword to declare a variable or to declare a constant value, such
[01:03] variables are such constants
[01:05] we can't update them, or we can't reinitialize them with a different value at later point of time
[01:11] inside the program. Whatever you are going to provide during the initialization, the same value is
[01:18] going to be final.
[01:19] For example, inside this program you can see I'm trying to declare a variable x along with the final
[01:25] keyword, and inside this x I have stored the value five.
[01:28] With that, I will not be able to update these x variable with some other value inside the program at
[01:34] later point of time.
[01:35] The compiler is not going to allow this.
[01:38] Similarly, whenever we are defining the final keyword as part of the method signature, then such methods
[01:44] behavior or the logic cannot be overrided by the subclasses.
[01:49] All the subclasses
[01:50] they have to simply accept whatever business logic defined inside the final method of a superclass.
[01:56] And at last we can also mention this final keyword as part of the class definition.
[02:01] Whenever we are mentioning the final keyword as part of the class definition, then in such scenarios,
[02:06] your class is not going to support any inheritance, no other subclass.
[02:11] they can extend your class as a superclass.
[02:14] So we are trying to completely disable the inheritance behavior with the help of final keyword inside
[02:21] the class definition.
[02:22] Now moving on to the next jargon, which is finally.
[02:25] We just now discussed inside this section where we talked about how to perform the exception handling.
[02:32] Whenever you are trying to define, try and catch blocks in such scenarios, we can define the finally
[02:38] blocks using finally keyword
[02:40] we can build the finally blocks we already discussed
[02:43] what is the purpose of finally block?
[02:45] With the help of finally block, we can specify a block of code that is going to be executed regardless
[02:51] of whether an exception is thrown or caught in the try or catch blocks.
[02:56] This finally block ensures that the code that you have written inside them, such as closing a database
[03:02] connection or releasing a lock.
[03:04] So all these kind of code, it is always going to be executed in both kind of scenarios like happy scenario
[03:11] and exception scenario.
[03:12] Now moving on to the last jargon which is finalize.
[03:16] Finalize is a method available inside the object superclass.
[03:21] We know inside Java there is a garbage collector which is responsible to clean up the object that are
[03:28] no longer being used.
[03:29] So with the help of garbage collection, the memory occupied by the unused objects inside the heap memory
[03:36] is going to be cleaned or retained regularly.
[03:39] So whenever a garbage collector is trying to remove an unused object from an heap memory.
[03:44] In such scenarios, if you want to perform any cleanup operations, or if you want to release any resources
[03:51] before the object is destroyed in such scenarios inside your class, you can override the method finalize()
[03:58] that is provided by the object superclass.
[04:02] So whatever logic that you are going to write inside this Overrided finalize() method, the same is going
[04:07] to be executed whenever the garbage collection is happening.
[04:11] But please note that JVM is not always going to invoke your finalize() method.
[04:16] It is not going to guarantee that it is always going to invoke the finalize() method that you have defined
[04:23] whenever a class object is being destroyed.
[04:25] In fact, this finalize() method is deprecated.
[04:29] Let me show you that very quickly.
[04:31] First, let me open the Object superclass.
[04:34] So this is the superclass for all the classes inside Java.
[04:38] So if you see there is a method called finalize().
[04:40] As of now it is empty.
[04:42] If needed we can override these method inside our respective Java classes.
[04:48] But these methods you can see it is deprecated from Java 9.
[04:51] And this is going to be removed in the near future permanently from the Java library.
[04:57] We can also see some documentation
[04:59] around this.
[05:00] After this deprecated you will be able to read this information.
[05:03] Finalization is deprecated and subject to removal in a future release.
[05:08] The use of finalization can lead to problems with the security, performance and reliability.
[05:13] That's why they are trying to remove these.
[05:16] For now
[05:16] they mark this method as deprecated.
[05:18] With that you may have a question.
[05:20] Then what is the alternative for these finalize() method?
[05:23] The alternative options are also highlighted here.
[05:25] Inside the documentation they clearly highlighted use java.lang.ref.Cleaner() and
[05:32] java.lang.ref.Phantom() reference as a safer ways to release resources whenever an object becomes unreachable.
[05:40] So these are the alternatives.
[05:41] But for now, let's not worry about these advanced topics or the alternative options we are right now
[05:47] try to understand what is the purpose of finalize() jargon.
[05:50] So finalize() is a method inside the Object superclass, which is going to be invoked by garbage collector
[05:58] before a specific object is going to be destroyed.
[06:00] The reason why I'm trying to explain these three important jargons are the three important topics is
[06:07] people will try to ask these kind of tricky questions inside interviews.
[06:10] I want you to be prepared for all such questions.
[06:13] That's why I spent few minutes on this.
[06:15] I hope you are clear about these three jargons, and as of now I'm thinking you don't have any confusion.
[06:22] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
