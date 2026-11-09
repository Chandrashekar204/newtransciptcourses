# 13.4 — Demo of Java Basic Input

> Section 13: Accept input using BufferedReader and Scanner

[00:00] As of now, we have a clear understanding on how to print a given data onto the output stream like console.
[00:08] Now let's shift the gears and focus onto the how to accept the input from an end user.
[00:14] While we are trying to execute a Java program. For the same, let's look for any variable with the name
[00:21] in inside the System class, because we already have a variable with the name out, which is helping
[00:27] us to print the output onto the console with the help of PrintStream object.
[00:33] That's why in the very similar lines, let's look for an variable which is quite opposite of out.
[00:39] So what will be the opposite word of out it is going to be in?
[00:43] That's why let me look for in static variable inside the System Java class.
[00:49] So if I can scroll down here there should be a static variable with the name in.
[00:54] So let me click on this.
[00:56] You can see this is also following the same syntax like public static final.
[01:01] But the type of this variable is InputStream.
[01:04] So this InputStream is going to help us to accept the input from the end user and processing the same
[01:11] inside our Java program.
[01:13] Let me show you the documentation about these InputStream.
[01:16] This represents standard input stream.
[01:18] This stream is already open and ready to supply input data.
[01:23] Typically this stream corresponds to keyboard input or any other input source specified by the host
[01:31] environment
[01:32] or user, like we know, one of the most common approach to ask the input data from an end user is
[01:38] with the help of keyboard, so we can detect what the end user is typing from the keyboard.
[01:44] And the same we can read inside the Java program with the help of this InputStream object.
[01:49] The other common approaches are reading the data from an existing file.
[01:54] So there are multiple ways on accepting the data.
[01:57] But in the most of the scenarios, we will ask the end user to enter the data with the help of keyboard.
[02:03] So that's why we are going to put good amount of effort on understanding how to achieve this.
[02:09] So now we are very happy because we are able to find an variable with the name in which is going to
[02:15] help us to create the object of InputStream, and with the help of this InputStream object, what
[02:21] we are going to achieve, we are going to make our program to accept the input data from the end user.
[02:27] Let me open this InputStream Java class.
[02:29] So this class is present inside the java.io package.
[02:34] Even the PrintStream class, which is helping us to display the output with the help of out variable.
[02:40] It is also present inside the same java.io package.
[02:43] Here IO indicates input and output, so this is one of the important package inside the Java library.
[02:51] As a next step, let me build a Java program, and inside the Java program we can try to build some
[02:57] logic to accept the data from the end user.
[02:59] For the same, I'm going to create a new class.
[03:01] Since we are into the new section, I have created a Java project with the name section13.
[03:07] And inside this as of now you can see the source folder is empty.
[03:10] Here I'm going to create a new Java package.
[03:14] The package name is going to be com.eazybytes.input, because I'm going to build the logic
[03:22] related to the input inside this package.
[03:25] Once this package is created I'm going to create a Java class which is JavaBasicInputDemo.
[03:34] So these are Java class name.
[03:36] Inside this Java class we can try to create the main method.
[03:40] Once the main method is created I'm going to invoke first the System class.
[03:45] And inside the System class we have a static variable with the name in and this static variable it is
[03:51] going to give the object of InputStream.
[03:54] So once the InputStream object is created, I can use the method which is read().
[03:59] So with this I'm going to ask my end user.
[04:02] You can enter a input data on the console using your keyboard, and the same will be read by the input
[04:09] Stream object with the help of this read() method.
[04:12] But as soon as we are trying to invoke the read() method, we are getting a compilation error saying that
[04:19] Unhandled exception java.io.IOException.
[04:23] We are going to talk in detail about the exceptions and how to handle them in the coming sections.
[04:29] For now
[04:29] to resolve this compilation error, you can click on this link which is add exception to the method
[04:35] signature.
[04:35] The method signature is going to be updated with the new statement like you can see throws IOException.
[04:42] So whenever someone adds throw statement along with the type of exception like IOException, it is
[04:48] an indication to client parties are the other applications who are going to invoke your method.
[04:54] Saying that when you try to invoke this method, there is a very good chance that you may get
[05:00] IOException.
[05:01] That's why on your side.
[05:02] Please take care of handling these exception.
[05:05] So this is what we are trying to communicate with the help of these throws
[05:09] IOException.
[05:10] If something is not clear, don't worry.
[05:12] Like I promise, we are going to talk in detail about the exception handling in the coming sections.
[05:17] Now our compilation error is resolved.
[05:19] If you can hover on this read() method, the return type from this method is int.
[05:25] The same you can see here like it is going to return into data type.
[05:28] That's why on the left hand side I'm going to mention int num is equal to as a variable name.
[05:36] But before I try to execute this program, I'm going to mention some System.out.println() saying
[05:41] that please enter a value.
[05:45] So I'm just asking the end user to enter the value.
[05:49] After printing the statement inside the console.
[05:52] My Java program is going to wait for my end user input because we are using these read() method.
[05:59] So let's see this magic.
[06:01] So I'm trying to execute this program in a debug mode.
[06:04] And as of now you can see I have a statement which is please enter a value.
[06:09] Now I'm going to enter a value which is five.
[06:13] So as soon as I enter five I'm going to press enter.
[06:16] And you can see right now the program is terminated after taking the input.
[06:20] But we're not doing anything with the input inside our program.
[06:23] Maybe what we can do is we can try to print a statement which is the user entered a value followed by
[06:33] colon space, and I can append the variable num.
[06:37] So this is what we are trying to print once the user entered his input.
[06:42] So now let me try to execute the same program this time
[06:45] also I'm going to enter a value inside my console.
[06:47] You can see my program still running here and it is waiting for my input.
[06:52] So I'm going to enter the value as five.
[06:54] So if I press enter you can see I'm getting the output as the user entered a value 53.
[07:00] Why it is showing 53 because I only entered five, it should display five, right?
[07:05] The reason why it is showing 53 is whenever you try to use this read() method available inside the
[07:11] InputStream class, it is going to return the Ascii representation of your input data.
[07:17] For example, this is a Ascii table.
[07:19] If you see for input data five the Ascii value, it is going to be 53.
[07:24] You can also confirm this here.
[07:25] Like here I have the Char value as five and its Ascii value
[07:29] it is going to be 53.
[07:31] Maybe this time I am going to enter dollar as an input.
[07:35] And with that I should get the output as 36.
[07:38] Let me try this.
[07:39] So let me execute this program and this time I'm going to press dollar.
[07:44] And with that I'm going to get the output as 36.
[07:47] Hooray!
[07:48] This is working like we expect.
[07:50] And now my program is capable of accepting the input data from the end user.
[07:55] But there is a drawback with the read() method that we are trying to invoke.
[08:00] It is always going to give you the Ascii representation of a given value.
[08:04] On top of that, it is only capable of accepting a single character.
[08:09] For example, if I try to enter multiple values, maybe I'm trying to enter five six, seven as an input
[08:15] value, but it still it is going to give me the Ascii value representation of five only because it is
[08:22] simply going to ignore the second and the third character.
[08:26] This confirms the read method is only capable of accepting a single character value.
[08:32] On top of that, it is always going to return the value as Ascii representation of the given input data.
[08:38] But can we live with this?
[08:40] Off course not, because it has a lot many disadvantages, and this is a very basic way of asking the
[08:46] end user to enter his data.
[08:49] And we should also highlight to the end user, I'm only going to accept only one character at a time.
[08:54] So this is not going to work in real projects or in real interviews.
[08:58] This should be a better way.
[08:59] Off course, we are learning one of the top language in the world, which is Java.
[09:03] So Java should have some better approach.
[09:06] So let's try to see what are those better approaches that we have inside Java to accept the input data
[09:13] from the end user.
[09:14] For your reference inside this slide, I have mentioned all the points that we have discussed so far
[09:18] about the System.in and the read() method and the code that we need to use to read the single character
[09:26] value with the help of read() method.
[09:28] So these three points we already discussed now coming to the last point, which is what are the efficient
[09:34] ways available inside the Java to accept the input data from the end user?
[09:39] There are two different approaches.
[09:41] The very first one is with the help of BufferReader class, and this class is present inside the same
[09:49] package, which is java.io.
[09:51] The object of BufferReader class is also enable you to accept the data from an InputStream object,
[09:58] like a keyboard or from
[10:00] a file, but it has a lot of advantages, which is it allows you to accept any kind of data, not only
[10:06] single characters
[10:07] someone can enter a sentence.
[10:08] The same can be accepted and processed by the BufferReader.
[10:12] So this BufferReader option is available from that day one of Java, like from the initial version
[10:19] of Java.
[10:20] Whereas if you look at the second approach, which is with the help of Scanner class, and this Scanner
[10:25] class is available inside the package java.util.
[10:29] The second option, which is Scanner class, is added or introduced only from the Java 1.5 version.
[10:37] Or in other words, we can say Java fifth version.
[10:40] So we are going to explore in detail about these two options.
[10:44] And using the same, we are going to accept the data from the end user inside our Java programs.
[10:50] I hope you are clear.
[10:51] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
