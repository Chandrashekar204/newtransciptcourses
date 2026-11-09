# 6.15 — Searching for a value in String

> Section 6: Deep dive on String in Java

[00:00] Searching for a given value inside String is a most common scenario in real projects.
[00:07] For example, think like I have a sentence stored inside a String object.
[00:12] The sentence goes like this
[00:14] my name is Madan.
[00:16] If I want to search this String, if it contains my name which is Madan, I need to search for it.
[00:22] If the name Madan available inside the given String, then it is a match
[00:26] otherwise it is not a match.
[00:28] So how to perform this kind of searching in a given String data, there are multiple approaches to search
[00:35] a given String.
[00:37] The very first approach is with the help of indexOf() method.
[00:40] indexOf() is a instance method or a non-static method, which we can invoke with the help of
[00:46] String object.
[00:47] To this indexOf() method, you need to pass what you are trying to search and to whatever input data
[00:53] that you have provided to this indexOf() method is going to be searched inside the original String that
[01:00] you have provided, and if there is a match for your given input data, then this indexOf() method is
[01:07] going to return the index number at the position where the given word or given data is available inside
[01:16] the original String.
[01:17] Here you can see I have an example where inside the original String I stored that data, which is Hello,
[01:23] World!.
[01:26] If I want to understand if my original String as a word world or not, I can use this indexOf() method
[01:34] and to this indexOf() method I can pass the input which is world.
[01:38] Since this world word is available inside my String data, this indexOf() method is going to return
[01:44] the index value at the position where my world word is starting
[01:50] inside my String. We can see what is the index number that we are getting in this scenario as part
[01:56] of the demo.
[01:57] But how about the negative scenario?
[01:59] Think like whatever input data that you have provided to these indexOf() method is not available inside
[02:06] your original String.
[02:07] In such negative scenarios, the output from the indexOf() method is going to be -1.
[02:13] So whenever you are getting index value as -1, that is an indication to you that given String
[02:20] data is not available inside the original String.
[02:24] So these are very first method which will help you to identify whether the given data is available inside
[02:30] the original String.
[02:32] The next approach is with the help of contains() method.
[02:35] This contains() method is going to give you an boolean value as an output, just like indexOf() method.
[02:42] This method also is going to accept input data, and if the input data is available inside the original
[02:48] String, you're going to get true.
[02:50] Otherwise you're going to get false.
[02:52] Here inside the example you can see under the third Java statement for the contains() method, I have
[02:58] passed the @ symbol to search if it is available inside the original String.
[03:03] So inside the original String.
[03:04] Since I don't have the special character, I'm going to get the output as false.
[03:09] So these two methods, they are going to give you an indication whether the given input data is available
[03:15] or not.
[03:16] But there is other flavors of searching a value as well.
[03:20] The other flavor that we have is startsWith() and endsWith().
[03:24] Sometimes you may want to understand whether your String is starting with a specific word or ending
[03:30] with a specific word or a specific letter.
[03:33] The requirement can be anything you are more concerned about the starting value or ending value.
[03:39] In such scenarios, you can use these instance methods that are available inside String class, which
[03:45] are starts with and ends with to the startsWith() method
[03:49] If you provide an input, it is going to check whether the original String is going to start with your
[03:54] input data.
[03:55] If yes, it is going to give a boolean value.
[03:58] Very similarly, endsWith() method is going to look at the end of the string if it is ending with the
[04:04] given input data.
[04:06] Apart from these three approaches, we also have fourth approach which is matches() method.
[04:12] This matches() method can be used for more complex search operations.
[04:17] So how to achieve those complex operations with the help of regular expression regular expressions in
[04:24] short form, we can call them as rejects expressions or rejects patterns.
[04:29] With the help of this rejects expression, we can give an expression based upon your requirement.
[04:35] Here
[04:35] inside the example you can see I have given an expression.
[04:38] The purpose of this expression is,
[04:40] my sentence can have any kind of data just before the world, and similarly it can have any kind of
[04:46] data just after the word world.
[04:48] That's why I have given these dot asterisk.
[04:51] Dot asterisk means it can contain any kind of data just before world.
[04:55] If I mention the same dot asterisk just after the world word that
[05:00] means my original String can contain any kind of data just after the world word.
[05:05] So these kind of complex patterns are complex search operations we can achieve with the help of matches()
[05:13] method to use this matches() method, definitely you should be aware about how to build these regular
[05:19] expressions.
[05:19] Don't worry for now about them because this is an advanced topic.
[05:23] In the coming sections we are going to talk about what are regular expressions.
[05:28] But now let's focus on String alone.
[05:30] So based upon your regular expression that you have provided to this matches() method, it is going to
[05:35] search the original string and it is going to give the output in an boolean format.
[05:40] And at last I want to highlight all the four approaches that we have discussed.
[05:44] They all are case sensitive.
[05:46] If you are looking for a case insensitive search operation, there is a technique that you can follow.
[05:52] First, you can convert your original String entirely into the uppercase or lowercase and post that
[05:59] you can also provide your search input data as well, either completely in lowercase or uppercase.
[06:06] So using this technique you can make your search operation in case sensitive.
[06:12] Here we have seen four different flavors of search operations that we can perform with the help of String
[06:18] class.
[06:18] So these are the most commonly used.
[06:20] Please use them based upon your own business requirements and the situation you are trying to handle.
[06:26] There are no good or bad approaches, so they all serve different different scenarios.
[06:31] I hope you are clear with these theory discussion.
[06:33] Let's quickly try to see the demo of this searching operation inside IntelliJ by creating a Java class.
[06:40] To see the demo of String search operation, I have created a class with the name StringSearchDemo.
[06:46] Inside this class I also created a main() method and I created a String object with the name original
[06:52] string.
[06:53] And inside this original String object I'm trying to store this data, which is hello comma, space
[06:59] world exclamatory Mark.
[07:01] Now let's try to write the Java statement by using all the four options that we have discussed.
[07:07] First I'm going to create a variable of type int with the name as index.
[07:12] Post that by using the String object, I'm going to invoke indexOf() method.
[07:18] When I type indexOf(), you can see I have so many overloaded methods which I can use based upon my
[07:25] search criteria.
[07:26] If I'm trying to understand the index value of a single character value, I can use the first index
[07:33] off method that is going to accept the char value.
[07:36] So here this method is showing the int as the input parameter type.
[07:41] I can still provide the char value with a single quote, because why it is allowed is every char value
[07:48] has an int value inside Unicode.
[07:50] So you can pass a car value or you can pass into value as well.
[07:55] When you pass into value behind the scenes, the Java is going to look for the character based upon
[08:01] your into value position.
[08:03] Very similarly, we have another method which is going to accept the String data as an input.
[08:09] And we also have other type of overloaded methods where they can accept a char and String, and at the
[08:14] same time they can also accept from which index you want to search.
[08:19] Maybe first five indexes you don't want to consider.
[08:22] You are looking after five indexes.
[08:24] In such scenario you can pass this from index value very similarly.
[08:29] You also have indexOf() method that is going to accept a char, String,
[08:33] beginIndex and endIndex.
[08:36] If you have a scenario where you want to search a given data between two indexes, then you can use
[08:43] these methods that are going to accept beginIndex and endIndex.
[08:47] And very similarly we also have last indexOf() method.
[08:51] The difference between indexOf() and last indexOf() methods is your indexOf() method is always going
[08:57] to give the position number or index number when it finds the given input data very first time, it
[09:03] is not going to perform the search operation and look for all the indexes.
[09:08] As soon as it identifies a given input data, it is going to simply give the first index value and it
[09:14] is going to terminate the search operation.
[09:16] But if you are looking for last index value, maybe your original String has the given input data at
[09:22] multiple places.
[09:23] If you are not interested about the first index occurrence, then you can always use the last indexOf()
[09:28] method, which is going to give the index number or position number based upon the last match happened
[09:35] inside the search criteria.
[09:37] I hope you are clear.
[09:38] For now, let me invoke this indexOf()method that is going to accept a single char.
[09:43] So to this single char I'm going to pass the char, which is !.
[09:48] Very similarly, I can also invoke the same indexOf() method, but this time I'm going to mention the
[09:55] String data as an input and the data that I want to pass here
[09:59] is world.
[10:00] Let me change this variable name as index1.
[10:03] Now if I try to execute this program, we can see that we are going to get some index values.
[10:10] Let's see what kind of index values we are going to get.
[10:12] So here the exclamatory mark is found at an index our position 12.
[10:18] Let's validate if the position is correct like the position are
[10:21] the index is always going to start at zero.
[10:24] So this is 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
[10:30] 10, 11, 12
[10:32] it is correct.
[10:32] Now very similarly you can see the next index is showing as seven.
[10:37] Let's see whether the world word is starting at the index 7.
[10:41] So 0 1 2 3 4 5 6 7.
[10:46] So this is also correct.
[10:47] If the same world is present one more time inside the original String, then my indexOf() method still
[10:54] is going to give the index value as seven, because indexOf() method is always going to check for the
[11:00] first match itself, it is not going to do the search operations till end of the original String.
[11:06] If you are looking for the last index, then you need to use another method that we have discussed which
[11:11] is last indexOf() method.
[11:13] So let me release this breakpoint.
[11:15] This time I'm going to provide an input data which is not available inside my String.
[11:21] And let's see what is going to happen.
[11:23] I'll try to give @ symbol.
[11:25] This symbol is not present inside my original String.
[11:29] If I run this program under index 2, you will be able to see a negative value which is -1.
[11:35] So whenever we are receiving -1 from the indexOf() method, or lastIndexOf() method, then
[11:40] that indicates there is no match found in the original String for the given input data.
[11:46] I hope you are clear with these
[11:47] first approach, let me release this breakpoint and show you the demo of second approach.
[11:53] For the second approach I'm going to create boolean values with
[11:57] the name isContains and after that I'm going to use the original String object.
[12:03] And using this object I'm going to invoke the contains() method to.
[12:07] This contains() method I'm going to pass the substring I want to search
[12:11] here is world.
[12:13] Very similarly, let me copy this line of code, and this time let me search for a content which is
[12:18] not available inside my String.
[12:21] And I'm going to change this boolean variable value as isPresent().
[12:25] Now if I try to execute this program like you can expect, these contents is going to have the value
[12:31] true, whereas is present is going to have the value as false.
[12:34] I hope you are also clear with the second approach.
[12:37] Let me release this breakpoint.
[12:38] Now let me show you the third approach.
[12:41] For the third approach, I'm going to first copy these two lines of code and change this boolean variable
[12:46] names to startsWith and the second one I'll change to endsWith.
[12:53] First
[12:53] here I want to check whether my original String is starting with a String, which is hello instead of
[13:00] hello
[13:00] we can also mention simply H whatever input data you are providing to
[13:05] this startsWith() method using the same
[13:07] It is going to search.
[13:08] The original String is starting with the given input data.
[13:12] Very similarly, we can also invoke endsWith() method and for these endsWith() method
[13:17] if I pass this at the @ symbol, I'm going to get the false value because my original String is ending
[13:24] with the semicolon.
[13:26] First, let me show you by giving these @ symbol, we are going to get the output as false.
[13:31] You can see startsWith is working fine because our original String is starting with hello.
[13:36] So that's why it is true, whereas ends with is false.
[13:40] If I try to change these ends with two !, I'm going to get the output as true.
[13:46] And here I want to highlight you that it is not mandatory to give only a single character for the
[13:53] endsWith we can give a partial data or an word
[13:56] It's up to us
[13:57] what we want to give for, startsWith and endsWith. To provide more clarity, I can change
[14:03] this endsWith input data to ld! exclamatory.
[14:07] You can see with these input data
[14:08] also, we are going to get the output as true because our String anyway is ending with ld! exclamatory
[14:15] mark.
[14:15] So let me run this program and show you so you can see endsWith
[14:19] right now it is showing the value true.
[14:21] Now, as a next step, let me show you the last approach that we have discussed, which is with the
[14:26] help of matches() method.
[14:28] For the same I'm going to create a boolean which is isMatched(), and to this variable I'm going to
[14:35] assign the output that I am going to get from the matches() method.
[14:38] So how to invoke the matches() method with the help of String object and post that I need to type matches
[14:44] and to this matches() method, I need to give my regular expression in a String format.
[14:50] So how to do that?
[14:51] First I need to mention double quotes, and inside that the regular expression that I want to give is
[14:57] dot asterisk and post that
[14:59] I'm going to type a word followed by dot asterisk with this
[15:03] my Java is going to search for my String for a word called world, and it is not going to worry about
[15:11] what is before world word and what is after world Word.
[15:15] We can expect a true value as an output.
[15:18] Let me execute
[15:19] this program you can see isMatched right now it is showing as true.
[15:23] With this
[15:23] we saw the demo of all the four common approaches that we have discussed.
[15:28] I hope you are clear.
[15:29] My humble request is to do more practice, try with various combinations and see how the output is changing.
[15:36] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
