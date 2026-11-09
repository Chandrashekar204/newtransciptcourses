# 26.10 — Demo of Streams filter() method

> Section 26: [JAVA 8] Streams API

[00:00] The next two most commonly used intermediate operation of streams API is filter method.
[00:06] The purpose of this filter method is to filter or to exclude certain elements inside a collection based
[00:13] upon a specified condition, like you can see here.
[00:16] Initially, my list object has four different elements or four different string object.
[00:21] If I'm trying to filter the elements that starts only with the carry s, then I can use the filter intermediate
[00:29] operation.
[00:30] In this kind of scenario, you can see I'm trying to first invoke the stream method post that I'm trying
[00:36] to invoke the intermediate operation, which is filter, and to this filter we need to provide a lambda
[00:41] expression, which is capable of identifying whether a given element should be filtered or not.
[00:46] So the filter method always going to accept a lambda expression which built based upon the predicate
[00:52] functional interface.
[00:54] So what is the purpose of predicate function interface.
[00:56] It is always going to accept any kind of input, and the return type from the predicate is always going
[01:02] to be boolean.
[01:02] So based upon the boolean returned by your lambda expression.
[01:06] The stream API is going to decide whether a given element needs to be filtered and moved to the new
[01:13] stream object it is going to form after the filter.
[01:16] At last you can see I'm trying to invoke the terminal operation, which is for each using which I'm
[01:21] trying to display all the filtered elements onto the console.
[01:25] So if you try to visualize this, this is how it is going to look like.
[01:28] I'm going to provide an input stream with the four different elements to the filter method, where it
[01:33] is going to have a lambda expression to filter the elements.
[01:36] That starts with a car S.
[01:38] That's why on the output stream side I have only two elements with the name supply and sales.
[01:44] All the remaining elements like HR and marketing.
[01:47] They are filtered out because they're not starting with the car.
[01:51] S this should be pretty easy to understand, but it is so powerful that why in the real projects filter
[01:57] and maps, they are going to be used to a large extent to process your business logic instead of writing
[02:03] ugly if and else conditions.
[02:05] This filter method can be used to filter your elements with a very less amount of code.
[02:11] Let's see the demo of this filter method very quickly.
[02:14] What I'm going to do is I'll try to copy this treemap operation into the same package, but I'll try
[02:19] to rename this to Stream Filter Operation Demo post that you can see I have a list object with the name
[02:27] department list.
[02:28] Now what I'm going to do is I'll try to remove all this code and instead of map method I'm going to
[02:34] invoke the filter method.
[02:36] So to this filter method we need to pass the lambda expression that is built based upon the predicate
[02:41] function interface.
[02:42] Inside the documentation.
[02:43] You can also see this is highlighted as an intermediate operation.
[02:47] So it is going to return a new stream consisting of the elements of this stream that matches the given
[02:54] predicate.
[02:54] So predicate is a condition.
[02:56] So if a element matches to your condition, it is going to be moved to the new stream object which is
[03:02] going to be returned by this filter intermediate operation.
[03:05] So let me go to the stream filter operations demo.
[03:08] So here inside the lambda expression we are going to accept an input parameter with the name word post
[03:15] that I'm going to invoke.
[03:16] The method starts with and I'm going to mention the car value, which is S.
[03:22] With that you can see the compilation error also resolved, because now the return type of this is going
[03:28] to be a boolean.
[03:29] And with that this filter intermediate operation, it is going to give me a new stream.
[03:33] By using this new stream object, I'm trying to invoke that terminal operation, which is for each to
[03:38] display all the filtered elements onto the console.
[03:42] So let me execute this program and you'll be able to see I'm getting the output as supply and sales.
[03:48] Are you seeing the beauty of streams API?
[03:50] If needed we can also add map intermediate filter, maybe think like I want to convert them into uppercase
[03:58] before I try to filter them.
[04:00] So that's why I'm trying to put map here first, followed by I'll try to write a lambda expression which
[04:05] is word, the lambda symbol, and using word I'm going to invoke the method which is to uppercase.
[04:12] So this is going to act as a first intermediate operation followed by filter is going to be a second
[04:17] intermediate operation.
[04:18] And at last we have a terminal operation I try to move these to multiple lines so that you can read
[04:24] it very easily.
[04:25] But once you become a pro in Functional Programming and Streams API, you can try to mention all this
[04:31] logic in a single line.
[04:32] So this time, if I try to execute, you'll be able to see I'm getting the output of two elements with
[04:38] completely capital letters.
[04:39] This way you can always use the filter method for any kind of objects.
[04:44] Think like you have some thousand employee objects inside a list.
[04:48] If you are looking to build a new list with only permanent employees, then you're going to use a condition
[04:54] inside your lambda expression, which is going to identify whether an employee is a permanent employee
[04:59] or a temporary employee.
[05:00] Accordingly, you're going to call that terminal operation collect to collect the filtered elements
[05:06] into a new list object.
[05:08] I hope you're clear.
[05:09] Like I said, it is very simple to understand filter.
[05:12] Before I try to close this lecture, let me show you one funny image around the usage of filter method.
[05:18] Previously we were discussing about the map.
[05:21] Similarly, let's see how the filter method is going to work.
[05:24] So to this filter method we are trying to pass multiple elements that we received from the map, like
[05:29] this is a bug.
[05:31] And these are the French fries followed by chicken leg piece followed by popcorn.
[05:35] So to this filter, if you try to pass a lambda expression, which is going to identify whether a given
[05:40] element is an vegetarian element or not.
[05:43] The output is always going to be like you can see here since burger has beef which was produced by cooking
[05:50] the meat of cattle like cow, it is considered as non-veg.
[05:54] Previously, when we were discussing about the map, I thought from the milk of cow, they're going
[05:58] to prepare the cheese.
[05:59] But I was wrong.
[06:01] Seems they're trying to refer to the beef here.
[06:03] So that's why this burger is not present in the output as it is not a vegetarian item coming to the
[06:09] French fries.
[06:10] Since they are made from potato, they are pure vegetarian items followed by leg piece is going to be
[06:16] ignored or filtered.
[06:17] And the class popcorn which is made from the corn.
[06:20] It is also considered as a pure vegetarian item.
[06:23] That's why on the output we are getting the two items French fries and popcorn.
[06:28] I hope you like this.
[06:29] Thank you and I'll catch you in the next lecture.
[06:32] Bye.

----------------------------------------
