# 26.9 — Demo of Streams flatMap() method

> Section 26: [JAVA 8] Streams API

[00:00] Let's see the demo of flatMap() intermediate operation by creating a new Java class with the name
[00:08] DreamFlatMapOperationDemo. Inside this class,
[00:12] first let me create the main() method, followed by
[00:16] I'm going to create an array of String with the variable name as arrayOfWords.
[00:22] Inside this array, I'm going to store couple of words with the name Eazy and Bytes.
[00:29] As a next step, I need to create a stream with the help of these arrayOfWords.
[00:34] So how to do that,
[00:35] it is simple.
[00:36] First we need to invoke the Arrays.stream(), which is a static method.
[00:40] To this stream we can pass the array variable name, which is arrayOfWords.
[00:45] On the left hand side
[00:46] I need to catch the output with the help of Stream of String and with the variable name as streamOfWords
[00:53] .
[00:53] So now using these streamOfWords, I'm going to write an intermediate operation with the help of map().
[01:00] So to this map() operation I'm going to send a lambda expression which is an implementation of Function
[01:06] functional interface.
[01:07] So first I'm going to accept the word as an input followed by using the same word that I have received
[01:14] I'm going to invoke the split() method, to this split() method
[01:17] the delimiter I'm trying to mention is empty space.
[01:20] So with that, each of my word is going to be converted as an array of String.
[01:26] So that's why on the left hand side, we need to catch the Stream object as stream of
[01:32] inside the angle brackets I need to mention String array.
[01:36] Now coming to the variable name I'm going to mention as streamOfLetters.
[01:40] So if I try to use these Stream object and try to invoke the terminal operation which is for each by
[01:47] mentioning System.out::println(), you'll be able to see that I'm going to get
[01:55] an Arrays object as an output.
[01:57] So if you see here I have two different arrays received. Instead of displaying these elements,
[02:01] if you try to collect these elements into some other collection data structure, with the help of collect
[02:07] terminal operation, you're going to get a List or Set object which is storing array of String elements.
[02:13] So this kind of data is not comfortable for processing it or for displaying it.
[02:19] That's why we need to flatten this data.
[02:21] So to flatten this data what we can do, we can use the same streamOfLetters and invoke the method
[02:27] which is flatMap().
[02:29] So if you see here this flat map is an intermediate operation.
[02:33] You'll be able to see here.
[02:35] This is an intermediate operation.
[02:37] We also have documentation around this.
[02:39] Feel free to read the same, but this documentation should convey the same that we have discussed in
[02:45] the previous lecture.
[02:46] So let me go back to my Main class and here to this FlatMap,
[02:50] I'm going to send a lambda expression as an input, which I'm going to build with the help of method
[02:55] reference.
[02:56] So first I'm going to mention arrays post that I'm going to mention stream() method name.
[03:01] So what is going to happen with these lambda expression inside my streamOfLetters I have two different
[03:06] arrays.
[03:07] So these two different arrays they are going to be converted as a streamOfElements.
[03:12] So that's what is going to happen behind the scenes.
[03:14] So now what I can do is, I can directly invoke these for each terminal operation after my flatMap() intermediate
[03:23] operation.
[03:23] So with that we'll be able to see a proper output on the console.
[03:28] You can see this time we have a stream of elements like E a z y B y t e s.
[03:34] So if you try to store these elements into some other collection data structure, you're going to have
[03:39] each of these chars as different elements inside your List or Set.
[03:44] I hope this makes sense to you.
[03:45] Let's see the demo of one more example that we have discussed. For the same,
[03:50] first, I need to create a model class with the name Person.
[03:54] Inside this Person class, I'm going to create a couple of fields with the name private String name,
[04:01] and the next field is private List of String and the variable name I'm going to mention as phone numbers.
[04:09] Post that by pressing the command n shortcut, I'm going to generate the constructor by using these
[04:15] two fields
[04:16] after the constructor, I'm also going to generate the getter method, because I don't have a scenario
[04:22] where I want to update the data with the help of setter method.
[04:26] So let me click on this
[04:27] okay.
[04:27] You can see I have a getter method.
[04:29] So now I can go to the StreamFlatMapOperationDemo here.
[04:33] First I'm going to build a list of Persons object.
[04:37] So let me type person inside the angle bracket followed by the variable name I'm going to mention as
[04:43] persons.
[04:44] And on the right hand side I'm going to invoke Arrays.asList() and to this as List I'm going to pass
[04:51] the Person objects that I'm going to create with the help of constructor of Person.
[04:56] So the very first person name I'm going to mention as Alice followed
[05:00] by.
[05:00] I'm going to pass a list of phone numbers with the help of arraysAsList(), and to this phone number
[05:06] list, I'm going to pass various phone numbers like one, two, three, followed by four, five, six.
[05:11] Similarly, let me create one more person as an element inside this List.
[05:16] So this time I'm going to mention the person name as Bob and this Bob phone numbers
[05:23] they are going to be seven, eight, nine, and second phone number I'm going to mention as 101, followed
[05:29] by I'm going to mention the third phone number as 112.
[05:32] You can see I have built a Persons List object which has names and their list of phone numbers.
[05:39] As a next step, I need to invoke the streams() method to create a Stream object followed by
[05:45] if I try to use a map() operation in this kind of scenario, just to get the phone numbers of all the
[05:50] persons, I'm going to get List of List as an output.
[05:54] So let's confirm the same by passing the lambda expression, which is Person:: and get phone
[06:01] numbers.
[06:01] So you can see I'm trying to use the method reference.
[06:04] Using this method reference I'm trying to fetch the phone numbers for each Person object that I have
[06:10] inside my stream.
[06:11] And at last I'll try to collect the elements that are processed by my stream with the help of collector
[06:17] terminal operation.
[06:18] To this collector terminal operation, we need to pass the input as Collectors.ToList().
[06:25] So what will be the output that we are going to get on the left hand side?
[06:28] We are going to get List of List of String.
[06:31] First, let me try to catch the output just by typing List of String and with the variable name as mapResult
[06:38] .
[06:39] So here you can see I'm getting a compilation error saying that the collect operation it is trying to
[06:43] return.
[06:44] List of List of String, but I'm trying to catch with the List of String.
[06:47] So to resolve this I just need to wrap this list of String around one more list inside the angle brackets.
[06:54] With that, the compilation error is going to be resolved.
[06:57] So now if I try to print out the elements present inside this List, which is mapResult, you'll be
[07:03] able to see the output.
[07:05] It is not going to be in a decent format.
[07:07] Inside this List I have two different elements which are of type list, so one, two, three, four,
[07:12] five, six is one list and the second list is 789101112.
[07:17] Processing are printing these kind of information is not easy.
[07:21] That's why in this kind of scenarios, we should always try to use the flatMap() instead of map() operation.
[07:27] So let me go to the Main class.
[07:29] This time I'm going to copy this code and use the flatMap() operation as an intermediate operation.
[07:37] I'm also going to rename this to flatMapResult().
[07:41] So when we are using these flatMap() operation, we need to write the lambda expression, which is going
[07:46] to give the stream as an input for my flatMap() operation.
[07:51] So first each element we are going to accept with the help of person variable name followed by lambda
[07:57] symbol, and after that using the same Person object reference
[08:01] I'm going to invoke the get phone numbers, which is going to give me the list of phone numbers.
[08:05] So on top of this list of phone numbers, I want to invoke the Stream object so that my flatMap() can
[08:10] flatten the data.
[08:11] So now you can see I'm getting a different compilation error, which is saying that my collector terminal
[08:16] operation, it is trying to provide me List of String, but I'm trying to catch List of List of String.
[08:21] So to resolve this we just have to remove the outer List.
[08:24] And with that the compilation error is going to be resolved.
[08:27] Now, if I try to print out this flatMapResult() with the help of System.out.println(), you're going
[08:32] to see a single list with all the phone numbers like 123, 456, 789, 101, 112.
[08:39] I hope you are clear about the purpose of flatMap() operation, so always use these flatMap() operation
[08:45] whenever you are getting a data in a format of one to many based upon your intermediate operation.
[08:52] Just like how we have map() and flatMap(), we also have other similar methods inside the Stream.
[08:59] Like you can see there is a mapToInt() method, mapToLong(), mapToDouble().
[09:04] Similarly we have flatMapToInt(), flatMapToDouble(), flatMapToLong().
[09:08] So the purpose of these methods are
[09:10] if you are ever into a scenario where you are expecting an IntStream, like if you see here it is
[09:17] mentioned as map to int, that means you are going to get IntStream as an return type.
[09:22] So in these kind of scenarios you can use these specific map and the flatMap() method.
[09:27] So if you try to observe closely that these method it is accepting and function interface which is of
[09:33] type ToIntFunction.
[09:34] So what is this functional interface.
[09:36] It is going to accept any type as an input, but it is going to return int as an output.
[09:42] So whenever you have these kind of requirements where you are expecting int as an output, long as an
[09:47] output double, you can use these mapToLong, mapToDouble.
[09:51] And similarly we have flat map to int flatMapToLong, flatMapToDouble.
[09:55] I hope this all makes sense to you.
[09:56] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
