# 8.5 — Demo of if, else if, else statements in Java - Part 2

> Section 8: Control flow statements in Java

[00:00] Let's try to build more examples using the if statements. For the same,
[00:05] first, I'm going to create a new class here and the class name is going to be NotOperatorExample.
[00:10] .
[00:11] Inside this class I'm going to use the NotOperator along with the if statement to identify if the given
[00:18] number is a zero or not. For the same
[00:20] first, I need to build a main() method, and inside the main() method I'm going to create an int variable.
[00:26] The variable name is going to be number and to this I'm going to assign a value zero.
[00:31] So if this number variable holds a value zero then I want to display an output which is the given number
[00:38] is zero.
[00:39] So how to achieve this with the help of if statement.
[00:43] So I can simply write an if statement.
[00:46] And the condition that I can mention here is, if number is equal to zero, then I can try to print the
[00:53] statement which is the number is zero.
[00:55] So if I try to execute this program, you can see I'm going to get the output as the number is zero.
[01:00] But sometimes you may want your if block to be executed if the given condition is false.
[01:07] So for such scenarios you can use the not operator.
[01:11] So if I mention the not operator just before, the number is equal to zero expression.
[01:18] So first my expression within the parentheses is going to be evaluated.
[01:23] If this is true,true of not operator is going to become false. In such scenarios, my if condition is
[01:31] not going to be executed, whereas if the number is equal to is equal to zero is evaluated as a false,
[01:38] then not or false is going to be true.
[01:41] Then in such scenarios, then this statement is going to be executed.
[01:46] That means I'm trying to reverse the behavior of my if block with the help of not operator.
[01:52] Since I'm trying to reverse the behavior, then I should also change the output.
[01:56] Here I should mention the number is not zero. So this if statement is going to be executed,
[02:03] if the number is not zero, think like if I given the number as zero, then this is going to be true
[02:10] and true of not is going to be false and this is not going to be executed.
[02:14] Whereas if I have given the number as nine, since this is not equal to zero, we are going to get the
[02:20] output as false here, and the false of not operator is going to give true as an overall output.
[02:27] In such scenarios, this statement is going to be executed, and whatever we are going to display,
[02:32] which is the number is not zero, is going to make sense to the end user.
[02:36] So for example here I can try to execute this program.
[02:40] And this time you can see we are getting the output
[02:42] the number is not zero though
[02:44] the expression is evaluated to false because we are using the not operator.
[02:49] So now if needed I can build the else block also for this if statement where I can print the statement
[02:56] which is the number is zero.
[02:58] So here this time what I'm going to do, I'm going to put the number value as zero.
[03:02] And if I try to execute this program I'm going to get the output as the number is zero, which like
[03:08] we can expect.
[03:09] And one more important information that I want to share here is, whenever you have only a single Java
[03:14] statement inside your if block or else block or else if block.
[03:20] Mentioning these curly braces is optional.
[03:23] For example, I can completely remove this curly braces and still my compiler is not going to complain
[03:30] anything.
[03:31] So if I try to execute this program, I'm going to get the output, which is the number is zero.
[03:36] So the behavior is going to be the same.
[03:38] But there is a disadvantage with this approach, which is if someone writes an statement which is immediately
[03:44] after the else the new Java developers, they may get confused whether the last statement is going to
[03:49] be executed as part of else, or if it is going to be completely outside of this if and else.
[03:56] Since this is going to bring some confusion, it is always advisable to define the curly braces around
[04:03] the if statement and the else statement and else if statement.
[04:08] So with that reason only, I am going to bring the curly braces here.
[04:12] And with this now anyone can easily understand that these System.out.println()
[04:18] that I have at the end, it is always going to be executed once this entire piece of code is executed.
[04:25] So there is an advantage, which is it is going to improve the readability.
[04:29] That's why always mention the curly braces.
[04:32] Now let me remove this last statement.
[04:35] This time I'm going to build one more example with the help of if statement.
[04:40] The class name I'm going to mention as CanVote.
[04:43] So we're going to build a logic to identify if a given person can vote or not.
[04:48] So let me create this class.
[04:50] Inside this class I'm going to create the main() method first.
[04:54] Inside this main() method I'm going to first create an boolean variable, which is is a citizen.
[04:59] To this isCitizen, I am going to assign the value as true, and after the boolean variable, I am
[05:05] going to create an integer variable with the name age.
[05:08] And inside this age I am going to mention the value as 19.
[05:12] So now using these two variables, I want to build an logic which will help me to identify if a given
[05:19] person can vote or not.
[05:21] Most of the countries they will allow a person to vote only if the person is a citizen, and if the
[05:27] age is greater >18.
[05:29] Let's try to consider the same logic.
[05:32] And with the help of if statements, we can identify if a given person can vote or not.
[05:37] So first I'm going to mention if statement to this
[05:41] if statement I'm going to write a condition which is,
[05:43] first I'm going to check if the given person is a citizen or not.
[05:47] But do you think this check alone is sufficient,
[05:50] off course not.
[05:51] We need to also check if the age of the person is greater than 18 or not.
[05:56] That's why this time I'm going to use the and
[05:59] operator.
[06:00] And after mentioning the and operator, I'm going to check whether the given age is greater than 18.
[06:06] If both these conditions become true, then overall condition for my if block is going to be true in
[06:14] such scenarios only, I'm going to print the output, which is the person can vote.
[06:20] Otherwise inside the else block I'm going to print the statement, which is the person cannot vote.
[06:28] So let me copy this and mention cannot vote.
[06:32] So with this input, if I try to execute my program, I'm going to get the output as the person can
[06:38] vote because both of my conditions are evaluated as true.
[06:43] If I try to change one of the data like isCitizen to false, I'm going to get the output as the person
[06:50] cannot vote.
[06:51] This way we can use any type of operators that we have discussed while we are trying to write the condition
[06:58] expression inside the if block or else if block.
[07:02] So please always think about the problem that you are trying to solve.
[07:05] I can only teach you the syntax on how to build the if block or else block or else if block.
[07:11] I cannot teach the business logic for all the scenarios that you may face inside your real projects.
[07:16] So you as a intelligent human, you need to think about what is your problem, what is the problem that
[07:23] you are trying to handle?
[07:24] What is your business requirement?
[07:26] Once you understand your business requirements, you need to think what operators that you can use based
[07:32] upon these operators.
[07:34] You can build the if statement, else if statement and else statements.
[07:39] I hope you are clear.
[07:40] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
