# 5.3 — Single line Comments in Java - Theory

> Section 5: Comments in Java

[00:00] Now, inside this lecture, let's try to understand the very first approach that we have to provide
[00:06] comments in Java.
[00:07] This approach is single line comments.
[00:10] Whenever we want to provide comments
[00:12] with this approach, we need to start the comments with the // slashes.
[00:17] After mentioning these // slashes, whatever you are going to write will be considered as a
[00:22] single line command by your Java compiler, so anything after the slashes will be ignored by the compiler.
[00:29] And with that, you are free to use your own words to explain your code.
[00:34] For example, I have provided some single line comments examples inside the screenshot.
[00:39] First, I'm trying to create a variable which is int age and this just a declaration
[00:45] I'm not trying to do any initialization. After the Java statement
[00:48] you can see I'm trying to mention two //, followed by I'm trying to explain more details
[00:55] about this field.
[00:56] So this field represents the age of the customer.
[00:59] So this gives more details to someone who is trying to read my code.
[01:03] Very similarly I'm trying to create the second variable
[01:06] and this variable is a static variable
[01:09] and it is going to be a final.
[01:11] That's why I'm trying to declare this variable name with all capital letters by using Snakecase style.
[01:17] So the variable name here is max retry attempts and it has a final value three.
[01:22] So if I don't provide any comments to these variable, it may confuse other developers.
[01:27] What is the significance that these final variable holds inside a given Java program?
[01:32] So to overcome these kind of challenges, anytime you feel there is a ambiguity inside your code, you
[01:38] can provide the single line comments like you can see this time I have mentioned the single line commands
[01:44] just about the final variable that I have created.
[01:47] So what I have mentioned inside the single line command maximum number of login retry attempts allowed.
[01:54] So this will give more details to any developer that these three value that I have defined inside this
[02:00] variable is representing the how many retry attempts my end user can attempt inside the login page of
[02:07] an mobile application or a web application.
[02:10] I'm assuming you are seeing the power of comments inside Java.
[02:12] With comments
[02:13] we can make our programs more readable and more understandable.
[02:18] After this final variable
[02:20] I have created two other char variables with y and n, and inside these y and n char variables.
[02:26] I'm trying to hold the capital char values Y and N respectively.
[02:31] But what are these
[02:32] Y and N indicates. I can provide more details with the help of single line comments saying that, Y indicates
[02:38] yes and N indicates no.
[02:41] So whenever I'm trying to refer this Y char variable inside my Java program, I'm trying to evaluate
[02:47] an yes scenario.
[02:48] Otherwise N means no scenario.
[02:51] This way we can provide single line comments inside the Java programs.
[02:54] There are some restrictions
[02:56] also, whenever we are trying to use single line comments, one such restriction is we cannot use a
[03:02] single line comments in the middle of a Java statement, because that will make your Java statement
[03:08] invalid and compilation will fail.
[03:10] For example, think like I'm trying to declare a Java statement which is int num = 0;.
[03:18] If I try to put single line comment in between my Java statement like you can see in the screenshot,
[03:23] whatever I have defined after the num variable is going to be considered as a comment by the Java compiler,
[03:30] and with that, my compiler will assume I have not terminated my Java statement with a semicolon, and
[03:37] that's why it is going to throw an compilation error.
[03:40] That's why
[03:40] very careful, whenever you are trying to define single line comments, you can always mention the single
[03:45] line comments on top of your Java statements before the Java statements or after the Java statement,
[03:52] but not in between the Java statement.
[03:55] I also highlighted here with a cross mark saying that this approach is completely invalid.
[04:01] Apart from documenting our Java code.
[04:04] With the help of single line comments, we can also comment out any existing Java code.
[04:10] So what do I mean
[04:11] here?
[04:11] Let me try to explain.
[04:12] Since Java compiler is going to ignore all the code or all the statements just after that
[04:19] //.
[04:19] Sometimes developers
[04:21] they are also going to use this single line comments to comment out any existing code temporarily.
[04:27] For example, inside my main() method I'm trying to invoke other method.
[04:32] This method name is perform() alternative operation.
[04:35] If I put these // just before my method invocation Java statement, it is going to
[04:41] comment that entire line of Java statement.
[04:44] And with that, my Java is never going to invoke the method perform() alternative operation from my main()
[04:50] method.
[04:51] So here you may have question why developers will comment out the code.
[04:55] The reason is very simple.
[04:56] Sometimes developers they want to test their code by
[05:00] removing a piece of logic in such scenarios, instead of blindly removing all the code, they can comment
[05:06] out the code and evaluate the scenario if it is working properly or not.
[05:10] Or there can be some scenarios where the developer might have written some code which he wants to be
[05:16] executed only inside the local system, but not in the production server or inside the dev server or
[05:22] UIT server.
[05:23] In this scenario
[05:24] also the developer, once he tested the code inside his local system, he can comment that code, which
[05:30] he don't want to be executed in the higher environments.
[05:33] So in all these kind of scenarios, developers, they're always going to use this single line comments
[05:39] to temporarily disable the Java code or to temporarily ignore the Java code.
[05:44] I know you may have too many questions here.
[05:46] Let's try to implement these single line comments by taking some examples in the next lecture, so that
[05:52] it will be very clear for you.
[05:54] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
