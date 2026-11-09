# 4.8 — Introduction to methods in Java - Part 2

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's try to understand how to define a Java method by taking a simple example.
[00:06] I want to get started with a very, very simple example.
[00:10] The reason is as of now, you're like a baby inside the Java world.
[00:14] You're just trying to get started with the Java programming language, just like how we feed a semi-fluid
[00:20] food or fluid food to the newborn babies.
[00:22] Very similarly here, I'm trying to take a very simple scenario so that you can easily digest this information,
[00:29] and in the same process, you will get used to the syntax of the methods inside Java programming language.
[00:36] I hope you are fine with that.
[00:37] Like you can see here, I'm trying to define a method which is going to accept two numbers as an input
[00:44] and inside the method we have to add these two numbers and return the result to the invoking entity.
[00:51] So the very first keyword here you see is public.
[00:55] So this is a modifier of the method.
[00:57] This describes who can invoke your method.
[01:00] This modifier is completely optional, but it is always a good practice to define the exact modifier
[01:07] that you want to use for your method.
[01:09] For now, let's use the public after the public keyword
[01:13] we should give a space followed by what is the return data type of your method.
[01:18] So you can see here we are trying to return a variable which is result from my Java method
[01:23] and this result is of data type int.
[01:27] So the same int primitive data type I have to mention inside the return type after the public keyword.
[01:33] So once you have defined these return type as a next step we should give a name to the method.
[01:38] So since here I'm trying to add two numbers, I can give a name as sum or add whatever makes sense for
[01:45] my business logic.
[01:47] After the name of the method, I'm trying to give the parentheses, so there will be a open and close
[01:52] parentheses, and inside these parentheses you can define any number of input parameters for your method
[02:00] based upon your requirements.
[02:01] And every parameter has to be separated by a comma.
[02:05] So there is a first parameter which is int num one and the second parameter which is inter num two.
[02:11] So here you should also follow a syntax whenever you are trying to provide a input parameter details
[02:17] to your method.
[02:18] So the syntax that you need to follow is first you need to make sure you are mentioning what is the
[02:23] data type of your parameter.
[02:25] So here I'm trying to follow a primitive data type which is int.
[02:29] That's why I'm mentioning the int.
[02:31] And after the int I need to mention what is the parameter name.
[02:35] So whoever is going to invoke my method they're going to pass two input numbers like 9, 10 or
[02:43] 8, 10.
[02:44] So in such scenarios so whatever first value we have the same will be binded to the first variable which
[02:51] is num1.
[02:52] The same variable we should also use inside our method business logic.
[02:56] So here it should be pretty clear for you.
[02:58] Inside my method body I'm trying to add two numbers like num1 and num2.
[03:03] So inside these variables only I have inter values.
[03:06] These two inter values I'm trying to add with the symbol plus.
[03:10] So inside Java, how to add two numbers with the help of the plus symbol and the outputs that I get
[03:17] from this expression, like num1+num2, I'm trying to catch that inside a variable on the left
[03:23] hand side.
[03:23] And this variable name is of data type int and the variable name is going to be result.
[03:29] So the same variable I'm trying to return from the method as an output.
[03:35] So every Java statement inside your method body has to be terminated with the semicolon.
[03:40] So whatever you see highlighted in the dark green we call all these lines as method body
[03:46] because these method body is present inside the opening and closing curly braces of your method.
[03:52] I hope you are clear with this syntax.
[03:54] As a next step, let me give you more details about what are parameters and arguments of Java methods.
[04:00] Most of the times you see developers using the jargons like parameters and arguments interchangeably,
[04:08] but there is a clear difference between what is a method parameter and what is a method argument.
[04:13] First, if you try to talk about what is a method parameter, when you're trying to define a method,
[04:17] you can specify any number of input parameters.
[04:21] So a parameter is a variable that is used to store an argument that is passed to the method by the caller
[04:28] or the invoking entity, whereas argument is a value that is passed to your method whenever it is trying
[04:36] to be invoked.
[04:36] If you try to understand the same arguments and parameters with an example, you can see here we have
[04:42] a method which is public void printMessage(), and to this method we have a input parameter which is
[04:48] String message.
[04:49] So the same message we are trying to print it with the help of System.out.print() and inside the
[04:54] method body.
[04:55] So here you can see the message variable that we receive as an
[05:00] input to the method.
[05:01] We call this variable as an parameter, whereas whoever is trying to invoke your method, they'll pass
[05:07] a value.
[05:08] For example, you can see someone is trying to invoke my method, which is printMessage().
[05:12] And when they're trying to invoke this method, they should pass the value which is matching to my parameter
[05:18] data type.
[05:19] So here I have defined the parameter data type as String.
[05:22] So the same data type value I have to pass the value that I'm trying to pass here is Hello, World.
[05:28] So this Hello, World value will become the argument for my Java method.
[05:33] I hope you are very clear about what is a Java method parameter, or what is a argument inside a Java
[05:39] method.
[05:40] Most of the developers, they use these jargons or definitions interchangeably.
[05:45] That's perfectly fine as long as you understand what is a parameter and argument.
[05:49] I hope this all clear to you.
[05:51] In the next lecture, let's try to define some Java methods inside the Java classes that we have created
[05:57] so far.
[05:57] Thank you and I'll catch you in the next lecture.
[06:00] Bye.

----------------------------------------
