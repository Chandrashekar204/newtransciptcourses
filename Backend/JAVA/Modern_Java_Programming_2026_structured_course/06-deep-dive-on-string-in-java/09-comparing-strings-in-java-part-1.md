# 6.9 — Comparing Strings in Java - Part 1

> Section 6: Deep dive on String in Java

[00:00] Sometimes we want to compare the content of two string objects if they are holding the same content
[00:06] or different content.
[00:08] But these kind of scenarios, we have a method which is going to help us to compare two different string
[00:14] objects.
[00:14] So let's try to understand what is that method here
[00:17] to save some time, I have created a new class with the name StringComparisonDemo, and inside this
[00:23] class I have created a main() method.
[00:26] Inside the main() method I have created three different String objects with the new operator and the String
[00:32] constructor.
[00:33] The reason why I have followed this approach is so that you will get familiar with this approach as
[00:38] well.
[00:38] Otherwise, you are going to forget about this approach to create the String objects.
[00:43] Here inside these String objects, I'm trying to store various kinds of data like hey, hello and hey, since
[00:49] we are using new operator, all these objects are going to be created separately and the data inside
[00:55] them is going to be stored inside different memory locations.
[00:59] Now let's assume I want to compare the content of two different String objects.
[01:05] Maybe I want to check whether the content of string one and string two objects is same or not.
[01:11] For the same
[01:11] first I am going to mention str1, which is the object variable name of very first object that we
[01:17] have created.
[01:18] Post this object name I'm going to invoke the equals() method to this equals() method.
[01:24] We can pass what is the second object of the String?
[01:28] What is the second object of String?
[01:29] It is str2.
[01:32] So let me pass the same and mention the semicolon.
[01:34] And this equals() method is going to give an output which is of type boolean.
[01:40] So you will be able to see the method details.
[01:43] If you try to hover on this method you can see my intellIj is trying to show me the method details
[01:49] that this is the method definition where it is going to return the boolean data type.
[01:53] If you want to read the Java documentation, you can also read them here.
[01:57] So this is one of the easy way to understand more details about a method.
[02:01] You can always hover on it, and your intellij is going to show you all the details inside the same
[02:07] class.
[02:08] Since my equals() method is going to return a boolean value, I want to catch that with the help of boolean
[02:14] data type.
[02:15] The variable name I'm going to mention as b1.
[02:17] Very similarly, I also want to compare str1 with str3 object, so I can copy the same line
[02:24] of code and rename the variable name to b2, and this time instead of str2, I'm going to mention
[02:32] str 3.
[02:33] So what is the output you're expecting for b1 we can expect the output as false, whereas for b2
[02:39] we can expect the output as true.
[02:41] So let me keep a breakpoint here and try to execute this program.
[02:44] Inside b1 we have a value called false.
[02:47] And inside b2 we have a value called true.
[02:50] This should be pretty clear for you because the content that we are storing inside str1 and str3
[02:56] is same.
[02:57] That's why we are getting the output as true.
[02:59] Here with this code, we are trying to compare two string objects.
[03:03] Instead of this approach.
[03:04] We can also follow other approach where we can try to compare a given string object with the hard coded
[03:11] String data, or hard coded String literal value.
[03:14] I can show you how to do that.
[03:16] So let me copy these two lines into the next lines.
[03:19] And here I'm going to change the variable names to b3 and b4.
[03:24] This str1 I want to compare with the string Hey,
[03:28] for the same I can directly mention the String value, which is Hey.
[03:32] So since my str1 and this String literal, they both are representing the same content.
[03:38] This b3 is going to hold the value, which is true if needed
[03:43] we can also invoke this equals() method from the String literal itself.
[03:47] For example, here instead of str1, I can mention the Hey String literal value.
[03:53] Since this is also a String object, I'm able to invoke the equals() method, and after that I can mention
[03:59] whatever object that I want.
[04:01] So here I'm mentioning str1
[04:03] again.
[04:04] That means even before also is going to be true.
[04:07] We can also try to compare two String literal values as well.
[04:12] I can show you an example here like boolean b5 is equal to,
[04:17] I'm going to mention a String literal which is "Hey".equals("Hello").
[04:23] And to this equals() method I'm going to pass another String literal value, which is
[04:27] hello.
[04:28] Since the content of these two string literals is not same, I'm going to get the b5 value as false.
[04:35] We can see by running the program in a debug mode.
[04:37] Here it is very clear b3 is true, b4 is true, and b5 is holding a value false.
[04:43] So this is working like we expect.
[04:45] Please note that previously when we are trying to compare two object to memory locations, we have used
[04:52] the double equal to operator.
[04:55] With the help of double equal operator, we can compare the memory locations of the
[05:00] the two objects, whether the two objects are same or not.
[05:03] Whereas with the help of equals() method, we can compare the content of the String object.
[05:09] Whenever we are using equals() method, we are not going to worry about the memory location.
[05:13] We are only worrying about the content of the String data.
[05:17] There is also a another flavor of equals() method, which is going to help you to compare the content
[05:24] of two Strings by ignoring the case sensitivity.
[05:27] Let me show you a demo here.
[05:29] For the same, I'm going to create a String object with the name str4, and to this I'm going to
[05:34] assign a String data, which is Java in all small case letters.
[05:39] Very similarly, I want to create one more String object with the name str5.
[05:44] And the content of this object is going to be Java only.
[05:48] But this time I want to use all capital letters.
[05:51] If you try to compare these two Strings with the help of equals() method, you're always going to get
[05:57] the value as false because equals() method is going to consider the case sensitivity very seriously.
[06:04] So here I'm trying to compare two String objects.
[06:08] One is str4 and str5.
[06:11] So the content of these two methods is going to be compared
[06:15] and we are going to get an boolean value as an output.
[06:18] We can expect that b6 is going to hold the value which is false.
[06:22] I can also confirm you that here the b6 variable is holding the value false.
[06:27] So how to ignore the case sensitivity?
[06:29] Whenever we are trying to compare two Strings for these kind of scenarios, instead of equals(), we can
[06:35] invoke the method which is equalsIgnoreCase().
[06:39] If you try to hold on this method, you can see the Java documentation clearly saying compares the String
[06:45] to another String
[06:46] ignoring case considerations.
[06:48] So this should be pretty clear for you.
[06:50] Now if I try to run this program, the b6 is going to hold the value, which is true.
[06:55] You can see here right now we are holding the value which is true.
[06:59] So this confirms that equals() ignore case is ignoring the case sensitivity while comparing two Strings.
[07:06] I hope you are clear with the two methods that we have discussed which are equals() and equalsIgnoreCase().
[07:11] .
[07:12] In the next lecture, I want to discuss about one more method that we can use whenever we want to compare
[07:18] two strings.
[07:19] Let's continue this discussion in the next lecture as well.
[07:22] Thank you
[07:23] bye.

----------------------------------------
