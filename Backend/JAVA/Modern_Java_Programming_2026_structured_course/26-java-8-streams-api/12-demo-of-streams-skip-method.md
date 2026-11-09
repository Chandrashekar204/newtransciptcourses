# 26.12 — Demo of Streams skip() method

> Section 26: [JAVA 8] Streams API

[00:00] Just like we have a limit() intermediate operation.
[00:03] Very similarly, we also have skip() intermediate operation.
[00:06] We can use a skip() intermediate operation in the scenarios where we have a business logic to skip a certain
[00:12] number of elements before we try to further process the elements inside a Stream object.
[00:18] Let's try to understand how this skip is going to work. Like limit(), skip() also
[00:22] it is going to accept number of elements as an input.
[00:27] If you provide ten as an input to the skip() method, then first ten elements inside your Stream object
[00:34] or inside your collection data source object, they are all going to be skipped and only the remaining
[00:40] elements they are going to be processed.
[00:43] Here I have an example where with the help of iterate, I'm trying to generate the infinite number of
[00:49] elements where each element it is going to be derived based upon the previous element by adding one.
[00:56] But I'm trying to start with the initial seed value, which is one.
[00:59] So the output is going to be one, two, three, four.
[01:02] So this way I'm going to have a infinite stream.
[01:05] By using these infinite stream objects, I'm trying to invoke the skip() method.
[01:10] And to this skip() method I'm trying to pass the input as five.
[01:13] With that first five elements will be skipped.
[01:16] Like you can see here
[01:17] initially my input stream has infinite number of elements.
[01:21] Was that the skip() operation,
[01:23] it is skipping the first five elements, and with that we get a new stream, which is going to start
[01:28] from six and it is going to keep on continue infinitely.
[01:32] But since we don't want to process the infinite stream, I also use the limit after the escape.
[01:38] With the help of limit(), I limited the processing of elements up to five.
[01:42] That's why after this limit() operation is executed, I'm going to get the output stream which is six,
[01:48] seven, eight, nine, ten.
[01:50] Using this output stream, I'm going to invoke the terminal operation, which is forEach(), which will
[01:55] help me to print the elements like six, seven, eight, nine, ten onto the console.
[02:00] With this discussion, I am assuming you also understand a point which is limit() and skip() are complementary
[02:08] to each other.
[02:08] They are going to do the exact opposite behavior.
[02:13] So with the skip() you're going to completely skip the elements, whereas with the limit() you're going
[02:18] to process only the limited number of elements.
[02:21] So let's see the demo of this skip() method inside IntelliJ.
[02:25] First I'm going to create a new Java class with the name stream SkipOperationDemo.
[02:32] So let me remove this limit() and mention skip() here and post that
[02:36] I'm going to create a main() method inside the main() method
[02:40] with the help of Stream.iterate(), I'm going to generate an infinite stream.
[02:45] So to this iterate()
[02:46] first we need to provide what is the initial seed value.
[02:49] So I'm trying to mention initial value as one, followed by I will provide the lambda expression, which
[02:54] is going to take n as an input, and it is going to add plus one and return the same.
[03:00] So this is my lambda expression.
[03:01] So we know this code is going to give us an infinite stream.
[03:05] But we want to invoke the intermediate operation skip().
[03:09] And to this skip() I'm trying to pass the output as five.
[03:12] Post this I want to invoke the limit() method, to this method()
[03:16] also, I'm going to pass the input as five and at last I'm going to invoke the terminal operation.
[03:21] To this terminal operation I'm going to pass a lambda expression with the help of method reference.
[03:27] So if I execute this program, I'm going to get the output as 6, 7, 8, 9, 10
[03:32] like we discussed.
[03:33] I hope you are clear with this discussion.
[03:35] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
