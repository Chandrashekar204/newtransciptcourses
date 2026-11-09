# 2.9 — Deep dive on boolean primitive data type

> Section 2: Primitive data types in Java

[00:00] As of now, we discussed on a high level what are the primitive data types available inside Java?
[00:06] What are the variables and what are the standards that we need to follow,
[00:10] while we are trying to declare variables with these primitive data types?
[00:13] And we also saw a few examples on how to store various kinds of data with the help of these primitive
[00:19] data types.
[00:20] But from this lecture, we are going to focus in detail about each and every primitive data type available
[00:26] inside Java.
[00:27] In this lecture, the focus is going to be on the boolean data type we already know what is the purpose
[00:33] of boolean data type.
[00:34] With the help of boolean data type, we can store true and false values.
[00:40] So what are these true and false represents,
[00:42] these values represent states like on or off,
[00:46] yes or no.
[00:47] true or false.
[00:48] So whenever you want to conditionally execute a business logic then you need to create variables with
[00:54] these boolean data type.
[00:55] In the coming sections we are going to discuss about various control flow statements that are available
[01:01] inside Java.
[01:02] During the same discussion, I'm going to show you the demo on how to control the flow of Java statements
[01:08] inside a Java program, with the help of boolean variables.
[01:12] We also discussed already on how to declare variables with the help of boolean data type.
[01:18] Here you can see I have created three variables.
[01:20] hasChildren, isValid, isMeasure, hasPassport regardless of whatever primitive data type that you
[01:27] are trying to use to declare your variables.
[01:29] The syntax is going to be always similar.
[01:32] If you are only trying to declare your variable, then you just need to mention what is the primitive
[01:36] data type and what is your variable name followed by semicolon.
[01:39] Like in the very first variable which is hasChildren, I'm trying to do only the declaration, whereas
[01:45] in the next variable which is isValid, I'm trying to do both declaration and initialization.
[01:51] You already know about all these topics, but the important point that I want to highlight here is whenever
[01:56] you are trying to declare variables with the help of boolean data type, the recommendation is to always
[02:03] have a prefix like is, has so that your variable is going to represent like a question.
[02:09] For example hasChildren,
[02:11] so that is a question to someone who is reading your code.
[02:14] This boolean is going to tell whether a particular person has children or not.
[02:20] And very similarly isValid indicates a question.
[02:22] So if someone is trying to read your code if this isValid boolean variable have a value of true, that
[02:29] means something is a valid, otherwise it is invalid.
[02:33] The most commonly used prefixes is and has, but if needed you can use other prefix as well.
[02:39] But according to me, is and has is going to make more sense to you.
[02:43] And your Java compiler also is not going to stop you even if you don't use these prefixes.
[02:49] So it is completely fine from Java compiler perspective if you use simple words without any prefix.
[02:56] But like I said, we need to use this prefix to improve the readability of our code.
[03:01] Always note that in order to be recognized as a good developer, your code should be always easily understandable
[03:08] by others, because in IT career developers will move from one company to other company.
[03:15] If a developer writes a Java code which can be understand by himself, then it is not a good situation
[03:21] for the new developer who is joining the team in the place of older developer.
[03:25] That's why always make sure your code is readable by following all the standards, like using proper
[03:32] variable names.
[03:33] So there are many, many other standards that are available in Java that a good developer has to follow
[03:39] throughout the course.
[03:40] I'm going to teach them as and when we are discussing about a particular topic.
[03:44] Now, let's try to take this knowledge and try to test various scenarios about boolean data
[03:49] type inside the jshell.
[03:51] Here I'm into my jshell,
[03:53] the very first variable that I will try to create is boolean hasChildren. This variable,
[04:00] I'm not going to do any initialization, I'm trying to do only declaration.
[04:04] So what is output that you can expect here.
[04:06] You can expect that hasChildren is going to have a default value false.
[04:11] So you can see the default value
[04:13] right now we see inside this variable is false.
[04:16] Very similarly we can also try to define one more variable which is isValid,
[04:21] but this time I will try to do initialization as well along with the declaration.
[04:26] Since I'm trying to assign a value true, the same will be assigned to this variable name, which is
[04:32] isValid and the same is printed by my jshell.
[04:35] This way we can create any number of variables using boolean primitive data type, if needed
[04:40] you can also define multiple boolean variables in a single Java statement.
[04:46] For example, I can first create a variable which is isMajor.
[04:50] After that isMajor,
[04:52] I'm going to mention comma and post
[04:54] this
[04:54] I'm going to mention hasPassport is equal to true.
[04:58] So here I'm trying to
[05:00] create two variables of boolean data type.
[05:02] The
[05:03] isMajor is going to hold the default value.
[05:05] Because I'm not doing any initialization, I'm only trying to do the declaration for the isMajor.
[05:11] Coming to the hasPassport here, I'm trying to do both declaration and initialization.
[05:16] So the output that we are going to get is for isMeasure
[05:19] it is going to be false and hasPassport
[05:22] it is going to be true.
[05:23] The main purpose of creating boolean variables inside Java programming language is to control the flow
[05:30] of your Java statements or your Java program.
[05:33] Do you want to see a quick demo around that?
[05:35] I can show you, but please don't blame me if something you're not able to understand, because we are
[05:40] ready to discuss about various control flow statements available inside Java, but I can quickly show
[05:45] you a demo.
[05:46] There is no wrong in seeing a demo here, so what I'm going to do is using these isValid variable.
[05:52] I'm going to write a Java logic, which is going to be executed conditionally based upon the value present
[05:57] inside my isValid. For the same,
[05:59] here I'm going to write if and else statements inside Java.
[06:04] So whenever you want to check for a condition, you need to use if inside Java after
[06:09] if I need to mention parentheses and inside these parentheses I need to mention what is a boolean variable.
[06:15] So the boolean variable that I want to use here is isValid.
[06:19] And after mentioning this boolean variable I need to mention the curly braces.
[06:24] And in the next line I'm going to mention System.out.println().
[06:31] And inside this println() I'm simply going to print a statement valid statement.
[06:37] Post this I'm going to close this if block with a closing curly brace after the if statement,
[06:43] I'm also going to provide the else statement.
[06:46] So this else statement is going to be executed in the scenarios whenever the isValid is false.
[06:52] So let me copy this value and paste inside the else.
[06:57] And inside this statement I'm going to mention the statement as invalid statement.
[07:03] So let me close this else block.
[07:06] So now I'm going to press enter.
[07:08] And you can see I'm getting an output which is valid statement because the boolean value that we have
[07:14] here is true.
[07:15] Since it is true then my if condition is going to be executed but not the else statement.
[07:21] So this is how inside Java we are going to write conditional business logic.
[07:27] If something is not clear about if and else don't worry.
[07:30] We are going to discuss about the control flow statements inside Java in detail in the coming sections.
[07:36] But with this, I'm assuming at least you have some basic idea.
[07:39] What is the purpose of boolean data types inside Java programming language.
[07:44] I hope this all making sense to you.
[07:46] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
