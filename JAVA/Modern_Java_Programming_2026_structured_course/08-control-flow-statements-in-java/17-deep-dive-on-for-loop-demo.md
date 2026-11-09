# 8.17 — Deep dive on for loop - Demo

> Section 8: Control flow statements in Java

[00:00] Inside my Java project
[00:01] let me create a new Java class and the class name is going to be ForLoopDemo.
[00:08] Inside this class, as usual, first we need to create the main() method and inside the main() method I'm
[00:15] going to build a logic with the help of for loop, which is going to help me to print that table of
[00:20] five.
[00:20] So whenever you want to build a for loop, first we need to type the for keyword followed by parentheses,
[00:27] and after the parentheses you can mention the curly braces.
[00:31] So you can see there is a opening and closing curly braces.
[00:34] Inside my for loop parentheses, I need to write three expressions.
[00:39] The very first expression is the initialization expression, which means when my for loop is about to
[00:45] start for the very first time, this initialization logic is going to be executed.
[00:51] So when this initialization expression is going to be executed, I want to create a variable which is
[00:58] int i = 1 because every multiplication is going to start from the one.
[01:04] That's why I'm defining an variable ,i which is going to hold the initial multiplier value one.
[01:11] And after that we need to write the conditional expression which is going to be executed or evaluated
[01:17] before each iteration of my for loop.
[01:21] So the expression that I want to hear is i <= 10.
[01:26] Since I want to print a five table up to the multiplier of ten, I have defined this expression with
[01:31] this expression,
[01:32] whenever the i value become less than, my for loop execution is going to stop.
[01:38] After this conditional expression, we need to write the update expression.
[01:42] So after each iteration execution, I want my i variable to be incremented by one.
[01:49] That's why I'm mentioning this i++.
[01:52] Once we define these three components, we should be good
[01:55] and inside the for loop body we can write the actual business logic.
[02:00] So the logic that I want to write here is, int result = i * 5.
[02:07] So each time I'm going to have a multiplier like 1,2,3, 4 up to ten the same, I want to multiply
[02:14] with the five and the output from this multiplication, I want to store inside a variable result.
[02:20] After this multiplication, I'm going to write a System.out.println() statement and inside this
[02:25] statement
[02:25] first I'm going to define a String value which is five space asterisk space followed by I'll use a plus
[02:33] symbol which is going to perform the String concatenation.
[02:36] Here I'm going to mention the multiplier value.
[02:39] So the multiplier value is going to be represented by the variable i.
[02:43] And after this I'm going to mention the plus symbol again followed by inside the double quotes I'm going
[02:49] to mention the is equal to symbol
[02:51] and at last I'm going to append the variable which is result.
[02:55] So when I try to execute this program you'll be able to see the five table like 5 * 1 = 5
[03:02] .
[03:03] So this is completely coming from the expression that we have written here like five asterisk,
[03:08] it is always going to be the same for all kind of iterations.
[03:12] That's why I hard coded this String value.
[03:15] After that the multiplier value is going to change based upon the current iteration.
[03:20] So that's why instead of hard coding a value, I have defined the variable i.
[03:24] And after the multiplier we need to mention is equal to the same.
[03:28] I'm trying to append to the String with the help of this
[03:30] hard coded is equal to symbol, and at last I'm going to append the result value. In case if you want
[03:37] to print the five table up to the multiplier of 20, you can simply change this 10 to 20.
[03:43] And with that, you will be able to see a table up to that 20.
[03:47] And very similarly, if you are looking to build that table for another numeric value, maybe you want
[03:53] to build for nine instead of five
[03:55] here you can replace nine.
[03:57] And with that you're going to get nine table.
[04:00] But before that inside your System.out.println().
[04:02] And also you need to change this 5 to 9.
[04:05] And if I try to execute this program this time you should see an nine table inside the console.
[04:11] I hope you're clear on how the for loop is going to execute.
[04:14] I can also show you by debugging this.
[04:16] So to debug this I'll change this value to ten.
[04:19] And I'll keep a breakpoint inside my for loop.
[04:22] So let me execute my program in a debug mode.
[04:26] The breakpoint is going to stop during the first iteration.
[04:30] Here you can see during the first iteration the i value is going to be one.
[04:34] So that's why the result is nine.
[04:36] So if I try to release the breakpoint by clicking on this resume program, the breakpoint is going to
[04:42] stop again, this time with the i value two and the result is going to be 18.
[04:47] The same is going to happen for each iteration, like for three, four, five, six, seven, eight,
[04:54] nine, ten.
[04:55] This time if I release the breakpoint, the for loop execution is going
[05:00] to stop because the i value is going to become 11.
[05:03] So let me release the breakpoint and you can see the program is terminated.
[05:08] And this is the output that we have on the console.
[05:10] I hope you are clear about this example.
[05:13] Herev we can try to do some optimization.
[05:16] If you see here we are trying to declare this entire result variable during the every iteration execution.
[05:23] So instead of that what we can do is we can try to declare this variable outside of the for loop with
[05:29] an initial value zero and the same
[05:32] I can try to use inside my for loop.
[05:35] And with this, the declaration of the result variable is going to happen only once, but the reinitialization
[05:43] of the result variable is going to happen after the execution of each iteration.
[05:48] So here I'm getting a warning which is defining zero is unnecessary because the default value of int
[05:55] is anyway zero.
[05:55] So let me remove that.
[05:57] With that the warning is resolved.
[05:59] Now let me show you how to build the infinite for loop.
[06:02] Like I said before, whenever you are trying to define the for loop, mentioning the three components
[06:08] of for loop like initialization, condition and update expressions is optional.
[06:13] So in such cases you can simply mention colon two times, which will make three components as optional
[06:22] or as empty inside your for loop.
[06:24] If needed, you can build an statement like System.out.println().
[06:28] And here I'll just say hi.
[06:31] If I try to execute this program this time
[06:33] the second for loop that we have, it is going to execute continuously and print the value hi multiple
[06:40] times.
[06:40] But since we have a breakpoint here, my program execution passed.
[06:44] So let me remove this and release the breakpoint
[06:47] and inside the console you'll be able to see the hi value continuously printed onto the console.
[06:52] So this is one form of building the infinite for loop.
[06:56] The other style is like I said, if you don't like mentioning any statement, you can simply mention
[07:03] the semicolon.
[07:04] You don't even have to mention the curly braces because semicolon represents an empty statement or null
[07:11] statement inside Java.
[07:12] Here I can take this for loop.
[07:14] After this for loop, I can simply mention a semicolon, and with that I'm going to get an compilation
[07:20] error saying that unreachable statement.
[07:23] This is because you already have an for loop, which is going to execute infinitely, and this for loop
[07:30] is never going to be executed.
[07:31] That's why we are getting this compilation error.
[07:34] So let me comment out this for loop post that the compilation that we have here will get resolved.
[07:40] So this time also we are going to execute the program continuously, but we are not going to print anything.
[07:46] So let me run this program.
[07:48] You can see the program is continuously executing behind the scenes, but we are not able to see that
[07:53] because we're not printing anything onto the console.
[07:56] I hope you are clear.
[07:58] Let me stop my program before I try to close this lecture.
[08:01] I want to share a fun fact about the for loop.
[08:04] Most of the developers, like 99% of the Java developers, whenever they are trying to declare a variable
[08:11] inside the for loop, they're going to use the character i.
[08:15] i represents index, but instead of i, you can use any other character or any other variable.
[08:21] But for some reason it became a tradition that inside for loop, everyone has to use the i character
[08:29] to define the variable and to control the execution of the for loop.
[08:33] In the scenarios where someone is trying to build a nested for loops, then after i they will use j
[08:39] and after j they are going to use the k, so I j k
[08:43] these are the most commonly used variables by 99% of the developers.
[08:49] I can confidently say that even if you go to any project, you will see a lot of for loops built with
[08:55] the variables I, j, k.
[08:58] So there is no hard rule around that.
[09:00] But it's a tradition that someone started long back, two decades back, and the same is being continued
[09:06] by all the programmers.
[09:07] I also have some funny memes around this, which I'm going to show you in the coming lectures.
[09:13] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
