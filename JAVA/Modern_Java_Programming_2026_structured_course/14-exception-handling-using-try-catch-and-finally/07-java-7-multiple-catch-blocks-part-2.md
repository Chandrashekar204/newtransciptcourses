# 14.7 — [JAVA 7] multiple catch blocks - Part 2

> Section 14: Exception handling using try, catch and finally

[00:00] Sometimes, while we are trying to define multiple catch blocks to handle different kinds of exceptions
[00:07] with a different exception handling logic, you may have a requirement which is to have a same exception
[00:14] handling for few set off exceptions.
[00:17] For example, as of now you can see we have a catch block to catch an exception of StringIndexOut
[00:22] StringIndexOutofBoundsException.
[00:23] Very similarly, I may want to add one more catch block to handle the exception, which is array index
[00:31] ArrayIndexOutofBoundsException.
[00:32] Think like for a second that we want to have a same business logic are same exception handling logic
[00:39] to be executed for these two exceptions because they both extend the same class like index out of bound
[00:47] IndexOutofBoundException.
[00:47] So these kind of exception happens whenever you are trying to access an index which is not available.
[00:54] It can be inside an Array or it can be inside String object.
[00:57] That's why having a same business logic or same exception handling logic for these kind of exceptions
[01:03] makes sense.
[01:04] So in these kind of scenarios, instead of repeating that two catch blocks multiple times, we can have
[01:11] a single catch block which is capable of handling multiple exceptions.
[01:15] Let me show you how to achieve the same.
[01:17] So to handle multiple exceptions with a single catch block, you need to use the pipe symbol after an
[01:25] exception data type.
[01:26] As of now you can see I have the first exception data type as StringIndexOutofBoundsException.
[01:31] After mentioning the space pipe symbol, I need to mention one more space and post that I can mention.
[01:37] What is a second exception.
[01:39] So with this
[01:40] single catch block is capable of handling both these exceptions that we have configured here.
[01:46] We are getting a compilation error here because we already handled these exception in the second catch
[01:52] block.
[01:52] That's why let me remove this and post that
[01:55] I'm going to update the statement as IndexOutofBoundsException occurred.
[02:01] Please check your input data so the data can be it can be a string data or it can be an array data.
[02:07] That's why I'm trying to have a generic statement here for these two kinds of exception.
[02:12] So the syntax that we are discussing right now, which we can mention multiple exceptions in a catch
[02:17] block with the help of a pipe symbol, is introduced as part of the java7.
[02:23] Before Java seven, developers are forced to define multiple catch blocks, even though the business
[02:29] logic or the exception handling logic is same for different exceptions.
[02:33] But from java7, we can happily use this syntax that right now we are discussing.
[02:38] And here you should not be under the assumption that we can only handle two exceptions.
[02:42] With this kind of syntax, we can handle any kind of exceptions with this pipe symbol.
[02:48] For example, after the ArrayIndexOutofBoundsException, I can mention the space pipe symbol space,
[02:55] and I can mention some other exception.
[02:57] Like I can try to mention some other exception which is InputMismatchException.
[03:02] This way we can add any number of exceptions to the same catch block.
[03:08] By using these pipe symbol and all these exceptions, they are going to have a single object reference
[03:14] variable name which is ex, because at any time your code is going to throw only one type of exception,
[03:22] but not all three types of exception.
[03:24] In the scenario where your code is going to throw InputMismatchException, then this ex object reference
[03:30] it is going to hold the object of InputMismatchException class.
[03:35] There is a guideline or a restriction that you need to be aware whenever you are using this syntax.
[03:40] The restriction is whatever object reference that you are trying to assign to these multiple exceptions.
[03:47] Inside your catch block, this is going to be final.
[03:50] You will not be able to assign a new value to these ex object inside the catch block body.
[03:57] For example, I can show you a demo.
[03:58] Before that, let me remove this unnecessary exception that we have here.
[04:03] Post that inside the catch block body, I'm going to assign a new object of some exception like
[04:10] ArrayIndexOutofBoundException.
[04:12] With that, you can see we are getting a compilation error saying that cannot assign a value to the
[04:17] final variable ex.
[04:18] We didn't mention final before this ex, but behind the scenes, whenever you are going to use this syntax,
[04:25] the object reference, it is going to be implicitly final.
[04:29] That's why we are seeing a restriction here, which is we are not able to assign a new value to the
[04:35] object reference that we have defined inside this catch block.
[04:39] I hope you are clear with these new syntax.
[04:41] Whatever we have discussed around the multiple catch blocks, I have mentioned the syntax and the important
[04:47] points around them in these two slides.
[04:50] Here in this slide you can also see I have highlighted that these syntax, which we can build with the
[04:55] help of pipe symbol is only available from the java7.
[04:59] So
[05:00] please make a note of that.
[05:01] Thank you, and I'll catch you in the next lecture bye.

----------------------------------------
