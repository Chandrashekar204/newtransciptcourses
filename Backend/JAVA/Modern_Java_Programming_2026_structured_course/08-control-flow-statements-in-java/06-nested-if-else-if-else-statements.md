# 8.6 — Nested if- else if - else statements

> Section 8: Control flow statements in Java

[00:00] Java allows you to define nested if statements or else if
[00:05] statements or else statements, that means you can write an if statement inside another if statement
[00:11] or inside another else statement, or else if statements.
[00:15] So there are no limitations on how deep you want to leverage these if statements or else if statements
[00:21] or else if statements.
[00:23] I can also show you an example here.
[00:25] So inside this business logic, based upon the day of the week, I'm trying to display various messages
[00:31] to my end user.
[00:33] If you try to understand this program on a high level inside my if block, I have another if else block
[00:39] and similarly inside a else block
[00:41] also I have another if else block.
[00:44] If you have very complex business logic, I can try to define these kind of nested statements.
[00:50] And here I went only to one level deep and if needed I can go to any level.
[00:56] For example, inside this inner if loop, I can try to define one more if, else if, else statement.
[01:03] So it's up to me based upon how complex my business requirements I can leverage these nested statements.
[01:09] I know you may have some questions.
[01:10] Let's try to build the same logic inside a Java program, and try to understand the same
[01:15] by debugging the program. Inside my IntelliJ, I'm going to create a new class and the class name
[01:22] I'll keep it as MessageForDay.
[01:26] Inside my main() method, I'm going to paste a few lines of logic so that we can discuss the logic very
[01:32] quickly, just to save some time,
[01:34] I'm trying to paste these lines of code.
[01:36] You will always have these code inside the GitHub repo as well, but don't worry, the code looks very
[01:42] lengthy and very complex.
[01:43] But I'm there for you.
[01:45] I'm going to make you understand each line by line. In the very first line,
[01:49] as usual, we are trying to define a string object with the name dayOfWeek, and to this object I
[01:55] have assigned the value, which is Wednesday.
[01:57] Once I have defined the dayOfWeek, first, I have written an if statement.
[02:03] Inside this if statement, you can see I'm trying to check two values.
[02:07] If the dayOfTheWeek equals to Saturday, or if the day of the week equals to Sunday.
[02:12] If my day is Saturday or Sunday, then the code that I have written inside this if block is going to
[02:18] be executed.
[02:19] So anytime inside intelliJ just after this curly brace, if you can double click, it is going to
[02:25] highlight all the code that is defined as part of this if block.
[02:29] So first we are going to print these
[02:31] hooray!
[02:32] It is a weekend and later on I have an nested if else statement where I'm trying to check if the given
[02:38] day is Saturday.
[02:39] If it is Saturday, I'm trying to print a statement which is time for a relaxing day, or maybe some
[02:46] outdoor activities.
[02:47] Otherwise, if it is Sunday, I'm going to execute the else block where I'm trying to print the statement,
[02:52] which is lazy Sunday vibes perfect for a cozy day indoors.
[02:56] So if my day is not Saturday or not Sunday, then my execution will go to the else block inside the
[03:03] else block.
[03:04] First we are trying to print,
[03:06] it's a weekday time to work or attend the classes, so once this statement is printed again inside my
[03:12] else block, I have if and else statements.
[03:15] As part of this else block, you can see
[03:17] first, I'm going to check if the dayOfWeek is Wednesday or Thursday, or Friday.
[03:23] If it is, then I'm going to print the statement which is midweek,
[03:27] Hazel, keep going
[03:28] the weekend is approaching.
[03:30] Otherwise, if the day is Monday or Tuesday, I'm going to print the statement which is Monday Blues,
[03:37] grab some coffee and powered through the day.
[03:40] So this is a simple logic that I have written, but the main concept that I want you to understand here
[03:46] is, we can write nested if statements are nested if else if else statements based upon our own business
[03:55] requirements.
[03:55] Let me try to execute this program and see what is going to happen at runtime.
[04:00] So I'm trying to execute this program since the day of the week is Wednesday.
[04:04] This if statement is not going to be executed.
[04:08] So let me press F8 here.
[04:10] So the execution entered into the else statement
[04:13] and this message is going to be printed on the console post that since the day is equal to Wednesday,
[04:19] it is going to enter into this if block and my program is going to print this message.
[04:25] And at last all the logic inside my program is executed.
[04:29] So if I release a breakpoint and go to the console, you can see I have two messages, which is it's
[04:35] a weekday time to work or attend classes.
[04:38] And midweek
[04:39] Hazel, keep going,
[04:40] the weekend is approaching.
[04:42] I hope you like this program.
[04:44] My humble request here is,
[04:45] please refer this solution which is present inside the GitHub repo if you have any questions.
[04:50] So try to change these program messages.
[04:53] Maybe I have printed my own messages.
[04:55] You can make it more fun based upon your own messages
[04:59] that way you
[05:00] going to make your hands dirty by implementing the example of nested if statements.
[05:06] I hope you are clear.
[05:07] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
