# 12.6 — Iterate elements of Array using for loop

> Section 12: Arrays in Java

[00:00] Let me show you how to iterate the elements of an array with the help of for loop.
[00:06] For the same, I'm going to create a new Java class inside the main package, and the Java class name
[00:12] is going to be ArrayForLoopDemo inside this class
[00:17] first I need to create the main() method so that we can execute this program.
[00:21] Now inside this main() method I'm going to create an array of type int with the variable name as
[00:30] mobileNumbers.
[00:32] And to this I'm going to assign the size which is 116.
[00:37] So this is the length of my mobileNumbers array.
[00:40] Now let's try to iterate this array and try to display all the elements along with their values.
[00:47] We know by default into primitive data type is going to have the value zero, which means all the 116
[00:55] elements
[00:55] right now inside my mobileNumbers array, they are going to have the value zero.
[01:00] I can also confirm you the same by using a for loop.
[01:03] So the syntax to use a for loop is,
[01:04] first we need to mention for followed by parentheses and after the parentheses
[01:09] I'm going to mention the curly braces.
[01:11] Now as part of the for loop
[01:13] first we need to mention the initialization expression.
[01:17] So I'll define an variable which is int i is equal to zero, followed by what is the check that we want
[01:24] to perform before each execution of my for loop iteration.
[01:28] So the condition that I want to check is, if my I less than the length of the mobile numbers array
[01:35] followed by
[01:36] for every iteration I want to increment the I value by one.
[01:41] Always please make sure you are following the similar kind of code
[01:45] whenever you are trying to iterate the elements of an array, you need to make sure you are starting
[01:51] the i value as zero, because inside array the very first position or
[01:55] the very first index is going to start from zero, and since we want to access all the elements inside
[02:01] an array, we need to define i less than mobileNumbers.length.
[02:06] We should not use i less than or equal to because if you mention is equal to, then the for loop is
[02:11] going to try to access an array element which is equal to the length of your array.
[02:17] But the maximum index that we are going to have inside an array is length -1 , because each array
[02:24] element is going to start at the index zero.
[02:26] So that's why please make sure you are always using i < mobileNumbers.length followed by
[02:32] i++.
[02:33] So now inside these for loop I'm going to write a System.out.println() with a statement the element
[02:41] at index to this index I'm going to append the index value, which is available through the i variable
[02:49] post that I'm going to append one more String statement, which is space, is followed by what is the
[02:57] element?
[02:57] So how to access the element present inside an index?
[03:01] We need to use the array variable name, which is mobileNumbers, and inside the square bracket we
[03:07] need to mention the index value, which is i.
[03:09] With this you can see I'm trying to assign the value that I fetched from my array at the index i to
[03:15] this String statement.
[03:16] So if I execute this program, I'll get the output as like you can see here the element at index zero
[03:22] is zero
[03:23] similarly, I also have other statements displaying the element value at various index values.
[03:30] So if I go to the end they'll be an index value which is 115.
[03:35] So this confirms all my indexes right now they are holding that default value zero.
[03:40] As a next step, let me try to assign some data to my mobileNumbers array.
[03:45] For the same, let me copy the code present inside my ArrayBasicsProgram.
[03:50] I'll take this code and mention inside my ArrayForLoopDemo.
[03:54] So this time instead of 0, 1, 2, 3, 4, I'll try to randomly assign these mobile numbers like you can
[04:01] see the second mobile number I'm trying to assign at a position 16, followed by 24, followed by 38,
[04:08] followed by 94.
[04:10] So if I execute this program right now at these positions, I'll be able to see these values inside
[04:16] my output console.
[04:17] So let me execute this program.
[04:19] You'll be able to see at 94 we have this mobile number.
[04:22] Similarly at 38 we have this mobile number followed by 24 followed by 16 followed by zero.
[04:30] So the output confirms that our code is, working like we expect.
[04:34] Anytime you want to assign a value to an array index or update a value inside an array index.
[04:41] So please use this syntax which is the array variable name followed by square brackets and inside the
[04:46] square brackets
[04:47] you can mention the index number.
[04:49] This time
[04:50] let me try to create an array of String.
[04:53] So let me type String followed by square brackets, followed by what is an variable name after
[05:00] the variable name
[05:01] I'm going to mention new followed by String array, and the size I'm going to assign is three.
[05:07] So if I try to iterate the elements of these names array with the help of for loop, I'm going to get
[05:13] the default values of String object.
[05:16] So what is an default value for any object?
[05:19] It can be String object or it can be a Person object
[05:21] the default values for any object is always going to be null.
[05:26] So let's try to confirm the same by copying these for loop and mentioning the same here.
[05:31] So instead of mobileNumbers.length, I'm going to mention names.length followed by here
[05:37] also I'm going to mention names instead of mobileNumbers.
[05:41] So if I try to execute this program you can see I'm getting an output at the end.
[05:46] The element at index zero is null.
[05:48] The same applies for one and two.
[05:51] If I try to assign a String object randomly.
[05:53] For example, names of two is equal to
[05:57] I'll assign my name, which is Madan this time
[06:00] at the last two index will be able to see a value Madan, so the same is printed here as well.
[06:07] I hope you are clear on how to iterate the elements of an array with the help of for loop.
[06:13] So please always make sure of using the same kind of code to iterate all of your elements inside an
[06:20] array.
[06:21] Whatever points that we have discussed in the previous lecture around the length, and in this lecture
[06:26] around the for loop iteration.
[06:28] The same I have mentioned in these two slides.
[06:31] Please refer them if you have any questions.
[06:34] Thank you,
[06:34] bye.

----------------------------------------
