# 26.8 — Introduction to Streams flatMap() method

> Section 26: [JAVA 8] Streams API

[00:00] Inside this lecture, let's talk about another important intermediate operation which is flatMap().
[00:06] Understanding flatMap() is complex compared to the map() operation.
[00:11] That's why I'm not going to explain about the definition.
[00:14] First, I'll straight away try to discuss an example.
[00:17] Once we are clear about the example, we can try to understand the definition of flatMap().
[00:21] Like you can see here
[00:22] I have a code snippet, and after this code snippet, I also have an image explaining the steps that
[00:28] will happen behind the scenes.
[00:30] So first I have an arrayOfWords.
[00:32] So this is just an array which is holding two different words like Easy and Bytes.
[00:37] So anytime, whenever we want to deal with the streams API, first we need to create an Stream object.
[00:42] That's that's what I'm trying to do inside the line two.
[00:45] So how to create a stream from an Arrays object?
[00:47] It is very easy.
[00:48] We just need to invoke the stream() static method available inside the arrays to the stream() method
[00:54] we need to pass the arrayOfWords as an input.
[00:57] And with that you're going to get a Stream object that is capable of processing String elements.
[01:02] You can see the name I have given to this is streamOfWords.
[01:06] So this is going to be my first stream like you can see here
[01:10] Easy and Bytes.
[01:11] They are being referred as two different elements inside my Stream object.
[01:17] Later on I'm trying to invoke one of the intermediate operation which is map().
[01:22] With the help of map(), I'm trying to invoke the split() method with the delimiter as empty value.
[01:29] So here I have mentioned double quotes without any space that means.
[01:32] So with the help of this split(), I want to separate each and every letter inside my word like Eazy and
[01:39] Bytes.
[01:39] So whenever we invoke the split() method available inside the String class, we are going to get an output
[01:45] which is array of car values.
[01:47] So that's why by the time these intermediate operation executed, the Stream object that I'm going to
[01:53] get is a Stream of String array.
[01:56] So this is how it is going to look like.
[01:58] So once my map() method is executed this word Eazy and Bytes they are converted into an string array.
[02:05] So this is an array like E a z y B y t e s.
[02:10] So what is a type of my Stream object.
[02:12] It is going to hold the array of string.
[02:15] So this is what the outcome from the map intermediate operation.
[02:19] So if you see here based upon our business logic we are getting an array of String.
[02:25] If you try to display this kind of information obviously you're going to display the array details but
[02:31] not the element details.
[02:33] And similarly if you want to store these elements inside another collection data structure with the
[02:38] help of terminal operation, you are never going to store these individual elements.
[02:42] Instead, you're going to store two different arrays.
[02:45] In this kind of scenarios, whenever your intermediate operation is giving another collection data structure
[02:52] or another array elements, you need to flat them by applying the flatMap() operation.
[02:57] So here you can see in the last line with the help of this stream of letter Stream object, I'm trying
[03:02] to invoke another intermediate operation which is flatMap().
[03:06] And to this flatMap() I'm saying convert all these arrays into the Stream objects by invoking the stream()
[03:14] static method available inside the Arrays class.
[03:17] With that, all these arrays, they are going to be converted into a normal elements and all these individual
[03:24] elements.
[03:25] I can store them inside a collection data structure, or I can try to print them with the help of terminal
[03:30] operation like forEach().
[03:31] So here, after this flatMap() operation, I'm trying to invoke the terminal operation, which is forEach()
[03:35] and I'm trying to print each and every element.
[03:39] So that's why I'm going to get the output as like you can see here, I hope it is making sense to you
[03:44] when to use flatMap() operation.
[03:45] If you try to understand the definition of flatMap(), it says it is used to handle the scenarios where
[03:51] you have a stream of elements and each element contains multiple sub elements are one to many mapping.
[03:59] So if you see here this is an single element inside a stream initially, but by the time you applied
[04:04] the map operation with your business logic where you have used the split() method, it converted into
[04:10] one to many, like like one element became many elements inside an array.
[04:15] So in this kind of scenarios, we can use flatMap() to flatten the stream of elements into a single stream
[04:22] by applying a mapping function that returns a stream for each element.
[04:27] In other words, we can say flatMap() is a combination of map() and a flat() operation.
[04:32] So it is going to apply a map() function to the elements as well as flatten them.
[04:36] So if you see here for the flatMap() also I'm giving some lambda expression to execute.
[04:41] That means this lambda expression is going to be applied for the each of the element present inside
[04:46] your input stream.
[04:48] I'm assuming this is clear to you, but if something is not clear, don't worry.
[04:51] I have one more example to explain to you so that you're going to be super clear about this.
[04:56] So let me show you the other example like you can see here first
[04:59] I have a person Pojo class inside the Person Pojo class.
[05:02] I have the fields like name and phone numbers. So name is of type String.
[05:06] But coming to the phone numbers it is of type List of String.
[05:10] So a person can have multiple phone numbers.
[05:13] That's why I mentioned the phone numbers as List of String post that we have a constructor Get'er method
[05:18] there is no setter method.
[05:20] Now on the right hand side you can see I'm trying to build a List object with the help of Arrays.asList().
[05:26] And inside this List object, I'm trying to store two different persons along with their name
[05:31] and their mobile numbers. As of now, just to make sure that this code is being fitted into this screenshot,
[05:37] I have given the phone numbers as three digit phone numbers, but we know in real life, phone numbers
[05:43] always are at least a 9 or 10 digit numbers.
[05:45] So once we have created these Persons List object as a first step, we are going to invoke the stream()
[05:52] method to create a Stream object.
[05:54] Once the Stream object is created, I'm trying to invoke the map() operation.
[05:58] So inside the map() operation, I'm trying to fetch the phone numbers of each person.
[06:04] Since get phone numbers is an method available inside the person, I'm trying to use the method reference
[06:10] here post that I'm trying to use a terminal operation which is collect.
[06:14] So using this terminal operation collect, we can convert the Stream of object into some other collection
[06:20] object.
[06:20] So here you can see to this collect terminal operation I'm passing the input which is Collectors.toList().
[06:26] .
[06:27] That means as soon as this terminal operation is executed, my Stream of objects, they are going to
[06:32] be converted into an List object.
[06:35] We're going to discuss about this terminal operation in detail in the coming lectures.
[06:39] But for now, I'm assuming you are clear what we are doing with this line of code.
[06:43] If you try to see on the left hand side what I'm trying to catch, I'm trying to catch list of List.
[06:50] We know the phone numbers field is List.
[06:52] That's why when this map() operation executed, I'm going to get list of List as an output.
[06:59] So if you try to process these kind of data it is going to be super confusing.
[07:03] But if you are looking for a single List of phone numbers, belongs to the all the persons, then you
[07:09] can apply the flatMap() operation.
[07:12] So here I'm trying to apply the map() operation.
[07:14] Instead, I'll try to apply the flatMap() operation with a lambda expression, which is
[07:19] I'm trying to get the get phone numbers for each person, followed by I'm invoking the stream() method.
[07:24] With that, all the phone numbers are going to be flattened into a single list based upon the terminal
[07:30] operation that we have here.
[07:32] So since here I told to convert all the phone numbers into a list, I'm going to get the results in
[07:37] the format of List of String.
[07:39] And if you try to print out this List of String, it is going to make more sense to you.
[07:43] You're going to see the list of phone numbers which you can easily understand by looking at them.
[07:48] So here also you can see we have handled a problem where the intermediate operation, when it is resulting
[07:54] into the a more complex data structure like List of List or array of array.
[08:00] So for all such scenarios we can use the flatMap() intermediate operation.
[08:04] I hope you are clear with this theory discussion.
[08:06] In the next lecture, we can try to implement these two examples that we have discussed so far, so
[08:12] that it is going to be more clear for you.
[08:14] Thank you,
[08:15] and I'll catch you in the next lecture, bye.

----------------------------------------
