# 12.9 — Copying Arrays using loops

> Section 12: Arrays in Java

[00:00] One major disadvantage of using arrays is arrays supports a fixed size, and these arrays they can only
[00:08] store a specific number of elements. Like we discussed in the previous lecture
[00:13] arrays do not grow in size during runtime, which can be a major problem in real projects.
[00:20] To address this limitation in Java, we have collections framework which can automatically grow as needed
[00:27] at runtime based upon the data that we are trying to add.
[00:31] We are going to focus a lot about collections in the coming lectures.
[00:34] For now, let's try to answer a question, which is we know that arrays has certain size limitations.
[00:41] Does that mean there is no workaround to overcome this challenge?
[00:44] Let me try to answer the same inside this lecture.
[00:47] Let's imagine you have an array declared and initialized with the size of 500, and later on you end
[00:54] up storing only 300 elements inside your array.
[00:58] Unfortunately, you can't just disregard the extra 200 elements that you have assigned inside your array.
[01:06] Similarly, if you realize you need 550 elements to be added to the array, you can't simply add additional
[01:13] 50 elements to the existing array.
[01:16] So whenever you end up in these kind of scenarios where you want to change the size of an existing array,
[01:22] the only workaround a solution that we have is, to create a new array with the desired length, and copy
[01:29] the elements from the original array into the new array.
[01:34] As part of this process, we may end up copying the old array into the new array.
[01:40] When I say copying array, it can be a complex process.
[01:43] Suppose think like your old array has 1000 elements, and you want to copy these 1000 elements into
[01:50] the new array.
[01:51] So in this kind of complex requirements you may have a question how to perform the copying of arrays
[01:57] in a more efficient manner for the same inside Java we have three different majorly used approaches.
[02:04] The very first and basic approach is with the help of a loop.
[02:08] It can be a for loop or it can be a while loop.
[02:11] And the second approach is with the help of array copy static method, which is available inside the
[02:17] java.lang.System class.
[02:20] And the last approach is with the help of copy of static method, which is available inside the java.util.arrays
[02:27] class.
[02:29] First, let's try to understand how to perform the copying of an array with the help of a loop.
[02:34] Inside my Java project, I'm going to create a new Java class and the class name I'm going to mention
[02:41] as ArrayCopyDemo.
[02:44] So this is the class name that I want to give inside this class
[02:47] first, let me try to create the main() method and post that
[02:51] I'm going to create a static method of type private, and this method is going to return an array of
[02:58] int.
[02:58] And after this I'm going to mention the static keyword.
[03:01] Since I want to create a static private method inside my class, the method name I'm going to mention
[03:07] as copy array using loop.
[03:11] This is the method name, and this method is going to accept what is the old array and what is the new
[03:18] array as an input parameters.
[03:20] So let me try to mention the first method parameter as oldArray.
[03:25] And similarly I'm also going to mention method input parameter with the name newArray.
[03:31] Once the method definition is defined inside this method, I'm going to write a traditional for loop
[03:38] with the help of oldArray.
[03:40] So let me first define int i = 0, followed by i less than oldArray.length, followed
[03:50] by i++.
[03:52] Now inside my for loop I'm going to write a simple logic which is newArray of index i is equal to oldArray
[04:01] of index i.
[04:03] That means using these statements, I'm trying to assign the value or the element available at index i
[04:11] inside the oldArray into the same position or index of newArray.
[04:16] And at last I'm going to return the newArray as an output parameter from my method.
[04:23] So let me mention newArray and getting a compilation error because I have mentioned static after the
[04:31] return type that is invalid.
[04:33] Instead, let me mention the static keyword just after the private access modifier.
[04:38] With this, all the compilation errors are resolved.
[04:40] As a next step, I'll go into my main() method and here first I'm going to create an oldArray with the
[04:48] values 1, 2, 3, 4, 5.
[04:52] So there are five elements.
[04:54] Now think like I want to create a new array with a greater size maybe
[04:59] I want to create an new array with the total size of 10, and in this new array, first I want to copy
[05:06] the first five elements of the old array, followed by
[05:10] at later point of time, I will populate the elements at the remaining indexes.
[05:15] Let's try to understand how to achieve the same here
[05:18] as a next step, I'm going to create an new array.
[05:22] The variable name is also going to be newArray.
[05:25] And to this I'm going to assign the size as oldArray.length + five, which means whatever might
[05:33] be the oldArray length
[05:35] I want to increase the size of my new array by adding five more memory locations.
[05:40] So now I have my oldArray which has some data and new array is also available with the new size.
[05:47] The only next step is pending is the new array does not have the oldArray data.
[05:53] So to achieve the same we can invoke the static method that we have created just now.
[05:58] So I'm going to invoke this copyArrayUsingLoop() to this method
[06:02] first we need to pass oldArray as a first parameter, followed by new array as a second parameter.
[06:09] As a return type
[06:10] from this method I'm going to get the newArray.
[06:13] So let me catch the same on the left hand side.
[06:16] So after completing this operation, I'll try to print out what values I have inside my new array with
[06:24] the help of for each loop that we have discussed previously.
[06:27] So let me mention System.out.println().
[06:30] And to this I'm going to pass the num variable.
[06:33] If I try to execute this program, you'll be able to see
[06:37] first five elements are copied from the oldArray 1, 2, 3, 4, 5 whereas remaining five
[06:44] elements we have default values.
[06:46] At least with this now we are able to increase the size of the new array, and it is capable of storing
[06:52] total ten elements.
[06:54] Now, based upon my business requirements, I can add new elements at these positions like 6, 7,
[07:01] 8, 9, 10.
[07:02] I hope you are clear on how to copy an array into another array with the help of loop.
[07:09] I'm also providing a sample code snippet for you inside this slide for your reference.
[07:14] With the help of loops, we have written all the business logic where we are iterating the entire array
[07:20] and post that we are manually copying each element by element.
[07:24] So this is a very basic way of doing.
[07:26] But, but we don't have to follow this approach because there are better approaches available inside
[07:32] the JDK or Java library.
[07:34] So let's try to understand what are those in the next lecture.
[07:38] Thank you,
[07:38] bye.

----------------------------------------
