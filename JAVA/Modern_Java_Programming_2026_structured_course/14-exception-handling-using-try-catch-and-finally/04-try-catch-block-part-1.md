# 14.4 — try-catch block - Part 1

> Section 14: Exception handling using try, catch and finally

[00:00] It might be a super surprising fact for you that our programs are throwing runtime exceptions, but
[00:06] don't worry, I'm going to teach you on how to handle the exceptions inside your Java program inside
[00:12] Java.
[00:13] To handle the exceptions, we need to build the try and catch block inside our Java code.
[00:19] We know that an exception is an event that can occurs during the execution of a program that is going
[00:26] to disrupt the normal flow of the program
[00:29] instructions.
[00:30] Let's see how to handle a runtime exception.
[00:33] Whenever you are trying to write a piece of logic inside a Java method, which may potentially throw
[00:39] an exception at runtime, all such code, you need to define them inside that try block.
[00:45] So how to define a try block?
[00:47] First you need to mention the try keyword, followed by the opening and closing curly braces.
[00:52] Inside this try block, you can write all your Java code which you feel it is a risky code, even if
[00:59] you have 1% of doubt on your code that it may throw an exception, then it is always advisable to keep
[01:06] all such code inside the try block immediately after the try block, you should also write the catch
[01:12] block.
[01:12] So what is the purpose of catch block?
[01:14] Inside the catch block, we are going to write the logic that needs to be executed in case of a runtime
[01:21] exception happens.
[01:22] So if you closely look at the screenshot that I have provided in the slide, the format that you need
[01:27] to follow to define a catch block is, first you need to mention the catch keyword, followed by inside
[01:33] the parentheses you need to mention what is the exception type.
[01:38] Are you talking about an ArrayIndexOutOfBoundsException or are you talking about
[01:44] InputMismatchDataException.
[01:45] Are you talking about a NullPointerException.
[01:47] So you need to define your exception type along with a object reference of it.
[01:52] Post that inside the curly braces of your catch block
[01:55] you can write all the code that needs to be executed in case of a runtime exception happens based upon
[02:03] the code that is being executed inside the try block.
[02:06] So these are very quick introduction, but I know you may have some confusion or you may have some questions.
[02:12] That's why let's go to our Java programs and try to implement these
[02:17] try and catch block and see how the behavior is going to be changed once we implement these try and
[02:23] catch blocks.
[02:24] As of now you can see inside my exception demo class, I have a main() method inside my main() method.
[02:29] I have written all these Java code.
[02:32] As of now
[02:32] we know that there is a good chance that I may get exception while I'm executing these highlighted code.
[02:39] That's why I'm going to first create a try block with the help of try keyword, followed by opening
[02:45] and closing curly braces.
[02:47] After that, I'm going to move all this code into that try block.
[02:52] If you only try to define a try block, you're going to get a compilation error.
[02:56] That's why let's try to define a catch block
[02:59] immediately after that, try block I need to type catch keyword post that I need to mention the parentheses
[03:06] followed by the curly braces inside the parentheses.
[03:09] We need to mention what is the exception type that we are targeting.
[03:13] So as of now we are trying to handle the exception type which is InputMismatchException.
[03:20] After mentioning the exception data type I need to mention an object reference.
[03:25] It can be an ex or exception
[03:27] so using these object reference I can try to find out more details about an exception inside my catch
[03:34] block.
[03:35] For example, using the ex, I can try to invoke many other methods available inside the Exception object.
[03:42] Few of the common methods that most of the developers they are going to invoke is getCause(), getMessage(),
[03:49] getStrackRrace().
[03:50] So these methods are going to provide you more details about your exception.
[03:56] For example, I can try to print out cause details with the help of getCause().
[04:01] So if I try to execute this program now, this time I'm going to enter the three as an input.
[04:07] And if I press enter you can see this time the program did not shut down abruptly.
[04:13] Instead the execution went to the catch block.
[04:16] And the reason why my program did not executed completely is the input data that is provided by the
[04:22] end user is invalid.
[04:24] That's why behind the scenes it is converted into a null value.
[04:28] So that's a cause determined by the Java for this scenario.
[04:32] Maybe I can try to keep a breakpoint inside my catch block and try to execute the program one more time.
[04:38] So this time also I'm going to enter three.
[04:40] So if I press enter you can see the execution stopped inside the catch block and inside the exception
[04:46] object I will be able to see lot many details like under the cause.
[04:50] You can see the detail message we have here is null.
[04:53] That's why we are getting the same null inside the output.
[04:56] Whereas if you try to look for other details maybe
[05:00] stackTrace() you'll be able to see complete details why an exception happened.
[05:04] Maybe this time I can try to invoke the stackTrace() method.
[05:08] Let me resume my program and this time I'll try to invoke getStackTrace() method post that
[05:15] I'm also going to write a statement which is exception handled.
[05:21] So this is just a dummy statement I want to put to demo you that that this statement is also going to
[05:27] be executed, even though a runtime exception happened inside the try block.
[05:32] So let me execute the program this time I will try to enter three again and post that
[05:37] I'm going to release the program, and inside the console you can see we are having an information based
[05:44] upon the method that we have invoked which is getStrackTrace() .
[05:47] It is trying to print the object related to the exception, which is not making any sense to us.
[05:53] We are going to fix that.
[05:54] But if you observe the next line here, we have a statement which is exception handling.
[05:58] That means our program is getting shut down gracefully after executing all the code that we have written
[06:05] inside the catch block.
[06:06] I hope you are understanding this time
[06:08] instead of getStackTrace(), I'm going to invoke the printStackTrace() method is an utility method
[06:14] which is available inside all exception objects.
[06:18] So as soon as I try to invoke the printStackTrace() method and getting an compilation error because the
[06:24] printStackTrace() method is going to return void.
[06:27] That's why I'm getting an compilation error.
[06:29] So whenever you're trying to invoke the printStackTrace() method of an exception, you don't have to
[06:34] specifically use the System.out.println().
[06:37] If you can simply mention ex.printStackTrace(), all the exception details will be printed onto the
[06:44] console.
[06:45] I can also show you a demo here.
[06:46] I'm entering a invalid data which is three and releasing the breakpoint.
[06:52] You can see all the exception details are printed onto the console and at last there is also a statement
[06:59] which is exception handled printed based upon the code that we have written inside the catch block.
[07:05] So this should give a confirmation to you that the catch block is going to be executed only in the scenarios
[07:11] of runtime exception, which is matching with the type of InputMismatchatchException.
[07:16] If my program is executing properly, then only the logic inside the try block is going to be executed.
[07:23] Let's see a demo around this.
[07:24] This time I'm going to enter a proper input value, which is three in a numerical format.
[07:31] If I press enter, you can see I'm just getting the output three based upon the logic that we have written
[07:36] inside the try block.
[07:38] And my catch block is never going to be invoked as of now.
[07:42] Inside our catch block, we're just printing the exception details, which is not going to make any
[07:47] sense to the end user.
[07:48] That's why what we are going to do is I'm going to replace this System.out.println() content with a message
[07:56] saying that please provide input in numerical format only.
[08:03] So this is the message that I want to show to the end user whenever there is an exception happened due
[08:09] to invalid input data.
[08:11] So this time I'm going to execute the program and my end user, he's going to enter an invalid data
[08:18] and press enter.
[08:19] And you can see the end user is getting an meaningful message saying that please provide input in numerical
[08:25] format only and try again.
[08:28] And based upon this meaningful message, my end user will try to execute the program again with a valid
[08:34] data.
[08:35] So the handling mechanism can be any logic based upon your business requirements.
[08:40] But this small program, the handling mechanism, is educating the end user about entering a valid data.
[08:46] And nowhere my program is stopping abruptly, and it is not also throwing any runtime exception details
[08:54] onto the console for my end user.
[08:56] If I try to throw all the runtime exception details like InputMismatchException, it is not going
[09:02] to make any sense to my end user.
[09:04] You should only have some meaningful message based upon which he can act upon and re-execute the program.
[09:10] That's what I'm trying to achieve right now with the try and catch block.
[09:14] So let's try to implement try and catch block inside ArrayIndexOutOfBoundExceptionDemo as well
[09:21] in the next lecture.
[09:22] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
