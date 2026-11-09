# 4.32 — Static Initialization Block in Java class - Part 1

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] From this slide we can see a Java class can contain below components like fields, methods, constructors,
[00:08] instance initializers and static initializers.
[00:11] As of now, we discussed everything except static initializers.
[00:15] Let's try to discuss what are the static initializers and what is the purpose of them.
[00:20] So what is a static initialization block?
[00:22] In Java, a static initialization block is a block of code that is going to be associated with a class,
[00:29] rather than the instances or the objects of the class.
[00:32] Whatever code that we are going to write inside the static initialization block, it is going to be
[00:37] loaded by the JVM.
[00:38] When we try to execute the class for the first time, the primary purpose of the static initialization block
[00:44] is to initialize any static variables of a class.
[00:48] So how to define the static initialization block?
[00:50] It is going to be very simple.
[00:52] First we need to mention the static keyword followed by opening and closing curly braces.
[00:57] They should not be any name to your static initialization block.
[01:01] And this block we need to create outside of the method and constructors, but inside the Java class.
[01:06] So this is one of the sample reference that you can refer.
[01:09] So there is a class with the name Car.
[01:11] And inside this I have a static variable which I just declared.
[01:16] The static variable name is numberOfEngines.
[01:18] This static variable I want to initialize when I try to execute my class.
[01:23] So how to achieve this with the help of static initialization block, you can see I have defined a static
[01:29] initialization block here and inside the body of this block, I am trying to initialize the
[01:34] numberOfEngines to a value called 1.
[01:36] So whatever code that we mentioned inside the static initialization block, it is only going to be executed
[01:43] when the class is loaded into the memory of the JVM, which means it is only going to be executed only
[01:49] once, no matter how many objects or instances of the classes are going to be created, similar to
[01:55] instance initialization block
[01:57] the static initialization block also is not going to have any return statement.
[02:02] This static initialization block is very useful in the scenarios where you want to perform one time initialization
[02:09] of the static variables, or when the initialization logic is more complex and cannot be accommodated
[02:15] with a single line, which means I have some complex logic to calculate the value of a static variable,
[02:21] which I cannot achieve with the single line, like here I have a single line like static byte
[02:26] numberOfEngines.
[02:27] If I want to assign a simple value, I can directly mention here is equal to and what is a value.
[02:32] But in some scenarios, to calculate that initialized value, we need to execute a lot of code.
[02:37] In such scenarios, we can move all such complex initialization logic of the static variable into the
[02:44] static initialization block.
[02:45] If needed
[02:46] you can have multiple static initialization blocks within a class, and all of them are going to be executed
[02:52] in the order in which they appear in the class definition.
[02:55] Whatever code that we are going to write inside the static initialization block is going to be executed
[03:02] before your main() method.
[03:04] So inside Java, we know whenever we want to start or whenever we want to execute a Java program, we
[03:09] use the main() method.
[03:10] So the code inside the static block is going to be executed before the main() method itself, because
[03:16] the code inside this block is going to be invoked by the JVM when it tries to load the Java class.
[03:23] Some interviewers, they can ask a tricky question for you.
[03:26] Can I execute a code before the main() method?
[03:29] So that is perfectly possible.
[03:31] You can do that with the help of static initialization block.
[03:34] I'm also going to show you this in the demo.
[03:36] Now very quickly let's see the difference between a static initialization block and the normal instance
[03:42] initializer block.
[03:44] The very first difference is very simple.
[03:46] The static block is going to have the static keyword.
[03:49] Using the static keyword only, we can difference whether a given block is a static initializer block
[03:54] or the normal instance initializer block.
[03:57] Moving on to the next difference, the static blocks are going to be executed during the class loading,
[04:03] whereas the instance block is going to be executed during the every object creation or every object
[04:10] instantiation.
[04:11] The third difference that we have here is inside the static initialization block, we can refer only
[04:16] the static variables, whereas inside the instance block we can refer both static and non static variables.
[04:23] And the next difference that we have here is in terms of usage of ' this ' keyword inside the static block,
[04:29] we cannot use the this keyword, because this keyword will come into the picture only in the scenarios
[04:35] of object creation or objects
[04:37] related code.
[04:38] Since static block is specific to the class, we cannot use the this keyword, whereas inside the instance
[04:44] block we can use the this keyword without any issues.
[04:48] The last difference that we have here is,
[04:50] this is very important.
[04:52] The static block is only going to be executed only once during the lifetime of a Java program
[04:59] and the
[05:00] execution is going to be during the class loading into the memory and just before the execution of the
[05:06] main() method, whereas instance block is going to be executed each and every time you are trying to create
[05:13] an object.
[05:14] So these are the major differences that I want you to be aware.
[05:18] Please have them handy.
[05:20] I hope you are clear about what is the purpose of static initializer block.
[05:25] In the next lecture, let's try to create this block inside one of the Java class and see this block
[05:30] in action.
[05:31] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
