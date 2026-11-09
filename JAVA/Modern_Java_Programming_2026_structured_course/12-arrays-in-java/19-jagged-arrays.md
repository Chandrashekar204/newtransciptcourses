# 12.19 — Jagged Arrays

> Section 12: Arrays in Java

[00:00] Inside this lecture, let's try to understand about a flavor of two dimensional array which is jagged
[00:07] arrays.
[00:07] So what are jagged arrays?
[00:09] As of now we are trying to create two dimensional array where each row, they are going to have a fixed
[00:16] number of columns.
[00:17] That means we are maintaining uniformity across sub arrays or across nested arrays.
[00:24] However, Java also provides a concept of jagged arrays, and whenever you are building a two dimensional
[00:32] array which is going to contain sub arrays with varying sizes, such kind of two dimensional arrays,
[00:39] we are going to call them as jagged arrays.
[00:42] For example, you can see I'm trying to create a jagged array, and this jagged array is a two dimensional
[00:48] array.
[00:48] It has total four number of rows.
[00:51] And inside each row I have another sub array or nested array.
[00:56] If you see all my nested arrays are sub arrays
[00:59] they are having varying column size.
[01:03] First subarray
[01:04] it has a column size as four, followed by three, followed by two followed by one.
[01:08] So we are not getting a proper rectangular shape for our two dimensional arrays.
[01:13] So these kind of two dimensional arrays, we can call them as jagged arrays.
[01:18] Let's try to see how these jagged array is going to be visually created behind the scenes, inside the
[01:24] memory of the application.
[01:25] Like you can see we have total four rows.
[01:28] And inside each row we have another sub array or another nested array.
[01:32] So the first nested array it is going to hold four different elements.
[01:36] That's why you are able to see four different columns here.
[01:39] Whereas the second row it is going to have three elements followed by two elements followed by one element.
[01:45] So the purpose of this jagged array is you can use them in the scenarios where you want varying lengths
[01:51] for different set of data, and this provides a more flexible structure rather than following the regular
[01:59] rectangular two dimensional arrays.
[02:01] Let me show you one more example as well on how to create a jagged array like you can see here
[02:07] first, I'm trying to create a jagged array.
[02:09] During the initialization, I'm only mentioning how many rows my jagged array is going to have.
[02:16] I'm not mentioning any column details, because I want to maintain a varying column values for each
[02:23] row, so this is perfectly allowed inside Java while you are trying to create that jagged arrays.
[02:29] As a next step, I'm trying to create nested arrays individually.
[02:33] So this is a single dimension array like inside the array one I'm trying to store 5, 7, 3, 2, 1, 0.
[02:40] Similarly, I also created an empty array followed by array3, which is going to hold two different
[02:46] values, and array4, which is going to hold four different values.
[02:50] I can try to assign all these single dimension or simple arrays to my jagged array row number with
[02:56] the help of these code like jaggedArray at the index zero, I'm trying to assign the simple array which
[03:02] is array1.
[03:03] So with these assignments, this is how my jaggedArray is going to look like.
[03:08] At row number two we don't have anything because the array2 we have created as empty array.
[03:13] If you closely look at these jaggedArray as well, it is also not following any fixed length for the
[03:19] sub arrays or the nested arrays.
[03:21] Let's try to see that demo of this example inside IntelliJ.
[03:25] Inside my IntelliJ, I'm going to create a new Java class and the Java class name I'm going to mention
[03:32] as JaggedArrayDemo inside this class
[03:36] first, as usual, we need to create the main() method, followed by
[03:39] I'm going to first create a two dimensional array.
[03:43] I'll just try to declare the length details for my jaggedArray.
[03:48] So the name I'm going to mention as JaggedArray, and on the right hand side I'm going to mention int
[03:55] with two square brackets.
[03:56] And here I'm going to only mention the row size like four.
[04:01] I'm trying to mention and post that
[04:03] I'm trying to mention that semicolon.
[04:05] So this is perfectly possible, even though I'm not mentioning any lengthy details for my sub array
[04:11] or for my nested array Java
[04:13] still not complaining because Java supports jaggedArray, but if I try to not mention the row number
[04:20] details, then I'm going to get a compilation error saying that array initializer expected.
[04:25] That's why always mentioning the row length for your two dimensional array is mandatory.
[04:31] As a next step, let me try to create multiple single dimensional arrays.
[04:36] First one I'm trying to create with the variable name as array1.
[04:39] And inside this I'm going to store multiple values like 5, 7, 3, 2, 0.
[04:45] Similarly, let me try to create four more arrays.
[04:49] I'll try to change these variable names to array2, array3, and array4.
[04:54] So array2 I'm going to keep it as empty.
[04:57] Whereas for array3
[04:59] I will mention the values as 65, 74, and for array4, I am going to mention the values as
[05:07] 83, 2, 49, 2.
[05:11] So these are the four single dimensional arrays that I have created.
[05:15] As a next step, I can try to assign all of them by using jaggedArray variable.
[05:20] So since I want to assign the array1 variable at the row number zero, I need to mention the first
[05:27] index value as zero, and to this I'm trying to assign the single dimensional array with the name array1
[05:33] so let me do the same.
[05:34] Similarly, for remaining row index values like, I'll first update 1, 2, 3.
[05:41] Now I'll update the variable names to array2, array3, and array4.
[05:45] At last I'll try to print out these jaggedArray with the help of
[05:50] Arrays.deepoString() so that we can validate the output inside the console.
[05:56] So let me execute this program.
[05:57] You can see I have a two dimensional array inside my outer array I have four different arrays with different
[06:04] sizes.
[06:05] Like the very first nested array are sub array size is six followed by zero, followed by two followed
[06:12] by four.
[06:13] I hope you are clear.
[06:14] What are jagged arrays and how to build them?
[06:16] Please use them in the scenarios where you don't know the size of your sub arrays or nested arrays.
[06:23] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
