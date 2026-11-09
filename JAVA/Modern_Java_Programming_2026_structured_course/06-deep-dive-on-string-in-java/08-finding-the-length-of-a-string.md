# 6.8 — Finding the length of a String

> Section 6: Deep dive on String in Java

[00:00] Inside this lecture, let's try to talk about the length method available inside the string class.
[00:06] What is the purpose of length method?
[00:08] Using this length method, we can identify what are the total number of characters available inside
[00:16] my string object.
[00:17] Sometimes you may have to write your business logic based upon the length of your characters inside
[00:23] the string.
[00:24] In such scenarios, to identify the length of your string data, you can use the length method.
[00:30] This length method is a non static method or a instance method, which means you can only invoke this
[00:36] method with the help of object of string data type.
[00:40] I can also show you more details about this method.
[00:43] For the same.
[00:43] Let me look for the string class.
[00:45] I'm pressing command or shortcut which will open me a search box.
[00:49] Inside window the shortcut is going to be control N here.
[00:53] If I try to type the string class name, you can see I'm not getting any search result because as of
[00:59] now we are trying to search under the classes available inside this project.
[01:04] If you want to look even inside the Java libraries as well, you need to select these all.
[01:10] As soon as you select this, all you can see we are able to see a class which is string Dot Java that
[01:16] is available inside that JDK library.
[01:18] So let me open this.
[01:20] Inside this class we need to look for the method length like we discussed previously.
[01:26] To see the list of methods and fields inside a class, we can use a shortcut which is command F to.
[01:33] Well, this is going to show me the list of methods and variables inside the string class.
[01:38] Here I'm interested more about the length method.
[01:41] If I open this length method, you can see this is a non-static method or an instance method which is
[01:47] going to return the int data type value, and it is not going to accept any input data based upon the
[01:52] method.
[01:53] Comments.
[01:53] You can easily identify that this method is going to return the length of the string.
[01:58] The length is equal to the number of Unicode units inside the string.
[02:02] That means your length is going to be always equal to the number of characters available inside the
[02:08] string object.
[02:09] Let's see how to invoke this method for the same.
[02:11] I already created a class with the name length method demo.
[02:14] Inside this class I'm going to create main method here.
[02:18] First I'm going to create a string object with the name str one, and to this str one.
[02:24] I'm going to assign a string data, which is hello post that I'm going to also create one more string
[02:31] object with the name str two.
[02:33] And to this str two I'm going to assign the data which is world.
[02:38] After these two variables.
[02:40] I'm also going to create one more variable or one more object of string with the name combined.
[02:47] And to this variable, I want to assign that data from str one, followed by I want to append the space,
[02:55] followed by str two.
[02:57] That means this combined string object is going to hold the value.
[03:02] Hello space world!
[03:03] Now let's try to understand how to invoke the length method.
[03:07] As of now, we have created the objects of the string.
[03:10] Using these objects, we can easily invoke the length method.
[03:13] First, I'll try to mention a Java statement here, which is int length one to this length one int variable.
[03:22] I want to assign the output from the length method that I'm going to invoke with the help of str one
[03:28] object.
[03:29] So first let me mention object name and after that using dot operator I can look for the length method.
[03:36] So this length method is not going to accept anything.
[03:39] And as an output it is going to return an int value.
[03:42] So behind the scenes this method is going to give you the total number of characters inside the given
[03:50] object.
[03:51] So what is object str one.
[03:53] So here if you can count there are five characters like one, two, three, four, five.
[03:59] Obviously we are going to get the output as five.
[04:01] Very similarly, if I try to print out other length values like for str two with the variable name length
[04:09] two.
[04:10] And very similarly, I'm also going to do for combined object as well with the variable name as length
[04:16] three.
[04:17] This time, instead of printing these length values, I'm going to show you these values at runtime
[04:22] by putting a debug point.
[04:24] So I'm going to put a debug point just before this curly brace.
[04:28] That means my Java execution is going to stop at this point of time.
[04:32] So what is a debug point.
[04:33] The other name for breakpoint is debug point.
[04:36] So to stop the execution at the breakpoint we need to run the program using debug option.
[04:41] So let me run the same.
[04:43] You can see my method execution stopped and right now the execution stopped at the line number 11.
[04:50] That's why I'm able to see this highlighted line at this line.
[04:53] If I go to the debug window and try to expand it here, you'll be able to see what are all the variables
[05:00] available inside this main method.
[05:03] We are right now inside the main method at the line number 11.
[05:07] At this point of time, we have variables like str one, str two and combined.
[05:13] So all these are objects, whereas the other variables that we have created like length one, length
[05:18] two, length three.
[05:19] These are primitive data types which are going to hold only one value.
[05:24] So for the length one the value is five, whereas for length two also it is going to be five, but for
[05:30] length three it is going to be 11.
[05:32] The reason why it is 11, because we also added a space value, which means even the space value is
[05:39] also going to be considered as a valid character.
[05:42] That's why we're able to see the length here as 11.
[05:46] As a next step, I can try to create an empty string and let's see what is the length of the empty string.
[05:52] Before I try to do that, let me release this breakpoint and inside my main method, just after this
[05:57] length three variable, I'm going to create an variable which is empty string.
[06:03] And to this empty string I'm going to assign the double quotes without any values inside the double
[06:10] quotes.
[06:10] That means we are trying to assign an empty string to this object variable.
[06:14] Now, to understand the length of this variable, I can invoke the length method and try to cast that
[06:19] into another int variable.
[06:21] So that's a very lengthy process.
[06:23] Instead we can also use one shortcut here the shortcut is going to be int empty length.
[06:30] After mentioning this empty length I'm going to mention the empty representation of the string value.
[06:36] Now you can see I have mentioned the string value which is empty value.
[06:40] If I mention the dot operator after my string value, I can invoke all my methods of string, because
[06:48] even the literal value of string is going to be considered as an object by your JVM.
[06:54] That's why as soon as I type dot, I am able to see all the list of methods.
[06:59] So if I try to run this line of code, I'm going to get the output as zero.
[07:03] With this, we no more needed this line which we have on the top of the Java statement.
[07:08] Let me also mention one more example with the same syntax.
[07:12] For the same, I'm going to mention int length four.
[07:15] After the length four, I'm going to mention some random string, which is hello.
[07:20] And after that I'm going to mention dot operator and invoke the length method.
[07:25] So if I try to run this program, my program is going to be paused at this breakpoint.
[07:30] With that we should be able to see what are the values inside these two new variables that we have created.
[07:35] So let me run this program in debug mode.
[07:37] This time you can see we have two new int variables.
[07:41] Empty length represents zero and length four has a value which is five.
[07:46] This way, any time we can easily identify the total length value of your string data, you can store
[07:53] any amount of data inside your string.
[07:55] Maybe you can store one page of data.
[07:58] Still, with the help of length method, we can easily identify the total number of characters.
[08:03] The length method is going to be a savior inside real project scenarios like maybe you have a website,
[08:09] and inside the website you have a text box inside the text box at the max.
[08:13] You want to allow only 50 characters to be entered by the end user.
[08:18] Beyond 50 characters you don't want to accept in such scenarios, with the help of length method, we
[08:24] can easily identify how many characters entered by my end user, and if we exceed more than 50, we
[08:29] can throw an error.
[08:30] As usual, I have mentioned all the points that we have discussed inside this lecture in this slide.
[08:36] Please refer them for more details.
[08:38] I want to be super careful with the last point that I have mentioned here.
[08:43] Even the string literals like hello also is going to be considered as an object by your JVM.
[08:50] That's why after mentioning the values like hello are empty string, we are able to invoke the methods
[08:56] available inside the string class.
[08:58] But whenever we are following this approach, there is a drawback.
[09:01] Whatever string object that you have created, we cannot refer it in the next business logic that you
[09:07] have inside your program.
[09:09] So here I am trying to mention the hello string that means.

----------------------------------------
