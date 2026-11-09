# 27.7 — Quick tip to filter null elements with Stream API

> Section 27: [JAVA 8] Optional to deal with nulls in Java

[00:00] Since we are talking a lot about NullPointerException
[00:03] inside this section. I want to share a tip on how to handle the NullPointerExceptions.
[00:07] .
[00:08] Whenever you are trying to process collection of elements with the help of streams API.
[00:13] To show you this tip, I'm going to create a new Java class inside the package com.eazybytes.optional.
[00:20] So the class name is StreamsApiNull
[00:25] StreamsApiNullCheckTip.
[00:26] So this is some random ugly class name.
[00:29] I know you don't like this class name.
[00:30] That's why this just a training.
[00:32] Inside this method, I'm going to create a list of String objects with the help of of() method.
[00:38] So here to this of() method I'm trying to pass various country names like USA followed by India, and
[00:47] in between I'm going to pass null values also.
[00:50] And after null I'm going to mention Canada.
[00:54] And after the Canada I'm going to mention null again.
[00:57] And after this null, I'm going to mention UK.
[01:01] And after the UK I'll mention one more null, followed by one more null
[01:06] and at last I'll try to mention Germany.
[01:09] So if you see here there are good amount of random null objects or element present inside my List object.
[01:17] So whenever you try to process these kind of data with the help of streams API, there is a good chance
[01:22] that you may get a NullPointerException.
[01:24] So let's see how we are going to get a NullPointerException.
[01:28] So first on the left hand side I'm going to catch the output with the help of List of String and with
[01:34] the variable name as countryNames.
[01:37] Now using these countryNames, I'm going to invoke the stream() method post that I'm going to invoke
[01:43] the map() method.
[01:44] Using the map() method, I want to convert each of my country name into an completely uppercase letter.
[01:51] So for the same I'm going to give the lambda expression which is String colon colon toUppercase().
[01:58] And at last I'll try to invoke the collect() terminal operation.
[02:02] To this collect() terminal operation I'm going to pass the input which is Collectors.toList().
[02:07] With that I can catch the output and the left hand side with the help of List of String and with the
[02:13] variable name as capital names.
[02:16] And at last I'll try to print out these capital names onto the console.
[02:20] So if I execute this program, you can see I'm getting a NullPointerException.
[02:24] Do you know why I'm getting these NullPointerException?
[02:27] Because I'm trying to execute these map logic for each element.
[02:31] So in the case of null element it is going to invoke these toUppercase() directly with the help of null
[02:38] object.
[02:38] And with that we are going to get a our favorite NullPointerException.
[02:43] So here the fix is very simple.
[02:45] We just have to use the filter intermediate operation just before you try to perform any other business
[02:53] logic.
[02:53] So just after the stream I'm going to invoke the filter intermediate operation to this filter intermediate
[03:00] operation I'm going to pass a predicate condition with the help of objects.
[03:05] And inside the objects we have a method with the name non null.
[03:10] So what is this non null method is going to do.
[03:12] It is going to check if the given object is not null.
[03:16] If it is not null, it is going to return the value as true.
[03:19] With that, all the null elements that are going to be filtered by the time these next intermediate
[03:25] operation is going to be executed.
[03:26] So now if you try to execute this class we are going to get a proper output.
[03:30] But unfortunately we are getting the same NullPointerException.
[03:33] So this is going to be a tricky scenario.
[03:35] I want you to answer why I'm still getting the same NullPointerException.
[03:40] Do you know the reason
[03:41] because I'm using the List.of() method.
[03:44] Whenever we use the of() method, we are going to build an immutable List object.
[03:50] Since we are trying to filter some of the elements with the help of this filter, which are stored inside
[03:56] these immutable List object, we are getting the exception.
[04:00] That means though I'm trying to execute this filter, these elements, they never filtered because this
[04:05] is an immutable List object.
[04:07] So that's why in this kind of scenarios, let's make sure we are not using the immutable collection
[04:13] object.
[04:14] So here instead of List.of() I can try to use Arrays.asList().
[04:20] So with that I'm assuming we should have some good news.
[04:24] So let me execute this this time.
[04:26] Yay!
[04:26] We are getting the proper output.
[04:29] The main point that I want to convey from this lecture is always use these kind of logic to simply get
[04:36] rid of all null object inside your stream, or inside your collection data source.
[04:42] I hope you like this tip, and I'm assuming you're also going to use this a lot inside your business
[04:47] logic.
[04:48] Thank you and I'll catch you in the next lecture, bye.


########################################
