# 6.23 — Understanding how String objects are immutable

> Section 6: Deep dive on String in Java

[00:00] For the next few lectures, we are going to talk about the string immutability concept.
[00:05] I already gave a quick introduction in the previous lectures.
[00:08] That string is an immutable object.
[00:11] What is the meaning of immutable?
[00:13] Something cannot be changed once it is created.
[00:16] Whatever objects that we are going to create with the help of String class, they are always going to
[00:22] be immutable.
[00:23] Just like how we can't change the tattoos once created.
[00:27] Similarly, once a string object is created in Java, we cannot change the content of that String object.
[00:34] If needed, we can forcefully remove the tattoos with the help of some laser.
[00:39] But altering the String object is impossible in Java.
[00:44] Does that mean we don't have any option inside Java to create mutable string content?
[00:49] No.
[00:49] We have certain companion classes for the String class.
[00:53] The classes like StringBuilder and StringBuffer.
[00:56] Using these classes, we can modify the content of the string data, and we can make the string data
[01:02] mutable.
[01:03] Before we try to discuss about how to create a mutable string data with the help of StringBuilder and
[01:08] StringBuffer.
[01:09] First let me share you more details about the immutability concept of string.
[01:14] Here I have an example like you can see
[01:16] first, I'm trying to create a s1 string object, and inside this string object I'm trying to store
[01:22] the string data, which is hello. In the very next line
[01:26] by using the same String object, I'm trying to assign a new data, which is Hello World!
[01:32] This may give an illusion to you that we are able to change the content of the String object data,
[01:38] but that is not going to happen.
[01:40] Let's try to understand what is going to happen behind the scenes.
[01:43] Then you're going to agree with me that String objects are always immutable like you can see here.
[01:49] First we are going to have a heap memory.
[01:51] The heap memory is going to be empty before you try to start your program.
[01:56] Now think like I'm trying to execute a Java statement which is String s1 = Hello.
[02:01] As soon as we try to execute this Java statement, a String object will be created inside the Heap memory
[02:08] and the same will be stored in a memory location.
[02:11] How we can access that memory location with the help of s1, which is the object reference name or the
[02:18] variable name.
[02:19] Now think like I'm trying to execute the next Java statement, which is s1 = Hello World.
[02:25] So to the same object reference, I'm trying to assign the new String content.
[02:30] If we try to execute this second statement, let's see how the Heap memory is going to look like.
[02:36] Like you can see here a new String object behind the scenes is going to be created inside your heap
[02:42] memory at a different location.
[02:44] And this new object is going to hold the new content, which is Hello World to this new object or to
[02:51] this new memory location.
[02:52] Your object reference are your String variable is going to refer.
[02:57] So whatever object which was previously created, it is going to become an orphan object.
[03:02] At some point of time, my Garbage collector is going to collect it and destroy it.
[03:07] With this, it should be pretty clear for you when we say string immutability, the immutability applies
[03:13] to the String objects that are stored in a memory, not the reference variable, which means we can
[03:20] use the same reference variable for the new string content as well.
[03:24] But behind the scenes, the same reference variable is going to be pointed to a new object which is
[03:30] stored in a new memory location.
[03:32] If you are looking for an option where you don't want to give any flexibility to other programs to change
[03:39] the content of your String object, then you can use the final keyword whenever you are trying to create
[03:45] your String object.
[03:46] Here I have an example where when I'm trying to declare and initialize my String object, which is s1,
[03:53] I have mentioned final keyword with that in future if someone is coming, if they're trying to change
[03:59] my Java program by trying to assign new content to the s1 object, then they are going to get a compilation
[04:07] error.
[04:07] I can quickly show you this in the demo as well.
[04:10] For the demo I have created a Java class which is StringImmutableDemo.
[04:14] Inside the class we have a main() method and inside the main() method you can see
[04:18] first I have created a String object which is s1 and to this I'm trying to assign a hello and post that
[04:24] I'm trying to assign Hello World.
[04:26] With this, I'm getting an illusion that I'm able to change the String data, but like we discussed,
[04:32] we cannot change the String object behind the scenes
[04:35] a new String object is going to be created with the new content, and the previous old object will be
[04:42] deleted or destroyed by the Garbage collector.
[04:45] So if I try to run this program, you can see I'm getting an Hello World as an output.
[04:50] Now let me show you how to use a final keyword and how to avoid changing the string content inside our
[04:56] Java programs.
[04:58] For the same, I'm going to create
[05:00] a new string object with the name s2 for the same s2
[05:04] I'm going to assign the content which is high.
[05:07] So this is the normal syntax that we usually follow.
[05:11] If I keep a final keyword just before the string, then this object, whatever we have created is going
[05:17] to become final and no one can alter the content, and at the same time they cannot reuse the s2 object
[05:25] reference name to create another String object.
[05:28] For example, for the same s2 object reference
[05:32] if I'm trying to assign a new content, which is Hi World, I'm going to get a compilation error if
[05:38] let me show you the error details
[05:40] by hovering on to this, you can see I'm getting an error message saying that cannot assign a value to
[05:46] final variable s2.
[05:48] So this is one of the smartest way to avoid reusing the same object reference of string for the new
[05:55] data.
[05:56] So let me remove this compilation error and I'm going to check in this file for your reference into
[06:01] the GitHub repo.
[06:02] With this, I'm assuming you are clear about the immutability concept of String.
[06:07] So now you should be able to answer any questions around the String immutability concept.
[06:12] As a next step, let me show you how to create the mutable string data with the help of StringBuilder
[06:19] and the StringBuffer.
[06:20] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
