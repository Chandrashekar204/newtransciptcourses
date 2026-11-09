# 14.6 — multiple catch blocks - Part 1

> Section 14: Exception handling using try, catch and finally

[00:00] As of now, inside the Java programs that we have developed, we only have a single catch block after
[00:06] the try block.
[00:08] But in real project you may write hundreds of lines of code inside your try block and all the lines
[00:15] of code that you have written inside the try block.
[00:17] They may result into different types of exceptions, so having a single catch block may not be sufficient
[00:24] in such scenarios.
[00:25] Even inside the real projects, the business requirements will be super complex.
[00:30] For example, you may have a requirement in case of null pointer exception.
[00:35] Handle the exception this way or in case of array index out of bounds exception.
[00:40] Handle the exception this way.
[00:42] This kind of lot of business requirements you may have inside real projects based upon the type of exception.
[00:49] To handle these kind of scenarios, we can't live with a single exception, which is going to handle
[00:54] all kind of exceptions.
[00:56] Like you can see, this catch block is capable of handling all the exception, but unfortunately this
[01:02] catch block is going to have a common business logic for all kinds of exceptions.
[01:08] That's not a good practice to have a common logic for different kinds of exceptions, we should build
[01:13] different different handling logic based upon different, different exceptions.
[01:18] That's why to handle these kind of scenarios, Java allows you to define multiple catch blocks.
[01:24] And inside these multiple catch blocks, you can handle multiple exceptions and you can define different
[01:31] kinds of exception handling logic.
[01:34] Let me show you an example so that it is going to be super clear for you.
[01:37] For the same, I'm going to create a new Java class inside the package com dot easy bytes dot exception.
[01:44] The class name is going to be multiple catch demo inside this class.
[01:51] First, as usual we need to create the main method, followed by.
[01:54] I'm going to write a piece of logic inside this main method, which may result into multiple types of
[02:00] exception.
[02:01] Based upon the logic that I am writing.
[02:03] First, I'm going to define a string object with the name input.
[02:08] So these are simple variable that I have defined here.
[02:11] So these kind of simple declarations they will never throw any runtime exception.
[02:16] What is there here to throw a runtime exception.
[02:19] That's why all kind of declarations usually developers they will keep outside the try block.
[02:25] We don't have to keep the safe code inside that try block unnecessarily.
[02:28] That's why I'm trying to declare this input variable outside my try block, followed by I'm going to
[02:33] create the try block, followed by catch block.
[02:36] Inside this catch block.
[02:37] First I'm going to handle a null pointer exception.
[02:41] That's why I'm going to mention null pointer exception with the object reference as x.
[02:47] Now as a next step inside my try block, I'm going to intentionally create a null pointer exception.
[02:53] So how I'm going to create is using the string input object I'm going to invoke the method to uppercase
[03:00] which is going to help to convert all the letters inside a string object into completely uppercase values.
[03:06] But with this code, I'm getting a compilation error saying that variable input might have not been
[03:12] initialized.
[03:13] Maybe what I can do is I will try to initialize this variable to null, and with that the compilation
[03:19] error is resolved.
[03:19] So the outcome from the two uppercase I'm going to assign back to the input string object itself.
[03:25] With this.
[03:26] At this point of line, I'm going to get the null pointer exception.
[03:30] Why?
[03:30] I'm going to get a null pointer exception because I'm trying to invoke the method on top of a null object.
[03:37] Right now my input string object.
[03:39] It is not having anything stored inside it.
[03:42] Such kind of objects we call them as null objects.
[03:45] Since these try block it is going to throw null pointer exception.
[03:48] This catch block is going to be executed.
[03:51] So inside the catch block I'm going to write some logger statements for the same.
[03:56] First I need to define a logger object.
[03:58] Let me copy the logger object that I have here into the multiple catch demo was that I'm going to copy
[04:05] this class name and replace these array index out of bounds exception demo with the correct class name.
[04:11] With this.
[04:11] Now we have a logger object using which we can do the logging.
[04:14] So inside the catch block I'll just mention logger dot CVR.
[04:19] And to this CVR method I'm going to pass a string object to value, which is an null pointer.
[04:25] Exception occurred after this statement.
[04:29] I'll also mention please check your data.
[04:33] I'm just having some message to the developer or to the end user to recheck his program because we are
[04:40] receiving the null data.
[04:42] So if I try to execute this program, you can see I'm going to get a null pointer exception.
[04:46] That's that's why the logic present inside the catch block is executed.
[04:50] Now this time I'm going to create other kind of exception.
[04:54] Maybe this time I'll just try to define a value inside the input.
[04:59] Hurt with my name.
[05:01] I'll just mention my name.
[05:03] So with this, there won't be any null pointer exception if I try to print these input value with the
[05:09] help of logger info, I will be able to see the proper output.
[05:13] You can see we're able to see the output which is modern, so there is no null pointer exception right
[05:18] now.
[05:18] But let's try to create other kind of exception and see how it is going to behave.
[05:23] So to create other kind of exception I'm going to invoke one of the method available inside string which
[05:29] is substring.
[05:30] To this substring I can pass what is the starting index and what is the ending index.
[05:35] So if I try to mention starting index as one comma three and the output from this, I can assign back
[05:42] to the input and post that I can print the same using the logger.info inputs.
[05:48] So with this code there won't be any exception.
[05:51] You can see we are getting the output which is 80 based upon the substring method, but instead of three
[05:57] I can mention the end index as ten.
[06:00] With this, we are going to definitely get an exception because our string object it has only five characters.
[06:06] That means at a maximum I can send the end index as five, but I'm trying to mention ten.
[06:11] Let's see what is going to happen.
[06:13] You can see I'm getting a runtime exception which is string index out of bounds exception, and this
[06:19] exception I have not handled because there is no catch block to handle the new exception that we are
[06:25] facing.
[06:26] If we change this null pointer exception to the exception, then for all kinds of exception we are going
[06:31] to get the same output.
[06:33] We don't want that because we want to have different different logic for different different kinds of
[06:38] exception.
[06:38] That's why I'm not going to have a generic exception, which is exception.
[06:43] Instead, I'm going to create one more catch block with the type as string index out of bounds exception.
[06:50] And to this.
[06:51] Also I'm going to mention the object reference as x followed by.
[06:55] Inside this catch block, I'll just change the logger message to string index.
[07:01] Out of bounds exception occurred.
[07:03] Please check your string data.
[07:05] So this want I want to log to the end user or to the developer to check his data.
[07:10] Now if I try to execute the program this time, I'm not going to get any runtime exception.
[07:14] Instead, I'm going to get the output that we have written inside the catch block with the exception
[07:21] type as string index out of bounds exception.
[07:23] So this way we can define any number of catch blocks that are capable of handling different kinds of
[07:29] exceptions.
[07:30] With these two catch blocks, my program is only capable of handling null pointer exception and string
[07:36] index out of bounds exception.
[07:38] But what if some other kind of exception occurs inside my try block?
[07:42] Since we can't define catch blocks for all kinds of exceptions available inside Java a class, we can
[07:49] keep a generic catch block.
[07:51] Maybe I can copy this second catch block and mention the same as the third catch block, but this time
[07:58] I'm going to mention the exception, which is a generic exception, and I'll change the logger message
[08:03] to an exception occurred.
[08:06] Please check your program.
[08:09] So this is a generic message I want to throw from the exception block.
[08:13] So now with these three kinds of catch blocks, my program is capable of handling any kinds of exceptions
[08:19] because at the end we have a generic exception.
[08:22] But whenever you are trying to define multiple catch blocks, you need to be aware about a important
[08:28] point.
[08:29] The important point is you should always keep the generic exceptions towards the end.
[08:34] Suppose if I try to keep these exception catch block as a very first catch block, then I'm going to
[08:41] get a compilation error because inside my program, the very first catch block itself is capable of
[08:47] handling all type of exceptions because exception is a generic exception object.
[08:52] With that, these two catch blocks they are going to become irrelevant are absolute.
[08:58] That's why my Java is throwing compilation error saying that exception of type null pointer exception
[09:04] has already been caught.
[09:05] How it is caught with a generic exception object.
[09:08] If you try to open this null pointer exception, you can see it is being extended by runtime exception.
[09:14] If you try to dig into this runtime exception, it is internally extending exception.
[09:18] That means all the runtime exceptions inside Java.
[09:21] They are subclasses of exception class.
[09:25] That's why we are getting these compilation error.
[09:27] So whenever you want to handle multiple exceptions with a different business logic, always make sure
[09:33] you are mentioning the catch blocks of specific exceptions on the top and towards the end you need to
[09:40] keep the most generic exception.
[09:43] I hope it is clear.
[09:44] Let me revert back to the previous code where there won't be any compilation errors.
[09:48] Right now you can see my code is looking perfect.
[09:51] The best practice inside the project is always try to handle a specific exception, and that is going
[09:57] to give some flexibility to you.
[09:59] To handle different, different exceptions with a different, different exception handling logic.
[10:04] But at the end of your catch blocks, please make sure you also have a generic catch block so that if
[10:11] your try block is throwing some other kinds of exception, those exceptions also will be handled with
[10:16] that generic logic that you're going to write.
[10:19] I hope you're clear.
[10:20] Thank you.
[10:20] And I'll catch you in the next lecture by.

----------------------------------------
