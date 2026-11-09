# 6.20 — [JAVA 8] Joining Strings

> Section 6: Deep dive on String in Java

[00:00] In the previous lecture, we saw the demo of how to split a single string into multiple arrays of string.
[00:07] Now inside this lecture, let's see the opposite operation of split, which is joining strings.
[00:13] We want to join multiple string objects into a single string object.
[00:19] This can be achieved with the help of join() method available inside String.
[00:23] So the join() method is a static method that is introduced inside Java eight.
[00:29] So what is the syntax of this join() method?
[00:31] So when you want to club multiple strings into a single string, first you need to provide what is the
[00:37] delimiter?
[00:38] What is the special character that you want to consider to separate all the strings that you have provided.
[00:44] And after the delimiter, you can provide any number of string objects and all the string objects that
[00:50] you have provided as an input will be joined together, but all the string objects, they are going
[00:57] to be separated by a delimiter that you have provided.
[01:00] Let's see an example.
[01:01] Here
[01:02] you can see I'm trying to invoke the join method to this join() method.
[01:05] I'm trying to provide the very first parameter, which is a space.
[01:09] So I want to join all the words that I'm giving to this join() method.
[01:14] But all the words should be separated by a space character.
[01:18] After the join(), you can see I'm trying to provide three different string objects like Hello World and
[01:24] Java.
[01:24] Here I'm just providing three String objects, but if needed, you can provide any number of String
[01:30] objects to the join() method.
[01:32] But here you may have a question which is how join() method is going to accept any number of input parameters.
[01:39] Because like I said before, the methods inside Java they're going to accept a static number of input
[01:46] parameter based upon the method declaration or the method definition.
[01:51] But here I'm saying the join is capable of accepting any number of String objects and going to clarify
[01:57] your doubt when you are seeing the demo of join() method.
[02:00] So there is a beautiful concept inside Java, which can make our Java methods to accept any number of
[02:06] input parameters.
[02:07] So please hold your thought for few minutes.
[02:10] I'm going to discuss about it here
[02:12] here inside this example, I'm trying to pass multiple string objects to the join() method.
[02:17] Let's see few more examples as well, so that we can try to understand what are the various ways we
[02:22] can provide input to that join() method.
[02:25] Here I have an example where the delimiter is an empty string.
[02:29] That means I don't want my multiple strings to be separated with a delimiter.
[02:34] With this delimiter, my output is going to look like this.
[02:38] The very first word is Java space is, and the second word is fun space
[02:43] and between the first string and the second string, there is no delimiter,
[02:47] there is no space because we intentionally provided the delimiter as an empty string.
[02:52] So this confirms join() method allow you to provide an empty delimiter as well.
[02:57] And one more beauty of this join() method is instead of providing string objects separately, you can
[03:03] also provide a collection of strings or a List of string objects.
[03:08] So list and collections are advanced concepts that we are going to discuss in the coming sections.
[03:13] When we try to provide a list of strings to this join() method, the List can be empty.
[03:18] Even if the List is empty, your join() method is not going to throw an any error.
[03:23] It is going to handle the null behavior behind the scenes gracefully without throwing any exception.
[03:29] So when you pass an empty List to this method, you're going to simply get an empty string as an output
[03:34] instead of getting RuntimeException.
[03:37] Whenever we are using these join() static method inside our Java programs behind the scenes, it is going
[03:43] to leverage the Stringbuilder class, which is present inside the string ecosystem, to concatenate
[03:50] various multiple strings into a single string.
[03:52] So with the help of StringBuilder, only the join() is going to perform this joining operation very efficiently.
[04:00] StringBuilder is a class inside the string ecosystem, which we are going to discuss in the coming
[04:05] lectures.
[04:06] With the help of this class, we can overcome the challenges of String immutability.
[04:11] We know strings are immutable in nature for some reason
[04:15] if you want to make them mutable, then instead of String, we can use the classes like StringBuffer
[04:21] and StringBuilder.
[04:22] Hold your thoughts around this.
[04:23] In the coming lectures, I'm going to discuss about this StringBuilder class.
[04:28] But here the point that I want to highlight is the join() method.
[04:31] Internally, it is going to use the StringBuilder class to join() multiple strings into a single string
[04:37] very quickly.
[04:38] I hope you are clear with the purpose of the join() method.
[04:40] Let me show you the demo very quickly inside the intelliJ.
[04:43] To see the demo of join() method, I have created a class with the name StringJoinDemo and inside this
[04:49] class we have a main() method here
[04:51] first let me create a variable of string with the name result.
[04:56] After creating this variable, I'm going to mention the String class.
[04:59] Post that I want to invoke the join() method, because join is a static method, and we can invoke
[05:06] this directly with the help of class name.
[05:08] Here you can see there are two overloaded methods of join. In both of these methods
[05:13] first we need to pass what is the delimiter value that we want to pass after the delimiter.
[05:19] For the very first method, we can pass any number of char sequence elements.
[05:24] That means we can pass any number of String objects, whereas the second method is going to accept a
[05:30] collection of elements.
[05:32] So how I'm telling a collection of elements, you can see there is a Interface with the name iterable.
[05:37] So this indicates a collection of elements or a List of elements.
[05:43] As of now, we don't have to worry about these second overloaded method because we are ready to discuss
[05:47] about what are collections, what are Lists inside the Java.
[05:51] So we're going to discuss all these advanced concepts in the coming sections.
[05:55] That's why let's invoke the very first method to this very first method
[05:59] first I want to mention the delimiter value as comma post that I'm going to provide multiple string
[06:06] objects,
[06:07] very first one is Hello and followed by the second string is going to be World, followed by the last
[06:14] string
[06:14] object I want to pass is Java.
[06:16] Here I'm trying to pass three different String objects, but if needed you can pass even 100 different
[06:23] String objects as well.
[06:24] There is no limit on how many String objects that you can pass to this join() method.
[06:29] So how
[06:30] my join() method is accepting any number of input parameters that I'm trying to send.
[06:36] To understand the same, let me open this join() method.
[06:38] You can see there are three dots here just after the char sequence.
[06:43] So what is a char sequence?
[06:44] It is one form of representing our String data.
[06:47] So after this char sequence we have these three dots inside Java input method parameters.
[06:54] Whenever you are seeing these three dots, that indicates that this method can accept any number of
[07:01] input parameters of the data type that you have mentioned here.
[07:04] So this concept in Java is called as variable arguments because with the help of these three dots,
[07:11] the number of arguments that we can pass to the method can vary based upon how many arguments I'm going
[07:17] to send
[07:18] the method definition is going to be changed at runtime by the JVM.
[07:23] So this is one of the beautiful concept inside Java.
[07:26] We're going to talk in detail about this in the coming sections.
[07:29] But for now I just wanted to give you a quick hint around this.
[07:32] So let me close this String class.
[07:33] Now if I try to run this class, the result is going to have a single string with all these words that
[07:39] are separated by comma.
[07:41] Let me show you one more example of join() method.
[07:43] For the same
[07:44] I'm going to copy this line and change this variable name to result1.
[07:48] And this time I'm going to keep the delimiter as empty and post that
[07:53] the first String I want to mention as Java space is followed by the second String, I'll mention it
[07:59] as fun space, and at the end I want to mention the String as powerful.
[08:05] So from this last line of statements, you can expect the output all the words that we have provided.
[08:11] They are going to be joined without any delimiter because the delimiter we have given empty string.
[08:17] Let me show you the output at runtime.
[08:19] I'm going to run this program in a debug mode and you can see the result
[08:23] here is hello comma world comma Java.
[08:26] Because the delimiter that we have given is comma, whereas under the result one, each word is simply
[08:33] joined without any delimiter
[08:34] that's why there is no space after ease and even after the end
[08:38] also there is no space here.
[08:40] You can see the join() method is providing the exact opposite functionality of split() method.
[08:46] I hope you are clear with this demo.
[08:48] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
