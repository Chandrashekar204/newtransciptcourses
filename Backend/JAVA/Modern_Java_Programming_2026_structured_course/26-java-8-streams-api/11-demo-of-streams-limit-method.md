# 26.11 — Demo of Streams limit() method

> Section 26: [JAVA 8] Streams API

[00:00] Sometimes you may have a business requirement to process only a limited number of elements inside a
[00:07] collection.
[00:08] Maybe your collection may have millions of elements, but you want to process only the first hundred
[00:14] elements are first 1000 elements.
[00:16] In this kind of scenarios, where you want to enforce some business logic to limit the number of elements
[00:22] to be processed, you can use a limit() method available inside the stream API. Like you can see here,
[00:30] limit() method
[00:31] it is going to accept the number of elements inside a stream that needs to be limited, so it is not
[00:36] going to accept any number of lambda expression as an input, because your business requirement is only
[00:42] to limit certain number of elements to be processed.
[00:45] So that's why if you pass the number of elements to be limited to this limit, it is going to give a
[00:51] new Stream object with only the limited number of elements which you can transfer them into another
[00:57] collection object, or which you can process them further with the another intermediate operations like
[01:02] filter() or map()
[01:03] it's up to you what you want to do.
[01:05] So here I have an example
[01:07] also.
[01:07] You can see first with the help of generate() method, I'm trying to generate random int values.
[01:13] We know Stream.generate()
[01:15] it is going to give us infinite stream of into values, but I don't want to process all the infinite
[01:21] stream of values.
[01:22] Instead
[01:23] if I want to process only the first ten elements, then I'm going to give the ten as an input to the
[01:29] limit was that I'm trying to use a terminal operation, which is going to help me to print all the elements
[01:35] that I limited onto the console.
[01:37] So here I'm trying to use that ten as the limit, whereas in the picture I'm trying to use five as the
[01:44] input to the limit.
[01:45] On the left hand side you can see I have an input stream with some random integer values, but by the
[01:51] time these intermediate operation is executed on the output stream, I have only the first five elements
[01:57] one, two, three, four, five.
[01:59] Because my limit() method it is going to limit the number of elements to five based upon the input that
[02:04] I have provided. Inside collections we know we have List, and Set, List is going to maintain the order
[02:10] of elements.
[02:11] So whenever you are using an data structure which is guaranteeing the order of insertion, then obviously
[02:18] based upon your limit, you're going to get first five elements or first ten elements.
[02:24] But if you are using limit on top of a collection data structure like Set, where it is not going to
[02:30] maintain any order of insertion, in such scenarios, we can't predict what kind of elements you're
[02:35] going to get as an output.
[02:37] The limit
[02:38] it is going to randomly select the limited number of elements without worrying about their order.
[02:43] So this is a note that you need to be consider.
[02:45] So if your business logic does not care about the order of elements to be processed in such scenarios,
[02:51] you can use limit without any worries whether you are trying to deal with the List or Set.
[02:56] But if you have a business requirement where you want to process only the first 210 elements inside
[03:03] a list in the same order, then obviously you can't use the set object as a source for your stream.
[03:10] Instead, you should use the List object.
[03:12] I hope you are clear with this theory discussion.
[03:15] Let's see the demo of this limit() method very quickly inside the IntelliJ Idea.
[03:20] Here inside my IntelliJ Idea, I'm going to create a new Java class with the name StreamLimitOperationDemo.
[03:28] .
[03:28] So let me replace this filter() with limit post that I'm going to create a main() method.
[03:35] And inside this main() method first I'm going to generate an infinite stream with the help of Stream.generate()
[03:41] Stream.generate().
[03:42] And to this generate() I'm going to pass an lambda expression with the help of method reference by first
[03:48] creating the Random class object, followed by
[03:51] I'll mention two colons and post this
[03:54] I'm going to mention nextInt().
[03:56] So this is going to give me an infinite stream, but I want to use a intermediate operation which is
[04:02] limit().
[04:02] And to this limit() I want to pass the size as ten, so that only the first ten elements inside my stream
[04:10] there they're going to be processed.
[04:11] So after this limit(), if needed, I can also use a map() intermediate operation where it is going to accept
[04:18] the number as an input followed by it is going to double the number by multiplying it with two and at
[04:25] last using the
[04:26] for each terminal operation, I want to print out all the processed elements onto the console by using
[04:33] these method reference with the help of println() method.
[04:37] So if I execute this class, you'll be able to see that these are the first to ten randomly generated
[04:43] int values.
[04:44] The same
[04:45] I tried to double them by performing the multiplication with the map() operation as well. But the beauty
[04:50] here is we are only getting the ten elements as an output.
[04:55] The reason is we have this limit() in the intermediate operation.
[04:58] If I remove this, then obviously
[05:00] you're going to see a flood of elements keep on generated from your stream, which we want to avoid.
[05:07] That's why as soon as we keep this limit(), the output is going to be limited to only the first ten elements.
[05:15] I hope you are clear about the purpose of this limit()
[05:18] intermediate operation.
[05:19] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
