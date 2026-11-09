# 6.27 — Converting String to primitive data type values - Theory

> Section 6: Deep dive on String in Java

[00:00] Few lectures back, we discuss on how to convert a primitive data into an String value.
[00:07] Do you remember this?
[00:08] I hope you remember this concept with the help of the valueOf() method, which is available inside the
[00:14] String, we can convert any primitive data into an string representation.
[00:20] For example, here I have an int value 42.
[00:23] If I give this 42 as an input to the valueOf()method, which is a static method inside String, I am
[00:30] going to get an string representation of that 42.
[00:33] So what is the string representation of 42?
[00:36] A 42 with a double quotes value is a string representation.
[00:39] So this is a scenario where we want to convert a primitive data type into a String object.
[00:45] Sometimes we may want to convert a String object into a corresponding primitive data type.
[00:51] So let's try to understand how to achieve the same.
[00:54] The process of converting a String data into a primitive data type.
[00:58] We call that process as parsing.
[01:01] Parsing involves converting a string representation of a value into its corresponding primitive data
[01:07] type.
[01:07] So how to perform this parsing operation?
[01:10] I may have an int value in the format of String, but I want to convert that into a normal into primitive
[01:17] value.
[01:17] So for this kind of parsing scenarios we need to use a wrapper classes.
[01:22] Do you remember long back I told you that every primitive data type it has a corresponding wrapper class.
[01:29] For example, for into primitive data type, we have a wrapper class with the name Integer.
[01:34] Inside this Integer wrapper class, we have a static method which is parseInt().
[01:40] This parseInt() method is going to accept a String object as an input, and inside this String object,
[01:47] we need to make sure we are providing only the int values like numeric values.
[01:52] If you try to be oversmart and try to provide some alphanumeric values to this parseInt() method, it
[01:59] is going to throw an NumberFormatException.
[02:01] But if you give a proper int value using a String object, this pass int is going to give you an int
[02:08] value as an output.
[02:10] That's why here you can see for the parseInt() method, I'm trying to pass the string number as an input,
[02:16] and the return type that I'm receiving from this method is of type int primitive data type.
[02:21] Very similarly, if you are trying to convert a String object which has a double value into the double
[02:26] primitive data type, then you need to use a corresponding wrapper class which is Double.
[02:32] Inside the Double wrapper class, we have a method which is parseDouble(). To this parseDouble(),
[02:38] if you give a String object, it is going to convert your double number from string to primitive data
[02:44] type.
[02:44] For the float, it is going to be very similar.
[02:47] The wrapper class is going to be Float, and inside this wrapper class we have a method which is pass
[02:53] float that we need to invoke.
[02:54] After the float, we can see the example of Long.
[02:58] If you want to convert a Long string value into a primitive long value, you can use a wrapper class
[03:04] long.
[03:05] And inside this Long class we have a parseLong() method which we need to invoke, and this parseLong() method
[03:11] is going to convert your string data into a long primitive data type.
[03:16] In case if you are looking to convert your boolean string value into the boolean primitive data type
[03:22] value, then Boolean has a wrapper class with the name boolean where b is capital.
[03:27] Inside this Boolean wrapper class, we have a method which is parseBoolean().
[03:32] To this method, you need to pass your string representation of your boolean value.
[03:37] So here I'm trying to pass the true.
[03:39] So the output is going to be the true which is in the form of Boolean data type.
[03:44] If you try to be smart and if you're trying to send some values other than true and false, you're always
[03:50] going to get the output as false from this method.
[03:54] For example, I can pass my name as an input to this parseBoolean().
[03:58] If I pass my name as an input, then obviously that will be converted into an false value.
[04:05] So anything other than true and false always going to be converted into a false.
[04:10] Otherwise, if you are going to send the true value, you're going to get the true as an output.
[04:15] And similarly, if you send the false as an input, you are going to get the false as an output for
[04:19] the number scenarios like int, long, float, and double.
[04:23] If you try to send some invalid values, like maybe you're trying to send a alpha value.
[04:29] In such scenarios like we discussed, we're always going to get number format exception.
[04:34] So using the wrapper classes and invoking the static methods like parseBoolean(), parseLong(), parseInt()
[04:40] int parseFloat(), parseDouble().
[04:42] So this is one approach
[04:44] there is also another approach which you can achieve with the help of constructor of your wrapper classes.
[04:50] So here you can see I'm trying to create an object of wrapper class Integer.
[04:55] During the same process I can pass the String object as an
[04:59] input to the constructor.
[05:01] And with that, I'm going to get an object of Integer object.
[05:05] From this Integer object, we can fetch the actual valueOf() int, but this approach is deprecated from
[05:13] the Java 9.
[05:14] So what is the meaning of deprecated, Java team
[05:16] regularly they are going to deprecate some methods, some functionalities, some features.
[05:22] The purpose of deprecate is,
[05:24] in future versions they may remove these options.
[05:27] So here you may have a question like why Java team deprecate some features or some methods.
[05:33] The answer is very simple due to some performance issues are some security concerns,
[05:38] the reason can be anything Java team.
[05:40] Whenever they found some issues, they're going to make the features or the methods or classes deprecated.
[05:47] So when you try to use this deprecated approach inside our projects, it is considered as a bad practice.
[05:53] That's why always don't use that deprecated approaches.
[05:57] The reason why I'm sharing this information is you may work in an project where they are using Java 8,
[06:02] since inside the Java 8 this is not deprecated.
[06:05] You don't know that, but from Java 9 this method or this approach is deprecated.
[06:11] So all of a sudden a valid code inside the Java 8 is going to become invalid from the future versions
[06:19] like Java 9.
[06:19] So that's why regardless of which version you are using, please don't use this approach.
[06:25] As of now, we discussed the parsing process for the primitive data types like int, float, double
[06:31] long, boolean.
[06:33] How about the char value, for the char
[06:35] it is going to work differently because what is a String?
[06:39] String is a sequence of characters.
[06:42] For that reason, whenever you are looking to convert your String data into an char data type, you have
[06:48] two different approaches.
[06:50] One is with the help of charAt() method.
[06:53] We already discussed this method.
[06:55] Using your String object, you can invoke the charAt() method and you can mention what is the index number.
[07:02] Based upon your index number, you're going to get the char as an return type value.
[07:07] So this is the very first approach.
[07:09] And the second approach is using your String object
[07:12] you can invoke a method called toCharArray().
[07:15] And with that you are going to get an char [].
[07:19] So what is an array?
[07:20] In the previous lectures I gave a small hint.
[07:23] Array is a collection of elements.
[07:25] So in this scenario the array is going to have multiple car elements.
[07:29] Suppose if you're trying to fetch a specific char element from the given array, you need to pass your
[07:35] index value to the array.
[07:37] So here you can see first I'm trying to invoke that toCharArray().
[07:40] And with that I'm going to get an char [].
[07:43] That's why after the char I'm trying to mention square brackets using this charArray object I can pass
[07:50] the index which is one.
[07:51] So with that I'm going to get the second char, which is e, because the index I have mentioned as one.
[07:59] So this is the second approach.
[08:00] If this is not clear don't worry because this is going to make more sense to you when we discuss about
[08:06] the arrays in the coming sections.
[08:08] So this is all about the parsing process for all the primitive data types except a car data type, you
[08:14] can simply use the corresponding wrapper class and invoke the corresponding static parse methods like
[08:20] parseInt(), parseBoolean().
[08:22] Whereas coming to the char, you need to invoke the methods like charAt() and toCharArray().
[08:28] I hope you are clear with these three discussion in the next lecture.
[08:31] Let's see the demo of all these examples.
[08:34] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
