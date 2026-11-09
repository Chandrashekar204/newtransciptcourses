# 8.13 — Deep dive on while statement - Theory

> Section 8: Control flow statements in Java

[00:00] I'm going to show you a couple of videos closely
[00:03] look at those videos.
[00:04] So this is the very first video.
[00:06] Like you can see the ball is moving continuously without any interruption.
[00:12] Now let me show you the second video.
[00:14] Inside the second video you can see the drops are keep falling from the glucose bottle.
[00:20] If you closely observe these two videos, it is pretty clear the action that is being performed is being
[00:27] repeated continuously like a loop.
[00:30] Very similarly inside programming languages
[00:32] also, we may have some scenarios where we need to execute a piece of logic continuously inside a loop
[00:39] based upon a condition.
[00:41] So for these water drip falling, the condition is that the bottle should be empty.
[00:46] So till the bottle is empty, the drop should keep on falling.
[00:50] Very similarly inside this video, the condition is the ball is going to be keep moving until someone
[00:56] stops the moving of the wheel that we have on the down.
[01:00] I hope you are clear.
[01:01] What are loops?
[01:02] So let's try to understand what is the first option that we have
[01:05] whenever we want to implement loops inside Java. We can follow various approaches in Java based upon
[01:12] our own requirements.
[01:13] The very first approach is to build a looping logic with the help of while statement.
[01:18] So whenever we want to build the logic with the help of while statement, we need to follow the syntax
[01:24] which is
[01:24] first we need to mention the while keyword followed by condition inside the parentheses.
[01:30] So whatever condition expression that you are providing to the while statement, it has to be evaluated
[01:37] to a boolean value.
[01:38] So if the condition is evaluated as true, then the statements that you are going to write inside the
[01:44] while block, they are going to be executed continuously until the condition became false.
[01:50] Let's try to understand the while statement by taking a real time scenario.
[01:55] If you go to the same old childhood days, whenever you fall sick, or whenever you have some flu,
[02:01] your parents will take you to the doctor.
[02:03] The doctor is going to prescribe you saying that the baby temperature is high.
[02:09] So please use the medication until the body temperature of the baby returns to normal.
[02:16] So this is a kind of loop.
[02:18] The loop of giving medications by the parent to the baby is keep on going to continue until the body
[02:24] temperature of the baby is going to become normal.
[02:28] As soon as the body temperature of the baby becomes normal, then the medication is going to be stopped
[02:34] by the parents.
[02:35] The while statement is also going to work very similarly.
[02:38] If you try to implement the same scenario with the help of while statement first, you can see there
[02:43] is a boolean variable which is isHighTemp and it is holding a value true.
[02:48] So since this is true, whatever logic that you have written inside the while block, it is going to
[02:54] be executed.
[02:55] Like take syrup is the statement that I'm trying to print out inside the while block.
[03:00] At some point of time when the temperature became normal, then the boolean that is isHighTemp
[03:06] is going to become false based upon the business logic that you are going to write inside your while
[03:11] statement.
[03:11] And when such case happened, the while statement execution is going to stop.
[03:16] I hope you are clear with this very quick introduction.
[03:19] Let me show you one more example of the while statement.
[03:23] Here my requirement is to print the numbers from 1 to 10 using the System.out.println().
[03:31] If a developer is not aware about the while statement, he may write the System.out.println() ten times
[03:37] and for each statement of System.out.println() land, he's going to pass the numbers like one,
[03:43] two, three, four like that.
[03:45] He's going to write multiple lines of code, which is very basic way of doing.
[03:51] But if you try to take the help of while statement, the same can be achieved very easily.
[03:56] So here you can see first I have an integer declared with the value one.
[04:01] So the int variable is I and inside my while statement I have written a boolean expression which is
[04:07] if i <= ten,
[04:11] if these condition returns true, then please execute whatever I have written inside my while block.
[04:17] So first I'm going to print out whatever value that I have inside the
[04:22] i post that I'm going to increment the I value with the help of post increment operator.
[04:29] That means whenever my while statement is executed, the value of i is going to be incremented at some
[04:35] point of time when my I value becomes 11.
[04:39] This condition that we have after the while keyword is going to become false.
[04:44] And with that my while statement execution is going to be stopped.
[04:49] I hope this brings more clarity to you about the while statement.
[04:52] Now let me show you how to write an infinite loop with the help of while statement. Sometimes inside
[04:59] interviews
[04:59] people may ask you how to write an infinite loop with the help of a while statement.
[05:04] Infinite loop means which is going to run continuously.
[05:08] If you try to pass the value true to your while statement, maybe in the form of literal, or maybe
[05:14] with the help of boolean variable that holds true in this kind of scenarios, the while statement is
[05:20] keep on going to run continuously and nowhere you are trying to change this value to the false since
[05:26] it is always going to be true.
[05:28] The statement of System.out.println() is going to be executed continuously.
[05:33] I'm also going to show you this in a demo in the next lecture.
[05:36] For now, I'm assuming you are clear how to write an infinite loop with the help of while statement
[05:42] and whatever condition expression that we provide to the
[05:45] while it is always mandatory, you can't build a while statement without providing a boolean expression
[05:52] to your while statement.
[05:54] In the next lecture, let's try to build some Java programs with the help of while statement so that
[05:59] it is going to be super clear for you.
[06:01] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
