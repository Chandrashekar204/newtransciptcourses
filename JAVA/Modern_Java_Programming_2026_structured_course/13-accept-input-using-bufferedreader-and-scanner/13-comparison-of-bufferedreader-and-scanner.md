# 13.13 — Comparison of BufferedReader and Scanner

> Section 13: Accept input using BufferedReader and Scanner

[00:00] Let's try to understand the differences between BufferReader and Scanner approaches.
[00:05] Most of these differences we already discussed in the previous lectures, but there is no harm in revising
[00:11] one more time.
[00:12] The very first difference is whenever you are trying to use a BufferReader, it is only capable of
[00:17] reading the sequence of characters in a String format.
[00:20] Once the reading operation is completed, it is going to be the responsibility of the developer to convert
[00:26] that String object data into an corresponding output format like int, double, float based upon the business
[00:34] requirements of the developer.
[00:35] Whereas with the scanner we have various methods which are going to start with a prefix and next.
[00:42] So based upon the type of input data that we are trying to accept, we can invoke these next methods
[00:48] to get the output in various formats like int, short, byte, float, long, double, String, boolean.
[00:55] So please use them based upon your business requirements.
[00:58] The second difference, like you know, BufferReader is present inside the Java right from day one,
[01:05] whereas Scanner is introduced only from the JDK 1.5 release.
[01:11] So why Java team release Scanner?
[01:13] Since there are some drawbacks, and since there is some complexity in using BufferReader, they want
[01:19] to make the life of developers easy.
[01:21] That's why they have introduced Scanner under the java.util package as part of the 1.5 version.
[01:28] The next major difference that we have is BufferReader
[01:31] has a capability to hold the large buffer size, which is by default eight kilobytes, whereas
[01:38] with the Scanner the buffer size is going to be only 1kb.
[01:43] Apart from these buffer size differences, BufferReader allows you to customize this buffer size based
[01:49] upon your business requirements.
[01:51] If these 8kb is not sufficient, you can try to create the object of BufferReader with a buffer
[01:57] size of 16 kb or any amount of large buffer size, and the other side the Scanner.
[02:03] It is not going to provide you that flexibility.
[02:06] It is always going to allow you to create an object of Scanner with the default buffer size, which
[02:12] is 1kb.
[02:13] With these differences, it should be pretty clear for you when you are dealing with the large amount
[02:18] of data, like you're trying to read the data from a huge file.
[02:22] In such scenarios, the BufferReader is the most suitable one compared to the Scanner, because BufferReader
[02:28] at a time, it can load the data of around 8kb, whereas Scanner is only capable of
[02:36] 1kb.
[02:36] So due to these size differences, Scanner always has a disadvantage whenever you are trying to deal
[02:42] with the large files or large input data, whereas for a short input data or a small input files, you
[02:50] can happily use Scanner and there won't be any performance issue.
[02:54] The next difference is around the synchronization.
[02:57] Inside Java, there is a concept of multithreading.
[03:00] We are going to discuss in the coming sections.
[03:03] What is multithreading?
[03:04] Multithreading is a concept where your program is going to be executed at a single time by multiple
[03:10] threads, or by multiple requests, which are invoked by multiple end users.
[03:15] In such scenarios, it is always safe to use BufferReader because it is a synchronized class, which
[03:22] means you can share the same BufferReader object across multiple threads.
[03:27] Whereas Scanner is not a synchronized class, you cannot share this Scanner object across multiple threads.
[03:34] So if you are developing a business logic for a multithreading environment, always consider
[03:41] BufferReader.
[03:41] The next difference we have is around the exception handling.
[03:44] BufferReader always force you to handle the IOException, either by mentioning the throws statement
[03:51] inside the method signature, or with the help of exception handling techniques, which you are going
[03:56] to discuss in the coming sections.
[03:57] Whereas scanner does not force the developer to handle the IOException, it is going to hide it and
[04:03] behind the scenes it is going to handle this exception.
[04:07] And at last we can say BufferReader is faster and efficient because it supports larger buffer size
[04:14] of 8KB and if needed we can further increase it, whereas Scanner is slower and less efficient.
[04:20] That's why always please note that if you are dealing with a small input data, you can happily use
[04:26] the Scanner.
[04:27] Whereas if you are trying to deal with the large input data like large files, like 1MB, 2MB
[04:34] files, then in such scenarios always go with the BufferReader.
[04:38] I hope you are clear with these differences.
[04:40] These differences are very important from interview perspective.
[04:44] So people can always ask you what are the differences between them and under which scenarios.
[04:49] We should use BufferReader and Scanner.
[04:51] So these kind of questions you should be able to easily answer with the discussion that we had throughout
[04:57] this lecture.
[04:58] Thank you and I'll catch you in the
[04:59] next lecture bye.

----------------------------------------
