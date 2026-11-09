# 30.6 — [JAVA 25] Flexible Constructor Bodies - Part 2

> Section 30: New features from Java 25

[00:00] Before I try to solve these problems by using the Java 25 feature, let me show you a tricky interview
[00:07] scenario inside interviews.
[00:09] They may give you something like this where while invoking the savings account constructor, they're
[00:13] not passing any valid account number.
[00:16] So with this kind of setup, you might be assumed that it is going to throw a runtime exception with
[00:22] a message invalid account.
[00:24] But do you know what is the actual exception we are going to get.
[00:28] We're going to get null pointer exception because first the super constructor invocation is going to
[00:35] have.
[00:35] So with this the control will go to the superclass constructor.
[00:40] From there they are trying to invoke the check method.
[00:43] And since the check method is overriding inside the subclass, this logic is going to be executed.
[00:50] Since the account number is null, we're going to get null pointer exception if I can prove you the
[00:56] same as well.
[00:57] If I run this program, I'm getting a null pointer exception.
[01:00] So always be aware of these scenarios.
[01:02] Don't try to answer that.
[01:03] This program is going to result into runtime exception.
[01:07] Now let me change the Java version of my project.
[01:10] I'm going to select this and open the settings under the project settings.
[01:16] This time I'm going to select the query to 25 version.
[01:20] And I'll go to modules.
[01:21] And here also under the language level I will select Compact Source files comma module imports.
[01:28] Let me apply and click okay.
[01:31] So this time since we are using Java 25 we should be able to write logic before the super are this constructor
[01:39] invocation.
[01:39] So what I can do here, I can simply move this line just above the super constructor invocation.
[01:46] And this time you'll be able to see I'm not getting any compilation errors.
[01:51] This is due to the new enhancement that is introduced inside Java 25.
[01:55] The enhancement name is Flexible Constructor bodies.
[02:00] So with this setup, if I try to execute this program I'm not going to get.
[02:03] Null pointer exception.
[02:05] Instead I'm going to get these runtime exception with a message invalid account.
[02:10] Are you seeing the power of this new enhancement?
[02:13] Let me update these main method logic to have some valid account number.
[02:18] So this time if I try to execute this program I'm not going to get any runtime.
[02:24] Exceptions are null pointer exception.
[02:27] We have solved this problem.
[02:28] Now let's go to the car class.
[02:30] So here what we are doing.
[02:32] We are doing all this validation by using a static method.
[02:36] Instead I will try to move these validations into the constructor itself just above the super constructor
[02:45] invocation.
[02:45] So I can get rid of these verify speed method invocation and I can straightaway pass speed variable
[02:53] to the super constructor as well.
[02:55] This way we can do some validations.
[02:58] Are some variables assignments about the super constructor invocation, which is going to make the life
[03:05] of the developer easy.
[03:06] With the explanations that we have done so far, this slide should make sense now.
[03:10] Before Java 25, the first statement inside the constructor body should be the explicit constructor
[03:16] invocation by using super these followed by some block of Java statements.
[03:21] But with this feature above the constructor invocation, we can also write a block of statements.
[03:27] I have mentioned all the problems that we have discussed, along with the solution that we have discussed.
[03:33] So in total, we have discussed two problems.
[03:36] The details of these two problems I have highlighted in the slides as well.
[03:40] For your reference, before I try to close this feature discussion, let me share some more important
[03:46] details around this enhancement to give the flexibility to the developers to write some logic just about
[03:52] the super invocation and this invocation.
[03:54] The Java team, they have made some changes on how the constructors are going to be executed behind
[03:59] the scenes before Java 25, whatever parameters that we used to send to the constructor as arguments.
[04:06] They're going to be treated as static behind the scenes.
[04:09] But right now with these features, since we are going to perform some validations, since we are going
[04:14] to write some code, a new concept with the name Early Construction context is built by using these
[04:23] concept.
[04:24] The constructor is divided into three parts.
[04:27] Behind the scenes.
[04:28] You don't have to know all these as a developer, but I'm sharing these details for your in depth understanding
[04:34] whatever logic that we write about the super and this so that logic we call it as prologue.
[04:41] So this is the very first part.
[04:43] And coming to the second part, whatever logic that you're going to write to invoke the super are these
[04:49] that will come as a second part.
[04:52] The third part is called as epilogue.
[04:54] So whatever code that we write after the super and these that will be called as epilogue with these
[05:01] new feature or enhancement.
[05:02] Now developers, they can write some logic as part of the prolog, but this doesn't mean that we can
[05:09] write any kind of logic.
[05:10] We have to be responsible as a developer.
[05:13] So always keep your constructors lightweight, and the prolog should have the logic only related to
[05:19] the object instantiation.
[05:22] Our input parameters, validations and so on.
[05:25] Java team.
[05:25] They also enforce some restrictions.
[05:28] If you try to ignore those restrictions you're going to get an compilation error.
[05:32] Let's try to understand what are those restrictions.
[05:35] This is the example where I have highlighted few of the invalid code executions above.
[05:41] The super are this invocation.
[05:44] So there is a class with the name book, and from this book we are calling the superclass constructor.
[05:50] So this class does not extend anything.
[05:52] But let's assume this class is extending some parent class.
[05:55] So this is the super constructor invocation.
[05:58] So whatever logic that I have written above the super.
[06:01] So this is called as Prolog.
[06:04] So as I said the first part is called prologue.
[06:06] So inside the prologue there are some restrictions.
[06:09] The first one is you can't use the this keyword or super keyword as part of the prologue.
[06:16] If I do System.out.println this it is not going to work.
[06:20] Similarly, I can't refer the current instance fields like title and pages and assign them to some other
[06:27] variables.
[06:27] Here when I'm invoking the field title.
[06:30] Behind the scenes, the code will be like this dot title.
[06:34] So since this is present, the code is going to fail.
[06:37] And similarly we can't invoke the instance methods.
[06:40] Why I can't invoke this an instance method because the object of this class is yet to be constructed.
[06:46] But you can do the field initializations.
[06:49] For example, here there is a title that we have declared without any initialization to this field,
[06:55] we can assign some value.
[06:57] So this is all about the super are this invocation.
[07:02] But if a field is already initialized with some default value You can't reinitialize it with a new value.
[07:09] So that's why here I have highlighted about error as part of the prologue.
[07:13] You can do the field initializations.
[07:17] You can do some validations, you can invoke some static methods, but you can't invoke the instance
[07:24] methods are this keyword or you can't perform the reinitialization of the variables.
[07:30] I also have another example as well.
[07:32] Inside this class.
[07:33] If you see shape is a parent class and triangle is a subclass.
[07:37] So just above the super constructor invocation, I can't execute this code because I'm trying to access
[07:44] the super keyword.
[07:45] So by using the super keyword, I'm accessing the variables of the parent and instance methods of the
[07:52] parent.
[07:53] This is not allowed because the super class object is to be constructed by Java.
[08:00] So far we discussed about parent and subclass scenarios, but let me show you one example where we can
[08:07] strictly talk about this constructor invocation.
[08:10] So this is an independent class.
[08:12] It is not extending any parent.
[08:14] The class is course.
[08:15] And inside this class we have a couple of fields like course name and duration.
[08:20] And this class also has a couple of constructors which accept two parameters.
[08:24] And another overloaded constructor which accepts three input parameters.
[08:28] So the main constructor it is not doing anything.
[08:31] It is simply accepting the values and assigning to the instance variables of the object that is being
[08:37] constructed.
[08:38] But inside the second constructor, if you see they are invoking the first constructor by using the
[08:44] this keyword while invoking this first constructor, they are passing the prefix value and name value
[08:51] as the first parameter, and the duration value will be the second parameter.
[08:55] Since we are using the Java 25 feature, we are able to write all this logic before Java 25.
[09:01] If you write this logic, this is not allowed because as we discussed, the super are.
[09:06] This invocation has to be the first step.

----------------------------------------
