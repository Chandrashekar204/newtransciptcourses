# 26.4 — Creating a Stream from collections - Part 2

> Section 26: [JAVA 8] Streams API

[00:00] In the previous lecture, we tried to invoke the stream() method and parallelStream() method to get a normal
[00:06] Stream object and a specialized stream that is capable of processing the elements parallelly.
[00:12] But sometimes you may want to convert your normal stream as a parallel stream.
[00:18] So here you can see
[00:19] first I have created a normal stream, but later on I want to convert these two parallel stream.
[00:24] So in such scenarios what you have to do is using the Stream object which is departmentStream.
[00:30] You just have to invoke the parallel method with that your normal Stream object
[00:35] it is going to be converted as a ParallelStream object.
[00:39] So if you try to open this and read the documentation, you can see it is going to return an equivalent
[00:45] Stream that is parallel.
[00:47] I hope this makes sense to you, but for now I'm going to comment this line of code because I want this
[00:52] department stream to be a normal stream, because we already have a parallel stream that we built based
[00:58] upon the same department List object.
[01:00] So this process is going to be same regardless whether you are trying to use a set or a ArrayList or
[01:07] a LinkedList or any other collection object, you can always invoke the stream() default method or a parallelStream()
[01:13] method.
[01:14] In the scenarios where you don't have any collection object in your hand, you have only the data in
[01:20] your hand.
[01:21] In that scenario, by using the data directly, you can create the Stream object with the help of the
[01:27] Stream.of() method.
[01:29] As a next step, let me show you how to create a Stream object from a array object. For the same
[01:34] first, I'm going to create an array that is capable of storing String elements, so I'll just mention
[01:40] the variable name as arrayOfwords.
[01:44] Inside this array I'm going to store couple of String objects.
[01:48] One is Easy and the second one is Bytes.
[01:52] So this is my array.
[01:53] Whenever you want to convert an Array object as a Stream object it is going to be very simple.
[01:59] First you need to mention the Arrays class.
[02:01] Inside this Arrays class, we have a static method with the name stream().
[02:07] To this stream(), you can pass your original array, which is arrayOfWords.
[02:11] With that on the left hand side, you should be able to catch the output with the stream of String.
[02:19] So let me give the variable name as streamOfWords.
[02:23] You can see how simple it is.
[02:24] You have a static method stream() inside the Arrays class.
[02:27] Using the same, you can convert your Arrays object as an Stream.
[02:32] Once you created the Stream object, you can invoke lot many API methods available inside the streams
[02:37] API.
[02:38] On top of that, you should be able to program your business logic with the help of Lambda expressions.
[02:43] We also have other type of stream() method inside arrays.
[02:47] You can see this is other type of stream() method.
[02:50] Whenever you have a requirement to create a Stream object based upon a partial data inside your array,
[02:56] you can use this method.
[02:58] So to this method, first you need to pass your array object, followed by what is the starting index
[03:03] and what is the end index.
[03:05] So start is always going to be inclusive and the end is always going to be exclusive.
[03:10] I hope this makes sense to you.
[03:12] Next I want to show you how to create an empty stream.
[03:15] So there is also a option to create an empty stream with the help of Stream class.
[03:21] Inside the Stream class we have a static method with the name empty().
[03:25] With that, you're going to get a empty Stream object and you can mention whatever element type.
[03:32] So here I'm trying to mention String as a element type and the variable name I'm going to mention as
[03:37] emptyString.
[03:38] Sometimes creating an emptyStream is required in real projects.
[03:43] Think like you have a Stream object which built from a collection object that stores 1000 different
[03:48] elements.
[03:49] Using the streams API, you're going to filter the elements and you want to catch only the filtered
[03:56] elements based upon your criteria into your new stream.
[03:59] In such scenarios, you can first create an Empty stream and all the filtered elements can be transferred
[04:05] into these emptyStream.
[04:06] So that's why whenever you have a requirement to create an emptyStream, don't get worried too much.
[04:12] We have a static method with the name empty() inside the Stream class.
[04:16] So these are all the approaches that you can follow to create a Stream object.
[04:21] But before I try to close this lecture, I want to share a couple of important methods available inside
[04:26] the Stream class.
[04:27] One such class is Generate.
[04:29] So inside Stream we have a method called generate().
[04:33] If you try to open this generate, you will be able to understand it is going to return an infinite
[04:39] sequential unordered stream where each element is generated by the provided supplier.
[04:45] So this generate() method
[04:47] it is going to accept a lambda expression that is built based upon the Supplier functional interface.
[04:52] So whenever you are invoking these generate() you're going to get an infinite Stream. In real projects
[04:58] we will not use this very common.
[05:00] But inside interviews, people may ask you to generate an infinite stream and print all the infinite
[05:06] elements that are being generated onto the console, so that can be your one of the tough question inside
[05:10] the streams API related interview.
[05:12] So that's why let's try to understand how to use this method to generate an infinite stream of elements.
[05:19] So to this generate(), we need to pass a lambda expression that is built with the help of Supplier functional
[05:24] interface.
[05:25] So under which scenarios we need to use a Supplier function interface, Supplier, we need to use in the
[05:30] scenarios where we are not sending any input, but we are expecting an output.
[05:34] I want to build a lambda expression logic that is capable of generating a random integer value whenever
[05:40] it is invoked, so we don't have to stress out much around these requirements because we already have
[05:46] a class with the name Random inside the java.util package.
[05:50] Inside this Random class, we have a method with the name nexInt().
[05:54] So this nextInt() it is always going to give you an random integer value whenever we invoke this method.
[06:01] So my business logic is already available in some other instance method.
[06:06] Do you think we need to write a lambda expression from scratch?
[06:08] Off course not
[06:09] we can use our method reference friend to build the lambda expression from the existing logic present
[06:16] inside this instance method.
[06:17] So whenever you want to use the instance method for your method reference, we just have to create the
[06:23] object first.
[06:24] That's why I'm trying to create the object of random first here, followed by I'm going to mention couple
[06:30] of colons.
[06:31] And after these I'm going to invoke nextInt() method.
[06:36] So with this my generate is going to give me an infinite stream.
[06:40] But in order to show you a demo that I'm getting an infinite stream, what I'm going to do is I'm going
[06:45] to invoke the forEach() method from the infinite stream that is going to be generated.
[06:50] So inside this for each I'm going to write a lambda expression which is System.out::println().
[06:58] So basically we're trying to print out each and every random element that is getting generated.
[07:03] So if I execute this program you're going to keep getting a random int value.
[07:08] So this is one approach to generate a infinite stream.
[07:12] We also have other approach.
[07:14] Let me show you that.
[07:15] Before that let me stop this program.
[07:17] The other method that we have inside stream to generate an infinite stream is, iterate.
[07:23] So this iterate() method, it is always going to accept two parameters.
[07:28] One is what is your initial seed value.
[07:31] So if you have a requirement where you want to start stream generation from a initial value, you can
[07:37] always provide what is your initial value as a very first parameter.
[07:41] And the second parameter is the lambda expression that implements unary operator functional interface.
[07:48] So what is a UnaryOperator function interface scenario?
[07:51] It is always going to accept an input parameter of type T, and it is always going to give you the same
[07:57] type T as an output.
[07:59] I hope you recall our discussion around the function interface.
[08:02] So now what I'm going to do is to this iterate() method,
[08:05] I'll just mention the initial seed value as one, followed by I'm going to write a lambda expression
[08:12] which which is capable of accepting an input parameter.
[08:15] I'll give this variable name as n goes that I'll just mention a lambda expression symbol, followed
[08:20] by.
[08:21] I'll try to add one to these initial number that I have received as an input.
[08:26] So with this, what is going to happen is, first time when the stream is getting invoked, this n value
[08:32] is going to be one.
[08:33] So one will be fitted to this.
[08:35] And with that one plus one will get two.
[08:38] In the next iteration two is going to be fielded and two plus one is going to become three.
[08:42] This way we are going to get a stream of infinite numbers, which are getting incremented by one each
[08:49] time.
[08:49] So to see the stream of elements.
[08:51] So we need to write this for each and to this for each
[08:54] we need to pass the System.out.println() as an lambda expression.
[09:00] So here I'm trying to use the method reference.
[09:02] In order to see the demo of this code.
[09:04] First I need to comment these upper line of code, because this is never going to terminate since it
[09:11] is a infinite stream.
[09:12] So now let me execute this program and you can see the numbers are keep getting printed, but every
[09:18] time the next number is getting printed plus one is being added.
[09:22] I hope this makes sense to you.
[09:23] These are the two approaches that you can always use to generate an infinite stream.
[09:28] For now, I'm just commenting this code because when you take this code from GitHub repo, I want this
[09:34] program to run properly.
[09:35] That's why I have commented these infinite stream related code.
[09:39] Everything that we have discussed so far around creating a stream from a collection, or from a List
[09:44] of elements, or from an array.
[09:45] So all these points I have mentioned in these two slides for your quick reference, feel free to refer
[09:51] them in future for any questions.
[09:53] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
