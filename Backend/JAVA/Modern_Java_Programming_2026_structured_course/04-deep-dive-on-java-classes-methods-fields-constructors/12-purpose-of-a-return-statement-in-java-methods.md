# 4.12 — Purpose of a return statement in Java methods

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture
[00:01] let me talk in detail about this return statement.
[00:04] As of now, you can see inside the sum() method we are trying to return a variable result, which is going
[00:10] to hold the value that we calculated by adding two input parameters like num1 and num2.
[00:17] Sometimes you may see developers directly mentioning the expression inside the return keyword itself.
[00:24] For example, instead of me writing these two lines, I can try to combine these two lines and write
[00:30] return num1 + num2.
[00:34] After that, I need to mention the semicolon.
[00:37] You can see this is also completely perfectly fine, because I'm trying to send the output from these
[00:43] additions and the same
[00:44] I'm trying to return to the caller of this method, so this is also perfectly fine.
[00:49] In the coming sections,
[00:50] I'm also going to show you the demo of how to write some complex expressions as part of your return
[00:57] statement.
[00:57] Apart from using these variables and expressions, if needed, we can also directly return a hard coded
[01:04] value like I can say return 30 here
[01:07] this is also completely valid statement because I'm trying to return a hard coded value, which is 30,
[01:13] and this 30 is matching with the primitive data type that I have mentioned here, which is int.
[01:19] That's why my compiler does not going to throw any errors and simply accept these output.
[01:25] If I try to change this 30 to String value by mentioning double quotes, and you can see my compiler
[01:30] is throwing an error because we're trying to return a String value, whereas the return type of the
[01:35] method is mentioned as int.
[01:38] Since there is a mismatch, you're going to get a compilation error.
[01:42] So let me revert back to the previous code changes.
[01:45] To revert back to the previous code changes, you can always press command+Z inside the mac, whereas
[01:51] inside the windows you can press Ctrl+Z.
[01:54] So let me press command + Z multiple times so that all the code will be reverted back to the original
[02:01] code that we have written.
[02:02] And the next scenario that I want to discuss here is, if you go to the Car class here, we have a method
[02:08] with the return type as void.
[02:10] That means this method is not going to return anything even in these kind of scenarios
[02:15] also, I can mention the return keyword, but I should not provide any output value or Java expression
[02:23] to the return keyword.
[02:24] I should simply mention return followed by colon, and this is completely optional, and it is also
[02:32] not a standard to mention this return.
[02:34] This is a bad code practice because it is very obvious for your Java compiler.
[02:39] As soon as it executed the Java statements inside the method body, it has to return back to the caller.
[02:45] That's why we don't have to explicitly mention that return keyword in the scenarios of void methods.
[02:52] You can see I'm also getting an warning saying that return is unnecessary as a last statement in a void
[02:58] method.
[02:58] So that's why never ever try to mention this, though it is technically possible.
[03:04] So what is the purpose of return keyword inside any Java method?
[03:07] With the help of return keyword, we are trying to give control back to the caller.
[03:13] So when someone invoked our Java method, all the Java code that we have written inside our Java method
[03:18] will be executed.
[03:20] And at last, with the help of return keyword, we are telling to the compiler I am done executing.
[03:26] Please take the control back to the caller method.
[03:29] If there is an output, the output will be carry forwarded to the caller method.
[03:33] In case of void methods, the control simply return back to the caller method.
[03:38] So that's the purpose of return keyword, and it is also perfectly fine to have multiple return statements
[03:45] inside your Java methods.
[03:47] I know this might be very surprising to you, but when we start writing our Java programming with the
[03:53] help of conditional statements or conditional logic, in such scenario, we can mention the return statements
[03:59] in multiple places inside your Java method.
[04:02] We are going to discuss about this scenario in the coming sections,
[04:05] when we are enhancing our Java programs with the help of conditional flows or conditional logic.
[04:11] All the points that I have discussed inside this lecture, I have mentioned the same inside this slide
[04:16] for your reference.
[04:17] So please always read these points to quickly brush up your Java knowledge.
[04:22] I hope you are clear with the purpose of return statement in a method.
[04:25] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
