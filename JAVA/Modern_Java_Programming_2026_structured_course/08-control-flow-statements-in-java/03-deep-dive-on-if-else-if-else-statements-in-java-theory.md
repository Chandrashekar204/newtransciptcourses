# 8.3 — Deep dive on if, else if, else statements in Java - Theory

> Section 8: Control flow statements in Java

[00:00] Let's try to understand how to control the flow of the Java statements with the help of " if "statement
[00:06] we on day to day basis use if a lot.
[00:10] For example, while we're talking with our friends, we'll say if this happens, then do this.
[00:16] If this happens, then do this.
[00:18] So like this
[00:19] we use a lot of if's in our daily day to day conversations. Using the same,
[00:24] If we can also control the flow of the Java statements.
[00:30] In Java " if " statement is a control flow statement used to execute a block of Java statement or a block of code
[00:37] based upon the condition that you have defined.
[00:40] For example, if you look at the syntax of the if statement, after mentioning the if inside the parentheses,
[00:46] I need to mention the condition.
[00:48] So this condition is a Java expression which needs to be evaluated into a boolean value.
[00:54] So I can provide a Java expression which is going to give a boolean value
[00:59] or I can provide a boolean variable
[01:01] or I can mention a direct hard coded boolean value.
[01:04] So it's up to me what needs to mention inside the condition.
[01:08] But whatever condition that I mention it has to evaluated into a boolean value.
[01:14] Once your condition are boolean expression is evaluated.
[01:18] If the output is true, then whatever code that you have written inside your if block is going to be
[01:25] executed.
[01:26] Otherwise, the logic that you have written inside the if block is not going to be executed.
[01:31] So whenever you want to write an if statement, after mentioning if followed by parentheses and a condition
[01:38] inside it, you need to mention the starting curly brace and closing curly brace.
[01:42] Inside these curly braces, you can write any number of lines of code like one line, two lines, three
[01:48] lines, or 1000 lines of Java code
[01:50] also, you can write based upon your business requirement, but please note that all these Java statements
[01:57] that we have written inside the if block, they are going to be executed only if the condition is true.
[02:03] Let me give you a very real life example.
[02:06] Many times during our childhood, our parents, they might have promised to us inside your final exam,
[02:13] if you get an A+ grade, then I'm going to buy you a game console.
[02:17] So these kind of promises you might have heard from parents many times, so they'll try to encourage
[02:23] us to get good grades inside our final exams.
[02:27] So if you try to visualize the same statement with the help of if block, it is going to look like this.
[02:32] Inside migrate String, we are going to have a grade value.
[02:36] If these grade value equals to A+, then whatever logic that I'm going to write inside the if block
[02:43] is going to be executed.
[02:44] So how to check the content of the string object with the help of equals() method.
[02:49] So myGrade.equals()
[02:52] if it is same as A+ then this code which is System.out.println() is going to be executed and the
[02:59] same will be printed onto the console.
[03:01] So what do we have inside the System.out.println().
[03:04] We have a statement which is hooray!
[03:06] I got a gaming console.
[03:08] So inside my if block I have only one Java statement.
[03:12] So in this kind of scenarios where you have only a single statement mentioning the curly braces is completely
[03:20] optional, whereas if you have more than one Java statement inside your if block, then you need to
[03:26] make sure you are mentioning the curly braces. Though it is optional in the scenarios of single statement.
[03:32] I would strongly recommend you to mention this
[03:34] curly braces always, because mentioning the curly braces is going to improve the readability of your
[03:42] code.
[03:42] If you don't mention this curly braces, then someone who is very new to the Java, they may find it
[03:48] very difficult to read and understand your business logic.
[03:52] So using the if statement, we are only able to control the flow of an execution only if the condition
[03:59] is met.
[04:00] What if you have a scenario where you want to build the logic such a way that if the condition is met,
[04:06] I want to execute so on, so piece of code.
[04:09] If the condition is not met, then you want to execute some other piece of code.
[04:14] For such scenarios we have if-else statement.
[04:18] So let's try to understand what is this if-else statement. Using the if-else statement,
[04:23] we can execute different blocks of code based upon whether a boolean expression is evaluated to a true
[04:31] or a false.
[04:31] If you look at the syntax of the if-else statement first, as usual, we can write if condition with
[04:38] a set of statements after the if block
[04:41] immediately we need to start the else block.
[04:43] For the else block, we don't have to mention any condition.
[04:47] We can directly mention the curly braces, and inside the curly braces, we can write the business logic
[04:53] that needs to be evaluated whenever the given condition is false, so we're not mentioning the condition
[04:59] inside
[05:00] else because we already mentioned the condition under if statement.
[05:03] If this condition that we have mentioned under the if is evaluated to the false, then whatever code
[05:09] that we are going to write inside the else block is going to be executed.
[05:13] If you try to understand the if-else statement by looking at the same example we discussed in the previous lecture.
[05:19] Think of a scenario where your parents promise that if you are going to get A+ grade and
[05:26] going to buy you a video game console, if not for any other grades that you are going to get, I'm
[05:33] going to give you a motivational speech.
[05:35] That means they will take you to your room, and they will try to inspire you with some motivational
[05:41] tasks.
[05:41] Obviously, this motivational task is going to be boring.
[05:44] That's why the child in this scenario, he's always going to aim for the A+ grade.
[05:49] So this is a very classical example to implement the if-else statement like you can see here
[05:56] first I'm going to write an if statement where I'm going to check for the grade A+,
[06:00] if the grade of the child is A+ then we are going to print a statement, which is hooray!
[06:06] I got a gaming console.
[06:07] Otherwise inside the else we are going to print a statement which is motivation speech received.
[06:14] Since the string object migrate holds a A,
[06:17] in this scenario, the else block is going to be executed. While writing these if-else statements
[06:23] If your if block and else block if they have only a single Java statement mentioning the curly braces
[06:29] is completely optional.
[06:31] But please always mention the curly braces so that your code readability is going to be increased.
[06:38] So with the help of these if-else statement, we are able to evaluate a condition.
[06:44] And when this condition is true we are going to execute the statements inside the if block,
[06:49] otherwise we are going to execute the statements inside the else block.
[06:53] But what if you have a requirement where you want to evaluate multiple conditions.
[06:58] So here I'm always checking if my grade is equal to A+,
[07:02] but what if I have a requirement where I want to evaluate multiple conditions?
[07:08] For such scenarios we can use the if-else if-else statement.
[07:13] So let's try to understand what is the syntax of this statement.
[07:17] If you look at the syntax of this statement first, as usual you need to mention what is your condition
[07:23] one with the help of if block.
[07:25] When this condition one is evaluated to true, then whatever code that you are going to write inside
[07:31] this
[07:31] if block is going to be executed after mentioning the condition one
[07:35] if you want to evaluate another condition, then you can mention else if block by mentioning else space
[07:43] if and
[07:44] inside the parenthesis you can mention what is your condition.
[07:47] So if this condition two is evaluated to true, then whatever code you have written inside the else if
[07:54] is going to be executed.
[07:56] Similarly, you can define any number of conditions like condition three, condition four, condition five
[08:01] with the help of else if and at last
[08:04] if none of your conditions are not met, then you can define an else block which is going to be executed
[08:12] in the scenarios where all your conditions are not true.
[08:16] So mentioning the else block is completely optional only if you want to have a logic which needs to
[08:22] be executed
[08:23] if none of the conditions met.
[08:25] In such scenarios, only you can go with the else block
[08:28] otherwise, you can simply write all your logic with the help of if and else if itself.
[08:34] Always please note that you should start building your logic with the help of if statements only after
[08:40] the if statement and before the else statement
[08:43] you can build any number of else if statements.
[08:46] Let's try to visualize how we can leverage this statement in the example of great scenario that we have
[08:52] discussed previously.
[08:53] So here you can see this time the parent is promising to the child that if you are going to get the
[08:59] A+ grade, then I'm going to buy you a game console
[09:03] otherwise if you are going to get A grade then I'm going to buy your favorite ice cream.
[09:09] If you are not getting A+ or A, then obviously you're going to get a motivational speech from
[09:15] me.
[09:15] So if you try to implement this scenario with the help of if else statement, this is how it is going
[09:21] to look like.
[09:22] So first we need to start with an if statement where we need to write an boolean expression.
[09:27] So if this boolean expression is evaluated to true then I'm going to print,
[09:32] Hooray!
[09:32] I got a gaming console after the if block,
[09:35] next I have written the else if statement and you can see inside this else if statement
[09:41] I have mentioned another condition where I'm trying to evaluate if the my grade is equal to the A value.
[09:49] If it is, then I'm going to print my ice cream as an output.
[09:53] Otherwise, if the my great value does not hold A+ or A, then I'm going to execute the code present
[09:59] inside the else statement.
[10:01] So what do we have here?
[10:03] Motivation
[10:04] speech received.
[10:05] So based upon your scenarios, you can simply use only if statement which you are going to execute always
[10:11] if the given condition evaluated to true.
[10:14] Otherwise, if you want to handle both true and false scenarios of a condition, then you can go with
[10:20] the if and else statement.
[10:22] But if you have a requirement where you need to check for multiple conditions, then you need to consider
[10:28] if else if else statement.
[10:31] I hope you are clear with this discussion.
[10:33] In the next lecture, let's try to build some Java programs with the help of these statements.
[10:39] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
