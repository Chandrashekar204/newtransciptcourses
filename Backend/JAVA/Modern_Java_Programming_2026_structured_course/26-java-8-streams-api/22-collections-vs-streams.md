# 26.22 — Collections Vs Streams

> Section 26: [JAVA 8] Streams API

[00:00] We almost covered all the details around the stream API.
[00:03] We discussed everything around the intermediate operations, terminal operations, parallel processing.
[00:09] So now we have a very good understanding around the stream API and how to process the elements inside
[00:14] a collection with the help of streams and the lambda expressions.
[00:18] As part of this lecture, let's try to understand what are the differences between collections and streams.
[00:23] We know collections are present inside Java from day one, whereas streams they are introduced as part
[00:29] of Java 8.
[00:30] So this is one of the famous interviews around the Java Collections and Streams API.
[00:35] That's why let's try to put some efforts understanding the differences between the collections and streams.
[00:41] The very first and most important difference between collections and stream is, collections
[00:45] they are going to hold the elements inside the memory or inside the heap memory, whereas streams,
[00:53] they are not going to store the elements inside any memory, all the elements, they are going to be
[00:58] stored using the underlying collection data source.
[01:01] We already discussed in detail about this point in the previous lectures.
[01:05] Moving on to the next difference, a collection is going to be eagerly constructed and the elements
[01:12] can be added or removed.
[01:14] So whenever we are trying to build a collection object and try to add all the elements inside each,
[01:20] these operation is going to be done eagerly.
[01:23] That means before you try to perform any operations on top of your collection object, all the elements
[01:29] might have stored inside a heap memory, but coming to the stream, they are going to operate lazily.
[01:35] For example, if you are trying to run a map() operation with the help of Stream object, it is not going
[01:40] to load all the hundreds of elements inside your underlying collection data source.
[01:45] Instead, it is going to read the element lazily one by one.
[01:50] The next difference is pretty easy collections.
[01:53] They don't use any functional interfaces and lambda expressions, but on the other side streams they
[01:58] are going to use lot of functional interfaces along with the lambda expressions.
[02:03] We can't imagine streams API without lambda expressions and functional interfaces.
[02:09] The next difference is collections are non consumable.
[02:12] That means collections can be traversed to multiple times without creating again.
[02:18] If you have a List of object, you can try to iterate it any number of times with the multiple
[02:24] for loops and while loops, you're not going to get any exception.
[02:28] But on the other side, streams are consumable, which means you can only traverse them once if you
[02:34] want to traverse or iterate the elements inside stream one more time, the only option that you have
[02:39] is to create the stream one more time.
[02:42] If you try to traverse the same Stream object multiple times, like we discussed in the previous lectures,
[02:47] we are going to get an IllegalStateException.
[02:50] Coming to the last difference, it says collections are iterated using external loop like for loop and
[02:57] while loop only.
[02:58] So whenever we are dealing with the collections, we need to give low level instructions to the JRE
[03:03] or the Java and how to iterate the elements inside a collection.
[03:07] Whereas with streams we don't have to give any low level instructions, we can follow the functional
[03:12] style of programming as long as we are using intermediate operations or terminal operations to process
[03:18] the elements inside stream, the iteration responsibility is going to be taken care by the Java
[03:24] internally.
[03:25] We as a developers, we don't have to manually iterate the stream elements.
[03:29] So these are the differences between collections and streams.
[03:32] I hope you are clear.
[03:34] Thank you and I'll catch you in the next lecture, bye.


########################################
