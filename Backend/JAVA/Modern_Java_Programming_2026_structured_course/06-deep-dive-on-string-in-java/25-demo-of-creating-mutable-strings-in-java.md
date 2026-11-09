# 6.25 — Demo of creating mutable strings in Java

> Section 6: Deep dive on String in Java

[00:00] Inside this lecture, let's see the demo of how to build a mutable strings
[00:04] with the help of the approaches that we have discussed in the previous lecture.
[00:08] To show you the demo, I'm going to create a new class inside my Java project and the class name is
[00:14] going to be StringMutableDemo.
[00:17] Inside this class, as usual, first we need to create a main() method for the same
[00:22] I'm going to type the shortcut which is psvm.
[00:25] Now first I'm going to show you the first approach.
[00:28] That's why I want to type a comments here saying that Approach 1. As part of this approach one, first
[00:35] we are going to build a object of StringBuilder.
[00:38] So how to create the object?
[00:40] By using the class name and post that, I'm going to mention the object name as StringBuilder, and
[00:46] after the object name I'm going to mention is equal to followed by new operator, and I will invoke
[00:52] the default constructor of the StringBuilder().
[00:55] With this, we have created a StringBuilder object, and it is going to have empty string.
[01:00] Now, using the same StringBuilder object, I want to invoke the append() method to this append() method
[01:07] I want to provide the String data.
[01:09] The String data is going to be world after the append() method.
[01:13] The next method I want to invoke is StringBuilder.insert() and to this insert() method I want to first
[01:20] mention what is the index number.
[01:22] I want to insert the new data from the index zero.
[01:26] That's why I'm trying to mention zero here and post that
[01:29] I'm going to mention the string as hello Hello , so that these hello space is going to be added just
[01:36] before the world.
[01:37] With that, the data present inside the StringBuilder after executing this line is going to be Hello
[01:43] World!
[01:44] Now let me show you how to invoke the deleteCharAt().
[01:48] So to this deleteCarAt() method we need to pass the index number.
[01:52] So here I'm going to pass the index number four.
[01:55] With that whatever character that we have at the index number four will be deleted.
[02:00] So what is the character it is going to be.
[02:02] Let's try to calculate H is going to be present at the zero index next 1234.
[02:09] So at fourth index we are going to have the character
[02:12] o the same is going to be deleted after executing this line of code.
[02:17] So with the help of deleteCharAt() we are able to delete a particular char.
[02:21] Whereas if you want an opposite behavior we can use the insert() method.
[02:27] Using insert() method we can pass what is the index number and what is a char value that you want to insert.
[02:35] So here I want to insert a char value which is O.
[02:38] And with that I'm going to bring the previously deleted char at the index four.
[02:43] And after executing this line of code, the String data inside my StringBuilder object is going to
[02:48] be hello Space world!
[02:50] Now let me show you how to invoke the setLength() method.
[02:54] So to this setLength() method, if I pass value as five, whatever content inside my StringBuilder object
[03:01] is going to be reduced up to a maximum of length five, that means I'm going to have that data only
[03:08] up to the index for any time
[03:10] if you have any question about a given method, you can always open the method and you should be able
[03:16] to read the javadoc comments which are present on top of the method.
[03:20] I hope you are clear.
[03:21] Now let me show you how to invoke the interesting method that we have inside the StringBuilder.
[03:27] And this method is reverse() method.
[03:29] When we invoke this reverse() method, whatever content that we have inside the StringBuilder object,
[03:35] it is going to be reversed at last.
[03:37] Once you feel like you have done all the required changes to your String data, with the help of StringBiulder,
[03:42] you can either use this StringBuilder object or you can convert these back to the String
[03:48] object.
[03:49] So how to convert this into the String object?
[03:51] Let me show you that very quickly the String object name.
[03:54] Here I'm going to give uays str and post that with the help of StringBuilder object.
[04:00] I'm going to invoke that toString() method.
[04:02] So when we invoke these toString() method I'm going to get an string representation of the data which
[04:08] we are storing inside the StringBuilder object.
[04:11] Now we have the complete code of Approach 1.
[04:14] We can try to see what is happen at the runtime by executing this code line by line.
[04:20] For the same, I'm going to keep a breakpoint at line number six and try to run this program in a debug
[04:25] mode.
[04:26] Now I can type the shortcut which is F8, to move my execution line by line.
[04:32] So right now you can see after executing my first line, the StringBuilder object has content which
[04:38] is empty string.
[04:39] After executing the second line, the content is going to be changed to the world.
[04:43] Now after the third line, the content is going to be changed to Hello world.
[04:47] Now I'm going to run that deleteCharAt() method.
[04:50] And with that the o character at the index four is deleted.
[04:54] Now I'm trying to insert it back with the help of insert() method.
[04:58] And you can see now I got the o
[05:00] character back into my StringBuilder object.
[05:03] After the insert operation, I'm trying to invoke the setLength() method.
[05:07] With that, the content of my StringBuilder object is going to be reduced to a maximum length of five.
[05:13] Now let's see what is going to happen when we run this reverse() method.
[05:17] As of now you can see the content inside my StringBuilder is hello.
[05:20] If I execute the reverse() method, you can see the output inside the StringBuilder right now is completely
[05:26] reversed like first o is there followed by l l e h.
[05:31] And at last we are trying to convert the StringBuilder object into an String object.
[05:36] So the String object is going to have the content, which is o l l e h.
[05:41] I hope you are clear.
[05:42] Now if you want to try the Approach 2 it is going to be super simple.
[05:47] You just have to copy these entire lines of code and paste it here and change this comment to Approach 2
[05:53] and post that I'm going to create a object of StringBuffer.
[05:57] So let me invoke the class which is StringBuffer.
[06:01] The same I'm going to mention on the right hand side and the object name I'm going to change it to StringBuffer
[06:06] .
[06:07] Now as a next step I need to change the StringBuilder object to the StringBuffer in all the remaining
[06:13] lines of code here
[06:14] with this, it should be pretty clear for you the way how StringBuilder and StringBuffer they work
[06:20] is very similar.
[06:22] They have very similar methods.
[06:23] They work very similar way.
[06:25] The only advantage with StringBuffer is it is thread safe, whereas StringBuilder is not thread safe.
[06:31] Since its StringBuilder is not a thread safe, it is going to work fastly compared to StringBuffer.
[06:36] Now let's go to the Approach 3.
[06:39] Inside the Approach 3 we need to create the object of CharArrayWriter.
[06:45] So the object name I'm going to keep it as cw with the help of new and CharArrayWriter constructor
[06:52] I'm trying to create an object here.
[06:54] Now using this object, I can try to invoke the method which is write, and to this write method I'm
[07:01] going to pass hello and post that
[07:03] I'm also going to invoke the same line of code, but this time I'm going to write the data, which is
[07:08] space world.
[07:09] Here you are getting an error.
[07:11] Let me show you what is the error.
[07:13] The error is unhandled exception of type java.io.IOException.
[07:18] So this is something related to exception handling inside Java.
[07:22] We are ready to discuss about exception handling in Java
[07:25] that's why I'm not able to explain why we are getting this error.
[07:28] I'm going to explain about this in the coming sections.
[07:31] For now, you can simply click on this hyperlink, which is add exception to the method signature.
[07:37] With that, there will be a throws method added to your main() method where it is going to throw an
[07:43] IOException.
[07:44] After that, your error will be resolved.
[07:47] Now as a next step, I will try to convert this CharArrayWriter object to the String with the help
[07:53] of toString() method that we can invoke using the cw object.
[07:58] So now if I try to execute this program by putting a breakpoint at the end, I should be able to see
[08:04] what is present inside this string3 object.
[08:06] Before that, let me remove the breakpoint that I have at the starting.
[08:09] So I'm trying to remove this and executing this program in a debug mode.
[08:14] You can see the debug point stopped at the last line.
[08:17] Here you can see both cw and string3
[08:19] they have the same content which is Hello World!
[08:22] This way we can always try to append or change the string data.
[08:28] I hope you are clear with all the three options that we have discussed.
[08:31] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
