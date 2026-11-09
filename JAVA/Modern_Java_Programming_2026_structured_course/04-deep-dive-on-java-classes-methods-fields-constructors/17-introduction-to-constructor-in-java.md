# 4.17 — Introduction to Constructor in Java

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture.
[00:01] Let me answer your burning question.
[00:03] What is a Constructor in Java?
[00:06] What is the role that it plays
[00:07] while we are trying to create objects with the help of Java classes and new keyword.
[00:13] Before I try to explain you the formal definition of constructor, first let me give a real life example.
[00:19] Think like you want to construct your own house, our own building.
[00:24] So what are the steps that you follow?
[00:25] First, you're going to have a blueprint or planning for your building.
[00:30] By taking help from one of the architect, you're going to have a plan for your building.
[00:35] Once the plan is ready, you're going to start the construction. In the construction stage
[00:41] you're going to build the walls,
[00:42] you're going to fit the windows, doors, you're going to build bathrooms, you're going to lay down the
[00:48] tiles.
[00:48] You're going to do some drainage work, electric work, water piping work.
[00:52] So there are so many activities you're going to do as part of the construction.
[00:57] Once the construction is completed, you're going to get your final output, which is your own house
[01:03] or your own building.
[01:04] If you try to compare the same analogy with the Java whatever blueprint that you have initially inside
[01:11] the building scenario, the same kind of blueprint or template you are going to build with the help
[01:16] of Java classes.
[01:18] And the final output that you got in the building scenario, which is the building itself, it is like
[01:23] a object in the Java world.
[01:25] So using a plan you're going to build your own house, which is a final output.
[01:30] Very similarly inside Java programming using that Java class, which is a blueprint, I'm going to create
[01:37] as many objects I want.
[01:39] So object is a final output.
[01:41] But in between my class definition and my object to final output, they're going to be an intermediate
[01:48] stage, just like how you have construction stage inside the building scenario
[01:52] very similarly in the Java scenario also we have a constructor.
[01:56] So there is a similarity like construction stage and the constructor that's why the name constructor
[02:02] came using this constructor
[02:04] we are going to do some initialization activities that we want to take care
[02:08] before my object is completely created by the JVM.
[02:12] These initialization activities are like assigning the data inside my object.
[02:17] So all such initialization activities we are going to do with the help of constructor.
[02:23] I hope you are clear with the high level introduction about the constructor, in Java constructor always
[02:29] going to help you to initialize your object before it is completely created.
[02:34] Now let's try to discuss the formal definition of constructor.
[02:38] A constructor is a code block that is essential inside Java for creating an object.
[02:45] So what is an object?
[02:46] It is an instance of your class.
[02:49] In other words, we can also call our objects as instance of class, because if the class is a blueprint,
[02:55] object is going to be an instance of that blueprint.
[02:58] So this code block of constructor, it is going to look like very similar to your Java method inside
[03:05] your Java classes.
[03:06] But there are certain differences, which is going to help you to clearly identify whether a given code
[03:12] block is a Java method or a constructor.
[03:15] So let's try to understand what are those?
[03:17] The very first thumb rule that you need to follow to define a constructor for your Java class is,
[03:23] the constructor name has to be same as your class name.
[03:26] If my class name is Employee, then the constructor name also should be Employee.
[03:31] I cannot choose any other name.
[03:33] That's a very first rule.
[03:35] And the second rule that we need to follow while we are declaring constructor is, from the constructor,
[03:40] we are not supposed to return any value, not even void.
[03:44] So that's why inside the definition of constructor, we're not going to mention any return type, even
[03:50] void
[03:50] also, we should not mention.
[03:52] So what is the purpose of constructor?
[03:53] When we try to create an object inside Java, the JVM invokes your constructor and it is the developer
[04:01] responsibility to write some initialization logic, like assigning values to the fields of the object.
[04:09] So all such initialization tasks you need to perform them inside your constructor.
[04:14] But please note that this is completely optional.
[04:17] If you have a business requirement where you want to populate some data, or where you want to perform
[04:22] some activities before your object is completely created, then you can leverage the constructor.
[04:27] You can define your own constructor, and you can write all your business logic.
[04:32] Otherwise, you can simply ignore the constructor itself.
[04:35] Behind the scenes, your JVM compiler is going to create a default constructor, and this default constructor
[04:41] is not going to accept any parameters, and the body inside the constructor also is going to be empty.
[04:47] We also saw this in the previous lecture.
[04:49] So once the code inside the constructor is executed, your JVM is going to create your object by allocating
[04:56] memory inside your system.
[04:58] So here is a sample class
[04:59] and
[05:00] it's a default constructor.
[05:01] The class name is Employee.
[05:03] I have defined that by following the syntax public class Employee and inside the class only,
[05:09] just like how we define the methods.
[05:11] Very similarly we can define a constructor,
[05:14] so here I have just mentioned the default constructor.
[05:17] How I'm telling this a default constructor, you can see it is not accepting any input parameters.
[05:23] And at the same time this constructor does not have any business logic.
[05:27] So if your constructor does not have any code and it is not accepting any input parameters, then we
[05:33] can safely call it as a default constructor because it is going to look like the same constructor that
[05:39] is going to be generated by your JVM.
[05:41] The important thing that I want to observe here is your constructor name has to match exactly with your
[05:48] class name, otherwise you're going to get a compilation error.
[05:51] Like I said before, if you are not defining any constructor inside your classes, Java automatically
[05:58] provide a default constructor with an empty body.
[06:01] And that's what we are trying to invoke here.
[06:03] When I'm trying to create an object of Employee on the right hand side, just after the new keyword,
[06:09] I'm trying to invoke the constructor, which is Employee like you can see here employee and empty parentheses.
[06:15] So this is how you're going to invoke your constructor which is present inside your Java class.
[06:21] And whenever we are trying to invoke that default constructor our object does not going to have any
[06:27] values.
[06:28] All the fields are going to hold the default values like null, zero, false or blank space in the
[06:35] scenario of char data type.
[06:37] So those are all default values.
[06:39] The reason is when we don't define our constructor, that means we don't want to provide any initialization
[06:45] code.
[06:45] In such scenarios
[06:46] whatever default constructor is generated by the JVM, the same will be executed
[06:51] and since this default constructor has an empty body, no initialization will happen and your object
[06:58] is going to hold the default values.
[07:01] So if you see here on the right hand side first I'm using that new keyword.
[07:05] The purpose of new keyword or
[07:07] the new operator is,
[07:08] we need to use this to tell to my JVM that I'm trying to create a new object.
[07:14] After the new keyword, we need to invoke the constructor of the class.
[07:18] So here I'm trying to invoke the default constructor Employee with the blank parentheses.
[07:23] So the combination of your new and default constructor is going to return a reference of the newly created
[07:31] object, the same reference we are trying to catch onto the variable with the name myObj on the left
[07:38] hand side.
[07:38] Whatever default constructor that is going to be generated by the Java compiler,
[07:44] we are also going to call it as no args constructor.
[07:48] It is not going to accept any parameters.
[07:50] That's why many developers sometimes they'll also call this default constructor as no args constructor,
[07:56] which means no arguments constructor or no parameters constructor and the access level of the default
[08:03] constructor is always going to be the same as the access level of the class.
[08:08] So if you have defined the public as a access modifier for your class, the same modifier will be considered
[08:14] for the default constructor that is going to be generated by the JVM or Java.
[08:20] So let's try to understand more details about what is a constructor.
[08:23] Like I said before, the constructor they are going to look very similar to method.
[08:28] There are some differences that you can follow to identify whether a particular code is a constructor
[08:34] or a method.
[08:35] Method is a class member, whereas constructor is not a member of the class because it is not a method.
[08:41] The only purpose of the constructor is to be invoked.
[08:45] Whenever we are trying to create a new instance of the class or the new object from the class, like
[08:51] we discussed what kind of code we have to write inside the constructor, we need to focus strictly on
[08:57] initializing the instance variables or the Java fields of the newly created object.
[09:03] We should always restrict ourselves to the tasks related to the initialization of the variables or
[09:09] any other initialization tasks related to object.
[09:12] And we should also note that whenever we are trying to write some business logic inside the constructor
[09:17] to initialize our object, we should consider that object is not completely created inside the memory.
[09:24] Because it is in the process of getting created,
[09:28] my object is not fully formed.
[09:30] We need to assume this while we are trying to define some logic inside the constructor.
[09:34] Otherwise we are going to get an unexpected outcomes.
[09:38] Just like how we can create any number of methods inside your Java class.
[09:42] Similarly, we can create any number of constructors inside your Java class, but all your constructors,
[09:49] they are going to have the same name, which is same as your Java class name.
[09:53] Then how we are going to define multiple constructors inside a Java class is by defining the different
[09:59] set of input parameters.
[10:01] I can write a empty constructor, and I can write another constructor, which is accepting two input
[10:07] parameters.
[10:08] And very similarly, I can write one more constructor, which is accepting only one input parameter.
[10:13] This way, by having different, different set of input parameters, I can write any number of constructors
[10:19] which I can invoke them based upon my scenario.
[10:22] So defining multiple constructors in a same Java class, we call such concept as constructor overloading
[10:30] because we are trying to define multiple constructors in the same Java class
[10:34] that's why we call this scenario as constructor overloading.
[10:38] We also have concepts like method overloading, which we are going to discuss in the coming sections.
[10:44] Now you can see here this is the general syntax that we need to follow whenever we are trying to create
[10:50] a Java constructor.
[10:51] First you need to mention the modifier, modifier also is optional.
[10:55] After that you need to mention the constructor name.
[10:58] Please note that constructor name should be always same as your Java class name, and after that you
[11:04] need to mention the parentheses and inside the parentheses you can put it as blank without any input
[11:10] parameters or you can define some parameters as well based based upon your business requirement.
[11:15] And after the parenthesis, I can define Throws class to indicate what kind of exception my constructor
[11:22] logic can throw in the case of any error or runtime exceptions.
[11:27] For now, please don't worry about throws, because we are yet to discuss about the exception handling
[11:32] inside the Java programming.
[11:34] And after the Throws class, you need to define the curly braces, and inside these curly braces you
[11:40] can write all the business logic and these business logic, such as assigning some values to your instance
[11:46] variables present inside the object or performing any other initialization tasks.
[11:51] I have mentioned all the details about these syntax here itself.
[11:55] You can read them for more details.
[11:57] The same information we discussed just now.
[11:59] With this I'm assuming that you have a good clarity about what is a constructor.
[12:04] In the next lecture, let's try to define some constructors inside our Java classes, and in the same
[12:10] process let's try to explore more about constructor.
[12:14] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
