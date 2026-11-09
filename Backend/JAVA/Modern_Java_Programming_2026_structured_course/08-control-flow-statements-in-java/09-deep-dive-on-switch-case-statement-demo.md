# 8.9 — Deep dive on switch case statement - Demo

> Section 8: Control flow statements in Java

[00:00] To build the logic with the help of switch case statement.
[00:04] I'm going to create a new class inside my section8 Java project.
[00:09] The class name is going to be SwitchCaseDemo. Inside this class
[00:14] first let me create main() method and inside the main() method I'm going to define logic with the help of
[00:21] the switch case statement.
[00:23] First I'm going to create a String object with the name fruitName.
[00:28] And inside this I'm going to store a value which is mango.
[00:31] Mango is my favorite fruit,
[00:33] that's why I'm giving mango.
[00:35] But if you want you can give your own fruit name.
[00:38] As a next step, I'm going to type switch keyword in all small case letters followed by space and parentheses.
[00:46] So this space is optional.
[00:48] But to improve the readability, I would always recommend you to mention a space between the parentheses
[00:55] and the switch keyword.
[00:56] To this switch parentheses I want to pass an expression, so the expression is going to be my fruit
[01:03] name variable.
[01:04] So whatever variable that we are trying to pass here it is of type String.
[01:09] So it is completely acceptable inside Java to use String objects as an switch expression.
[01:15] After defining the expression we can provide a space followed by opening and closing curly braces.
[01:21] So inside these curly braces only we can define any number of cases along with their Java statements.
[01:28] So first let me create a initial case which is going to handle the String data
[01:34] Banana.
[01:35] After mentioning the case label, we need to mention colon followed by System.out.println().
[01:42] And inside this System.out.println() I'm going to mention $1.0 charged. As next step
[01:51] let me copy this entire case statement multiple times so that I don't have to type again and again.
[01:57] So I'm trying to paste total five times.
[02:00] So this is the third time,
[02:02] fourth time, fifth time.
[02:04] You can see we're getting a compilation error because we're trying to use the same labels for the multiple
[02:10] switch case blocks.
[02:11] This also we discussed previously.
[02:13] This error will automatically resolve when we update all the labels with the different fruit names.
[02:19] So the second fruit I'll give it as apple.
[02:22] For apple it is going to be $1.5 followed by grapes.
[02:27] For grapes I'm going to charge $2.
[02:30] After grapes I'm going to mention pineapple.
[02:34] For pineapple I'm going to charge $2.5.
[02:38] And after the pineapple we can mention mango.
[02:42] For the mango we're going to charge $3.
[02:45] So with this you can see I have built multiple case labels for my switch case statement.
[02:50] And I have not given break statement as of now because it is completely optional.
[02:56] First I'm going to show you the behavior without the break statements post that I'm going to add the
[03:01] break statement and I'm also going to introduce default statement.
[03:05] First, let me try to execute this program for the mango
[03:08] we are going to get the output as 3.0 charged.
[03:11] You can see the same here.
[03:13] Since mango is the last case, we got only this statement as an output, but this time I'll try to give
[03:19] the fruitName as apple with this apple fruit name,
[03:23] the case of the apple is going to be executed by the switch case statement, but since we don't have
[03:28] the break statement, all the following cases are also going to be executed the same
[03:34] we can confirm here.
[03:35] Inside the console you can see we have 1.5, 2.0, 2.5 and 3.0 charge.
[03:42] So all these statements are coming from these four case blocks.
[03:46] So to avoid these kind of behavior we can simply mention break statement with semicolon in each of the
[03:53] case.
[03:54] So let me do the same for grapes pineapples and at last mango.
[03:59] So with this if I try to execute, you can see this time I'm going to get the output as 1.5 dollar charge.
[04:05] And this is coming from the apple.
[04:07] And as soon as this statement is executed, I'm trying to break the execution of the switch case statement.
[04:14] I hope you are clear with the purpose of the break statement, and at last, I can also provide default
[04:21] to handle the scenarios where if none of the case labels are matched with the given input.
[04:27] So under that default I can try to build the same System.out.println() along with the break.
[04:33] So here I'm going to change the message to pick a valid fruit.
[04:39] So this time I'll try to give some invalid fruit name.
[04:43] Maybe I'll try to give some junk data,
[04:45] and if I try to execute this you can see I got an output which is a pick a valid fruit.
[04:50] I hope you are clear with this initial demo of SwitchCaseDemo.
[04:53] This time let me try to build a same logic for both banana and apple
[04:59] maybe.
[05:00] Think like for both banana and apple, I want to charge only $1 in such scenario.
[05:06] I can simply remove the logic that I have under the banana, and I can mention both cases immediately.
[05:14] And here I can change this statement to $1 charged.
[05:18] So with this, if I try to send the fruit name as either banana or apple, I'm always going to get the
[05:25] same output which is $1 charged.
[05:28] So this scenario also we discussed previously I'm trying to show you a demo of the same.
[05:32] Now let me show you a demo of another important point that we have discussed previously
[05:37] I said all these case labels, they have to be compile time constant values. Instead of these constant
[05:44] values
[05:44] if I try to pass a String variable or an Java expression, I'm going to get an error because inside
[05:53] switch statements for all your case labels, only constant values are allowed.
[05:58] Let me revert this back to the hardcoded value which is grapes.
[06:01] And with that you can see the compilation error is resolved.
[06:04] As a next step,
[06:05] we can also validate one more point.
[06:07] Like I said before, whenever we are trying to send an expression to the switch statement, the expression
[06:13] can only be evaluated to an int, short, byte, String or enum.
[06:19] So enum is a different concept which we are going to discuss in the coming sections.
[06:24] So apart from these valid data types, if your switch expression is evaluating to different data type,
[06:31] it is going to result into an compilation error.
[06:34] For example, here I can try to build an expression which is going to give boolean as an output.
[06:41] So I'll just mention 2 == 2.
[06:44] So this is always going to return the value as true as an output.
[06:49] Since true is a boolean data type it is not allowed.
[06:52] That's what you can see here.
[06:54] Select a type of boolean is not supported.
[06:56] So this point also we validated here.
[06:59] So let me revert back to the fruit name.
[07:02] With this the compilation error will get resolved.
[07:04] As a next step
[07:05] let's try to understand what is a switch expression that is introduced as part of Java 14, and how
[07:13] it is different from the switch case statement.
[07:16] I hope you are clear about the switch case statement.
[07:19] Let's jump into the switch expression.
[07:21] Thank you,
[07:22] bye.

----------------------------------------
