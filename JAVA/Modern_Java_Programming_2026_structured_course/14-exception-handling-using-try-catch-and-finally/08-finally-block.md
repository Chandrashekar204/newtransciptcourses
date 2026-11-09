# 14.8 — finally block

> Section 14: Exception handling using try, catch and finally

[00:00] Inside this lecture, let's talk about the finally block that we can write as part of exception handling
[00:07] inside Java programs.
[00:09] As of now, when we are trying to define a try block and a catch block, we are writing the respective
[00:15] business logic that we want to be executed as part of the try block and as part of the catch blocks.
[00:21] But sometimes you may have a business logic which needs to be executed in both scenarios, regardless
[00:28] of an exception is being thrown or not.
[00:31] You want a piece of logic to be executed in all type of scenarios.
[00:35] To solve this kind of challenge, you may be thinking to repeat the code in both the try block and catch
[00:43] block, but that is not necessary.
[00:45] Instead, we can go with the finally block.
[00:48] So what is the purpose of finally block inside Java?
[00:50] Using this block, we can write a piece of code that is going to be executed regardless of whether an
[00:57] exception is thrown or not.
[00:59] So how to define this
[01:00] finally block.
[01:01] This finally block should be declared after the try and catch blocks you can see.
[01:06] First we need to make sure there is always a try block followed by
[01:09] we can define any number of catch blocks and at last we can define a finally block.
[01:15] Inside the finally block, we can write the code that needs to be executed in happy scenario, or even
[01:21] in the exception scenario as well.
[01:23] But here you may have a question which is what kind of code we usually write inside the finally block.
[01:29] Before I try to answer that, let me tell you that finally block is always optional.
[01:34] It is not mandatory to define finally block after each and try catch blocks.
[01:40] But coming to the scenarios where we have to define this finally block is maybe you want to release
[01:46] some resources, or you want to close some files, or you want to perform some cleanup activities or
[01:52] cleanup tasks that needs to be executed regardless of the outcome of the code in the try block.
[01:58] In all such scenarios, you can use the finally block.
[02:02] I hope you are clear.
[02:03] Let me show you a quick demo around this finally block so that it will be super clear for you.
[02:08] Inside this ExceptionDemo class, we have a logic which we have written with the help of Scanner object.
[02:15] We know a thumb rule that we need to follow whenever we are using or
[02:19] whenever we are creating a Scanner object which is at the end of the program, we need to make sure
[02:24] we are closing the connection with the InputStream by invoking these close() method.
[02:28] But with this logic that we have written think like if I get an exception at line number 12, in this
[02:34] kind of scenarios, straight away, the catch block is going to be executed.
[02:38] And with that line number 14 never going to be executed.
[02:43] So what is going to happen in such scenarios?
[02:45] We are not closing the Scanner object inside production applications
[02:49] if you write these kind of buggy code, you will end up having lot of open connections or lot of memory
[02:56] leaks.
[02:56] So to avoid these kind of situations only we have finally block.
[03:00] So how to define a finally block?
[03:02] After that try and catch block you can type finally keyword.
[03:06] And inside this finally block we can write these piece of code which is scanner.close().
[03:12] So let me remove this code from try block and paste it inside the finally block.
[03:17] But you can see I'm getting a compilation error saying that cannot resolve the symbol scanner.
[03:22] This is because I have created the variable scanner inside the try block.
[03:27] So the scope of this scanner variable is going to be limited to these try block only.
[03:32] But since we are trying to access right now outside of the try block which is inside the finally block
[03:38] and getting a compilation error. To resolve this issue, I can simply try to perform the initialization
[03:45] just outside the try block, saying that Scanner scanner = null.
[03:51] You can see here,
[03:52] first, I am trying to create an object of Scanner without assigning any object to it.
[03:58] So it is a simply a null object.
[04:00] Later on inside the try block, I can simply assign the new object that I am trying to create with this
[04:07] code to the same variable.
[04:09] So with this now my finally block also will be able to access this variable.
[04:13] But what if we are getting an exception at this line of code only?
[04:18] That means when you are trying to create an object of Scanner, maybe there is an exception.
[04:22] In such scenarios, the Scanner will be null and inside the
[04:26] finally we are going to execute the code which is null.close().
[04:30] and with that we'll get a NullPointerException.
[04:33] So to avoid NullPointerExceptions what we can do is we can only execute these close related logic
[04:40] if the Scanner is not null.
[04:42] So how to check if the Scanner is not null?
[04:45] I need to use the exclamatory mark followed by is equal to followed by null.
[04:49] So if the Scanner object is not null, then only I'm going to perform the close() operation.
[04:56] Otherwise there is no need of close operation because the object itself
[04:59] is not created.
[05:00] That's why there is no meaning of trying the close() operation. To demo you, that the finally block is
[05:07] going to be executed in all type of scenarios.
[05:10] I can have a System.out.println() statement and to this statement I can pass a String value which is
[05:18] finally block is being executed.
[05:22] First, let me show you a happy scenario where I'm going to enter a proper data.
[05:27] So I'm trying to execute this program and I'll try to enter a number which is three.
[05:32] And you can see we are getting the output from the try block.
[05:35] Once the try block is completely executed, the finally block also is executed.
[05:41] This time I'll try to give some invalid input data.
[05:45] Maybe I'll try to give three in alpha value.
[05:48] Now if I try to press enter, you can see I'm able to see the statement that we have inside the catch
[05:54] block, and after the catch block is executed, we are also able to see the statement that we have inside
[06:00] the finally block.
[06:02] So this confirms our finally block is going to be executed in all type of scenarios, whether an exception
[06:09] happened or not inside your try block.
[06:11] So when to use this finally block?
[06:13] We need to use this finally block, especially in the scenarios where we want to close the connections,
[06:18] or we want to close a file or a database connection, or you want to perform any cleanup activities
[06:24] in all such scenarios, please use the finally block.
[06:28] But inside your method, if you're not performing any IO operations where you open some connections,
[06:34] in such scenarios, you don't have to define the finally block.
[06:37] You can simply live happily with the try and catch block.
[06:41] I hope this is clear.
[06:42] Thank you,
[06:43] bye.

----------------------------------------
