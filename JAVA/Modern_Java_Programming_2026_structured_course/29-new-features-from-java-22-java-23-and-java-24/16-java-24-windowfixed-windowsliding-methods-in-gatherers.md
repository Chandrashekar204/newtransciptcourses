# 29.16 — [JAVA 24] windowFixed, windowSliding methods in Gatherers

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] So far, we discussed three methods inside Gatherers with the name folder map and scan,
[00:05] very similarly, we have window fixed and a window sliding as well.
[00:10] Let's try to understand more details around the same.
[00:12] With the help of window fixed, we can split a stream into fixed-size chunks.
[00:18] Inside software industry there is a concept called windowing or window.
[00:23] It is nothing but splitting your input into a fixed size chunks. All these days,
[00:29] Implement these window fixed inside Java developers, they have to write a lot of logic, but wit
[00:35] the help of this method, it is going to be super easy.
[00:37] This window fixed() method,
[00:39] It is going to accept an int as an input based upon the int value that you have provided.
[00:45] Accordingly, the chunking of the input stream is going to happen .Here,
[00:50] there is a simple example where I have a stream of six int values.
[00:55] With the help of this stream object I'm trying to invoke.
[00:58] Gather. To this gather,
[01:00] I'm trying to assign the return type from the Gatherers. window fixed and to this window fixed,
[01:05] I'm trying to assign a int value 2 and towards the end I'm trying to invoke two list terminal operation.
[01:12] If I try to print the output, this is how it is going to look like.
[01:16] I'm going to get a list inside this,
[01:18] I'm going to have a few more lists with each list size as two.
[01:22] In case if you have one more element, you're going to have one more last list, which a single element
[01:28] as seven.
[01:29] I'm expecting lot of developers they are going to leverage this method to a great extent inside their
[01:34] real applications, especially while performing API batching, parallel processing chunks, database
[01:41] insert, batching, pagination,
[01:43] In all these scenarios where you need to chunk the input, we can happily use window fixed. In the similar
[01:50] lines,
[01:51] we also have window sliding() method as well.
[01:55] With the help of this method, we can create a overlapping or moving windows of elements.
[02:02] Unlike window fixed, it does not drop elements.
[02:05] It slides the window by step. this window sliding,
[02:08] also it is going to accept an input int value.
[02:12] So here I have mentioned 2.
[02:13] That's why all the elements inside my upstream they are chunked into list with the size of each two.
[02:21] But the beauty of window sliding is when it is trying to perform a chunk, it is going to move the elements
[02:27] one by one onto the right hand side.
[02:29] So first we have these one two.
[02:31] That's why we got this followed by it will move by one step from to.
[02:36] It will try to calculate a new chunk which will be two three.
[02:39] Next it is going to move by one step.
[02:41] And with that this time three and four will be the new set.
[02:46] So this will continue until it reaches the last element.
[02:49] And this is how the output is going to look like.
[02:52] The real use cases of windows sliding are calculating,
[02:55] Moving averages are rolling statistics.
[02:58] We can also detect anomalies in overlapping data windows with the help of these windows
[03:04] Sliding.
[03:04] I hope you are clear with all the five methods available.
[03:07] Gatherer's class.
[03:09] Overall, I see right now the stream API become even more better with the help of the Stream Gatherers
[03:15] API.
[03:16] Now the developers has flexibility to build their own intermediate operations .For simple use cases,
[03:23] don't try to build your own intermediate operation because that is not required.
[03:27] We have enough intermediate operations like map, filter, flat and so on.
[03:32] If your problem is unique and it cannot be solved by the existing intermediate operations, then you
[03:37] can happily build your own intermediate operation with the help of Gatherer API.


########################################
