# 6.24 — How to create mutable strings in Java

> Section 6: Deep dive on String in Java

[00:00] We know when we create objects with the help of String, they are going to be immutable.
[00:05] So how to build a mutable String data.
[00:08] There are three different approaches to build a mutable string values inside Java.
[00:14] The very first approach is with the help of StringBuilder.
[00:17] Using this class we can create, update, delete, insert string data, whatever update operation that
[00:25] you are going to do with the help of StringBuilder.
[00:27] The string data is going to keep changing on a single StringBuilder object.
[00:32] Unlike string, the StringBuilder object reference is always going to point to the same object.
[00:38] Here you can see I have given an example whenever you want to store String data with the help of
[00:43] StringBuilder, you need to first create an object of StringBuilder with the help of new operator and a constructor
[00:50] of the StringBuilder, and to the constructor of StringBuilder.
[00:53] You can either invoke the default empty constructor or to the constructor of the StringBuilder.
[00:58] You can also pass the input string data.
[01:02] Here inside the example, I'm trying to pass the hello as an input string data, so by the time my
[01:08] StringBuilder object is going to create, it is going to hold hello string data inside it.
[01:13] Later on, if I want to append new information to the same StringBuilder object, I can invoke the
[01:19] method which is append() available inside the StringBuilder.
[01:23] Using append(), I can try to update my original string with the new string.
[01:28] Here I'm trying to invoke the append() and I'm trying to add new content, which is space world.
[01:34] And with that, whenever we try to print out these StringBuilder object by converting into string,
[01:40] we are going to get the output as Hello world!
[01:42] This way we can always update the String data with the help of StringBuilder object.
[01:47] Once you feel like that, you are done with the update operations of your string data.
[01:52] At last, you can invoke the toString() method to convert your StringBuilder into a String object.
[01:59] Just like StringBuilder
[02:01] we also have another option which is StringBuffer.
[02:04] StringBuffer is also going to work very similar to StringBuilder.
[02:09] The way you create the objects, the way you append the data to the StringBuffer object,
[02:14] everything is going to be same as StringBuilder.
[02:17] But the reason why we have two options in the form of StringBuilder and StringBuffer is StringBuffer
[02:23] objects are thread safe, whereas StringBuilder they are not thread safe.
[02:28] Whenever you are trying to run your Java programs, you can run them in an multi-threading environment.
[02:34] We are going to talk about what are threads and what are multi-threading environments in the coming
[02:39] sections.
[02:39] For now, please note that thread is like a process that is going to accept the request from a single
[02:45] user.
[02:46] So if your Java code is deployed into a production server and if there are many end users, they are
[02:51] trying to access your Java code, then each end user they are going to get a thread.
[02:56] So using the threads the Java program is going to be executed in an isolated environment.
[03:03] So if your program is going to be executed in an multithreading environment, it is always advisable
[03:09] to use the StringBuffer.
[03:11] Because whatever objects that you are going to create with the help of StringBuffer, they are thread
[03:17] safe, whereas StringBuilder objects, they are not thread safe.
[03:20] So if you ask me when to use StringBuilder and when to use StringBuffer, I would say you can always
[03:26] use the StringBuilder.
[03:27] If you know that your code is going to be deployed in a single threaded environment, and if you are
[03:33] looking for a higher performance and thread safety is not a concern, then in all such situations you
[03:39] can use StringBuilder.
[03:40] Otherwise, if you are looking for an option where your code is going to be deployed in a multi threading
[03:46] environment, and you want to make sure that thread safety is always followed in that scenario, always
[03:51] go with the StringBuffer.
[03:53] As of now, we are able to update the content of the StringBuilder and StringBuffer objects with the
[03:59] help of append() method.
[04:00] Apart from the append() method, these classes, they have many instance methods using which we can try
[04:07] to update the string content that we are trying to store inside the objects of Stringbuilder and StringBuffer
[04:12] .
[04:13] Apart from these mutable operations methods, StringBuilder and StringBuffer, they also have an important
[04:20] method which is reverse() method.
[04:22] Whenever you invoke this reverse() method, with the help of the objects of StringBuilder and StringBuffer
[04:27] whatever content that you stored inside the objects of these classes will be reversed and stored
[04:34] as a new content.
[04:35] Inside the objects.
[04:36] We can see the demo of the reverse() method in few minutes.
[04:39] Now, as a next step, I want to show some code snippets on how to use these methods to alter the content
[04:46] of the objects of StringBuilder and StringBuffer.
[04:49] Here, like you can see the way we use the StringBuilder and StringBuffer, they are going to be same
[04:55] the methods available inside these classes, they are also going to be same like we
[05:00] discuss.
[05:00] The only difference is StringBuffer objects
[05:03] they are going to be thread safe, whereas StringBuilder objects they are not thread safe. Here in the
[05:09] both examples
[05:10] first, I'm trying to create an object of StringBuilder and StringBuffer with the default constructor.
[05:15] That means when I execute the first line of statement, there won't be any content.
[05:20] It is like an empty string.
[05:22] Later on you can see with the help of append() method
[05:25] I'm trying to append new content which is world, and with that, the content inside my object is going
[05:31] to be like this,
[05:32] like we are going to have only world after the append()
[05:35] you can see I'm trying to invoke the insert() method, and to the insert() method we can pass what is the
[05:42] index number at which the new content has to be inserted.
[05:46] Here I'm trying to give the index number as zero.
[05:49] That means I want this new content to be inserted from the starting position.
[05:54] And with that, the content that we have inside the object is going to become Hello World.
[05:59] And after the insert you can see I'm trying to invoke a method which is deleteCharAt().
[06:05] To this method, we can provide an index number based upon the index number that we are providing the
[06:12] char value at
[06:13] that particular index is going to be removed after the deleteCharAt() method.
[06:17] I'm trying to invoke the insert() method to the insert() method we need to pass what is the index number
[06:24] where you want to insert a char value.
[06:26] So I'm trying to bring back my o char value again at the same position.
[06:31] That's why I'm giving the insert index number as four and the value as o char.
[06:36] With that, the content inside my object is going to be Hello world!
[06:41] After the insert, I'm trying to invoke the set length() method.
[06:45] Whenever we are invoking this method, we can provide the length that we want to set.
[06:50] Here I'm trying to set the length as five.
[06:52] With that, whatever content beyond the length of five will be removed.
[06:58] We know the index is going to start at zero.
[07:00] That means with the length of five, my StringBuilder a StringBuffer, they are going to retain the
[07:06] data up to the index number four.
[07:09] After index number four, whatever data we are going to have will be removed because we are trying to
[07:15] falsely set the length as five with the method which is setLength().
[07:19] So by the time we execute this setLength() method, the content is going to look like
[07:23] Hello!
[07:24] at last I'm trying to invoke the reverse() method.
[07:26] reverse() method is an interesting method.
[07:29] It is simply going to reverse your content.
[07:32] So whatever char value that used to have at the end that will be moved to the initial position and
[07:38] whatever char value that used to have at the starting index, that will be moved to the end index.
[07:44] That's why you can see the output is o l l e h.
[07:48] Please make a note about the purpose of the reverse() method, because in the coming lectures, I'm going
[07:53] to give you an assignment based upon this reverse() method.
[07:56] So as of now we discussed two approaches and how to make the string data mutable inside Java.
[08:02] We also have a third approach which is going to be used very rarely by the developers.
[08:07] But I just wanted to show you that option as well, so that you are familiar with the third option as
[08:12] well.
[08:12] The third approach that we can use is with the help of a class called CharArrayWriter.
[08:18] So first we need to create an object of this class post that we can invoke a method called right().
[08:24] Whenever we invoke this write method, we can add the new content to the object of the charArrayWriter.
[08:31] So here you can see I'm trying to invoke the right() method two times.
[08:34] Post that I'm trying to write hello and post that I'm going to write new content, which is Space World.
[08:40] Once you feel like you have made all the changes and updates to your String data, at last you can invoke
[08:47] that toString() method using the object of CharArrayWriter.
[08:51] And with that, whatever content that you stored inside the object of CharArrayWriter is going to be
[08:56] converted into an String object.
[08:58] That's why if I try to print the output of this String object, I'm going to get an output, which is
[09:03] hello world.
[09:04] So we have discussed three different approaches.
[09:06] So all these three approaches they're going to let you build mutable string data.
[09:11] But please note that we always need to use this approaches only if it is necessary.
[09:16] Because all these mutable approaches that we have discussed, they are less efficient compared to the
[09:21] String class.
[09:22] That's why most of the times you see developers using the string.
[09:25] But if you have a business scenario where you're going to change your string data a lot, then please
[09:32] use any of the three approaches that we have discussed.
[09:35] I hope you are clear with this theory discussion.
[09:37] In the next lecture, let's see the demo of all these three approaches by writing a Java program.
[09:43] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
