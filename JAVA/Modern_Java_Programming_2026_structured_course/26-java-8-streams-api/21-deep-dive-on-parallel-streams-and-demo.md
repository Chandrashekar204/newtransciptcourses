# 26.21 — Deep dive on parallel streams and demo

> Section 26: [JAVA 8] Streams API

[00:00] I'm going to show you a few funny images around the multitasking.
[00:04] So these are very first funny image where the term it is trying to do the multitasking to play all the
[00:12] instruments by himself.
[00:14] Let's see the next image.
[00:16] Here you can see a robot is trying to perform multiple activities parallelly like it is trying to perform
[00:23] cleaning, washing, ironing so everything it is trying to perform at once.
[00:28] In the similar lines, we also have this image where this child is trying to play two different games
[00:35] at the same time.
[00:36] Let me show you one more image here
[00:38] this lady, she's trying to perform two different tasks.
[00:41] One is cleaning the house and the other one is doing the physical activity.
[00:45] And at last this is the image which shows a mother she's struggling with the multitask or the activities
[00:52] that she has on day to day basis.
[00:54] The reason why I'm showing you all these images right now is, just like how we prefer sometimes multitasking
[01:00] in real life.
[01:01] Very similarly, while you're trying to process your data or while you're trying to process your elements
[01:07] inside a collection object, sometimes you prefer them processing them parallelly with the help of streams
[01:13] API, it is going to be super easy to process the elements parallelly.
[01:17] So let's try to understand the same inside this lecture.
[01:20] Whenever we want to create a Stream object from the collection data source, we can invoke the stream()
[01:27] default method to create a normal Stream object.
[01:30] But if you are looking to process the elements inside your stream parallelly, you just have to invoke
[01:36] the parallelStream() method available inside the stream API.
[01:40] So what is going to happen with these parallelStream()?
[01:43] All your elements
[01:44] they are going to be processed parallelly or concurrently using multiple threads.
[01:50] All the modern laptops and the servers that we have these days, they are built with multi processors.
[01:57] So long back in 1990s when the laptop or the computer is invented very first time, they only have a
[02:03] single processor.
[02:04] And using these single processors, we used to process the data sequentially one by one.
[02:10] But now with the advancements happened, even the basic laptop these days, it is coming with the four
[02:16] different processors and it can go to 8 to 12, 16 processors.
[02:20] So instead of running your program with a single processor and with a single thread, if you try to
[02:26] run it with the multiple processors and with the multiple threads, your program is going to execute
[02:32] very quickly, which means the performance of your program is going to be improved.
[02:37] Think like you have 1 million elements inside a collection object.
[02:42] If you start processing all of them one by one, sequentially, with a single thread, or with a single
[02:47] process, it may take 10 minutes or 5 minutes.
[02:50] But if the same activity if you can perform with the help of parallel stream, the entire activity is
[02:57] going to be completed within one minute or 30s.
[03:01] So that's how powerful the parallel stream is, but not in all the scenarios
[03:05] we can use parallel stream. Only in the scenarios where your business logic is not going to be impacted,
[03:11] even if the elements are processed independently.
[03:14] In such scenarios, you can use the parallel stream processing.
[03:18] So how to activate the parallel stream processing.
[03:21] So based upon your collection object you just have to invoke the parallelStream() default method.
[03:26] So whenever we are making our Stream object as a parallelStream object behind the scenes, all the
[03:32] elements that are going to be splitted into multiple chunks.
[03:36] Each chunk is going to be processed with a different thread.
[03:39] So behind the scenes, all this complexity of dividing the elements into various chunks and handing
[03:45] over all these chunks to various threads and various processors, everything is going to be taken care
[03:50] by the stream API
[03:51] behind the scenes.
[03:52] Before this Lambdas and Streams API, which are introduced in Java 8 people.
[03:57] They have to struggle a lot to process their data.
[04:00] Parallelly with the multiple threads.
[04:03] So they have to manually program all this.
[04:05] But with the streams API, this job has been become very easy.
[04:09] That's why these days you will not see lot many developers building the multi-threading programming
[04:14] because there is no need of building multi threading programming, since the same can be achieved very
[04:19] easily by the parallelStream() method.
[04:21] So all the responsibility of processing your elements parallelly is going to be taken care by the JDK
[04:28] libraries.
[04:29] So here I have an example.
[04:31] So you can see first I have an List object which has various department details.
[04:36] So if I want to convert these List object as a parallel stream, I just have to invoke the
[04:42] parallelStream() method.
[04:43] For that I can invoke any intermediate operation or terminal operation.
[04:47] So with this code, all the elements inside my parallelStream object, they are going to be processed
[04:53] parallelly or concurrently.
[04:55] Apart from parallelStream() method, we also have a parallel() method available
[05:00] inside the stream API.
[05:01] Think like you first created a normal Stream object and you applied some operations which are going
[05:07] to be executed sequentially.
[05:09] All these intermediate operations, they are going to give you a new stream.
[05:13] So this stream, which is still a normal stream, can be converted into a parallel stream by just invoking
[05:20] these parallel() method.
[05:22] So this parallel() method you can only invoke with the help of Stream object, whereas the parallelStream()
[05:27] method can be invoked only by using the collection data source objects.
[05:31] I hope this makes sense.
[05:33] You can also process the elements with a combination of normal stream and a parallelStream as well.
[05:38] Like you can see here, I have an example.
[05:40] First, I'm trying to invoke the stream() method and try to run this filter() operation.
[05:46] So this first operation it is going to run sequentially.
[05:51] After this intermediate operation, we know we are going to get a new Stream object on top of the same
[05:56] new Stream object
[05:57] I'm trying to invoke the parallel() method, which is going to convert that normal Stream object into
[06:02] a parallelStream object.
[06:03] After this parallel, I'm trying to invoke one more map() and collect() operations.
[06:08] So both these two operations like map() and collect(), they are going to be processed in parallel.
[06:14] So this way we can always based upon our business logic
[06:17] for certain operations we can use the normal stream, whereas for other operations we can use the parallel
[06:24] stream.
[06:25] I know as of now we just discussed about the parallel stream on a high level.
[06:29] Let me show you a demo so that you're going to appreciate the advantages that these parallelStream
[06:35] is bringing to the developers.
[06:36] Inside my IntelliJ, I'm going to create a new Java class with the name ParallelStreamDemo to show
[06:44] you the benefits of ParallelStream
[06:46] first, what I'm going to do is inside my main() method, I'm going to generate a stream which is capable
[06:52] of storing 100 different int elements.
[06:55] So instead of manually creating a list of 100 different int elements, what I can do is, I can use the
[07:02] iterate() method available inside the stream
[07:04] to this iterate() the initial seed I'm going to mention as one, followed by I'll provide a lambda expression,
[07:10] which is num lambda symbol, followed by to the same num
[07:15] I'm going to add one every time.
[07:17] So with that, I'm going to get a infinite stream of int elements, which are going to be keep incremented
[07:24] by one value.
[07:25] But I don't want to have a infinite stream.
[07:27] That's why what I'm going to do is I'll limit the output to 100 elements.
[07:32] So what we are going to get as an output from this limit() operation, we are going to get another stream()
[07:37] object, which I'm going to catch on the left hand side with the stream of integer and with the Stream
[07:45] object name as num stream.
[07:48] So here you can see in this line what I'm doing is I just created a stream which is going to hold 100
[07:54] different elements like right from 1 to 100.
[07:57] Now using these normal stream(), I'm going to process all these 100 elements post that
[08:03] I'll also try to convert the parallelStream, and I'll try to compare that time taken by both these
[08:08] streams to process these 100 elements.
[08:10] So first here using these numStream, let me invoke the map() method.
[08:15] So inside this map() method I just wanted to write a lambda expression which is going to accept an input
[08:21] parameter of with the variable name as num followed by
[08:25] inside the method body
[08:26] I'm going to simply multiply the number by two.
[08:29] So the output from these multiplication I'm going to return as an output from my lambda expression.
[08:35] After this, I will try to collect the output using the collect terminal operation and by using
[08:43] Collect.toList().
[08:44] So basically from these operation I'm going to get a list object which I will try to print out with
[08:50] the help of System.out.println().
[08:52] So I can move all this entire code as an input to the println().
[08:56] So if I try to execute this simple code, I will not be able to see much difference.
[09:01] The reason is this is a very simple operation, and we have very limited number of elements to show
[09:07] you the
[09:07] real advantages of parallel processing.
[09:10] I'm going to create an intentional delay inside my map() method.
[09:15] So how to create an intentional delay inside Java program.
[09:19] So there is a class with the name Thread.
[09:21] Inside this class we have a static method with the name sleep().
[09:24] To this sleep() we can pass number of milliseconds.
[09:28] We want to sleep() the thread.
[09:29] So here I want my thread to sleep for 100 milliseconds.
[09:34] Post that only it is going to process this line of code.
[09:37] So here I'm getting a compilation error because the sleep() method it is going to throw an checkered exception
[09:43] which is interrupted exception.
[09:45] So to resolve this I can try to build my lambda code with the help of try and Catch().
[09:51] So let me click on this around with the try and catch.
[09:53] And with that you can see the compilation error is resolved.
[09:56] So now we have the code ready to test with the
[09:59] normal streaming and parallel streaming, but we don't know how to calculate that time taken by this piece
[10:05] of code.
[10:05] So these lines of code that I have highlighted, I want to calculate how much time they are taking to
[10:11] execute completely for 100 different elements.
[10:14] So whenever you want to understand how much time your piece of code is going to take, you don't have
[10:20] to worry much.
[10:21] You can invoke the System.currentTimeMilliseconds() method, which is going to give you what are the
[10:28] current milliseconds just before the time where your piece of code is going to be executed.
[10:34] So here I'm going to mention this variable name as startTime.
[10:38] Very similarly I'll also invoke the currentTimeMilliseconds after this code.
[10:44] So here I'll try to mention the variable name as end time.
[10:49] And at last I'll try to have a System.out.println().
[10:52] And to this I'll pass the output from the difference of end time and the start time.
[10:57] With that, we are going to get the total time taken by this entire code.
[11:01] So the time that we are going to get is in milliseconds, but not the seconds.
[11:05] So please make a note of it.
[11:07] So now let me try to run this program with a normal stream processing.
[11:11] And you can see it is going to take some time.
[11:15] Let's wait for this to complete.
[11:17] It took total 10,375 milliseconds.
[11:22] That means it took almost 10s to process all these elements.
[11:27] Now I'm going to convert my normal stream into a parallel stream.
[11:32] So how to convert that?
[11:33] We just have to invoke the parallel() method after these iterate() operation.
[11:39] So with this parallel() method I have converted the normal stream into a parallel stream.
[11:45] So this time if I try to execute this program, you'll be able to see the output we are getting only
[11:52] in 1062 seconds did you see where is 10,000 and where is 1000?
[11:57] Such a drastic improvement we are getting with the help of parallel processing.
[12:02] So always whenever you have a heavy logic that needs to be executed on a good amount of elements, try
[12:08] to give preference to the parallel processing with the help of parallel stream method.
[12:13] So here I'm trying to invoke the parallel() method because I'm going to get a Stream object.
[12:18] But if you have a collection object, you can simply invoke the parallelStream() method to get a stream
[12:24] that is capable of processing the elements
[12:26] parallelly, let me try to run this program one more time, but this time I'll try to reduce the sleep
[12:31] time to ten milliseconds only.
[12:33] So if I try to execute as a normal stream by removing these parallel first, you're going to see the
[12:40] total time that it is taking is, 1209 like 1.2 seconds.
[12:45] This time I'll try to bring back my parallel, and if I try to execute this, you'll be able to see
[12:51] that I'm getting the output within one 32 milliseconds.
[12:55] Such such a drastic improvement.
[12:57] As a developer, I don't even have to worry about how to create multithread how to interact with all
[13:02] the processors inside my system.
[13:04] I don't have to take all that headache as a developer, I just have to decide if my business logic supports
[13:10] parallel processing.
[13:11] If yes, please invoke the parallelStream() or parallel() methods.
[13:15] It just as such a simple task that that's why these days no one is building the programs by giving low
[13:21] level instructions around the multithreading.
[13:24] I hope you are clear and happy with these output.
[13:26] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
