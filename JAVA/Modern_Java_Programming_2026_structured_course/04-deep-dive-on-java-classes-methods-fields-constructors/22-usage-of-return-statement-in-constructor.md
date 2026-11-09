# 4.22 — Usage of return statement in constructor

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] You may have some questions around the written statements
[00:03] usage
[00:04] inside the constructor.
[00:05] Let's try to discuss about written statements inside Java constructors and clarify any doubts that we
[00:11] may have.
[00:12] We know that inside the constructor definition we cannot declare a return type.
[00:17] So these are one of the primary difference between a constructor and a Java method.
[00:21] Your Java methods
[00:22] they can declare what is the return type inside that definition, whereas constructors are not allowed.
[00:28] This is because we cannot return any value from the constructors.
[00:32] So inside the constructors we are only allowed to write the code which is related to the initialization
[00:39] of the object variables or other initialization tasks related to your current object.
[00:44] With that reason, we are not allowed to mention return statement inside the constructor body as well,
[00:50] though it is technically possible to use a simple return statement without any expression inside a constructor,
[00:56] but doing so is strongly discouraged as it is considered a poor practice.
[01:01] Let me show you some code screenshots about the return statements inside the constructor.
[01:07] Here
[01:07] in the very first screenshot, you can see I'm trying to return a String value, but do you think this
[01:13] is allowed?
[01:13] Off course this is not allowed.
[01:15] Your code is not going to compile because if you see the constructor definition nowhere we are telling
[01:21] that my constructor is going to return a String data type value.
[01:25] With that reason, the return statement with the Java expression are with a hardcoded value is not allowed
[01:32] inside the constructor body.
[01:33] Now, the very next question you may have here is can I simply mention only return keyword inside my
[01:39] constructor body?
[01:40] Off course this is allowed.
[01:42] Like you can see here, this is perfectly works.
[01:45] Your code is going to perfectly compile if you simply use the return keyword, but it is not recommended
[01:51] to mention the return keyword inside your constructor body, because it is very obvious at the end of
[01:58] the execution of your constructor body, the JVM is simply going to return the control back to the invoking
[02:05] caller or invoking entity.
[02:07] With that reason, just like how inside methods we try to avoid mentioning simply return keyword very
[02:14] similarly inside the constructor
[02:16] also, we should avoid mentioning only the return keyword.
[02:20] I hope this makes sense to you.
[02:22] Now let me quickly show you both of these two examples inside the intellIJ.
[02:27] So here I have two constructors.
[02:29] Let me consider my default constructor to make some changes.
[02:33] So what I'm going to do here is first I'm going to mention return keyword
[02:37] and after the return keyword I'm going to return some String value.
[02:41] Saying that some value is the String value which I want to return.
[02:45] You can see the code is not getting compiled.
[02:48] I'm getting an compilation error.
[02:50] So this confirms we cannot use the return keyword with the Java expression or a hardcoded value.
[02:57] If I try to remove these hardcoded value, the code is going to be compiled, but there'll be some warning
[03:03] saying that return is unnecessary as a last statement in a constructor.
[03:08] So if I try to execute the EmployeeMain, nothing wrong is going to happen.
[03:12] Your code is going to work perfectly without any issues.
[03:16] I can also show you that by running the program in the run mode.
[03:20] Why I want to run in the run mode.
[03:22] Because I don't want to stop my program at some breakpoints.
[03:26] I quickly want to validate the output.
[03:28] That's why I'm trying to click on this run button, and you can see we are getting the output based
[03:34] upon the logic that we have written.
[03:36] So nothing wrong is going to happen if you try to mention simple return keyword.
[03:41] But like I said, it is a bad practice.
[03:44] That's why let's remove this.
[03:46] And with that, the warning that you used to have will be resolved.
[03:50] So inside Java there is a difference between a warning and error.
[03:53] With the warning you can still run your programs, so you may face some warnings whenever you are not
[03:59] following some standards.
[04:01] Whereas with error you will not be able to run your program. Until you fix the error
[04:07] the JVM is not going to allow you to run your Java program.
[04:11] I hope you are clear about the difference between warning and error.
[04:15] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
