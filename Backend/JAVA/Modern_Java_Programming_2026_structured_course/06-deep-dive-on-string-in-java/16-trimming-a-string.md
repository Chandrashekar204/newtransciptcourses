# 6.16 — Trimming a String

> Section 6: Deep dive on String in Java

[00:00] Inside this lecture, let's try to understand how to perform trimming of a String.
[00:05] So what is trimming operation?
[00:07] Trimming is a process of removing blank spaces that we have at the starting and at the ending of the
[00:13] given String, with the help of the trim() method that is available inside the String class, we can get
[00:18] rid of any extra spaces or control characters that we have at the beginning and end of the given String.
[00:26] For example, you can see there are some examples I have given in the very first line of statement
[00:31] I have a String which has a space value just before and after the Java word.
[00:37] If I invoke the trim() method on top of the String object, all the leading and trailing spaces will be
[00:43] removed.
[00:44] And I'm going to get a simple output, which is Java.
[00:46] In the second Java statement, I have a space at the end of my String in this scenario
[00:51] also, the trim() method is capable of deleting the space that we have at the end of the Java word.
[00:57] Apart from removing or cleaning the space values, the trim() method is also capable of removing the control
[01:04] characters.
[01:05] So what are control characters inside Java
[01:07] there are some escape sequence values like \n means it indicates to Java that I want to store
[01:15] the value next line.
[01:16] So whenever we are storing these \n inside the string, my String is going to have the a blank
[01:23] line value.
[01:24] And similarly \t means tab space and \r means carriage return.
[01:30] So these type of control characters will also be removed by the trim() method.
[01:34] For example, inside the third Java statement just before and after my word Java
[01:39] there are so many control characters like next line, tab space.
[01:43] So all of them they are going to be removed when we invoke the trim() method.
[01:47] Apart from blank space and control characters, the trim() method is capable of removing all the Unicode
[01:55] character values that are less than the Unicode value, which is 0020.
[02:00] So the decimal representation of this Unicode character is 32.
[02:04] Let me show you the Unicode table so that it is more clear for you.
[02:08] So this is our Unicode table.
[02:10] Here we have some Unicode values which has decimal value which are less than 32.
[02:15] So you can see from 0 to 31 we have.
[02:18] So all these characters are also going to be removed by your trim() method like vertical tab line feed
[02:26] backspace bell character enquiry character.
[02:30] So these are all special characters that we can use inside a String.
[02:35] But 99% of the times we only use blank space.
[02:39] But I'm just trying to share this extra information since it is going to help you inside your Java interviews.
[02:45] Before we try to see the demo of this trim() method, I want to share an important information about this
[02:51] method.
[02:52] Whenever we are using this trim() method, it is not going to remove the extra spaces or control characters
[02:58] which are in between your String data.
[03:01] It is only going to remove the leading and trailing characters, but not the spaces and control characters
[03:09] which are available in between your String data.
[03:12] So here you can see I have given two examples.
[03:15] The first String has j a\nva space.
[03:21] When I invoke this trim() method, all the leading and trailing blank spaces will be removed.
[03:26] But whatever \n that I have in the middle of the String is going to be retained, because my
[03:33] trim() is not going to delete anything in between of the String.
[03:36] The same you can see inside the next example as well.
[03:40] I hope this is clear.
[03:41] Now let's see the demo of this trim() operation very quickly inside the intelliJ.
[03:46] To see the demo of the trim() method, I have created a class with the name StringTrimDemo and I also
[03:53] created a main() method.
[03:54] Please note that all the classes that I'm trying to create inside this section, they're all going to
[03:59] be available inside this section6 project, so please check the GitHub repo if you have any questions
[04:05] inside this main() method
[04:07] first I'm going to create a String with the variable name as java1.
[04:12] And using this String object I'm going to save a String data which is space Java space and post that
[04:20] I'm going to invoke that trim() method.
[04:23] Obviously, by the time the output is assigned to this Java one variable, all the trailing and leading
[04:29] spaces will be removed.
[04:30] We can also see the same in the demo in few seconds.
[04:33] But before that, let me try to copy these statements multiple times and rename these object names to
[04:39] java2 and java3.
[04:41] And here I will just mention the space at the end of the word Java.
[04:46] Now in the third statement I'm going to mention some control characters like \n,
[04:53] \t.
[04:54] So \t means tab space and \n means new line and
[05:00] let me mention some control characters just after that Java word as well.
[05:05] I'm going to mention \n and \r.
[05:09] If I try to execute this program inside the demo, it is going to be super clear for you.
[05:13] Like you can see, the java1 is going to hold the Java value without any trailing and leading spaces.
[05:20] The same applies for java2 and java3 object.
[05:24] Inside the java3 object
[05:25] you can see my trim() method is also deleted all the control characters.
[05:30] That's why we're simply seeing the word Java.
[05:33] Let me release the breakpoint and let me show you what will happen if you don't invoke that trim() method.
[05:38] So here I can change this variable name to java4.
[05:41] And I'm not going to invoke this trim() method.
[05:44] I'll show you how the String is going to look like so that you will be clear about this control characters
[05:49] that we have used.
[05:50] If I execute this program under the java4, you can see it is showing all the control characters.
[05:57] But if I open this here, it is pretty clear
[06:00] first we have a new line and post that there is a tab space given, and after the tab space, the Java
[06:06] word is added inside the String and post that we have a new line and return carrier.
[06:12] So if you want to remove all these kind of control characters, you can use trim() method like you can
[06:18] see under the third statement.
[06:20] Now let me show you the demo off trim() method by putting some space values in between the java String
[06:27] for the same
[06:27] I'm going to copy the first statement and paste it here two times, and I'll change these variable names
[06:34] to java5 and java6.
[06:37] This time I'm going to create a space in between my Java String data.
[06:42] And here also I'm going to mention some control character which is \n.
[06:48] Now let's see how the trim() is going to work.
[06:51] If I execute this program you can see the trim() method is removed
[06:55] all the spaces that we have at the starting and at the ending of the word, but it is not touching or
[07:01] it is not doing any deletion for the spaces and the special characters that we have in between the String
[07:07] data.
[07:08] That's why we are able to see a space here.
[07:10] And if you open this String, you'll be able to see ja, and the next value is moved to the next line
[07:16] because we have used a control character which is \n.
[07:20] With this I'm assuming your super clear about trim() method.
[07:24] Do you know what is the use case of trim() method in the real projects?
[07:27] Sometimes developers, they want to compare two different Strings, and when they want to compare two
[07:33] different Strings, they want to ignore all the starting and ending spaces and control characters.
[07:39] I can show you a demo as well here.
[07:41] Suppose think like
[07:42] I want to check if two different Strings hold the same data.
[07:46] So here I'm going to create a boolean and the name of the boolean variable is isSame.
[07:52] And here first I'm going to give a String data which is Java.
[07:56] Next I'll invoke the equals() method.
[07:59] And to this equals() method I'm going to pass Java.
[08:02] But at the end I'm going to keep a space we for humans both these words are same because we as humans
[08:10] we always ignore the space values at the end and at the starting of the word.
[08:14] But the missions are computers
[08:15] they are not going to work that way.
[08:17] We need to give very clear instructions.
[08:19] So if I try to execute this method, obviously the isSame variable is going to have a value false.
[08:26] To handle these kind of issues
[08:29] the developers, they're going to invoke that trim() method.
[08:33] So with this what is going to happen is my trim() method is going to remove this space.
[08:39] And the same it is going to send as an input to the equals() method.
[08:43] And with that we are going to get the same as true as an output.
[08:47] Do you see the power of trim() method.
[08:49] So whenever you are into these kind of scenarios please always use the trim() method.
[08:54] I hope you enjoyed this demo.
[08:55] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
