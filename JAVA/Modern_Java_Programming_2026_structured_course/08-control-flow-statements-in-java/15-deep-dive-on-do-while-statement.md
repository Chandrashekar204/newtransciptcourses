# 8.15 — Deep dive on do while statement

> Section 8: Control flow statements in Java

[00:00] Let's talk about the another flavor of whike statement which is do while statement.
[00:06] There is a very minor difference between the while and do while.
[00:10] Let me try to explain you about that.
[00:12] Whenever you are using do while statements, your do while statement is going to give an assurance to
[00:18] you that it is going to execute your piece of code at least one time, regardless whether the condition
[00:26] is true or false.
[00:27] How to define this do while statement like you can see here
[00:30] first you need to mention do keyword followed by opening and closing curly braces.
[00:35] At the end you need to mention the while keyword followed by parentheses and inside the parentheses
[00:41] you need to mention what is your boolean expression or a condition, and at last you can terminate that
[00:48] do while statement with the help of semicolon.
[00:51] So whenever you are into the scenarios where you want to execute your piece of logic or piece of code
[00:57] at least once, regardless of the outcome of the boolean expression, you can always use that do while
[01:03] statement.
[01:04] But in real projects you may see these very rarely being used by the developers compared to the while
[01:10] statement.
[01:11] Let's see an example of do while statement like you can see here.
[01:15] First, I have defined an int variable with the name n, and to this I have assigned a value six post
[01:23] that I have written and do while statement inside the do while statement,
[01:27] The logic that I have written is System.out.println().
[01:30] And with this statement I'm trying to print the n variable, and after that I'm trying to increment
[01:36] the n value by one with the help of this post increment operator.
[01:41] And the boolean expression that I have written is n less than six.
[01:44] So this boolean expression is never going to become true because we have assigned the value six to the
[01:52] n and six is not less than six.
[01:54] So though this condition is never going to evaluate it to true, this System.out.println() is
[02:01] going to be executed at least once.
[02:04] I can also show you this in the demo in few seconds, but I'm assuming you are clear.
[02:09] What is the difference between while and do while statement?
[02:12] There is a very minor difference.
[02:14] So please note of this difference and the way you define these statements also differ a lot.
[02:20] But the while statement you are simply going to use the while followed by condition followed by curly
[02:26] braces.
[02:26] Whereas for the do while you need to first mention do curly braces and after your curly braces you are
[02:33] going to mention while keyword along with the condition or a boolean expression.
[02:38] So let me go to the intelliJ and try to build an example with the help of do while statement.
[02:44] So here I'm going to create a new Java class and the class name is going to be DoWhileStatementDemo
[02:53] inside this class
[02:54] first we need to create public static void main() method and post that I'm going to create an int variable
[03:01] with the value six, followed by
[03:03] first I'll mention do keyword and after the do keyword I'm going to straight away start the curly braces.
[03:10] Inside the curly braces, I'm going to print the n variable, followed by
[03:15] I'm going to increment the value of n by using the post increment operator.
[03:20] And if you do like this, you're going to get an compilation error even if you keep the semicolon,
[03:25] because this is not the correct way of defining that do while statement.
[03:29] Once you have defined the do keyword along with your business logic, you need to mention while keyword
[03:35] and after the while keyword
[03:37] inside the parentheses, you can mention your boolean expression like n <6.
[03:43] After mentioning this expression at last, you need to mention the semicolon with this
[03:47] if I try to execute my program though, this condition is going to be evaluated as false.
[03:53] The logic that I have written inside the do is still going to be executed, because the do while is
[03:59] going to always first execute the logic present inside the do.
[04:04] After that only it is going to check the condition and based upon the condition outcome, the next iteration
[04:11] or the next time execution is going to happen.
[04:14] So let me try to execute this program.
[04:16] Here you can see we are getting six as an output.
[04:19] Now
[04:19] this time let me try to change the value here to ten.
[04:23] That means this time the do while statement is going to be executed multiple times.
[04:28] So let me execute this program.
[04:30] And you can see we have 6789 as an output.
[04:35] I hope you are clear with the both while and do while statement.
[04:39] Just like how we can write a nested if statements,
[04:42] very similarly, we can also write nested while statements nested do while statements based upon our
[04:49] business requirements.
[04:50] But in real projects, you will rarely see developers using the nested while and nested do while statements
[04:57] compared to the nested if statements.
[05:00] Before I try to close this lecture, let me show you a couple of funny memes around that do while statement.
[05:05] So this is the very first funny meme image.
[05:08] So whenever you are using do while loops it is always be like shoot first, ask questions later.
[05:15] So first your do while loop
[05:17] always blindly execute the logic present inside your do statement.
[05:21] Post that only it is going to ask questions, whether I need to execute the next time or not based upon
[05:27] the expression that you have provided.
[05:29] The next one is going to be super funny.
[05:31] I'm not sure whether you have seen these cartoon show during your childhood times.
[05:35] If you see here the bird that we have here, it is trying to follow the while loop.
[05:40] So the condition is if it is not edge then only run, otherwise stay ideal
[05:46] whereas a fox that we have it is trying to follow the do while loop.
[05:49] So inside the do while loop first it is simply going to do the running post that only it is going to
[05:54] perform the while check.
[05:56] That's why in this scenario, the fox is going to fall from the edge, whereas the bird is going to
[06:02] be saved because it has used the while loop.
[06:05] So always be very cautious inside your real project,
[06:08] if you are sure that there is no damage is going to happen.
[06:11] Even if you try to execute your Java statements with the help of do statement.
[06:16] In such scenarios, only go with the do while loop.
[06:19] Otherwise always go with the while statement.
[06:22] I hope you are enjoying the course.
[06:24] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
