# 29.15 — [JAVA 24] fold(),scan(),mapConcurrent() methods in Gatherers

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] Inside Stream Gatherers API, there is a utility class with the name Gatherers.
[00:06] This is very similar to collectors class inside collector API.
[00:11] Just like how Collectors class provides some factory methods or utility methods to perform some terminal
[00:17] operation very similarly
[00:18] this Gatherers class
[00:20] It is having five factory methods with the name fold(), scan(), mapConcurrent(), windowFixed() and
[00:27] windowSliding().
[00:28] By using these factory methods
[00:30] if your business scenario is matching with the logic that these methods are going to handle, then you
[00:36] can happily use these factory methods instead of writing your own intermediate operation with the help
[00:42] of Gatherer API from scratch.
[00:44] As of now, this class has only these five methods, but I'm assuming this list is going to grow in
[00:51] the future versions based upon the recommendations from the developer community.
[00:56] Let's try to understand the purpose of each of these methods, under which scenarios we can use them
[01:01] instead of writing the Gatherer API implementation from scratch.
[01:05] fold() is like a reduce() method in streams.
[01:08] This fold() is also accumulates value from a stream into a single result, but there is a difference between
[01:15] fold() and reduce().
[01:16] fold() is going to support the execution in an ordered and sequential manner.
[01:22] It is not parallel friendly.
[01:23] You need to use the fold(), especially when combining the values cannot be parallelized.
[01:28] The same points I also highlighted here.
[01:31] You need to use the fold() when you want to combine all elements into one result, and you can't use a
[01:36] combiner in order sensitive operations, and you only need a single output at the end of the stream.
[01:42] How to use the fold().
[01:43] You just have to invoke the same with the help of the Gatherers class and this fold(), it is going to
[01:49] accept two input parameters.
[01:51] The first one is going to represent the initial starting value for your fold logic, and the second
[01:57] parameter is on how to fold the elements that are receiving from the upstream.
[02:01] What is the meaning of folding?
[02:03] Folding is nothing but accumulating the values into a single value.
[02:08] Let me show you an example so that it is going to make more clear to you.
[02:12] Here I have an upstream with the elements like 10, 200,3 and 45.
[02:18] I don't want to calculate the sum of these elements.
[02:21] Instead, I want to check how many numbers are there in each element.
[02:26] And by the time I execute my entire gatherer logic, I want to display the total numbers.
[02:32] For example, this 10 has two numbers, 200 has three numbers, and this has one number, and this
[02:38] has two numbers.
[02:39] The output that I'm expecting is eight.
[02:42] Let's try to understand how to achieve the same with the help of fold() method.
[02:46] As you can see here, first, as usual I need to invoke the gatherer() method.
[02:52] To this gatherer() method, I need to assign the return type of the fold() method.
[02:56] So that's why I need to invoke gathers.fold(). To this fold() as a first parameter,
[03:01] I'm trying to pass the initial value as 0.
[03:04] The same 0 is going to act as a mutable state value inside my gatherer logic.
[03:10] Initially, this count will be zero, and this num indicates the element that you are going to receive
[03:15] from the upstream.Inside the folding logic,
[03:18] what I have defined is I'm trying to add the given count value to the number that I'm going to get by
[03:25] executing this piece of logic.
[03:27] First, I'm trying to convert the number to a string, followed by I'm trying to check the length of
[03:32] the string.
[03:32] So for the 10 I'm going to get the length as 2.
[03:35] So 0+2 will be 2.
[03:37] During the second element processing the count will be 2.
[03:41] Followed by this logic is going to return 3.
[03:44] With that, the overall count will become 5.
[03:47] 5+1 will be the calculation that is going to happen during the processing of the third element.
[03:53] And at last, while processing the last element 45, the count will be 6 to the same 6,
[03:59] It is going to append the length of 45, which will be 2.
[04:03] With this, the final outcome that we are going to get is eight.
[04:07] The same we can try to catch by invoking these findFirst() method.
[04:12] If you try to print out these total digits, you're going to get optional of 8 as an output.
[04:17] I'm not going to show you the demo of all these programs that I'm going to discuss inside this lecture,
[04:22] because all these are self-explanatory.
[04:24] In case if you are interested, you can find these examples inside the GitHub repo that I have shared.
[04:29] After the fold we have scan() method scan is like very similar to fold, but instead of producing only
[04:36] final result this scan(), it is going to emit intermediate result at each step.
[04:42] You can think this as an running total or a progressive reduction.
[04:46] Let's imagine I have an input stream that is going to hold 1, 2, 3, 4.
[04:52] I'm trying to build an output where each element is going to be calculated by adding to the previous
[04:58] element.
[04:59] This example we already discussed by building Gatherers API logic from scratch. But let's try to understand
[05:04] how to build the same with the help of scan() method.
[05:08] By the time my program executes. The first element will have 1, whereas the second element, for these
[05:15] two one will be added, which is the previous element.
[05:18] With that, this value will become 3.
[05:20] Similarly, this will become 6, followed by 10.
[05:23] As usual, first, with the help of these Stream object, I need to invoke the gather() method.
[05:29] To this gather() method, we need to assign the return type from the scan() method.
[05:34] So once you invoke this Gathers.scan().
[05:37] This scan() method is also going to accept two input parameters.
[05:40] As part of the first parameter, you need to provide what is the initial mutable state value.
[05:47] The second parameter will be a lambda expression using which you need to define your scanner logic.
[05:53] This is my lambda expression, which I'm trying to pass as a second parameter.
[05:57] As you can see here, the first parameter sum, it is going to represent the state value that my Gatherer
[06:03] API is going to use during the processing of the elements.
[06:07] The second parameter, which is next, it represents the element that is being injected from the upstream,
[06:14] Inside my lambda expression logic,
[06:16] I'm trying to simply add sum, and next the output of this addition will be returned from this lambda
[06:23] expression.
[06:24] Since a scan is going to emit the intermediate results at each step behind the scenes Gatherer API,
[06:31] It will take care of pushing the elements to the downstream.
[06:34] So here what is the downstream?
[06:36] Since I'm using these tolist as the terminal operation, this terminal operation is going to act as
[06:41] a downstream.
[06:42] That's why I need to catch the output by using List of Integer.
[06:46] If I try to print out these running sums, I'm going to get this output.
[06:50] I hope you're clear when to use fold() and scan().
[06:53] If you are looking to calculate a single result value by processing all your elements, then go for
[06:59] the fold().
[07:00] Otherwise, if you are expecting intermediate results at each step, then scan() is the ideal method.
[07:06] After the scan() we have mapConcurrent() method.
[07:10] The name itself is self-explanatory.
[07:12] This factory method is similar to map(), but for parallel streams.
[07:17] This method allows concurrent transformations perfect when you're mapping function is thread safe and
[07:25] independent.
[07:25] You need to use these mapConcurrent() whenever you want to transform many items at the same time safely
[07:32] independently.
[07:33] Make sure the mapping logic that you define with the help of this map Concurrent is Stateless,
[07:38] Thread-safe and Independent per element.
[07:41] Don't try to use this mapConcurrent().
[07:43] If your function depends on the shared state or order of the elements.
[07:48] I have an example as well on how to use these mapConcurrent().
[07:52] This example may look very lengthy and complex, but it's very easy,
[07:56] let me explain you the same.
[07:58] I have list of string. Inside this list,
[08:01] I have lengthy Strings ,as each element.
[08:05] As you can see, there are five different sentences,
[08:08] are articles present inside my source list.
[08:12] What I'm trying to achieve with the help of this program is I want to calculate number of words inside
[08:18] each article are inside the each string that I have inside my source String, and towards the end I
[08:24] want to display the word count against each article.
[08:28] This is my source list.
[08:30] Using the same,
[08:31] I'm trying to invoke the parallelStream() method.
[08:34] parallelStream() method is a shortcut.
[08:36] Instead of invoking stream.parallel(), we can directly invoke these parallelStream() method. With the
[08:42] help of this parallelStream() method,
[08:44] I'm trying to start my stream pipeline with the parallel setup.
[08:47] As we discussed previously, we should use this mapConcurrent() only when we are trying to process the
[08:52] elements parallelly.
[08:54] So that's why,
[08:55] please make sure you are marking your stream as parallel,
[08:58] when you are trying to use mapConcurrent(). From the Stream object,
[09:01] I'm trying to invoke the gather() method.
[09:03] To this gather() method,
[09:04] I need to assign the return type from the mapConcurrent() method.
[09:08] With the help of the gatherers, I'm trying to invoke the mapConcurrent() method.
[09:12] This mapConcurrent() method,
[09:13] It is going to accept two input parameter.
[09:16] The first parameter is an int value which represents what is the maximum concurrency that we want.
[09:23] Here I have defined 10.
[09:24] That means a maximum of ten different threads they are going to execute my business logic.
[09:30] As a second parameter, we need to pass a lambda expression using which we need to define our mapper
[09:35] logic.
[09:36] When I say mapper logic, this logic will have what we are trying to achieve with the element that we
[09:41] are going to receive from the upstream.
[09:43] This is a simple lambda expression with the help of this article, which is the element that is going
[09:48] to be injected from the upstream.
[09:50] Since this article is a string data type, I should be able to invoke the split()..To the split(),
[09:55] I'm trying to pass a regex expression.
[09:57] This regex expression is going to help to identify all whitespaces inside my String.
[10:03] So based upon the whitespaces, the entire String will be splitted.
[10:07] For example, Java will become one String, followed by is, followed by a all the individual words
[10:13] that are separated by space.
[10:15] They are going to be splitted and with the help of the length, I'm trying to identify how many number
[10:21] of words are there inside a given String or a given article.
[10:25] The length I'm trying to return from my lambda expression.
[10:28] The same will be pushed to the downstream by the Gatherer API behind the scenes.
[10:32] At last, as you can see, I have defined toList which is going to act as a downstream whatever int
[10:38] values that are going to be pushed by my lambda expression.
[10:40] I'm going to catch, with the help of these List of Integer.
[10:44] With the help of this for loop, I'm trying to print out what is the associated article, followed by
[10:50] how many words it has,
[10:51] by using these wordCounts.get(i).
[10:54] I have this program inside the GitHub repo.
[10:57] Please open the same and try to understand.
[10:59] Once you are clear, try to execute the program to see the overall output as well.
[11:03] Maybe I can show you the output very quickly.
[11:06] There is a Java class with the name K _ MapConcurrent.
[11:10] Whatever we have discussed in the slide, the same example is present if I execute this program.
[11:15] This is how the output is going to look like. For the Article 1 the word count is 8, followed
[11:19] by 10, 7, 10, and 11.

----------------------------------------
