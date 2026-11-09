# 26.14 — Introduction to Streams reduce() method

> Section 26: [JAVA 8] Streams API

[00:00] From this lecture, we're going to focus on the terminal operations available inside the streams API.
[00:07] As of now, we know how to create a Stream object to process the elements inside it.
[00:12] On top of that, we also learned what are the various commonly used intermediate operations, which
[00:17] we can use them based upon our business requirements.
[00:20] So the step two, which is the intermediate operations, is always going to be optional inside a streams
[00:27] pipeline.
[00:27] Inside this step two we can use any number of intermediate operations.
[00:32] But coming to the step three which is a terminal operation, this is always going to be mandatory if
[00:38] you want to derive the output from the elements available inside the Stream object.
[00:43] On top of that, we can only invoke a single terminal operation on a Stream object.
[00:49] We can't invoke multiple terminal operations on top of a single Stream object like intermediate operations.
[00:55] The reason is very obvious
[00:57] terminal means it is going to terminate your Stream, and it is going to give you the output based upon
[01:03] your instructions.
[01:04] So once you terminate it, if you try to invoke one more terminal operation, it is it is not going
[01:09] to make any sense.
[01:10] That's why inside streams API, we will be able to invoke the terminal operation only once on a given
[01:18] Stream object.
[01:19] Inside this lecture, let's try to focus on one of the most commonly used terminal operation, which
[01:25] is reduce.
[01:26] So what is this reduce() method.
[01:27] Using these reduce() terminal operation which is also known as reduction operation or a fold operation.
[01:35] We can combine all elements of a stream to generate a single value as an output.
[01:42] So to these reduce operation you're going to provide a lambda expression which is going to be executed
[01:48] on each of the element inside your stream.
[01:51] So this lambda expression, in other words, we can call it as a combining function, because it is
[01:57] going to combine the output from all the elements into a single value, and the same single value is
[02:02] going to be given as an output once this terminal operation is executed completely.
[02:08] Example of reduce operations include computing the sum, maximum, average count, and similar aggregate
[02:14] operations for a stream of elements like integers, double, long.
[02:19] When I show you the example, it is going to make more sense to you.
[02:21] For now
[02:22] please note that using reduce() operation, we can derive a single value as an output by applying a given
[02:30] combining function on each element inside your Stream object.
[02:35] So if you try to understand how this reduce is going to work is, there are different kinds of reduce
[02:40] overloaded methods available inside the streams API.
[02:42] But speaking about most commonly used reduce() method is, it is going to accept two types of input parameters.
[02:50] The very first one is what is your initial seed value followed by what is the combining function, or
[02:56] what is your lambda expression into a single value.
[03:00] So here you can see I have various numbers inside my input stream like n1, n2, n3 and n4.
[03:07] Using this stream, I'm going to invoke the reduce() terminal operation.
[03:12] To this reduce() terminal operation, I'm trying to pass what is the initial seed value along with the
[03:18] lambda function.
[03:19] So with this what is going to happen is behind the scenes my reduce() terminal operation
[03:23] it is going to iterate all the elements during the first element iteration.
[03:27] It will take what is the initial seed value and apply the same to the n1 value based upon your lambda
[03:35] function given. Post that the output from these is going to be fielded as a seed to the n2 element,
[03:42] so this is going to keep on continue till the last element, and at last we are going to get a single
[03:48] value as an result.
[03:49] Inside streams API there are some specialized reduce() operations that are also available like sum(), max()
[03:56] mean(), count().
[03:57] So these are specialized reduce() operations you can use directly instead of writing your own reduce() operation.
[04:04] For example, if you are looking to sum all the integer elements inside a stream, then you can directly
[04:09] use the sum() method which is going to give you the output.
[04:12] And similarly, if you are looking to identify a maximum number, minimum number, and the count of
[04:17] the number of elements.
[04:18] So in all these kind of scenarios you can use these specialized reduce() operations.
[04:24] Only if these specialized reduce() operations they are not able to help you in your business logic
[04:29] in such scenarios you can write your own reduce() operation with your own lambda expression.
[04:35] But please note that these specialized reduce() methods, they are not universally available for all type
[04:43] of streams.
[04:43] For example, if you want to use a sum terminal operation, you can't use it on top of the normal stream
[04:50] object because it is not going to make any sense
[04:54] adding reference type elements like two people are two employees, so that's why these kind
[05:00] specialized reduce() methods
[05:02] they are only applicable for Stream objects of type IntStream, LongStream, DoubleStream.
[05:08] So using these IntoStream, LongStream, DoubleStream, we can only store the elements of int, long
[05:15] and double, which we can add them with the help of some operation.
[05:19] But coming to the count() terminal operation, you can use these on top of any kind of Stream object,
[05:25] because at the end of the day, this count() terminal operation, it is going to give you the output by
[05:29] counting the number of elements available inside your Stream object.
[05:34] We are going to see the demo of these methods in the next lecture.
[05:37] For now, let me show you some examples on how to use the reduce() terminal operation.
[05:43] Here first, I have list of integers in the form of this numbers List object.
[05:48] Using the same, I'm trying to invoke the stream() method to form a Stream object.
[05:53] Post that I'm directly invoking the terminal operation reduce().
[05:57] So to this, reduce() the initial seed value I'm trying to provide is zero.
[06:02] Followed by
[06:03] the business logic that I want to use here is to sum all my elements with the logic present inside the
[06:09] sum() method of Integer wrapper class.
[06:12] So that's why I'm trying to use the method reference here.
[06:15] So once this terminal operation is completed, I'm going to get the sum of all these elements into this
[06:21] output variable the same I can try to print out.
[06:23] So what will be the output.
[06:24] You are going to get the output as 15.
[06:26] We can also use this reduce() operation if you have a List object that is holding custom data types like
[06:32] Person.
[06:33] So here you can see I have an example where I have a List object with the name Persons think like inside
[06:40] this Persons List object I have good amount of persons.
[06:43] So all these Person objects, they are going to have a field indicating what is the income of a Person.
[06:49] So I can get these income by invoking these getIncome() method.
[06:53] So what I'm trying to do here is first with the help of map() method, I'm trying to get the income
[06:59] details of each person inside my stream.
[07:02] So with that this is going to give me an stream which is going to hold only the int values.
[07:09] Post that I'm going to invoke the terminal operation reduce().
[07:12] Using this reduce() I'm trying to sum all the person income details and the output
[07:17] I'm going to get into this sum variable.
[07:19] So there are hundreds of ways on how you can use the streams API.
[07:24] I'm just trying to teach you the basics of the streams API.
[07:27] And and I'm trying to make you comfortable with the streams API syntaxes and operations involved.
[07:32] But like I said, it is a version which you need to swim yourself to know the depth of this ocean.
[07:38] But don't worry, as you start working on more and more examples and scenarios inside real projects,
[07:44] you should be able to easily catch up because you're already familiar with all the basics that we are
[07:49] discussing throughout this course.
[07:51] I hope you are clear with this
[07:52] reduce() method theory
[07:54] introduction.
[07:55] In the next lecture, let's see the demo of reduce() Terminal operation.
[08:00] Thank you
[08:00] and I'll catch you in the next lecture, bye.

----------------------------------------
