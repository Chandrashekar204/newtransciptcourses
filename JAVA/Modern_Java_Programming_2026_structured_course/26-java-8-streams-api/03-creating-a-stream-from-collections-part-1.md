# 26.3 — Creating a Stream from collections - Part 1

> Section 26: [JAVA 8] Streams API

[00:00] Inside this lecture, let's try to understand how to create a stream from a given collection object
[00:06] or from a given array.
[00:07] Creating a stream is very important, and this is the initial step that you need to follow always
[00:14] whenever you want to process the elements of a collection with the help of functional programming.
[00:19] That's why inside this lecture, we are going to put good amount of efforts in understanding how to
[00:24] create a stream from a collection object.
[00:26] Since we are into the new section, have created a new project with and
[00:30] inside this project I'm going to create a new package with the name com.eazybytes.streams.
[00:39] Since we are going to discuss everything around the streams, I have provided streams in the package
[00:43] name, so let me press enter and post that
[00:46] I'm going to create a new Java class with the name StreamCreationDemo. Inside this class
[00:54] first let me create the main() method, followed by
[00:57] first I'm going to create a collection object and inside this collection object I'm going to store various
[01:03] elements.
[01:04] We can create any kind of collection object.
[01:06] It can be an ArrayList, LinkedList or Set, or it can be a Map, or it can be a Tree.
[01:11] Regardless of whatever collection data structure that you are trying to use to store your elements,
[01:16] the process of creating the stream is always going to be the same.
[01:20] Here I'm going to create a List object which is capable of storing the String elements.
[01:26] I'll provide the list object name as department list on the right hand side.
[01:31] Let me create an ArrayList object.
[01:34] Now inside this department List I'm going to populate certain amount of data.
[01:39] So the very first element that I want to add here is supply.
[01:43] Supply is the department name.
[01:44] Similarly I'm going to create one more department which is HR followed by Sales.
[01:51] And after this I'm going to mention marketing as the next department name.
[01:56] So you can see as of now I have mentioned only four department names inside my department's List.
[02:01] But you can store any amount of department names inside this list for our discussion.
[02:06] This simple List object should be good enough.
[02:10] As a next step, I'm going to show you how to create a stream from the collection object.
[02:14] So this is a collection object.
[02:16] Using the same I'm going to invoke a method stream().
[02:20] So this stream() method, it is going to give a stream of elements.
[02:25] So that's why on the left hand side I need to catch the output with the help of Stream of String.
[02:32] Because since our collection object is storing the String elements, we need to create the stream also
[02:37] that is capable of storing String elements.
[02:40] Post that
[02:41] I'm going to give a name to this which is departmentStream.
[02:45] So these are variable name that I have given here.
[02:47] Once the stream is created, you can start invoking various methods available inside the stream API.
[02:54] And to this method you you can provide your lambda expressions based upon the functional programming
[02:59] style.
[02:59] For example, if you have a requirement to iterate all these elements and display them onto the console,
[03:05] you don't have to worry much.
[03:06] You don't have to write big for loops or while loops, or you don't have to call the iterator.
[03:12] With the help of these departmentStream, you can simply invoke one of the method which is forEach()
[03:18] and to this
[03:19] forEach(), we need to pass the lambda expression that built based upon the Consumer functional interface.
[03:26] So what is a Consumer function interface is going to do.
[03:29] It is going to accept an input but it is not going to return anything.
[03:33] So here since my requirement is to print each and every element, I'm going to accept an input parameter
[03:39] with the name department.
[03:41] After this parameter name, I'm going to mention arrow symbol, followed by
[03:45] I'm going to mention System.out.println().
[03:47] And to this I'm going to provide department as an input.
[03:51] You can see with the single line of code we are able to iterate all the elements.
[03:55] If I execute this program, you'll be able to see all the department names on the console.
[04:01] Here we can also do a better job.
[04:03] Instead of writing these lambda expression manually, we can leverage the method reference.
[04:08] So what is the method reference format that we need to use?
[04:10] First we need to type System followed by out followed by two colons followed by println().
[04:17] With that we are going to get the same behavior.
[04:20] Like you can see here, we are displaying all the department names, each and every collection object
[04:25] that you are going to create inside your project.
[04:27] They all have these three methods.
[04:29] So these are default method available inside the collection interface.
[04:34] We just have to invoke this method.
[04:36] And on the left hand side we are going to get a Stream object.
[04:40] Once the Stream object is available we can perform various kind of operations which we are going to
[04:45] discuss in the coming lectures.
[04:47] So this is one approach.
[04:49] The other approach to create the Stream object is, you can directly invoke the Stream class, which is
[04:55] the parent class for all the stream API related
[04:59] classes and interfaces.
[05:01] You can see this Stream.java is available inside the package java.util.stream.
[05:08] So you can construct this as the parent for all the classes available inside the stream API.
[05:14] So using this class you can invoke one of the static method which is of().
[05:19] To this of() method, you can pass any amount of elements as an input.
[05:25] For example, I can try to pass elements like Eazy followed by Bytes.
[05:30] So these are all the String objects followed by Java.
[05:34] So these are the three String objects that I'm trying to consider to create my Stream object.
[05:39] So on the left hand side we need to catch the output with the help of Stream of string.
[05:45] And here the variable name I'm going to mention inStream.
[05:49] So in indicates input.
[05:51] So this is the variable name.
[05:52] You can give any name
[05:53] it's up to you what you want to give.
[05:55] Now using this inStream I can invoke the forEach() and to this forEach() I can pass this method reference
[06:01] as an input which is System.out.println().
[06:04] So if I execute this you'll be able to see EazyBytes and Java on the console.
[06:09] So Stream.of() is another approach that we are going to follow to create a Stream object.
[06:15] After this I want to explain about one of the beautiful concept inside the stream API, which is
[06:22] ParallelStream.
[06:22] We know all our modern day laptops or modern day servers.
[06:26] They are going to have multiple cores multi-cores like octa core.
[06:30] So when you run your program with a normal stream, all your elements are going to be processed sequentially
[06:37] one by one with one of the processor.
[06:40] With that, all your remaining processes, they are going to sit idle.
[06:45] That's why if you have a business requirement to process your elements parallelly, with the help of
[06:50] all the process available inside a laptop or inside a server, you can achieve that very easily without
[06:57] streams API.
[06:58] If you want to achieve the same parallel kind of behavior, it is going to be very complex job because
[07:04] you need to write a code with the help of multi threading concept.
[07:07] Instead of doing all that, what you can do is instead of invoking the stream() method, you can invoke
[07:13] the parallelStream() method.
[07:15] So here I'm trying to type parallel
[07:18] and you can see there is a method with the name parallelStream().
[07:22] When you invoke this method, you're also going to get a Stream object which is capable of processing
[07:28] all your elements parallelly by leveraging all the processors available inside your system.
[07:34] So here I can mention the name as parallelStream, and the same I can use here and iterate all the
[07:41] elements.
[07:41] So let me execute this program.
[07:43] Here you can see the order it printed is different.
[07:46] Like first Sales came into picture next to Marketing, next to HR, next to Supply.
[07:51] Whereas here all the elements they are processed in a sequential manner inside List like first Supply,
[07:57] next HR, next Sales and next Marketing.
[08:00] In this scenario, the order of the elements maintained because the normal stream it is going to process
[08:07] the elements sequentially.
[08:08] But if you look here, the later output where we are trying to iterate with the help of parallel stream,
[08:13] here the elements are getting displayed randomly.
[08:17] This is because all your elements are going to be processed parallelly, and with that you're going
[08:22] to get lot of efficiency.
[08:25] If you have a business requirement where you want to process your elements with a good performance,
[08:30] then you can always look for these parallel stream approach.
[08:33] We are going to discuss in detail about the parallel stream in the coming lectures.
[08:37] For now, I just wanted to give you a simple demo.
[08:40] There are more details that we need to discuss around the creation of Stream objects.
[08:44] So let's continue this discussion in the next lecture as well.
[08:48] Thank you,
[08:48] bye.

----------------------------------------
