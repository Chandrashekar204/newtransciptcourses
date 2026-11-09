# 29.7 — [JAVA 24] Introduction to Stream Gatherers API

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] Java 24 is released in March 2025. As part of this new release,
[00:06] a new feature with the name Stream Gatherers is released.
[00:10] This gatherers feature,
[00:11] It is going to bring a complete new API into already existing stream API. Before Java 24,
[00:18] Inside Java, we use streams to process data while processing the data with the help of streams.
[00:25] We're also using some intermediate operations like filtering, mapping along with the terminal operations
[00:31] like collecting.
[00:32] But until now, developers they can only use predefined intermediate operations like map(), filter() and
[00:40] flatMap().
[00:41] But with the help of these gatherers API developers, they can define their own custom intermediate
[00:49] operations.
[00:50] This is how any developer is going to process the data with the help of streams API to use the streams
[00:56] API
[00:57] definitely the developers
[00:58] they have to use Lambda expressions as well.
[01:00] Let's try to revise for a few seconds how a data can be processed with the help of Java streams.
[01:06] As a very first step, a stream object has to be created.
[01:10] The stream that is going to be created as part of the step one.
[01:13] It is going to represent some source data.
[01:16] It can be a list of elements, or it can be a set of elements.
[01:20] Once we created a stream object as part of the step two, we are going to invoke one or more intermediate
[01:27] operations. Streams API
[01:29] it is going to allow us to define any number of intermediate operations.
[01:33] The very first intermediate operation can be a map() followed by a filter(), and the third intermediate
[01:40] operation can be a flatMap().
[01:42] So this way you can use any number of intermediate operations while you are processing the data.
[01:49] Once you are happy with the output of the intermediate operations as a step three, you need to invoke
[01:54] a terminal operation so that whatever data that is processed with the help of streams API, the same
[02:00] can be cached inside an list or inside a variable.
[02:04] It is also possible to completely skip the step two, which means we can directly call a terminal operation
[02:11] from a stream object without having any intermediate operation.
[02:14] So this intermediate operation is completely optional.
[02:18] When you are using the intermediate operation, you also have an option to use any number of intermediate
[02:23] operations.
[02:24] The Stream Gatherers API that you are going to discuss, it is going to allow you to define your own
[02:30] intermediate operation.
[02:32] This API has opened new options for the developers.
[02:36] If someone is asking what is a gatherer?
[02:38] We can say in simple words, a gatherer is a component that takes items from a stream, followed by
[02:45] it is going to transform our filters them like map() or filter(), based upon the business logic that developer
[02:52] has defined with the help of gatherer implementation, once the elements are transformed are processed,
[02:59] the same elements can be passed to the next step in the pipeline.
[03:04] This entire setup we call it as Stream Pipeline.
[03:07] A stream pipeline it is going to consist creating a stream, intermediate operations and terminal operation.
[03:14] Since we are going to define our own intermediate operation with the help of gatherers API, under the
[03:19] step two, the data for our gatherers API can come from the stream object, or
[03:25] it is also possible that data to our gatherer API can come from the another intermediate operation.
[03:31] For example, if I define my own intermediate operation, which I'm going to build with the gatherers
[03:37] API as part of this intermediate operation 2
[03:40] then in this scenario, my gatherers API, it is going to receive the Data from these very first
[03:46] intermediate operation.
[03:48] Once my custom intermediate operation processed the data, it is going to push that data to the next
[03:55] intermediate operation if there is any
[03:57] otherwise, it is going to directly push the processed data to that terminal operation.
[04:02] Here
[04:03] let's try to understand some new vocabularies around the gatherers API.
[04:07] If you are building a custom intermediate operation, this custom intimate operation, it is going to
[04:14] receive the data either from the step one or from another intermediate operation, the source where
[04:20] our gatherers API is receiving the data such sources we are going to call them as upstream and wherever
[04:27] our gatherer API is pushing the data.
[04:30] Such objects, we call them as downstream.
[04:33] From these streamlined perspective, if you try to understand what will be the upstream, the upstream
[04:38] can be the stream object that we create as part of the step one.
[04:41] Or it can be another intermediate operation that we have just before our custom intermediate operation
[04:48] coming to that downstream.
[04:50] The downstream can be another intermediate operation which is present next to our custom intermediate
[04:56] operation.
[04:57] Or if there is no intermediate operation available, the downstream can be that terminal operation.
[05:03] I hope you are clear with these vocabularies.
[05:05] The same I have highlighted in this slide as well.
[05:08] What is upstream,
[05:09] what is gatherer and what is downstream?
[05:11] The gatherer API is built on two main elements a Gatherer interface.
[05:17] And we also have GatherersFactory class.
[05:19] These gatherers API is heavily inspired from the collector API that we already have inside the Java
[05:26] ecosystem.
[05:27] Here I'm trying to give an example on how to use the gatherer API.
[05:30] I know it is too early and you won't understand anything from this code, but I just want to give you
[05:35] a glimpse if something is not clear, don't worry.
[05:38] We're definitely going to discuss all these parts in detail in a few minutes.
[05:42] Inside this code, if you try to understand first, I'm trying to create a stream object with the help
[05:47] of Stream.of() and to this stream
[05:50] I'm trying to pass two strings with the name Java and Python, so this will be my upstream for my gatherer
[05:57] API.
[05:57] Whenever you want to use the gatherer API, you have to invoke gather() method that is newly introduced
[06:05] under the streams API.
[06:07] This gather() method.
[06:08] It is going to accept the implementation of your Gather interface.
[06:13] Whatever logic that you are going to write
[06:15] by implementing the Gatherer interface, it is going to represent your custom intermediate operation
[06:21] to this gather() method
[06:22] I'm trying to pass my custom intermediate operation logic. For now
[06:26] I know you're not going to understand any of this logic, but please make sure that you are clear on
[06:31] how to use the gatherer API.
[06:34] To use the gatherer API, you need to invoke a new method available inside the stream API
[06:39] with the name gather to the same, we can pass our custom intermediate operation implementation.
[06:45] Once our gatherer API process the data based upon our business logic, here it is going to push that
[06:52] data to that downstream.
[06:54] Here the downstream is this terminal operation because here we are using the two list method which is
[07:00] a terminal operation.
[07:02] If I have to compare the stream gatherers to a real life analogy, I would say this gatherers is like
[07:08] a middleman in a factory assembly line.
[07:11] The factory person he is going to checks our transforms every item before passing it to the next worker.
[07:18] Since now we have some basic understanding on Stream Gatherers API.
[07:22] As a next step, let's try to understand on how to create our own intermediate operations with the help
[07:28] of this API.

----------------------------------------
