# 26.6 — Introduction to Streams Pipeline

> Section 26: [JAVA 8] Streams API

[00:00] As of now, we know how to create a Stream object from the Source collection data structure object.
[00:07] The very next obvious step is to process the elements with the help of stream API methods, by providing
[00:13] the business logic in the form of lambda expressions.
[00:16] So whenever you want to process your collection object elements with the help of streams API, there
[00:21] are three important steps that you need to take care.
[00:24] Using these three important steps, you are going to build a streams pipeline.
[00:29] So what is the streams pipeline?
[00:31] Let's try to understand the same inside this lecture.
[00:33] Like I said before, whenever we want to work with streams, we need to set up a stream pipeline with
[00:39] three different stages.
[00:40] The very first stage is to create a Stream object from the original collection data source.
[00:47] We already discussed about this in the previous lecture.
[00:50] So how to create a Stream object by invoking the stream() method or parallelStream() method, or by using
[00:55] the Streams.of() method
[00:57] or we can also use Arrays.stream() method.
[01:00] So using all these approaches, first we need to create a Stream object which is referring the elements
[01:07] present inside a original data source.
[01:09] So once the Stream object is created as part of the second stage, you can have one or more intermediate
[01:18] operations for processing the data with the help of streams or for filtering the data.
[01:23] Your business logic can be anything.
[01:25] All your business logic you're going to implement with the help of intermediate operations.
[01:31] So there are good amount of intermediate operations supported by the streams API.
[01:35] From the next lecture, I'm going to discuss most commonly used intermediate operations and how to use
[01:41] them to process that data with the help of streams API.
[01:44] So all the exciting concept we are going to discuss from the next lecture.
[01:48] For now, please note that the second stage is to to build one or more intermediate operations to process
[01:54] the elements with your business logic, and at last, we are going to apply a terminal operation to
[02:00] produce a result.
[02:01] So from the stage two, once all the business logic is executed, all the elements being referred inside
[02:07] your Stream object, they need to be collected into some other collection object.
[02:12] So from the original collection object, you are going to build a Stream object with the help of the
[02:18] Stream object.
[02:18] Inside the stage two, you're going to perform lot many operations to manipulate the data to filter
[02:24] the data.
[02:24] Once this manipulation of the data is completed by your streams API in the stage two, you're going
[02:30] to store the new data or new filtered data into another collection object with the help of this terminal
[02:38] operation.
[02:39] So what is this terminal operation it is going to do?
[02:41] It is going to produce a result based upon the Stream object that is generated from the stage two.
[02:47] So the combination of all these three stages we are going to call it as streams pipeline.
[02:53] So if you try to visualize the streams pipeline, this is how it is going to look like.
[02:57] We know streams are awesome.
[02:58] So what is making the streams as awesome?
[03:01] These streams pipeline.
[03:02] So in the very first step, what we are going to do, we are going to create a Stream object post that
[03:07] inside the step two, we are going to write one or more intermediate operations.
[03:12] I tried to highlight these intermediate operations in the below box so you can have one or more intermediate
[03:19] operations.
[03:20] So here I have an intermediate operation one.
[03:22] Later on it is followed by intermediate operation two followed by intermediate operation three.
[03:27] This way we can build any number of intermediate operations to process your collection data.
[03:33] So once all these intermediate operations are executed as part of step two, you're going to get a new
[03:40] Stream object which is holding the new data.
[03:44] So from the Stream object we are going to create a new collection object, which is capable of physically
[03:49] storing the new elements inside a separate memory location.
[03:53] So that's what this terminal operation is going to do.
[03:56] So always creating a Stream you're only going to do once.
[04:00] And the terminal operation also it is going to have a single operation.
[04:03] But coming to the intermediate operations it can have one or more operations because in real projects
[04:10] our business requirements will be very complex
[04:12] that's why we may have to manipulate or process the data by leveraging various intermediate operations.
[04:19] So as of now, we are good with the step one on how to create a Stream.
[04:22] From the next lecture, let's try to focus on the step two which which is how to manipulate our process
[04:28] that data inside a collection object with the help of stream API supported intermediate operations.
[04:34] I hope you are excited.
[04:35] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
