# 8.11 — [JAVA 14] Deep dive on switch expression - Demo

> Section 8: Control flow statements in Java

[00:00] Let's see the demo of the switch expression for the same
[00:03] I'm going to create a new class.
[00:06] This time the class name is going to be SwitchExpressionDemo.
[00:10] And inside this class first I'm going to create a main() method.
[00:15] And inside this main() method I'm going to write supermarket business logic with the help of switch expression.
[00:21] For the same,
[00:22] just to save some time, I'm going to copy this entire code that we have from the SwitchCaseDemo and
[00:29] paste it inside the SwitchExpressionDemo.
[00:32] So the very first change that we need to take care to convert a switch case statement into a switch
[00:37] expression is in the place of colon.
[00:40] We can use the arrow mark like
[00:43] first you need to mention minus followed by greater than symbol.
[00:47] That will give you an arrow symbol inside Java.
[00:50] After that you can mention whatever statement you have.
[00:54] So since I want to build a same logic for both banana and apple, I can straight away take this apple
[01:01] and mention just after the banana by using a separator comma.
[01:06] So you can see I have a case which is going to handle the fruit names banana and apple.
[01:12] So for these two fruits I want to print a statement which is $1 charged. Post that we can remove
[01:20] these case block.
[01:22] And we don't have to mention any break statement in a very similar manner
[01:26] let's try to update for remaining case labels as well.
[01:30] So I'll try to mention arrow symbol and I'll try to bring my System.out.println() immediately after the
[01:36] arrow symbol and post that I'm going to delete the break statement.
[01:40] So let me do the same for pineapple as well.
[01:43] Do you see how compact our code is becoming whenever we are using switch expression?
[01:48] Since a switch expression has a lot of advantages these days, like I said, many developers are using
[01:55] the switch expression only.
[01:57] I hope you are also going to use the same inside your projects.
[02:00] So you can see right now the entire switch statement were able to build just with the six lines of code.
[02:07] So if I try to execute this statement, I'm going to get the output as $1 charged.
[02:13] So I don't have any break statements.
[02:15] Still, my case expression behind the scenes is making sure to execute a specific case, but not all
[02:23] the following cases. As of now
[02:25] inside my switch expression, I only have a single Java statement, but if you have a scenario where
[02:30] you want to build multiple Java statement, you can simply surround them with the help of curly braces
[02:36] like you can see here.
[02:37] So this way I can build any number of Java statements inside my switch expression.
[02:43] But as of now we have only a single Java statement.
[02:46] That's why I don't want to maintain this curly braces to make my code very short and clean.
[02:53] Apart from building the switch expression to execute your Java statements conditionally, we can also
[02:58] use the switch expression to return a value based upon the given input.
[03:03] For example, I can try to use the same switch expression to assign to an String variable with the name
[03:13] output.
[03:13] So here I'm trying to create an String object and to the same I'm trying to assign the switch expression,
[03:20] but I'm getting a compilation error because from my case statements I'm not returning a String value.
[03:27] Instead I'm simply executing a System.out.println() statement.
[03:32] So to resolve this compilation errors, I have to remove these System.out.println() and simply mention
[03:39] a String value.
[03:40] So this String value is going to be returned whenever this case statement is going to be executed.
[03:46] So let me do the same for remaining case statements as well, so that all the compilation errors, they're
[03:53] going to be resolved and post that we'll be able to successfully return an value from the switch expression.
[04:01] So I'll keep a breakpoint at the end of my program post that I will try to invoke this program in a
[04:07] debug mode.
[04:08] You can see you'll be able to see under output we have an value which is $1 charged.
[04:15] So how we are getting this?
[04:17] Since we have the fruitName as banana, this String is going to be assigned to the variable output.
[04:23] So this is one of the great advantages that we have with the switch expression.
[04:27] The same is not going to be possible with the switch case statement.
[04:31] Let me release my breakpoint.
[04:34] As of now you can see inside this switch expression we have only one Java statement.
[04:40] That's why whatever String value I have mentioned here, the same is going to be returned by default.
[04:45] But in real projects inside your case blocks, you may write multiple Java statements in such scenarios
[04:52] by default, your switch expression is not going to return any value.
[04:56] You need to manually return a value from your
[05:00] case statement.
[05:01] So to demo you the same, let me create one more switch expression here.
[05:05] Here first I'm going to create an String object with the name day.
[05:10] And to this I'm going to assign a value which is Friday.
[05:14] Because we all like Fridays.
[05:17] From Friday evening we will be entering into the weekend mode.
[05:21] So since it is everyone's favorite day, I have mentioned that day as Friday here.
[05:26] So now based upon this day object, I want to build an switch expression that is going to return a value.
[05:33] Let me paste a few lines of code just to save some time here.
[05:38] Post that I'm going to explain you what is this switch expression is going to do.
[05:42] So from this switch expression I want to return number of letters that a given day has.
[05:49] Like Friday has six letters like one, two, three, four, five, six.
[05:55] So based upon the day that I'm giving as an input, I'm going to return the number of letters as an
[06:01] output from this switch expression.
[06:03] So first you can see I have written an switch expression like switch (day)
[06:07] And inside the curly braces I have defined many case statements since Monday, Friday, Sunday they
[06:13] are all going to have six letters.
[06:15] I'm going to first to print how many letters that they have like here six
[06:20] very similarly for Tuesday, seven, Thursday and Saturday it is going to be eight, and for Wednesday
[06:25] it is going to be nine.
[06:27] And for the default case I'm going to print a statement which is invalid day and I'm going to return
[06:32] the value as zero.
[06:33] But here, since we have multiple Java statements under each case, by default, whatever value we are
[06:41] trying to return, the same is not going to be assigned to this variable, which is num letters.
[06:47] We need to manually return that value from our case blocks.
[06:51] So how to do that?
[06:52] Can we try with the return statement.
[06:54] So if I try to use a return statement I'm going to get an error.
[06:58] Because return statements are not allowed inside the switch expression.
[07:02] Instead we should use yield.
[07:05] yield is a new keyword which is introduced for switch expressions.
[07:10] So when we use this yield.
[07:12] So whatever value that we have mentioned after the yield the same is going to be returned and assigned
[07:18] to this variable which is num letters.
[07:20] So let me do the same for other case blocks as well.
[07:24] So I'm trying to mention yield just before eight.
[07:27] Let me do the same for Wednesday case block and even for the default
[07:31] also I'm going to do the same.
[07:33] So this way whenever you have into scenarios where you want to return an value from your switch expression,
[07:39] you need to use a yield if your switch case statements has multiple Java statements.
[07:45] Whereas in the above example, since I have only one Java statement, my switch expression is take care
[07:51] of returning the String value as an output from this case block.
[07:55] I hope you are clear.
[07:56] So let me try to execute this program and see what we are going to see under the number of letters variable.
[08:04] So if I try to execute this you can see under numLetters we have a value six.
[08:09] And even inside the console you will be able to see a value six.
[08:13] Because we have an System.out.println() which is going to print the same value onto the console.
[08:19] Let me release my breakpoint.
[08:21] The next important point that I want to show you a demo here is whenever you are using the switch expression
[08:27] to return a value.
[08:29] In such cases, mentioning that default statement is mandatory.
[08:34] For example, here, if I try to remove this default statement, you can see I'm going to get an error
[08:40] saying that switch expression does not cover all possible input values.
[08:45] So to resolve this, I need to bring back the default statement.
[08:49] Whereas this is not mandatory
[08:51] if you try to build a switch expression simply to execute your Java statements conditionally.
[08:57] So in the very first switch expression that we have built here, we are not returning anything.
[09:02] We are just simply executing the Java statements conditionally based upon the given input.
[09:08] In this kind of switch expressions, default is completely optional.
[09:12] Even if I try to remove these, I'm not going to get any compilation errors.
[09:16] I hope you're clear.
[09:17] So please make a note of all these important points and make sure you are very, very clear about all
[09:23] these points.
[09:24] You can also try to practice them by writing your own Java programs.
[09:28] If you have any questions, you can always post me a question inside Udemy Q&A session.
[09:34] Especially even today
[09:36] many senior Java developers, they are not aware about the yield statement inside switch expressions.
[09:42] Most of the Java developers, they assume we don't have any yield keyword inside Java, but we can use
[09:49] the yield keyword inside Java and the switch expressions.
[09:52] Now, based upon our discussion inside this lecture, you are one of the few Java developers who know
[09:58] about the yield statement.
[09:59] So please be proud about yourself.
[10:01] For your reference, I have mentioned the example that we discussed around the yield statement inside
[10:07] this slide.
[10:08] So always refer this slide in future whenever you have question around the yield keyword.
[10:13] And at last, for your quick reference, I have mentioned the examples of both the traditional switch
[10:20] statement and the switch expression inside this slide side by side.
[10:25] With this, it should be pretty clear for you that switch expression is always a winner with the advantages
[10:31] that it provides.
[10:32] The main advantage of switch expression is with the help of this switch expression, we can build the
[10:37] logic in a very compact and concise manner.
[10:41] Apart from that, break statements are not mandatory.
[10:45] So with all these advantages always my recommendation is to follow the switch expression whenever possible.
[10:52] With this, we discuss everything about the switch statements inside Java,
[10:56] whenever you want to execute this Java statements conditionally, you can always go with the if statements
[11:02] or switch statements so they both have their own use cases.
[11:06] If you have too many conditions to be evaluated in all such scenarios, my recommendation is to go with
[11:13] the switch statement.
[11:14] I hope you're clear.
[11:15] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
