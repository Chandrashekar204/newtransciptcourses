# 15.19 — [JAVA 10] var (local variable type inference) - Part 1

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] One of the reasons why Java programming language is so successful inside the programming industry is
[00:06] it tries to evolve continuously based upon the feedback received from the developers.
[00:12] One such feature that got introduced in Java is var.
[00:17] This var feature is introduced in Java 10.
[00:20] With the help of this var, we can declare local variables without explicitly specifying their type
[00:29] on the left hand side.
[00:30] Instead, the type of the variable is going to be inferred by the compiler based upon the initialization
[00:36] expression that we have written on the right hand side.
[00:38] I know this definition may not make any sense to you, but let me share you an example post that it
[00:44] is going to be super clear for you.
[00:46] As of now, whenever we are trying to create a local variable, we are trying to create the variables
[00:51] like you can see here.
[00:52] Like
[00:53] first we are going to mention what is the data type on the left hand side like String message is equal
[00:59] to and what is the initialization expression on the right hand side.
[01:03] So on the right hand side I'm trying to assign the String data to the message object which is of type
[01:10] String.
[01:11] So this is the story that is happening before Java 10.
[01:14] But if you see here there can be some smart work can be done by the compiler here, since anyway, I'm
[01:21] trying to assign the String on the right hand side.
[01:24] What is the need for me to mention the String again on the left hand side?
[01:28] So this kind of feedback has been given by the developer community to the Java team.
[01:33] That's why they came up with a var feature
[01:37] in other words, we can call this var as local variable type inference.
[01:43] So this is introduced in Java 10.
[01:45] With the help of var we can change the same Java statement like you can see here.
[01:50] So instead of String we can mention var message is equal to hello world.
[01:55] So the data type of this message variable is going to be inferred as an String.
[02:00] Because on the right hand side we are trying to assign the String data.
[02:05] So there are a lot of advantages with these var.
[02:08] That's why let's try to understand more details about this var feature.
[02:12] VAR is a reserved identifier name, but not a keyword, which means any existing code that is written
[02:19] before the Java 10
[02:21] that is, using the var as a variable or a method or a package name, it is not going to be affected.
[02:28] However, any class or interface that has the name as var such classes and interfaces, they need to
[02:35] be renamed.
[02:36] If you are trying to use a Java version which is equal to or greater than Java 10.
[02:42] Whenever you are trying to use a var, you should always make sure you are using this var along with
[02:48] the initialization expression.
[02:50] For example, I cannot write a simple Java statement which is var message, so this is not going to
[02:57] be allowed
[02:58] I'm going to get a compilation error because my Java compiler is going to be clueless.
[03:03] What will be the data type of these message variable name, whether it has to allocate a memory for
[03:10] a String object or for an Integer object.
[03:12] Since it is going to be clueless with this statement.
[03:15] This is not going to be allowed by your Java compiler, you're going to simply get a compilation error.
[03:21] Let's see the demo of this var very quickly.
[03:24] First, I'll try to create a Java class with the name Var.
[03:28] So as soon as I press enter, you can see I'm getting a error saying that Var is a restricted identifier
[03:35] and cannot be used for type declarations.
[03:38] It can be a class or interface or any other type like Record, Enum, Annotation.
[03:44] So for all these kind of types, we can't use the var because this is a restricted identifier from
[03:52] java 10.
[03:52] That's why let me remove this name and mention the class name as VarDemo post that I'm going to create
[03:59] the main() method inside this main() method.
[04:01] First I'm going to mention Var message.
[04:04] So with this simple statement we are going to get a compilation error saying that cannot infer type
[04:10] without initializer.
[04:12] That means my compiler is not able to identify what is the data type of this message.
[04:17] To overcome these kind of issues, we should always use the var along with the initialization expression.
[04:23] On the right hand side
[04:24] if I mention the data as two.
[04:27] Now my message is going to be treated as a int variable.
[04:32] Similarly, if I try to change this to 4.5 now, it is going to be considered as a double.
[04:38] And instead of this double value, if you try to mention a String value like hello world, now my message
[04:45] variable is going to be treated as a String object by my compiler.
[04:50] I hope you are seeing the advantage of var the same var we can also use whenever we are trying to create
[04:56] an object off our custom classes.
[04:59] For example, while creating the Person object, instead of mentioning the Person class name on both
[05:06] sides, I can simply mention var here.
[05:10] So this is going to be super helpful in the scenarios where you have a very lengthy class name.
[05:16] I can also show you a demo around the lengthy class name.
[05:19] For example, think like I'm trying to create the object of ArrayIndexOutofBoundsException.
[05:25] So in this scenario I need to mention the class name on both sides, and this will make my code lengthy.
[05:34] And at the same time it is also unnecessary.
[05:36] Why should I mention the class name on both sides?
[05:38] If my compiler can detect what is the data type of my variable based upon the initialization that I
[05:45] have on the right hand side.
[05:46] So with the help of var keyword, we can minimize the code that we are trying to write.
[05:51] So you can see now my variable which is arr
[05:55] it is going to be act as a type of ArrayIndexOutofBoundsException.
[06:00] But there are certain limitations that you need to be aware while using the var keyword
[06:05] one such limitation is, you can't assign the same variable again to a different data type.
[06:11] For example, I have already assigned the String data to the message variable this time
[06:16] if I try to change this to four, it is not going to be allowed by my compiler because the compiler
[06:22] already decided the data type of this message variable as String.
[06:26] But now if I try to change the data by assigning a different value, the compiler is going to throw
[06:32] an error saying that required type is String.
[06:34] But we are trying to provide the int. So this is one limitation
[06:37] similarly, we can use the var inside the loop declarations are while declaring an array.
[06:43] Let me show you some examples around this as well.
[06:46] Here
[06:46] the very first point that I'm trying to highlight is, you can always use the var inside your normal objects
[06:54] declaration and initialization.
[06:56] We already saw the demo of this.
[06:58] Instead of mentioning the class name on both sides, we can simply mention on the right hand side and
[07:03] on the left hand side, we can replace the class name with the var.
[07:06] So the same statement we can convert it using var like you can see on the right hand side.
[07:12] So var is helping developers to avoid repetition and encouraging a development principle which is dry.
[07:20] So what is dry?
[07:21] Dry is a principle inside software which is a famous principle.
[07:25] The full expansion of Dry is don't repeat yourself unnecessarily.
[07:30] So here you can see we are trying to repeat the class name two times unnecessarily with the help of
[07:36] var, where only mention the class name one time.
[07:39] And with that we will end up following the principle dry
[07:44] inside our Java programs.
[07:46] Dry is one of the best coding practice that all the programming languages recommend developers to follow.
[07:52] It conveys if something is not required, don't repeat it in the similar lines
[07:57] Var also can be created while declaring an array.
[08:00] Here you can see in this statement the nums variable name is going to be inferred as an array, because
[08:07] on the right hand side we have an array expression which is going to create an array with the elements
[08:14] one, two, three, four, five and inside the loops
[08:16] also we can use the var like you can see here
[08:20] I'm trying to use a var inside for each.
[08:22] So the data type of num is going to be inferred based upon the values that I have inside these nums
[08:28] array.
[08:28] Since I have int values, the num is going to be interpreted as a int data type in the next line
[08:36] I have an example of traditional for loop inside the traditional for loop
[08:40] also, instead of mentioning inter counter is equal to zero, we can simply mention var counter is equal
[08:45] to zero.
[08:46] So in this scenario the counter variable is going to be inferred as a int because we are trying to assign
[08:53] a int value.
[08:54] But like I said before, there is a limitation.
[08:57] Once a value is assigned to a variable with the help of var, you can't assign a different value.
[09:03] So here first I'm trying to assign a int variable.
[09:06] Later on I'm trying to assign a String data.
[09:09] So this is going to result into a compilation error.
[09:11] But the same kind of code is allowed in few languages like JavaScript.
[09:16] If you are familiar with JavaScript this code is going to work without any issues.
[09:21] JavaScript is going to allow you to change that data at a later point as well, once the declaration
[09:28] and initialization complete.
[09:30] Because JavaScript is a very lenient programming language, which gives a lot of flexibility to the
[09:36] developers, it also has some drawbacks.
[09:38] That's why to overcome these kind of drawbacks in JavaScript, a new language TypeScript, came into
[09:44] picture, which is going to maintain a strong typing system for the JavaScript code.
[09:49] So inside the TypeScript, this kind of assignment is not going to be allowed, because TypeScript is
[09:56] going to be more strict compared to the
[09:58] JavaScript language.
[10:00] I hope you are clear with these initial discussion around the var feature.
[10:04] Let's try to continue the same in the next lecture as well.
[10:07] Thank you,
[10:08] bye.

----------------------------------------
