# 12.11 — Converting Arrays

> Section 12: Arrays in Java

[00:00] As of now, we understand how to perform a copy operation on an array.
[00:06] Using these copy options that we have discussed, we can copy the data from one area to another array.
[00:13] Very similarly, inside real projects you may have requirements to perform various operations.
[00:19] Maybe you want to sort the data inside an array, or maybe you want to search for an element inside
[00:25] an array.
[00:26] For all these kind of requirements, my humble request is always don't try to jump in and develop your
[00:33] own business logic.
[00:34] Since these are all common operations.
[00:36] First, you need to check if there is any existing method available inside the JDK library to help you
[00:44] inside your business logic implementation.
[00:47] Most of the arrays related helpful methods or
[00:50] utility methods are available inside these Arrays class.
[00:55] So this Arrays class is present inside the java.util package.
[01:00] So let me open this class.
[01:02] And inside this class, if you look for the list of methods you will be able to see there are so many
[01:08] static methods that you can directly invoke based upon your business requirements.
[01:14] For example, there is a method with the name binarySearch().
[01:18] So there are multiple overloaded methods.
[01:21] So using these binarySearch() method you can perform the searching operation inside your array.
[01:27] Similarly we also have compare() method to compare two arrays.
[01:32] copyOf() method we already evaluated previously,
[01:35] copyOfRange()
[01:36] also, we already saw the demo.
[01:38] And similarly if you can scroll down, there is a field related method which will help you to fill data
[01:44] inside your arrays and post that we also have sorting related methods like parallelSort(), sort().
[01:51] So there are more than 100 different methods which will help you in various operations related to arrays.
[01:58] So anytime if you have a requirement to perform an operation on top of your array, first please come
[02:05] into these Arrays class and check for any method that may help you in your scenario.
[02:11] We already saw how the arrays class is going to help us in the array copying operation.
[02:16] With the help of copyOf() method and copyRangeOf() methods.
[02:20] Inside this class, we're able to perform the copy operation very easily and efficiently.
[02:25] Very similarly, always look for a method which is going to help in your operation.
[02:30] Otherwise you are more than welcome to implement your own business logic, since it is not going to
[02:36] possible for me to discuss about all these methods, I'm going to put some efforts on explaining you
[02:43] about most commonly used methods inside these Arrays class to perform most commonly encountered operations
[02:52] inside your real projects.
[02:54] So let's try to understand what are those?
[02:56] The very first type of operation that I want to explain here is, converting your arrays to other format.
[03:03] For example, think like I have an Array with the name numbers.
[03:07] If I want to convert these entire array content into a String format, I can invoke the toString() method
[03:15] available inside the Arrays class to this toString() method
[03:19] I can pass my Arrays as an input, and with that I'm going to get the array content as an output in
[03:26] the form of String object and this String object
[03:29] I can use it to print the data of arrays very easily.
[03:34] Otherwise, if I want to print the content of my array, I need to keep on iterating all the elements
[03:40] instead
[03:41] if you want to quickly check what content we have inside an array, then in such scenarios, this
[03:47] toString() method is the go to method, and similarly, in real projects you may have requirements to convert
[03:54] your array as a list.
[03:56] What is a List?
[03:57] List is an one of the advanced data type.
[04:01] As part of the collection framework, we're going to discuss about the same in the coming sections when
[04:06] we are talking about collections framework.
[04:08] So how to convert your Array to List with the help of these asList() method.
[04:13] On the similar lines, we also have a stream method which is going to help you to convert your array
[04:20] as a stream object.
[04:21] Stream is also an advanced topic inside collections.
[04:25] For now, let's focus on how to use these toString() method and convert your array to a String object.
[04:32] To show you the demo around toString(), I'm going to create a new class inside the main package.
[04:37] I'll just mention the class name as ToStringDemo, and inside this I'm going to create a main() method
[04:45] followed by
[04:46] I'm going to create a array of type int and the variable name is going to be numbers.
[04:52] And inside this array I'm going to store the values like 1, 2, 3, 4, 5 if I want to
[04:59] understand
[05:00] what is the content of my array?
[05:02] The most basic approach is we can iterate the elements of this array with the help of for loop or for
[05:08] each.
[05:08] Instead, I can simply try to print out the content with the help of Arrays.toString(), and to this
[05:17] toString() method, I'm going to pass my array as an input.
[05:21] If I execute this program, you can see I'm going to get the content of my data in my console.
[05:27] Let me show you what will happen if you directly try to print out these numbers
[05:32] array.
[05:32] Since every array is an object, we're not going to get the output in an understandable format.
[05:39] So let me show you the same as well.
[05:41] If I try to execute this program, you can see I'm getting an object data of my array.
[05:47] So this is the object representation of my array.
[05:50] By looking at this I will not get anything
[05:52] that's why we need to always make sure we are using that two String method to convert your array object
[06:00] into a String, which is going to help you to understand the data that you stored inside an array.
[06:06] I hope you are clear about these toString() method.
[06:08] Let's try to continue this discussion about other operations as well in the next lecture bye.

----------------------------------------
