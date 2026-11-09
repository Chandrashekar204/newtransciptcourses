# 12.10 — Copying Arrays using arraycopy and copyOf methods

> Section 12: Arrays in Java

[00:00] The second option that we have to copy an array is, with the help of a static method
[00:06] arraycopy(), which is available inside the System class.
[00:09] Using this method is going to be super easy.
[00:12] Like you can see
[00:13] first you need to have a source array or oldArray and post that you need to make sure you have created
[00:20] an new array or targetArray.
[00:22] Once you have the sourceArray and targetArray, you can invoke the arraycopy() static method which
[00:28] is available inside the System class.
[00:30] To this array copy method, you need to pass what is your source array as an first parameter, followed
[00:37] by what is the source start position?
[00:40] Whether I want to copy from the first index or from any other index value.
[00:46] If you mention source start position as zero, then the copy will start right from the first element
[00:52] inside the sourceArray.
[00:54] And the third parameter that you need to pass is, what is that destination array?
[00:58] That's why I'm trying to mention targetArray here, followed by what is the destination start position
[01:05] inside that targetArray
[01:07] what is the index that we want to consider to start the copying?
[01:11] If we mention destination start position as zero right from the first position, the copying is going
[01:19] to happen into the new array.
[01:21] And at last this method, it is also going to accept length to be copied.
[01:26] That means this method is giving a flexibility to you how many elements that we want to copy.
[01:33] If I provide sourceArray.length, that means I'm trying to convey to this method.
[01:38] Please copy all the elements, whereas if I mention only three, then the three elements from the source
[01:45] to start position is going to be copied.
[01:48] So let's try to understand how this is going to work by exploring inside our intelliJ.
[01:53] First, I'm going to comment this line of code which we have implemented using the for loop approach.
[02:01] Instead of this approach, I'm going to invoke the System class, and inside the System class we have
[02:08] array copy method to this array copy method.
[02:12] First we need to mention what is the sourceArray.
[02:15] In our scenario, the source array is oldArray followed by from which position we want to start the
[02:22] copying from the oldArray.
[02:24] Since we want to start the copying from the first element, I'm going to mention the index zero, followed
[02:31] by what is the targetArray?
[02:34] Here the targetArray is new array and after this I need to mention what is that destination start position.
[02:41] So here also I'm going to mention zero followed by what is the length of the elements to be copied.
[02:47] Since I want to copy this entire array, I can simply mention the length as oldArray.length.
[02:55] So with this now my new array is going to have all the five elements from the oldArray.
[03:01] Let me confirm the same by running this program this time
[03:04] also, you can see we are getting the same output.
[03:07] The first five elements are copied and the next five elements we have the default zero values.
[03:12] Let me try to show you one more flavor here instead of zero.
[03:15] This time I'm going to mention one.
[03:18] That means I want to start the copying from the index one to the length of two.
[03:24] With this I'm giving instructions to the arraycopy() please
[03:28] only two elements from the oldArray starting from the index one.
[03:33] But in the new array, the pasting of the element should start from the index zero.
[03:37] So let's try to understand how the output is going to be.
[03:40] You can see the first two elements of my new array.
[03:44] They are copied from the index one and two.
[03:48] Because we said the starting index should be one and the total length should be two.
[03:53] That's why two and three values copying started from the zero position inside the new array, and for
[03:59] all the remaining elements, we have the default value as zero inside the new array.
[04:04] That means this array copy is also giving me a flexibility to partially copy the data from oldArray
[04:11] to the new array.
[04:12] I hope you are clear.
[04:13] Let me roll back to the previous changes so that the entire array will get copied into the new array
[04:20] let me execute this and confirm one more time.
[04:23] Yes, we are getting the correct output like we expect.
[04:26] The third approach is with the help of copyOf() static method which is available inside the Arrays class.
[04:33] So this method accept what is your sourceArray or what is your oldArray followed by what is the new
[04:40] length that you want to consider for the new array or targetArray that is going to be created by
[04:46] the copyOf() method.
[04:47] This method is further simpler than second approach.
[04:51] The reason is you don't have to create the new array or targetArray.
[04:55] You can simply pass what is your sourceArray and what is the new
[04:59] length that you want to give to your targetArray.
[05:02] And with that, this method behind the scenes, it is going to do the magic, and it is going to give
[05:08] you the new targetArray based upon your instructions.
[05:11] So let's try to evaluate this method as well inside IntelliJ here inside my main() method I'm going to
[05:18] invoke the Arrays class post that I'm going to invoke the copyOf() method.
[05:25] But you can see we have multiple overloaded methods of copyOf().
[05:30] If you are working with an int array, then in such scenarios you need to invoke the method which accepts
[05:36] the int array as an input.
[05:38] Similarly, we also have copyOf() method for byte array char array, long array, float array, short
[05:45] array, double array, boolean array and similarly for objects
[05:49] also, we have a copyOf() method which is going to accept any object array as an input.
[05:55] Whether you pass a String array or a person array, it is going to accept.
[05:59] So whatever t that you see here that indicates generic data type.
[06:05] Since this is not possible to create the multiple overloaded methods of copy off for all the data types,
[06:13] or for all the object data types that you may have inside your Project Java team, they will simply
[06:19] mention T.
[06:20] T indicates it's a generic representation.
[06:22] So if you pass a person off array, then this T is going to represent Person data type.
[06:28] And similarly if you pass an String object array as an input to this copyOf() method, then this T is
[06:35] going to represent the String data type.
[06:38] For now, since we are trying to copy an int array, let's try to invoke the very first copyOf() method.
[06:44] To this
[06:45] I'm going to first mention what is my sourceArray.
[06:48] So the sourceArray name is going to be oldArray followed by what is our new array total length that
[06:54] we want to consider.
[06:56] Either we can give directly ten or we can give an expression which is oldArray.length + 5.
[07:04] That means to my existing oldArray I want to add five more memory locations.
[07:09] So the output from these method is going to be your new array.
[07:13] That's why on the left hand side, let's try to catch the output with the help of a variable of type
[07:19] array.
[07:19] For the same, let me type int array followed by what is the name?
[07:24] The name I'm going to give here is targetArray.
[07:27] So the output we are going to get inside the targetArray.
[07:30] So let me copy this targetArray and mention inside this for each loop.
[07:35] So if I try to execute this program you can see we are going to get the same output like 1, 2, 3, 4, 5.
[07:41] That means all the values are copied into the new array successfully with the help of this copyOf()
[07:48] method.
[07:49] Now let's see what is going to happen if I mention the new array length as three.
[07:55] In this scenario, only the first three elements of the oldArray are going to be copied into the new
[08:02] targetArray.
[08:03] Let me confirm the same by executing this program.
[08:06] You can see the new array size is going to be three, and only the first three elements of oldArray
[08:13] are copied.
[08:13] I hope you are clear on how this second parameter is influencing the whole array copying process.
[08:20] With this copy of method, the copy always going to start right from the zero index.
[08:26] But sometimes you may want to copy from a desired start position to desired end position.
[08:32] You want to maintain a range of values to copy.
[08:35] Maybe I want to copy from the first index to the third index only for these kind of scenarios, we also
[08:43] have copyOf() range method available inside the arrays only.
[08:47] So let me copy this entire line.
[08:50] And this time I'm going to invoke the copyOfRange().
[08:56] So for the copyOfRange() also we have multiple overloaded methods for each primitive data types.
[09:03] We have a copyOfRange() method.
[09:05] And similarly we also have a copyOfRange() method for object data types as well.
[09:09] The same you can see it is represented with the help of a generic data type, which is T.
[09:14] We are going to talk about generics a lot as part of the collections framework.
[09:19] But now if you have any questions, please hold your thoughts.
[09:22] We are going to talk in detail in the coming sections.
[09:25] So here I want to invoke the copyOfRange() method that accepts int array as an source or as an optional
[09:34] Array.
[09:34] To this I need to pass what is the from index and the two index.
[09:38] So let me select this method.
[09:40] So we are passing the oldArray as a sourceArray or the original array.
[09:45] Since I want to start the copying from the first index, I need to mention the second parameter as one,
[09:52] followed by up to which index you want to copy.
[09:55] So here I want to do the copying up to the third.
[09:59] That means these two, three, four values
[10:03] I want to be copied, but here we should not mention the index as three.
[10:07] Instead, we need to mention the index as four.
[10:10] Because the from index or
[10:11] the start index is always inclusive, whereas the end index is always exclusive.
[10:17] Since I have mentioned the value as four, the copying will happen only up to the third index.
[10:24] So let me try to catch the output with the help of targetArray1 variable name the same
[10:29] I'm going to use it to iterate the elements of targetArray one, and this time you can see I'm getting
[10:36] the desired output, which is 2, 3, 4.
[10:38] If I mention the index as three, then only two and three will be copied because the third index is
[10:46] going to be excluded.
[10:47] I hope you are clear.
[10:48] Let me execute this program and confirm you the same.
[10:52] You can see we are right now getting the output as two and three.
[10:55] With this, I'm assuming your super clear about all the three commonly used approaches on copying the
[11:01] arrays, so please refer these slides if you have any questions.
[11:05] I have mentioned all the examples and the important points that we have discussed so far about these
[11:12] array copying.
[11:13] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
