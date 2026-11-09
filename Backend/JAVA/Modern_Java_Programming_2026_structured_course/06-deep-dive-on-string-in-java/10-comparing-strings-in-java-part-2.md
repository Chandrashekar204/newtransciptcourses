# 6.10 — Comparing Strings in Java - Part 2

> Section 6: Deep dive on String in Java

[00:00] As of now, we are able to compare the content of two Strings with the help of equals() and equalsIgnoreCase()
[00:07] methods.
[00:08] But sometimes we may want to sort the String objects or String data and display the same to the end
[00:15] user after performing the sorting.
[00:17] So we have two types of sorting ascending order and descending order.
[00:21] So ascending order means small to big and very similarly, descending order means big to small.
[00:27] Whenever we are dealing with the alpha numeric values like String data, if you want to identify which
[00:32] object or which String data has to come before as part of the sorting process, we have a method to
[00:38] handle these kind of scenarios.
[00:40] The method name is compareTo().
[00:42] Let me show you a demo here.
[00:44] First I'll try to create a String data, which is Java after the String data.
[00:49] Since this is going to act as a String object, I can invoke the method which is compareTo().
[00:55] So we also have compare to ignore case as well.
[00:58] Just like how we have equals() and equalsIgnoreCase() in the compareTo().
[01:03] Also, if you want to ignore the case sensitivity, you can invoke compareToIgnoreCase().
[01:08] Or if you want to consider the case sensitivity, you can simply invoke the compareTo(). To this compare
[01:14] two method
[01:15] I can pass one more String object or String data.
[01:18] So here first I'll try to pass same data, which is Java.
[01:22] Let's see what we are going to get whenever we are using comparedTo() method.
[01:26] This comparedTo() method is going to return a value of type int.
[01:31] You can read the documentation about this method also compare to strings Lexicographically.
[01:37] Here they also mention if the result is zero.
[01:40] That means both strings are equal.
[01:43] In this scenario, we are going to get the output as zero because we are trying to compare two different
[01:48] object with the same content.
[01:50] So let me try to catch the output on the left hand side with the variable comparison one.
[01:57] If I try to execute this program, I'm going to get an value inside comparison zero.
[02:03] So zero inside comparedTo() method indicates both of your Strings are same.
[02:08] It doesn't matter which one you are going to display first inside your sorting.
[02:13] Now let's try to compare two different objects with the two different content for the same
[02:18] I'm going to copy the same line of code and rename this variable to comparison2.
[02:24] This time I want to compare Java with the value Python.
[02:28] Let's see what output we are going to get when we run this program.
[02:32] The output that we can see inside comparison2 is a negative number which is -6.
[02:39] How we are getting this -6
[02:41] Let me try to explain you the same whenever we are trying to compare two different strings.
[02:46] First, my compareTo() method is going to compare the first character since the first character.
[02:51] Here we have j and p , so it is going to compare these two characters, since inside the Unicode, the
[02:58] p is going to come after six characters of J, we are getting the -6.
[03:05] That means my JVM is going to take the Unicode character position of J, and from this position it is
[03:12] going to subtract the position value of the p Unicode value.
[03:17] Since always p is going to come after j, we are trying to subtract a lower number from a bigger number.
[03:24] That's why we are getting a -6 value.
[03:27] And since these two characters are separated by six positions, we are getting the output as -6.
[03:33] That's what we are able to see here.
[03:35] Inside that debug window, you don't have to come to the debug window every time to check a variable
[03:40] you can directly see inside your IntelliJ.
[03:43] As of now, the breakpoint stopped.
[03:44] At this point of time, you should be able to see what is the value against your each variable here
[03:50] inside your Intellij IDE as well.
[03:52] So here comparison2 is going to hold -6.
[03:56] comparison1 is going to hold zero.
[03:58] So this is the beauty of IntelliJ.
[04:00] It is going to show you the inline data for your quick reference.
[04:04] Now as a next step I want to compare Python with Java.
[04:08] Before I try to do that, let me release my breakpoint.
[04:11] As a next step
[04:12] I can copy this line of code and rename the variable to comparison3 and the content
[04:19] also, I'm going to reverse it.
[04:20] Like first I'm going to mention Python and post it.
[04:23] I'm going to mention Java this time for comparison3
[04:27] you should get the A positive value, which is six because we are trying to compare in a vice versa
[04:33] manner.
[04:33] So let me try to execute this program and you can see here for the comparison three we are storing a
[04:40] value which is six.
[04:41] So based upon this comparison output you can decide how you want to display your objects content or
[04:48] your objects inside your sorting order.
[04:51] So with this the python is bigger compared to Java.
[04:55] So if you want to display this data in an descending order, the first element is.
[04:59] Is going to be Python.
[05:01] Whereas if you want to display your data using ascending order, then Java is going to be the first
[05:08] element, because the position of j comes before p position.
[05:12] And here you may have question which is what if the first character of two strings is same?
[05:18] Maybe I have p here and even in the second string object.
[05:21] Also I have a p.
[05:22] In such scenarios, JVM is going to move to the next character.
[05:27] Even if the second character is same, it is going to move to the third character.
[05:31] This way it is going to give an integer value representing which word is bigger and which word is smaller.
[05:38] Accordingly, you can sort your words.
[05:40] So as of now, I'm trying to teach only the purpose of the important methods inside string.
[05:46] I'm not trying to build any business logic using all these methods.
[05:50] In order to build the business logic, you need to understand lot many concepts inside Java.
[05:55] Like you need to understand how to write conditional logic, how to write looping logic.
[05:59] So once we discussed all these concepts inside the coming sections, post that we are going to write
[06:05] good amount of programs by taking lot many business scenarios and business problems at that time, you're
[06:12] going to understand how important these methods that we have discussed as part of these string related
[06:18] section.
[06:18] So don't get demotivated with all these discussion why you are trying to learn each method.
[06:23] So there is a good amount of concept inside each method of the string.
[06:27] That's why I'm trying to explain in the same process, I'm also trying to show you how to invoke the
[06:33] methods, how to create the objects, how to debug the code.
[06:37] I'm assuming you are also learning a lot and maturing a lot inside the Java programming.
[06:42] If you have any questions or if you stuck any place, please post your question inside the Q&amp;A section.
[06:48] I should be able to help you to clear your issue or to clear your roadblock.
[06:52] Let me release this breakpoint.
[06:54] Whatever concepts that we have discussed around the comparing strings, I have mentioned all of them
[06:59] inside these two slides, I have mentioned all details about equals equals ignore case and compare two
[07:06] methods.
[07:06] So please refer them whenever you want to quickly brush up string related concepts.
[07:11] Thank you and I'll catch you in the next lecture by.

----------------------------------------
