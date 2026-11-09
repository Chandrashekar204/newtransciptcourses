# 13.7 — BufferedReader examples to identify even number and sum

> Section 13: Accept input using BufferedReader and Scanner

[00:00] Right now we have a very good understanding on how to accept the input data from an end user, with
[00:06] the help of BufferReader.
[00:08] As a next step, let's try to solve few problems with the help of BufferReader by accepting the input
[00:15] data.
[00:15] The very first Java program that I want to build here is I want to accept an number from an end user.
[00:23] Once the number is accepted, I want to write a business logic inside the Java program to identify whether
[00:30] the end user entered an even number or odd number.
[00:33] So this is going to be super simple.
[00:35] I want you to pause this video and try by yourself.
[00:39] Otherwise you can simply follow this video as well.
[00:42] First we need to create a Java class.
[00:44] So let me create a Java class with the name BufferReader even art demo.
[00:52] So these are class name.
[00:53] And inside these class I want to first create the main method followed by.
[00:58] We need to create the object of BufferReader so that we can start accepting the input data from an
[01:03] end user using the keyboard.
[01:05] We already have this logic inside these BufferReader demo.
[01:09] I can simply copy this code and paste it inside the new class that I have written.
[01:14] So first I'm trying to create the object of InputStream reader by passing the parameter to the constructor,
[01:21] which is system dot in.
[01:22] So whenever we are using System.in, we are telling to the InputStreamReader to read the data
[01:28] from the keyboard.
[01:30] After the InputStreamReader object is created, we are passing the same to the constructor of
[01:35] BufferReader.
[01:35] So the BufferReader object is providing a method which is readLine() to read that data that is entered
[01:42] by my end user.
[01:43] So here we are getting a compilation error because we are not handling the exception of IOException.
[01:49] For now, we can simply click on this add exception to the method signature, which will add this throw
[01:54] statement to your method post that I'm going to update this statement saying that please enter a numeric
[02:02] value.
[02:02] So I'm telling to the end user only.
[02:04] Enter the numeric value post that the value that is going to be entered by the end user.
[02:09] I'm trying to read with the help of this readLine() method, and the same will be assigned to the variable
[02:14] input.
[02:15] As a next step, I want to check whether the given input number is an even number or not, so I can
[02:21] write a if condition followed by else.
[02:25] So the condition I want to write inside this
[02:27] if block is, I want to divide the numeric value present inside these input variable with the two.
[02:33] If the remainder is exactly zero, then it indicates it is an even number.
[02:38] So let's try to do the same.
[02:40] So if I try to mention the condition by using the modulus operator on top of input variable, I'm going
[02:47] to get a compilation error because as of now input is a String variable or a String object.
[02:53] We can't use the modulus operator on top of a String object.
[02:57] It can only be applied on top of an int value.
[03:00] That's why I need to convert these input to String object into an int value.
[03:05] I can try to do the same here by creating a variable which is into num, and after this, on the right
[03:12] hand side, I'm going to invoke the wrapper class off int primitive type which is Integer.
[03:17] And here I'm going to invoke the parseInt() method.
[03:21] We discussed about this method long back.
[03:23] I hope you remember them.
[03:24] So to this passInt() method we can pass the String object which is input.
[03:30] By the time this line is executed, the content present inside the input variable is going to be assigned
[03:36] to the num variable.
[03:38] Now I can simply mention num modulus two is equal to is equal to zero.
[03:43] Then I'm going to print out a statement saying that you have entered an even number.
[03:50] So this is the output.
[03:52] Similarly I want to mention a statement inside the else statement which is you have entered a odd number.
[04:00] I hope you are clear with this.
[04:02] Now let me execute this program.
[04:04] You can see it is asking me a numeric value.
[04:06] I'm trying to enter some 456 so this is a random number I'm trying to enter.
[04:12] And the output I'm going to get is you have entered an even number.
[04:16] Similarly, this time I'll try to enter an odd number.
[04:20] Maybe I'll try to type some odd number.
[04:22] So this is an odd number.
[04:24] Let's see what is going to happen.
[04:25] You can see we are getting an output which is you have entered a odd number.
[04:30] And here you may have a naughty thought, which is I want to enter some alphanumeric value and see what
[04:36] is going to happen.
[04:37] I like to not to thought let's do the same.
[04:39] I also want to try with a naughty input, so I'll try to give 143 followed by some String value.
[04:47] So like I have given 143 are.
[04:50] With this, let's see what is going to happen.
[04:52] You can see we are getting an RuntimeException which is NumberFormatException because when we were
[04:58] trying to convert the String
[05:00] object into a numerical value.
[05:01] With the help of this parseInt() method, it is not able to convert it because it found alpha numeric
[05:07] value.
[05:08] So that's why we are getting a RuntimeException.
[05:11] So this kind of surprises may happen in real projects as well.
[05:15] We can't believe always the end user with an assumption that he's always going to be a good end user
[05:21] and he will always provide a good data.
[05:24] So this kind of bad data can also be sometimes given as an input to your program.
[05:30] Your program should always be ready to handle any kind of scenario.
[05:34] So this is where exceptional handling come into picture.
[05:38] We're going to discuss about this in the coming sections in detail on how to implement exception handling
[05:45] inside a Java program.
[05:46] For now, let's not worry about the bad data.
[05:49] I hope you're clear with this demo.
[05:50] And here you may have a question which is as of now we are only accepting a single input data.
[05:56] Is it possible to accept multiple input data.
[05:59] So this might be your question.
[06:01] And the answer is very simple
[06:02] off course you can ask any number of input data from an end user.
[06:07] Let me show you a demo as well
[06:08] around this I can try to copy this class inside the same package, but I'll try to rename it to BufferReaderSumDemo
[06:16] .
[06:18] So I will be doing the addition of two numbers inside this class.
[06:22] That's why I'm trying to give this name.
[06:24] So inside this class you can see as of now we have the logic from the BufferReaderEvenOddDemo
[06:30] class.
[06:30] So here you can see as of now I'm trying to ask only a single numerical value.
[06:35] That's why my end user is going to enter only a single value.
[06:38] But this time let's ask two numerical values for the same.
[06:42] I'm going to update this code to please enter a first numeric value.
[06:47] So this is the first statement and post that I'm going to copy the same two lines and paste it again.
[06:54] And this time I'll say please enter a second numeric value.
[06:59] So whenever we are invoking this redLine() method using the BufferReader object in those scenarios,
[07:05] the console or your Java program, it is going to keep wait to accept an input data from an end user
[07:13] with the help of keyboard.
[07:14] Since I'm trying to invoke this readLine() method are to two different places, it is going to wait two
[07:20] times throughout the Java program, so let me replace this input variable names as input one and input
[07:26] two, followed by
[07:27] I'm going to convert the input1 into the int value and assign to the variable, which is int num1
[07:34] .
[07:35] I'm going to do the same for input to two variable as well, and rename this into variable to num2
[07:41] and post that
[07:42] I'm going to remove this if else condition, and I'm going to write a simple logic which is into result
[07:50] is equal to num1 + num2.
[07:54] And at last I'm going to print out the statement which is the sum of two
[08:00] given numbers is colon followed by what is our result that we have.
[08:07] So we are storing the result inside the result variable.
[08:10] Now let me try to execute this program.
[08:12] First you can see I have a statement which is please enter a first numeric value.
[08:16] So I'll try to enter some 46 as an input post that I need to press enter immediately.
[08:22] It is going to ask me please enter a second numerical value.
[08:26] So this time I'm going to enter 54 as an second numerical value.
[08:32] And after entering this 54 value, I'm going to press the enter button one more time.
[08:37] And with that, my entire Java program is going to be executed.
[08:41] And at last you can see we are getting the expected output, which is the sum of two given numbers is
[08:47] 100.
[08:48] I hope you are clear with these examples.
[08:51] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
