# 13.10 — Introduction to Scanner & Demo - Part 1

> Section 13: Accept input using BufferedReader and Scanner

[00:00] We know inside Java we have two different efficient approaches to read the data.
[00:07] The very first one is with the help of BufferReader, which is available inside the java.io package.
[00:13] As of now, we discussed everything about the BufferReader.
[00:16] As a next step, let's try to understand the second approach that we have, which is with the help of
[00:22] Scanner class available inside the package java.util.
[00:26] This option is introduced only from the 1.5 version of Java.
[00:31] Using Scanner, we can overcome the drawbacks of BufferReader and compared to the BufferReader, using
[00:38] Scanner is very easy.
[00:39] That's why most of the developers they use Scanner a lot on day to day basis, but that doesn't mean
[00:45] you should avoid BufferReader completely.
[00:47] There are certain scenarios where BufferReader has its own advantages.
[00:51] We are going to discuss all of them in few minutes.
[00:54] For now let me try to explain you what are the drawbacks that we have with the BufferReader and post
[00:59] that we can try to understand how to overcome them with the help of Scanner option.
[01:04] This is the program that we have written to identify if a given number is a prime number or not.
[01:10] You can see at this point of time we are trying to accept the input from the end user.
[01:16] And what is the input here?
[01:18] It is a numerical value regardless of the type of your input data
[01:22] always BufferReader, readLine() method.
[01:25] It is going to give that data in an String object format later on, based upon your business requirements
[01:32] you can convert these String object into an int variable or double variable, or a float variable or
[01:39] a boolean variable, and accordingly you can try to perform operations on the input data.
[01:44] For example, here we are receiving a number from an end user.
[01:48] The same is getting assigned to this String object.
[01:51] But since we can't perform the modulus operation on top of a String object, we need to make sure we
[01:58] are converting the String object into a proper numerical int value.
[02:03] That's what we are trying to do here.
[02:05] So this is one of the drawback of BufferReader.
[02:07] So every time you receive the input data using BufferReader, it is always going to give you in a String
[02:13] format.
[02:13] It is the responsibility of the developer to convert the input data into corresponding data format,
[02:19] to proceed further inside his business logic.
[02:22] And the second drawback of BufferReader is you can see whenever we want to create the BufferReader
[02:27] object, we need to create the object of InputStreamReader.
[02:31] And to this InputStreamReader, we should tell the what is the input stream source, whether it is
[02:37] a file or whether it is an keyboard.
[02:39] So it is a two step process to create the object of BufferReader.
[02:43] So all these challenges we can try to overcome with the help of Scanner class.
[02:49] Like I said before, Scanner class is available inside the package java.util inside this class
[02:56] like you can see here,
[02:57] by default, the buffer size it is going to maintain is one KB or 1024 bytes.
[03:04] So this buffer size we can't change.
[03:06] Whereas in BufferReader we can change this based upon our own requirements.
[03:11] But with Scanner there is no option.
[03:12] You need to execute your program with the default BUFFER_SIZE which is 1024.
[03:17] So we're going to discuss about the differences between BufferReader and Scanner in the coming lectures.
[03:22] For now, let's try to understand how to create an object of Scanner class and how to accept the input
[03:30] with the help of Scanner object.
[03:32] For the same, I'm going to create a new Java class.
[03:36] The Java class name is ScannerDemo inside this class,
[03:40] first, as usual I'm going to create
[03:42] the main() method post that I want to create the object of Scanner.
[03:47] So for the same I'm going to mention Scanner sc
[03:50] is our object name followed by new Scanner.
[03:55] And when we try to invoke that default constructor of Scanner() we are going to get a compilation error.
[04:00] Because even with the Scanner, when we are trying to create the object of it, we need to tell from
[04:06] where the data it needs to read.
[04:08] So with the Scanner, we don't have to pass the object of InputStreamReader like we did for the
[04:14] BufferReader.
[04:14] Instead, we can directly mention the input stream source which is System.in.
[04:22] So with this I'm telling please accept the input data using this keyboard.
[04:27] So did you see how easy it is to create the object of Scanner?
[04:30] Whereas for the BufferReader it is a two step process.
[04:34] So this is the drawback of BufferReader which we are able to overcome with the help of Scanner class.
[04:40] Once the object of Scanner class is created, I'm going to write a business logic to ask the end user
[04:46] about his name and age.
[04:48] So first I'm going to have an System.out.println() statement using which I'm going to print a
[04:54] statement which is enter your name, followed by I will try
[05:00] to read that data with the help of Scanner object.
[05:04] By using sc. I need to use the next() method.
[05:09] So using the next() method we should be able to read the input stream data entered by the end user.
[05:16] We know the name is always going to be in an alphanumeric format.
[05:19] That's why I'm trying to invoke the next() method, which is going to return that data in a String representation.
[05:26] Now I'm going to take these two lines of code and paste it again.
[05:31] This time I'm going to ask to enter his age details.
[05:35] That's why I'm trying to update the statement to enter your age.
[05:38] We know the age is always going to be a numerical value.
[05:42] So that's why instead of next(), I'm going to invoke the nextInt() method.
[05:48] So whenever we are invoking the nextInt() method we are telling to the scanner please read the data
[05:53] entered by my end user and convert the same into an int value.
[05:58] So if you try to hover on to this nextInt() method, you'll be able to see that the return type of
[06:03] this method is int.
[06:05] That's why on the left hand side we can say int age as the variable name.
[06:10] And at last I can write a System.out.println() statement with the value hello space.
[06:17] And to this hello, I'm going to append the name entered by my end user, followed by a String.
[06:23] And inside this String I'm going to mention comma followed by you are space, followed by.
[06:31] I'm going to append the age value to the String, and after the age value I'm going to mention one more
[06:37] String, which is years old.
[06:41] So this is the statement that I'm trying to print based upon the input data entered by my end user.
[06:47] And at last, just like how we close the BufferReader object.
[06:50] Similarly, we need to make sure we are closing the Scanner object as well.
[06:55] That's why I'm trying to invoke this close() method, which is available as part of the Scanner class.
[07:00] Let me try to execute this program and you can see first it is going to ask me the name.
[07:06] Please make sure you are entering your name only with a single word.
[07:10] I'm going to show you more details.
[07:12] What is going to happen if you try to enter a input data more than one word, which are separated by
[07:17] a space?
[07:18] For now, let's try to mention a single word name.
[07:21] So here I'm trying to mention the value as maiden followed by it is going to ask me what is my age?
[07:28] I'm going to type an age here, but this is not my real age.
[07:32] I'm trying to hide my real age.
[07:34] For now, I'm just trying to mention 25.
[07:37] And after this, if I press enter, you can see I'm getting an output statement, which is hello Madan,
[07:43] you are 25 years old.
[07:45] So did you see the beauty of Scanner?
[07:47] We are overcoming the advantages of BufferReader like
[07:52] we are able to create the object of Scanner very easily.
[07:54] On top of that, we have various methods available inside the Scanner class which we can invoke based
[08:01] upon the input data that we are trying to accept.
[08:04] For example, here I'm trying to accept String data.
[08:07] That's why I have used next, whereas for the int i need to use next int very
[08:11] similarly, we have other type of methods like nextByte(), nextShort(), nextBigdecimal(), nextBigInteger()
[08:17] nextBoolean(), nextDouble(), nextFloat() nextLong().
[08:22] So all these methods we can use based upon that type of input data that we are trying to accept.
[08:28] On top of that, whenever I'm trying to use the Scanner object, I will not be forced to handle the
[08:35] exception of IOException.
[08:37] Previously, when we are trying to use the BufferReader, whenever we are trying to invoke the readLine()
[08:41] method, it will force you to have.
[08:44] This throws IOException inside your method signature, whereas with the Scanner all these exception
[08:50] handling is going to be handled gracefully behind the scenes inside the Scanner class itself.
[08:57] So it is making developer life as easy as possible.
[09:01] I hope you are liking this.
[09:02] Let's try to discuss more details about Scanner in the next lecture as well.
[09:07] Thank you,
[09:07] bye.

----------------------------------------
