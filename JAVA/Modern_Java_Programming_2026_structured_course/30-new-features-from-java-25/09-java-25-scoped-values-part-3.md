# 30.9 — [JAVA 25] Scoped Values - Part 3

> Section 30: New features from Java 25

[00:00] To see the demo of scoped variables, I'm going to create a sub package with the name scoped.
[00:08] Inside this new sub package, I'll try to create a new Java class with the name simple example.
[00:15] Inside this simple example class.
[00:17] First I'm going to create a new scoped to variable.
[00:21] So how to do that?
[00:22] We just have to type private static final followed by scoped value.
[00:29] So this scoped value is present inside the Java dot lang package.
[00:32] That's why we don't have to specifically import this class.
[00:36] So inside the scope to value I want to store a data of type string.
[00:41] Let me give the variable name as user underscore name followed by I'm invoking the scoped value dot
[00:50] new instance.
[00:51] Right now this will have a null value.
[00:53] In the very similar lines, I'm going to create one more scoped value with the variable name as transaction
[01:00] Section underscore ID.
[01:02] Let me create a method with the name do work, and inside this method I'll try to assign some values
[01:09] to the scope to value variables.
[01:11] So how to do that.
[01:12] So first we need to use the scope to value class.
[01:15] Using the same we need to invoke the where method to this where method, we need to pass the key followed
[01:21] by value that we want to assign.
[01:23] So the key is obviously this user name.
[01:27] And coming to the value I want to store allies, followed by I'm going to invoke the where method one
[01:34] more time.
[01:34] And this time I'm passing the key as transaction ID along with the value 12345.
[01:41] So after the where we need to invoke the run method, and to this run method, we need to pass a lambda
[01:47] expression.
[01:48] From this lambda expression, we should be able to invoke other methods or we can execute any amount
[01:54] of business logic.
[01:55] Let me create other methods with the name process task followed by call.
[02:01] Another method.
[02:02] So these are the two methods that I have created.
[02:05] And towards the end I'll try to create a main method by typing public static void main, so that from
[02:13] this main method I can invoke that do work method.
[02:16] From these do work method, and inside these run logic I can invoke the process task.
[02:21] Inside the process task I am going to paste a couple of lines of code.
[02:26] So first I'm trying to get the information present inside these user name scope to value by invoking
[02:32] the get.
[02:33] And next I'm going to invoke the IO dot println method to print these data.
[02:39] Let me do the same for transaction ID as well by pasting the same code.
[02:44] And here I'll mention the variable name as transaction ID and the scope to value variable will be transaction
[02:52] id.
[02:53] Using the same, I need to invoke the get method and this is going to return 12345.
[02:58] The same I can try to print by using these println statement.
[03:03] And here I can say processing for that transaction ID.
[03:07] After defining this logic inside the process task, I'm going to invoke the call another method inside
[03:12] the call another method.
[03:14] Also, I'm going to copy the same logic, but this time I'll change the statement that I'm trying to
[03:20] pass to this println.
[03:21] So instead of simply mentioning processing for the user, I'll just mention still processing for the
[03:26] user and still processing for the transaction ID.
[03:30] If I save these changes and execute this main method, we are going to get the expected output.
[03:37] As you can see, first we got the output from the method process task, followed by from the other method
[03:45] with the name call another method.
[03:47] So this is working as we expected.
[03:49] Next, let's try to understand what is going to happen if you try to access a scoped value outside of
[03:56] its scope.
[03:57] We know what our scoped values that we have created so far with the name, user name, and transaction
[04:01] ID they can be accessed only within the scope of this run method, which means we should be able to
[04:08] access them inside.
[04:09] These curly braces are inside the process task method.
[04:12] Are any of the methods that are invoked from this process task method.
[04:16] Let's try to access the scope to values outside these run scope.
[04:20] So what I'll do is I'll try to copy all these four statements and paste here and execute the program.
[04:28] This time we are going to get an exception with the name no such element exception.
[04:34] So this gives a confirmation to us that if you try to access a scope to value outside of its scope,
[04:40] we are going to get runtime exception.
[04:42] That's why it is recommended always to check whether the scoped value is bounded to the current execution.
[04:50] Before invoking this Get method, we have a method to check if the scope to value is bounded or not.
[04:57] What is that method?
[04:58] So there is a method that you can invoke by using the scoped value variable name, which is user underscore
[05:04] name.
[05:05] The method name is.
[05:06] He's bound.
[05:07] So this is going to return a Boolean variable.
[05:10] If the value is bounded to the scope to value, you can invoke these two lines.
[05:16] Otherwise you can skip invoking that logic.
[05:19] The same applies for other scoped value.
[05:22] Also here.
[05:23] Also I'll try to execute transaction id dot is bound.
[05:27] Since this is going to return false.
[05:30] I'm not going to execute these two statements, but if I do the same check inside these process task
[05:36] method or inside these call.
[05:38] Another method are inside these run execution logic.
[05:42] I'm going to get the boolean value as true.
[05:45] I can confirm the same by keeping the same check here.
[05:49] So let me mention this if condition and move these logic into this if condition.
[05:56] I'll do the same for that transaction ID as well.
[06:00] So here I'll move these two lines of code into this if block.
[06:06] If I try to execute this code this time, I'm not going to get any runtime exception and I'm going to
[06:13] get expected output.
[06:14] So whatever logic that we have outside of this run scope.
[06:19] So this code is never going to be executed because the east bound method is returning the false value.
[06:24] So please make sure you are aware about the important methods available inside the scoped value.
[06:30] The first one is new instance.
[06:32] Using this, you should be able to create a scoped value that can store any kind of data.
[06:38] Next, by using this where you should be able to assign some data followed by.
[06:42] By using this run, you can start initiating the scope of the scoped value, and by using these use
[06:48] bound method, you can check whether a value is bounded to the given scoped value variable.
[06:54] Let's see another example to see the demo of nested scoping.
[06:58] I'll try to create a new class with the name Nested Scope.
[07:04] Inside this class, I'm going to paste few lines of code which we discussed already as part of the slides.
[07:10] Let's try to understand what code I have written inside this class one more time.
[07:14] So first I have created a scope to value with the name level.
[07:18] From this outer method, I'm trying to invoke the where method and assign the level one value.
[07:23] So whatever logic that we are trying to assign as part of these run method, they are going to have
[07:28] the value as level one.
[07:31] So at this point of execution, level one will be printed and even here as well, level one will be
[07:38] printed next inside the inner method.
[07:40] So this System.out.println.
[07:42] It is going to print level one followed by.
[07:45] Since we are trying to invoke the where and run one more time inside this method, the Java is going
[07:50] to create a nested scope with the new value level two.
[07:54] So this nested scope value level two will be accessible inside this run method.
[08:00] So here we are going to get level two.
[08:02] And since we are invoking the deep method again, this deep method value also is going to have access
[08:08] to the level two scoped value outside these run logic.
[08:12] We are going to have the scoped value as level one, which is from the outer scope.
[08:18] We can confirm the same by executing this main method.
[08:21] As you can see we have level one, level one, level two, level two, level one and level one.
[08:26] I hope it is making sense to you on how to build the nested scope by using the scoped value.
[08:33] The beauty of scoped value is as soon as I run, logic is executed, the corresponding scope to value
[08:40] like level two will be deleted automatically by the Java library itself.
[08:45] The developer.
[08:46] They don't have to invoke the remove method manually like they have to do for Threadlocal.
[08:52] If you are building multithreading logic, please make sure to use the scoped values, especially the
[08:57] scoped values that are going to change a lot in the scenario of virtual threads.

----------------------------------------
