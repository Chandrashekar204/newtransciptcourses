# 4.35 — Where does Java store classes, objects, variables, methods

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now we are trying to create lot many Java classes, Java objects, Java fields, Java methods.
[00:06] We are creating lot of code.
[00:08] But do you know where all these classes, objects, variables, methods are going to be stored inside
[00:15] our system?
[00:16] Let's try to answer the same question inside this lecture.
[00:19] We as humans, we store the information and we try to process the information with the help of our brains.
[00:27] Very similarly, when you write some business logic with the help of Java classes, objects, variables
[00:32] and methods, JVM is going to handle the memory management.
[00:37] So JVM is like our brain.
[00:39] It is responsible for allocating and deallocating memory for the Java programs.
[00:45] When we try to run a Java program at runtime, JVM is going to create various types of memory in each
[00:52] of the memory
[00:53] it is going to hold different kinds of data.
[00:55] So let's try to understand what are the important types of memories that are going to be created by
[01:01] the JVM.
[01:02] The very first important memory is heap memory.
[01:05] So what is the purpose of heap memory?
[01:07] Inside this area of memory, only the objects are going to be allocated.
[01:12] That means whenever an object is created, a space for the object is going to be assigned inside the
[01:18] heap memory to store its data.
[01:21] And whenever the object is reclaimed, that means whenever we are done with a particular object, the
[01:26] space occupied by that object is going to be reclaimed by the jvm's " Garbage collector ".
[01:33] Behind the scenes, when we try to run a Java program, a process called Garbage collector is going
[01:39] to run continuously, and the job of this Garbage collector is to free up the memory by deleting the
[01:45] object, which we are no longer being used.
[01:48] How JVM knows if I am not using a particular object or not, it is going to scan the execution of the
[01:54] program continuously.
[01:56] For example, in the previous lecture we created so many methods like method1(), method2(), method3() and
[02:01] method4().
[02:02] As of now, you can see I'm trying to create an object inside the main() method.
[02:07] If I try to create the same object inside the method4(), then these variable or
[02:13] these
[02:13] object reference is going to be localized for this method only. You can see the same variable name demo
[02:20] object and creating both in method4() and main() method.
[02:23] But the compiler is not complaining anything because both of these variables are present in a different
[02:29] scope, which are different methods in this case.
[02:32] But if you try to create another object with the same name inside the same method, you will get an
[02:37] error saying that variable demo object is already defined in the scope.
[02:41] So what is the scope here?
[02:42] Whatever we write inside
[02:44] the curly braces of a method is going to be considered as a local scope for a given method.
[02:50] That's why creating the objects or
[02:52] creating variables with the same name is not allowed within the local scope.
[02:57] Now coming to the Garbage collection discussion, you can see as of now I have created a object inside
[03:02] the method4().
[03:03] As soon as I'm done with the method4() execution, the control will go back to the method3().
[03:09] At that point of time, my Garbage collector know that this demo object is no more used and it is an
[03:16] unused object.
[03:17] That's why behind the scenes it is going to delete these objects, and with that, it is going to free
[03:23] up the heap space for the future objects that we are going to create inside the Java code.
[03:28] Just like objects, we can also create variables inside the methods.
[03:32] You can see here there is a variable called output inside the method2().
[03:35] So this variable we call it as a local variable because this variable is going to make sense only within
[03:43] this method.
[03:44] If I try to access this output variable inside another methods, then I'm going to get a compilation
[03:51] error because the output is not going to make sense for other methods.
[03:55] So these kind of local variables are also going to be regularly deleted whenever the method execution
[04:02] is completed.
[04:02] But please note that Garbage collector is only responsible to clean up the objects.
[04:08] So what are objects object we can only create with the help of reference data types like a Java class.
[04:14] So String also is one of the Java class.
[04:17] So whatever variable that we create with the help of String it is also an object.
[04:21] So my JVM can delete these object whenever I'm done with these method2() execution.
[04:27] But coming to the primitive data types like number here, the Garbage collector is not going to track
[04:32] these because these are only local primitive variables, but not the objects we're going to discuss
[04:39] in few minutes.
[04:41] Who is going to maintain and delete these kind of variables inside the Java program?
[04:45] I hope you are clear,
[04:46] what is heap memory?
[04:47] Always remember, heap memory means it is a place where Java is going to store all the objects.
[04:53] After heap memory
[04:53] the next important memory that we have is stack memory.
[04:57] This is the area of memory where
[05:00] local variables and method calls are going to be stored.
[05:03] In the previous lecture, I showed a demo of method invocations where all the method invocations are
[05:09] going to be maintained with the help of stack data structure, so all the method invocations with the
[05:15] help of stack data structure is going to be saved inside the stack memory.
[05:19] So whenever a new method is being called, a new stack frame is going to be created on the stack, which
[05:25] will contain all the methods, local variables and parameters.
[05:29] And whenever the method returns the execution or completes the execution, the stack frame is going
[05:35] to be removed along with the local variables and the parameters.
[05:39] So here you can see we have a local variable which is of type int.
[05:43] So since it is a primitive data type we can call it as a local variable instead of local object.
[05:48] So whenever we try to invoke the method1(), a stack frame is going to be created inside the stack
[05:54] memory along with the method input parameters method local variables.
[05:59] Once the method is returning the execution or once the method is done with the execution, all the
[06:05] local variables and parameters that we stored inside the stack memory will be deleted along with the
[06:11] stack entry
[06:12] related to this method, always please remember stack memory means it is an area where method calls
[06:18] are going to be stored along with the local variables of a method.
[06:21] After the stack memory, the very next important memory is method area or class area.
[06:27] This is the place where we are going to store all the class definitions, method definitions and other
[06:34] runtime constants like static variables are going to be stored.
[06:38] We previously discussed objects are going to be stored inside the heap memory.
[06:41] But how JVM is going to remember?
[06:44] What is the definition of a class?
[06:45] What is a method definition or what is a static variables.
[06:49] So all such information are going to be stored inside the method area.
[06:53] This method area we also call it as class area because inside this memory only we are going to store
[06:59] all the class definitions.
[07:01] And at last the next important memory we have is native heap.
[07:05] This is the area of memory where native libraries and the code are going to be loaded are stored.
[07:11] So what is native code?
[07:13] When we discussed about the compilation and interpretation process of Java, I explained about a process
[07:19] called JIT compilation Just In Time compilation.
[07:22] So what my JIT compiler is going to do, my JIT compiler is going to identify the hotspots inside my
[07:29] classes and methods, which are going to be executed many times or very frequently all such hotspots
[07:35] bytecode is going to be converted into a native executable code by the JIT compiler, and it is going
[07:42] to cache it inside a memory.
[07:44] And that memory is native heap.
[07:47] So this native heap is going to be used by JVM for runtime memory allocation, and to store some native
[07:53] related libraries and code inside this native heap
[07:57] my JVM is also going to create some objects with the help of native code and native libraries.
[08:03] But whatever objects that JVM is going to create inside the native heap, they are not going to be tracked
[08:09] by the Garbage collector.
[08:10] My Garbage collector is only going to clean the objects inside the heap memory, but not inside the
[08:17] native heap.
[08:18] As a developer, we don't have to worry much about the native heap because JVM is going to take care
[08:23] of it behind the scenes.
[08:25] Now here you may have a question like how my JVM will have the space or disk space to create all these
[08:33] memories at the runtime.
[08:34] Let me answer that question.
[08:36] Whenever we try to execute a Java program with the help of a JVM, the JVM is going to receive a portion
[08:43] of memory from the underlying operating system.
[08:46] So based upon that JVM version and the platform that you are trying to run, a portion of memory is
[08:52] going to be received by the JVM like 1 GB or 2 GB.
[08:56] Most of the times these memory is more than enough to run any large amount of Java code.
[09:02] But in some special scenarios where you want to customize this memory allocation to the JVM, you can
[09:08] do that.
[09:09] But that is a very rare scenario where developers, they are going to increase the space assigned to
[09:15] the JVM by the underlying operating system.
[09:18] With this, I'm assuming you have some good understanding where Java is going to store all our classes,
[09:24] objects, variables, and methods.
[09:26] Please have this information handy always, because in any interview related to Java, there will be
[09:32] definitely questions around the memory like heap memory, stack memory, method area.
[09:38] With that reason only, I'm trying to share this information with you.
[09:42] Let's continue this discussion around the memory management by JVM in the next lecture as well.
[09:48] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
