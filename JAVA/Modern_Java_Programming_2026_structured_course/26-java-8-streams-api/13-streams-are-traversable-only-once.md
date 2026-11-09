# 26.13 — Streams are traversable only once

> Section 26: [JAVA 8] Streams API

[00:00] As of now, I provided the details of the most commonly used intermediate operations we discussed about
[00:07] map(), flatMap(), filter(), limit(), skip().
[00:10] We discussed good amount of intermediate operations.
[00:14] These intermediate operations are good enough to get you started on using the stream API.
[00:19] There are more than ten different intermediate operations.
[00:22] We don't have to discuss all of them, but in future whenever you have a requirement which you are not
[00:28] able to achieve based upon what we discussed so far in such scenarios, you don't have to worry much.
[00:34] You just have to go to the Stream class, which is the parent of all the stream API. Inside this class,
[00:40] just keep scrolling each method by method.
[00:43] Wherever you see an intermediate operation inside the documentation, you
[00:47] can safely consider that as an intermediate operation and try to read the documentation
[00:52] look inside the internet for the example.
[00:55] With that, you'll be able to easily understand what is the purpose of that particular intermediate
[01:00] operation.
[01:01] In the interest of time, I'm not discussing all the intermediate operations available inside the stream API.
[01:07] So you can see filter() we discussed similarly map(),
[01:10] we discussed mapToInt()
[01:12] we discussed, mapToLong(), mapToDouble() post that we have flatMap() we discussed.
[01:17] So you can keep scrolling inside this class.
[01:19] Wherever you see intermediate operation you can construct that as an intermediate operation.
[01:24] And similarly if you are looking for terminal operation you will be able to identify that on top of
[01:29] the method name
[01:30] like forEach() you can see here we have the operation name as terminal operation.
[01:35] We are ready to discuss in detail about the terminal operations.
[01:37] We are going to do that in the coming lectures.
[01:39] For now, I just wanted to give this tip for you so that you are empowered with these information in
[01:44] future
[01:45] if you are trying to use some operation which we have not discussed inside this course, by following
[01:49] the tips that I have shared, you should be able to easily use them.
[01:53] I hope this makes sense.
[01:55] Now inside this lecture I want to share you one important information about the Stream objects.
[02:01] Whenever we are using a Stream object to process the elements inside it, we can only traverse just
[02:10] once.
[02:10] So when I say traverse, we can only iterate the elements, or we can only loop the elements inside
[02:18] the Stream object only once.
[02:20] Once the traversing of all the elements is done, you can't use the same Stream object again to perform
[02:26] one more traversing or one more iteration.
[02:29] Let me share more details around this. Like you can see here
[02:32] first, I have a List object.
[02:33] From this List object, I tried to get a Stream object by invoking the stream() method.
[02:38] I have given the Stream object name as department stream, so using these depStream, I'm trying
[02:43] to invoke the terminal operation directly without any intermediate operation.
[02:48] So what is the terminal operation I'm using here forEach() ?
[02:51] So at this first terminal operation I'm not going to get any exception.
[02:55] But in the last line, if you see I'm trying to invoke another terminal operation with the help of the
[03:01] same Stream object which is depStream in this kind of scenario, like I said, it is not possible
[03:07] to traverse the elements one more time by using the same Stream object.
[03:12] So you're not going to get any compilation errors.
[03:14] You are going to get a runtime surprise in the form of IllegalStateException.
[03:20] So you'll get a IllegalStateException
[03:22] with the message stream has already been operated upon or closed.
[03:27] That's why
[03:27] please make sure you are traversing the Stream object only once.
[03:31] Let's see the demo of this very quickly inside Intellij.
[03:33] Inside my IntelliJ, I'm going to create a new Java class with the name StreamTraverseDemo.
[03:41] Here
[03:42] first I'm going to create the main() method post that I want to create a List object with the department
[03:47] names.
[03:47] We already have such list here inside the StreamMapOperationDemo class.
[03:52] So let me copy these lines of code and paste it inside the class that we have created, which is
[03:59] StreamTraverseDemo.
[04:00] So here inside this main() method I'm trying to paste, once this code is pasted with the help of my List
[04:07] object name, I'm trying to invoke the stream() method, and the output from the stream() method is going
[04:12] to be a Stream object, which is capable of processing String objects.
[04:16] So I'll give the variable name as departmentStream.
[04:20] Now using this departmentStream, I'm trying to invoke the terminal operation, which is forEach() post
[04:26] this I'm going to pass the logic to the forEach() which is System.out::println().
[04:34] So if I execute this, my Java will be happy and I'm getting the proper output.
[04:39] But if I try to repeat this line one more time, this time I'm going to get a runtime exception saying
[04:45] that IllegalStateException stream has already been operated upon or closed.
[04:50] I hope this makes sense to you, but here you may have a question which is,
[04:54] in the many places we try to invoke multiple operations like skip(), limit() and for each based upon
[04:59] the same Stream object.
[05:01] This can be your question, but here
[05:02] to clarify your question, I want to reiterate the basics of streams one more time.
[05:07] So any intermediate operation that you're going to perform inside streams API, it is always going to
[05:13] give you a new Stream object.
[05:16] By the time they skip() operation is completed, I'm going to get a new Stream object based upon the same
[05:21] new Stream object.
[05:22] We are trying to invoke the another intermediate operation, and this limit() is again going to give me
[05:28] another new Stream object.
[05:29] And using the another new Stream object at the end, I'm trying to invoke the terminal operation.
[05:35] So here know where we are trying to use the same stream object to traverse multiple times.
[05:41] That's why we're not getting any compilation error.
[05:44] I hope you are clear how the streams traversing they are going to work, and what is going to happen
[05:49] if you try to traverse the same Stream object multiple times?
[05:52] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
