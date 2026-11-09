# 26.2 — Introduction to java.util.stream API

> Section 26: [JAVA 8] Streams API

[00:00] Inside this new section, we are going to focus on streams API that are introduced as part of the Functional
[00:07] Programming in Java 8 release.
[00:09] As of now, we have very good understanding around the collections, how to store the elements inside
[00:15] collections, how to iterate them, how to process them with the help of various data structures like
[00:20] List, Map, Set, Tree.
[00:23] By using all these data structures, we know how to build a business logic.
[00:26] But with the knowledge that we have so far, we are building the business logic with the help of imperative
[00:32] approach where we are giving low level instructions to the collection framework, saying that to iterate
[00:38] the elements with the help of for each or for loop or iterate our while loop during the iteration.
[00:44] If you have any filtering requirements, we are writing various if conditions or if you want to build
[00:49] any transformation logic.
[00:51] We are trying to achieve everything with the help of low level instructions, but by combining streams
[00:57] API and lambda expressions, we should be able to process the elements inside a collection with a very
[01:04] less amount of code.
[01:05] Once you master the streams API, like I promised before, you are going to love Lambda a lot and you
[01:13] will be using this lambda a lot inside your code as well.
[01:17] So what are streams API?
[01:18] When I say streams API, there are list of classes and interfaces available inside the package
[01:25] java.util.stream.
[01:27] So all the classes available inside this package, we can construct them as streams API.
[01:32] If you ask a non-technical person about what is a stream, he may answer saying that stream is a continuous
[01:38] flowing of water like in a river.
[01:41] Similarly, inside Java, whenever someone is saying stream, we can consider it as a flow of data,
[01:48] like someone can store their data or their elements inside a collection object.
[01:53] Using these collection objects, we can build a stream, and from this stream the data is going to flow
[02:00] element by element for the processing
[02:02] based upon the lambda expressions that we are going to write. We are going to discuss in detail about
[02:08] this stream API throughout this section.
[02:09] So brace yourself and hold your excitement around this.
[02:13] Inside this lecture, let's try to understand the basic details of the streams API.
[02:17] Whenever someone says streams API don't get confused with the package java.io, inside java.io
[02:25] also, we have streams, related classes and interfaces which are going to help us to write the data
[02:32] or to read the data from the source like a file.
[02:34] So this stream, which is available inside the java.io package, is different from the stream which
[02:40] is available inside the java.util.
[02:42] So here io indicates input and output.
[02:46] So that's why if someone is trying to confuse you, don't get confused.
[02:49] If they ask you what is the difference between these two stream related packages, simply answer them
[02:54] if you are referring to the streams API available inside the java.io package, they are going to help
[02:59] us to read or write the data to and fro from the files. Whereas the streams API which are available
[03:04] under the package java.util
[03:06] they are going to help us to process the elements inside the collection data structure objects with
[03:11] the help of lambda expressions.
[03:13] So that should be your answer.
[03:15] The next important point is, like I said, with the help of collections like List, Set, we will be
[03:20] able to store the data physically, which belongs to a single data type, whereas with the help of streams,
[03:28] we will be able to process the group of objects available inside a collection.
[03:33] We should be able to process the elements inside a collection object without the help of stream API
[03:40] as well.
[03:40] But with that imperative, our old approach, you will end up writing lot of low level code when we
[03:46] start exploring these streams API in the coming lectures, you're going to understand this point in
[03:51] detail.
[03:52] We should be able to create the streams from the collections or from arrays or from iterators.
[03:58] So it's not mandatory that streams API is going to work only with the collections.
[04:03] The streams can also be created, and the streams API can also be used
[04:07] on top of the arrays are iterators as well.
[04:10] At last I want to highlight whenever we are trying to use the streams API, we are going to write the
[04:16] code in a declarative way.
[04:18] So what is the meaning of declarative way?
[04:20] Declarative way means we are going to give instructions to the Java or JRE in a more like a English
[04:27] language, but not like a low level instructions with the help of loops with the help of if conditions,
[04:33] with the help of variable names, we're not going to do all that.
[04:36] So this declarative approach, it is going more like a query style, as opposed to specifying how to
[04:43] implement an operation.
[04:44] With the help of imperative approach, you're going to give every detail to the JVM and how to execute
[04:50] your operation.
[04:51] But with the help of declarative way or with the help of streams API or with the help of functional
[04:56] programming, you are only going to give the high level
[04:59] instructions in a query style are in a declarative style.
[05:02] I hope you are clear with these basic introduction of streams API.
[05:06] If something is not clear, don't worry.
[05:08] As usual, we are going to see a lot of demos around these API.
[05:11] Once we complete the demos then all these points are going to make more sense to you.
[05:16] I hope you are excited about these streams API.
[05:19] Let's start the journey of streams API from the next lecture.
[05:23] Thank you,
[05:24] bye.

----------------------------------------
