# 6.19 — Splitting Strings

> Section 6: Deep dive on String in Java

[00:00] Inside this lecture, let's try to talk about the splitting concept inside strings.
[00:05] With the help of a split() method available inside string class, we can split a original string into
[00:13] an array of substrings based upon a specified delimiter.
[00:17] I know the definition is not clear, but when I show the example, it is going to make more sense to
[00:23] you.
[00:23] Before I try to show you the example, let me show you the syntax that we need to follow whenever we
[00:29] want to invoke the split() method.
[00:31] Since a split() method is a instance method available inside String class, we can invoke this method
[00:37] only with the help of String object, and whenever we are invoking the split() method, we need to pass
[00:43] delimiter value as an input to this method.
[00:46] So here you may have multiple questions like what is a delimiter?
[00:50] How this split() method is going to work?
[00:52] To answer all your question, I want to show you a simple example.
[00:56] Think like I have a oirginal string with the name fruits and inside these fruits string I stored a lot
[01:03] of fruit names like apple, orange, banana, grape and each fruit name is separated with the help of
[01:11] a special character which which is comma.
[01:13] In this example, my words are separated with the help of comma, but it can be any other special character.
[01:19] Regardless of what is your delimiter, you can always pass the same to your split() method.
[01:24] When you pass the delimiter to the split() method, your
[01:27] split() method is going to give you an output, which is an String[].
[01:33] We are yet to discuss about what is an array inside Java array is a very big concept.
[01:39] We are going to discuss about that in the coming lectures.
[01:41] For now, please note that with the help of array, we can store multiple objects of same data type.
[01:49] So here what my split() method is going to do is all the fruit names that are separated with the help
[01:55] of comma.
[01:56] It is going to split them into multiple individual string objects.
[02:01] And all these multiple individual String objects
[02:05] they are going to store inside an array.
[02:08] And the array name is going to be fruit array.
[02:10] So how to represent an array inside Java?
[02:13] After your data type like String, you can simply mention the square brackets like you can see in the
[02:19] screenshot.
[02:19] With that, your fruit array is going to become an array object and it can store any amount of String
[02:26] objects inside it.
[02:28] I hope this is clear.
[02:29] Can we see the demo of this split() method?
[02:31] Let's see for the same
[02:32] let's go to the IntelliJ.
[02:34] Inside my IntelliJ, I have created a new class with the name StringSplitDemo, and inside this class
[02:40] we have a main() method and inside the main() method I have a string with the name fruits and you can see
[02:46] this is a single string.
[02:47] And inside my single string object I have various fruit names like apple, orange, banana, grape and
[02:54] all of them are separated with the help of a delimiter, which is comma.
[02:58] Now as a next step, using the fruits object, I am going to invoke the split() method, and to this split()
[03:06] method I am going to pass,
[03:08] what is that delimiter?
[03:10] The delimiter I want to use here is comma.
[03:13] If I execute my split() method, it is going to return the String[] as an output.
[03:18] That's what you can see inside the definition here.
[03:20] So that's why on the left hand side I'm going to accept String[].
[03:25] So how to define String[].
[03:27] After the String you need to mention open square bracket and close square bracket.
[03:32] And after that you can give the name for your array object.
[03:36] So the name that we want to give here is fruitArray.
[03:40] And inside this object only we are going to store all the strings of fruits.
[03:45] I'm going to keep a breakpoint here and try to run this program.
[03:48] And here you can see my fruit array has multiple string objects.
[03:54] Like at the very first portion I have a string object which is apple post I have orange, banana,
[04:01] grape, even inside the array
[04:03] also the first element is going to have the index zero.
[04:07] So please note that inside Java always the first element index are portion is going to be zero.
[04:13] So this is how array is going to look like.
[04:15] We're going to talk a lot about arrays in the coming sections.
[04:18] But for now I'm assuming you are clear with the purpose of the split() method.
[04:23] If you have these kind of strings where you want to separate the words present inside them with the
[04:29] help of a delimiter, you can always use this split() method.
[04:32] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
