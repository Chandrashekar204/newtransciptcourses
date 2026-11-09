# 8.7 — Ternary operator in the place of if-else statement

> Section 8: Control flow statements in Java

[00:00] While we are discussing about the operators, we talked about ternary operator.
[00:06] Ternary operator is also going to work very similar to the if else statement.
[00:12] Does that mean we can use ternary operator always in the place of if else?
[00:17] Let's try to understand the same inside this lecture.
[00:20] You can see here I have created a Java class with the name TernaryOperator, and inside the main() method
[00:26] I have written an simple if else statement.
[00:30] If my x value is greater than five, I'm going to assign the value 20 to the y variable
[00:36] otherwise I'm going to assign the value as 30.
[00:39] So here, since my x value is ten, the if statement is going to be executed and the final output we
[00:46] are going to get as 20.
[00:48] Now I'm going to build a same behavior with the help of ternary operator.
[00:53] So let me do the same.
[00:55] Before that, let me comment these blocks of code after this commented code, first I'm going to mention
[01:02] y is equal to and as part of the ternary operator.
[01:06] First we need to mention what is the boolean expression that needs to be executed.
[01:11] So the expression is going to be x greater than five.
[01:15] If x greater than five then I want to assign value as 20 to y otherwise 30.
[01:22] So after this expression we need to mention question mark.
[01:25] And what is the value that we want to assign
[01:28] in the case of true we want to assign the value as 20
[01:31] otherwise we want to assign the value as 30.
[01:33] So with this ternary operator also we are going to get the same output.
[01:37] And here you can see there is an advantage with the ternary operator.
[01:42] Like with the help of ternary operator we can write a very compact code within a single line
[01:48] I'm able to achieve my business logic, whereas with the if and else statements, we need to write at
[01:54] least a five lines of code, which will make your business logic lengthy.
[01:58] Does that mean we can always use a ternary operator in the place of
[02:02] if else?
[02:03] off course not.
[02:04] Let's try to understand under which scenarios we can use ternary operators.
[02:09] You can only use the ternary operator if your business logic has only a single statement to be executed.
[02:16] So here I have a single statement to be executed in the case of true, and similarly in the case of
[02:22] false
[02:22] also, I have a single statement to be executed.
[02:25] So as long as you have a single statement to be executed, and both of the statements that you have
[02:30] mentioned here, if they are returning the same value as an output from your expression, then in these
[02:37] kind of scenarios, you can always use that ternary operator.
[02:40] But if you have a business logic where you want more than one statement to be executed in the scenario
[02:47] of true and in the scenario of false, then in those scenarios, obviously you cannot use that ternary
[02:53] operator.
[02:54] You should always go with the if and else statement.
[02:57] For example, think like after assigning these value 20
[03:01] I also want to print out a statement.
[03:03] So after 20, if I try to write any code, I'm going to get the compilation error.
[03:08] Because inside the ternary operator expression only one statement is allowed, whereas inside your if
[03:14] block or else block you can write any number of statements.
[03:18] So these are one of the major difference.
[03:20] And one more important note that you need to be aware is, you can send this ternary expression as an
[03:26] method input argument, but you cannot send your if else statements as an method input arguments.
[03:33] I can also show you a demo here.
[03:36] First, let me try to create a static method.
[03:38] So I'll type public static void sum().
[03:44] And to this method I'm going to accept two variables like int x and int y.
[03:49] So inside this method I'm simply going to print out a statement by adding the x and y values.
[03:56] So there is a sum() method inside my class.
[03:59] And this sum() method is going to accept two input method parameters.
[04:03] While I'm trying to invoke this sum() method, I can pass this entire ternary expression as an one of
[04:09] the method input argument.
[04:11] Let me show you that very quickly here.
[04:13] So just after my System.out.println() statement, I'm going to invoke the sum() method and to the sum() method
[04:19] the very first parameter I'll send the x variable.
[04:22] And after the first method argument
[04:24] regarding the second argument, I can pass this entire ternary expression as an one of the method input
[04:32] argument.
[04:33] So this expression is going to be evaluated at runtime.
[04:36] Since my x is greater than five, this expression is going to send the method input argument value as
[04:43] 20.
[04:43] We can also confirm the same by keeping a breakpoint inside my sum() method.
[04:48] If you see here the x value holds ten and the y value holds 20.
[04:52] If I try to release this breakpoint, you'll be able to see that 30 as an output.
[04:57] So this is one of the advantage with the
[05:00] ternary operator.
[05:01] But if you try to do the same with the if and else block like if you try to send this if else block
[05:07] as an method input argument, it is not going to work.
[05:12] You are simply going to get the compilation error.
[05:15] You can see here we are getting the compilation error.
[05:18] So these are the important point that you need to be aware whenever you have confusion to use ternary
[05:24] operator or if else statements.
[05:27] I'm assuming you are clear based upon our discussion.
[05:29] For your reference, I have mentioned all the important points that we have discussed inside this slide.
[05:34] In future
[05:35] if you have any questions or confusion around ternary operator and if else statements, always please
[05:42] refer to this slide.
[05:43] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
