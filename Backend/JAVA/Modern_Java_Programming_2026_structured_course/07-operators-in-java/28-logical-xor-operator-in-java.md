# 7.28 — Logical XOR operator in Java

> Section 7: Operators in Java

[00:00] Inside this lecture, let's try to talk about logical XOR
[00:05] operator.
[00:06] We should not call this operator as XOR operator.
[00:09] We can either call it as XOR or Exclusive OR operator.
[00:15] The symbol that we need to use for this is caret ( ^ ) symbol.
[00:18] So this carrot symbol, you can find it on top of the number six inside your keyboard.
[00:23] When I say caret it's not vegetable carrot which we eat.
[00:27] The correct correct spelling is c a r e t.
[00:30] The syntax to use is logical
[00:32] XOR operator is, in between your operands
[00:36] we can use the caret operator.
[00:38] The rules that these operator is going to follow is,
[00:41] if both of your operands have same values, then you're always going to get the output as false,
[00:48] otherwise, if both of your operators have different values, then you're going to get the output as
[00:53] true.
[00:54] So the same you can see inside the table.
[00:56] I can tell you a shortcut to remember this table rules whenever you're talking about Logical XOR operator,
[01:03] think about the rules of electricity.
[01:05] Just like in electricity, we have a rule which is like charges
[01:10] they always repel each other, whereas unlike charges they always attract each other.
[01:16] So the same rules applies here.
[01:18] If you are having the same values in both operands, you're always going to get the negative output
[01:23] which is false.
[01:24] Whereas if you have different values like true and false, false and true, then in such scenarios you're
[01:31] going to get the positive output, which is true.
[01:33] And for this operator there is no short circuit operator.
[01:37] Do you know what is the reason?
[01:39] The reason is very simple.
[01:40] If you look at the table in order to derive the overall result, my Logical XOR operator always need
[01:48] to look both of the operands.
[01:50] That's why there is no Short-circuit operator for the exclusive OR operator.
[01:55] I hope it is clear.
[01:56] Now let's try to see a few code examples on how to use this or operator.
[02:01] You can see I have mentioned some expressions.
[02:03] With the help of Num1 and Num2 variables
[02:06] you should be able to guess the output very easily,
[02:09] if you understand the rules that I have mentioned in the table.
[02:12] Let's try to evaluate the very first expression.
[02:15] In the very first expression on the left hand side, I have an expression which is num1 greater than
[02:20] five.
[02:21] Since nine is greater than five, I'm going to get the output as true and the left hand side
[02:25] and now on the right hand side,
[02:27] since my num2 < 10 here
[02:30] also, I'm going to get the output as true.
[02:33] So for your Logical XOR operator, if both operands are true, then obviously the output is going to
[02:39] be false.
[02:40] Very similarly, you can also try to evaluate other expressions as well
[02:43] here, let me show you the demo of the same example inside IntelliJ inside my LogicalOperatorsDemo
[02:49] class, I'm going to create a boolean variable c, and to this I'm going to assign an expression, which
[02:57] I'm going to build with the help of Logical XOR operator
[03:01] or Exclusive operator.
[03:03] First, on the left hand side, I'm going to write an expression which is num1 greater than five, followed
[03:10] by I'm going to mention the caret symbol.
[03:12] And on the right hand side I'm going to write an expression which is num2 less than ten.
[03:17] So if I try to execute this line of code, I'm going to get the output as false.
[03:22] I can also confirm you that by printing these variable c.
[03:25] So let me try to execute this program.
[03:27] At the end you can see we are getting the output as false.
[03:31] Whereas if you try to change one of the operand to give the different result, then you're going to
[03:37] get the output as true.
[03:38] Let me change this less than symbol to the greater than.
[03:42] And with that and the left hand side, I'm going to have true
[03:45] and on the right hand side I'm going to have false.
[03:47] That's why the overall result I'm going to get as true.
[03:51] That's what we can see on the console as well.
[03:53] I hope you are clear with this demo and explanation.
[03:56] Before I try to close this lecture, I want to share an important update inside the Java programs that
[04:02] we are writing.
[04:03] You will be seeing a lot of warnings.
[04:05] You can see there is a warning and the variable name isValid.
[04:09] The warning says I have declared this variable, but nowhere I'm using this variable inside my business
[04:14] logic.
[04:15] So these kind of warnings you may get inside your code as well.
[04:19] If you follow my examples for now, please ignore all these warnings.
[04:23] Like I said before warnings.
[04:25] They are not going to stop your program execution.
[04:28] Even with 100 warnings or 1000 warnings, you can still execute your program, whereas compilation errors
[04:35] we should be solving all of them.
[04:38] Even if you have a single compilation error, you will not be able to run your program.
[04:42] Since we are learning the Java program by taking some baby steps, you may get these warnings, but
[04:48] in real projects, you should put a very good amount of efforts to make sure that your program has zero
[04:55] warnings.
[04:56] Think like you are working in a project and inside the project you have written
[04:59] a logic and as part of your logic, you have created so many variables which you are not using inside
[05:05] your business logic.
[05:06] Obviously, in such scenarios you're going to get these kind of warnings and whoever is doing your code
[05:11] review, maybe your team lead or your manager.
[05:14] So they will simply ask you why you have created these variables if you are not using them.
[05:19] So to avoid such scenarios, please make sure you are resolving all the warnings before you are trying
[05:24] to submit your code for your lead review or for your manager review.
[05:29] But throughout this course, you don't have to worry about these warnings because we are just learning
[05:33] the operators are basics of Java.
[05:36] We have not reached a level where we build the complete business logic inside a class.
[05:40] When we reach to that complexity, then we can focus on these warnings and make sure there are no warnings
[05:46] inside our program.
[05:47] I hope you are with me
[05:48] thank you and I'll catch you in the next lecture bye.

----------------------------------------
