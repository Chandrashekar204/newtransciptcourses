# 26.20 — Quick revision about stream pipeline

> Section 26: [JAVA 8] Streams API

[00:00] We discussed a good amount of intermediate and terminal operations that are available inside the streams
[00:07] API.
[00:07] In this lecture, I just wanted to quickly revise how the streams pipeline they are going to work by
[00:13] taking an example. So that this lecture is going to act like a revision for your understanding about
[00:18] the streams API.
[00:19] Like we know we can form a chain of stream operations using multiple intermediate operation and a single
[00:27] terminal operation.
[00:28] So the single terminal operation is going to help us to give that desired output.
[00:33] So this type of chaining of multiple stream operations, we can call in other words as stream pipeline.
[00:40] Let me try to show you visually how a stream pipeline is going to formed by taking a business problem.
[00:47] Think like I have an requirement where I'm going to receive a list of int values.
[00:52] So from these list of into values, first I'm going to form the Stream object, followed by I want to
[00:57] filter all order numbers from the List.
[01:00] Once the filtering of the odd numbers is completed, I want to have another intermediate operation,
[01:06] which is going to help me to multiply the inter element by themselves.
[01:10] Once this multiplication operation is completed, I want to perform the sorting of the elements, and
[01:17] at last I want to display all the inter elements by storing them into a List.
[01:22] So if you try to visualize this problem, this is how it is going to look like.
[01:26] So first you're going to have an input stream.
[01:29] So all these green highlighted operations are intermediate operations.
[01:33] So this should give a confirmation to you that we can have any number of intermediate operations.
[01:38] So whenever we execute an intermediate operation it is going to give you a new Stream object with the
[01:44] new data or with the new elements.
[01:47] So first I'm going to have a filter() intermediate operation to filter only the odd numbers.
[01:52] Later on
[01:53] since I want to multiply each number by itself and return the output, I can use some map() intermediate
[02:00] operation and at last to perform the sorting of the elements, I can use the sort intermediate operation
[02:08] available, and after these all these intermediate operations are executed
[02:12] eventually I can invoke only one terminal operation.
[02:16] So here I'm trying to invoke the terminal operation with the name collect().
[02:20] Using this terminal operation only, I'm going to collect() all my elements into a list post that I'm
[02:26] going to print the same.
[02:26] So let's try to understand this in detail by looking at a flow diagram like you can see.
[02:31] First I have a list of elements.
[02:33] Using this list of elements, I'm going to form a stream by invoking the streamDefault() method.
[02:38] After that, for the filter() method I'm going to give my predicate condition.
[02:42] So if the number is not exactly divisible by zero, then filter it and move it into a new stream.
[02:49] So this is my new stream where I have only the odd numbers.
[02:52] The even numbers like 2, 4
[02:55] they are removed completely in the new stream.
[02:57] Now this new stream which has only odd numbers, we are going to feed it to another intermediate operation
[03:04] with the name map().
[03:05] Inside this map() intermediate operation, we're just multiplying each element by itself.
[03:10] So phi into phi it is going to become 25 followed by 11.
[03:13] It is going to become 121.
[03:15] For seven it is going to be nine for 13, it is going to be 169, and for nine it is going to be 81.
[03:21] So this is again a new stream.
[03:23] And this new stream I want to feed it to the another intermediate operation which is sorted().
[03:28] So we just have to invoke the sorted() method.
[03:30] We don't have to send any lambda expression.
[03:33] So based upon these intermediate operation I'm going to get a new stream which has the elements in a
[03:40] sorted manner.
[03:41] So you can see all the elements are sorted in an ascending order 25, 4981, 121 and 169.
[03:48] And at last I'm going to invoke that terminal operation with the help of toList() method available inside
[03:55] the collectors.
[03:56] So the same is going to help me to move the elements inside the Stream into a List object.
[04:02] The same List object I can send as an input to the println() method to display all the elements onto my
[04:07] console.
[04:08] So always refer these two slides to quickly revise about the streams pipeline.
[04:13] These are very important inside the Java interviews.
[04:16] People can try to confuse you by asking various questions around the intermediate operations, terminal
[04:22] operations, traversing of the stream again and again so they can be good amount of questions around
[04:28] these inside interviews.
[04:29] That's why I'm trying to emphasize again and again so that it is going to be clear for you.
[04:34] I hope you are clear with these discussion about the stream pipeline.
[04:37] Thank you
[04:38] and I'll catch you in the next lecture, bye.

----------------------------------------
