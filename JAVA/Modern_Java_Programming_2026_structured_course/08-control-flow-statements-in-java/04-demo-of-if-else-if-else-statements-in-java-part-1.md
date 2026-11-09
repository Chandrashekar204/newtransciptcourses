# 8.4 — Demo of if, else if, else statements in Java - Part 1

> Section 8: Control flow statements in Java

[00:00] To get started around the if statements.
[00:02] Since we are into the new section, I have created a new Java project with the name section8 the
[00:09] same
[00:09] I am going to check in into the GitHub repo as well for your reference.
[00:13] Since you already aware about how to create new Java projects, I have not created this project in front
[00:19] of you.
[00:20] Now, inside this section8 project I'm going to create a Java class and this Java class name is
[00:26] going to be EvenOddNumber.
[00:30] So these are Java class name.
[00:32] Now inside this Java class I'm going to write an logic which is going to help me to identify whether
[00:39] a given number is an even number or odd number.
[00:42] So how we can achieve this.
[00:44] We can achieve this with the help of if-else statements.
[00:48] So let me first create an main() method.
[00:51] Once the main() method is created, I'm going to first mention an int variable with the name input number
[00:59] and to this I'm going to assign a random value which is nine.
[01:03] After defining this int variable, first I want to write an if block to check if my given number is
[01:10] an even number or not.
[01:12] So how to identify if a given number is an even or not?
[01:16] If you go back to your school days, the definition is very simple.
[01:20] If an given number is completely divisible by two, then it is an even number.
[01:26] Otherwise it is going to be an odd number.
[01:28] So, using the same formula, I'm going to build my if block.
[01:32] First I need to mention if followed by parentheses and post that, I'm going to mention the curly braces.
[01:39] So to my if statement I need to mention a condition or a Java expression, which is going to evaluate
[01:45] as a boolean value.
[01:47] So here the condition that I am going to mention is by taking the input number variable, I'm going
[01:52] to perform the modulus division with the help of percentage symbol.
[01:57] And the denominator
[01:58] I'm going to mention as two.
[02:00] If the output from this expression is equal to zero, then it is an indication for me that the given
[02:07] number is an even number.
[02:09] Otherwise it is an odd number.
[02:11] So please make sure you are mentioning these double equal operator.
[02:15] If you mention only a single equal, you're going to get a compilation error because the single equal
[02:21] operator we are going to use only in the scenario of assigning a value to a variable.
[02:26] But here we want to evaluate if the left hand side expression is going to give an output as zero.
[02:33] So that's why we need to mention double equal.
[02:35] To post that, I'm going to mention an System.out.println(), saying that the given number is
[02:44] even.
[02:44] So, if I try to execute this program, obviously we're not going to get anything in the output because
[02:50] nine is not an even number.
[02:53] If I try to change this input number to six, then I'm going to get the output, which is the given
[02:58] number is even.
[02:59] You can see I'm getting the same output.
[03:02] So this confirms our if block is working perfectly.
[03:06] Now think like I also have an requirement to print whether a given number is an odd number or an even
[03:13] number.
[03:13] So in this kind of scenarios we should also build an else block.
[03:17] So after the curly brace of if I'm going to mention else followed by curly braces.
[03:23] So you can see this else block, I can start immediately after the if statement
[03:28] or I can start it in the very next line.
[03:31] So it's up to us.
[03:32] But the recommendation is always to start immediately after the if block.
[03:36] Now inside this else statement I'm going to mention the statement which is the given number is odd.
[03:43] So if I try to execute this program with an input number as nine, I'm going to get the output as the
[03:50] given number is odd.
[03:51] This way you can always write the conditional logic.
[03:55] So based upon the input that I'm giving to the program, my Java statements are getting executed conditionally.
[04:02] So this is a story of if and else.
[04:04] Now let's try to take another example and try to build the same with the help of if else if and
[04:12] else statements for the same
[04:13] let me go to my source folder.
[04:16] And here I'm going to create a new Java class.
[04:18] And the class name is going to be FindTheDay.
[04:22] So this is the class name inside this class
[04:24] first I'm going to create an main() method with the help of the shortcut public static void main().
[04:30] So first I'm going to create an String object with the name whatIsToday.
[04:35] So to this I'm going to randomly assign Saturday as an String value.
[04:41] Now based upon the data that I have inside this String variable, I want to display whether a given
[04:46] day falls on a weekend or a weekday.
[04:48] So there are multiple ways on how we can achieve this.
[04:52] One of the way is with the help of if, else if and else condition.
[04:56] So let me try to build a logic here.
[04:59] I'm going to write an if condition.
[05:01] If whatIsToday.equals ("Monday").
[05:06] I'm going to write output saying that it is a weekday.
[05:10] So similarly now I'm going to check for the remaining days with the help of else if.
[05:15] So, when you try to type else if as soon as you type else, you can see the intelliJ is giving
[05:22] an else if shortcut.
[05:24] So if you try to select that and press enter, you're going to get an syntax of else if automatically
[05:30] populated by the intelliJ. Inside this else if
[05:34] I'm going to mention the condition as if the given day is equal to Tuesday
[05:40] if yes, then I'm going to print the same statement, which is it is weekday.
[05:45] So this way I can try to perform the same for all the remaining days, like here
[05:51] I'm going to change this Tuesday to wednesday, followed by next
[05:56] I'm going to mention the else if statement, which is going to help me to evaluate the condition of
[06:02] Thursday.
[06:03] Next, I'm going to write the else if statement for the Friday check,
[06:07] and after the Friday I'm going to do the check for Saturday.
[06:12] And at last I'm going to do the check for Sunday.
[06:15] So for the Saturday and Sunday, it should be weekend.
[06:19] That's why I'm going to update the statement as it is weekend.
[06:22] So let me do the same for Sunday as well.
[06:25] So with this you can see I did not write any else statement.
[06:28] I have written only the if and else if statements.
[06:31] So here I'm trying to evaluate multiple conditions.
[06:35] So if I try to execute this program obviously you can expect the output as it is
[06:39] Weekend.
[06:40] So this confirms else is always optional.
[06:43] Now let me try to write the else block
[06:45] also, after writing the else block inside this block I'm going to write the statement which is invalid
[06:54] input,
[06:55] please check the same.
[06:57] So this is the statement that I want to print.
[06:59] If someone gives some invalid value, maybe instead of Saturday I have given some random word,
[07:05] so if I try to execute this, you can see I'm going to get the output which is invalid input,
[07:10] please check the same.
[07:11] Whereas if I try to mention some other day which is Monday, I'm going to get the output as it is weekday.
[07:17] So this confirms our program is working perfectly.
[07:20] So here you may have a question like can't we check multiple conditions with a single if statement,
[07:27] because we have discussed about the logical operators like OR operator and AND operator, can we leverage
[07:34] them to shorten this code?
[07:36] Off course we can do that.
[07:37] Let's try to do the same.
[07:39] So this time I'm going to write a different piece of code.
[07:43] And here first I'm going to copy the if statement and mention the same here.
[07:48] So if you see here first I'm trying to check whether the given day is equal to Monday.
[07:53] If it is Monday then I'm going to print the weekday as an output.
[07:56] We know the same output has to be printed even for other days like Tuesday, Wednesday, Thursday,
[08:03] Friday.
[08:03] So we can easily achieve these with the help of Logical operators so we can write a compact code or
[08:10] a short code with the help of Logical OR operator.
[08:14] Just after these condition, I'm going to mention the OR operator, and I'm going to copy these condition
[08:21] and mention the same.
[08:22] And here you can see I'm going to mention Tuesday with this,
[08:26] I'm telling if the given day is Monday or Tuesday, then print this output.
[08:31] Very similarly, I can write any number of conditions with the OR operator.
[08:37] So this time I'm trying to define for Wednesday followed by Thursday,
[08:43] after the Thursday and at last I'm going to mention Friday condition.
[08:48] So with the help of these OR
[08:49] operator,
[08:50] we are telling if the day is either Monday or Tuesday, or Wednesday or Thursday or Friday.
[08:56] Always print this output. After this if statement,
[09:00] we can build the else if block and inside this else if block,
[09:05] we can try to build a condition where it is going to check for Saturday or Sunday.
[09:13] In both these scenarios we can print the output as it is, weekend. And at last we can copy paste the
[09:18] same else block.
[09:20] If the input is not falling under any of these values, we are going to print this value.
[09:24] So let me keep a breakpoint here.
[09:26] And I'm also going to keep a breakpoint at the starting as well.
[09:30] So if I try to execute this program you can see the very first condition that we have mentioned with
[09:36] the help of if condition is going to be true.
[09:38] That's why my Java program is going to execute the statement present inside the if block.
[09:45] So if I try to press F8 here, you can see right now the execution entered into the if block.
[09:51] If I try to press F8 one more time, none of my else if blocks and else blocks are not executed.
[09:58] So now my execution is at the next if block.
[10:01] This time also my one of the if condition, which is whatIsDay.equals("Monday"), is going to
[10:07] be evaluated as true since the very first operand itself is true
[10:12] my Java is not going to evaluate any of the other operand expressions that we have written on the right
[10:19] hand side.
[10:19] So with that, we are going to get the output as one more time
[10:23] It is weekday. So if I try to release the breakpoint, we will be able to see two statements inside
[10:28] the console, which is it is weekday, it is weekday.
[10:31] So this way you can always use the if else and else if statements based upon your business requirements.
[10:39] So always think about the operators that we have discussed, especially the OR operator AND operator
[10:45] NOT operator.
[10:46] So they are going to be super useful for your real projects.
[10:51] Here seems I have a spelling mistake,
[10:52] let me correct this with that
[10:54] now I should be good.
[10:56] I hope you are clear with these initial demo of the
[10:58] if blocks.
[10:59] Let's see more examples inside the next lecture as well.
[11:02] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
