# 12.16 — Two-Dimensional or 2D Arrays - Theory

> Section 12: Arrays in Java

[00:00] Let's start the journey of multidimensional or nested array by discussing about the two dimensional
[00:07] or 2D array.
[00:08] Before I try to explain about how to build two dimensional or 2D array, you may have a question here
[00:15] under which scenarios I need to use these 2D arrays or two dimensional array to store my data inside
[00:22] real projects.
[00:23] Let me try to answer the same.
[00:24] Most of the gaming applications they need to store the data of the objects, or the people or the vehicle
[00:32] inside the game in a two dimensional space.
[00:35] How are we going to represent a GPS position?
[00:38] By using longitude and latitude.
[00:41] In this kind of scenarios, where you want to store two dimensional data or spatial data, the developers,
[00:48] they are going to consider using 2D arrays to store the data.
[00:52] Whenever we are creating a two dimensional array, we can visualize it as an table with rows and columns,
[01:00] and using these row number and column number, we will be able to store the data and access the data.
[01:07] First, let's try to understand how to declare an 2D array like you can see here
[01:12] these are
[01:13] all the valid formats or valid syntaxes to declare a two dimensional array.
[01:19] Since we are going with the two dimensional array, we need to mention two square brackets as part of
[01:25] the array declaration.
[01:26] Whereas if you are looking to understand and how to declare and initialize the array with a specific
[01:33] size, then you can use this syntax, which is
[01:36] first you need to mention what is your data type.
[01:39] Here I am mentioning int as the data type, followed by two square brackets followed by space and what
[01:44] is the variable name?
[01:46] The array variable name that I'm giving here is, 2D array and after the variable name
[01:51] as usual we need to mention is equal to followed by new operator and after the new operator, what is
[01:56] the data type and after the data type, we need to mention two square brackets.
[02:01] And you can see in the very first square bracket I'm telling the size should be three.
[02:06] Whereas inside the second square bracket I'm going with the number four.
[02:11] So let's try to understand how these 2D array is going to be stored inside the memory of your application.
[02:18] If you try to visualize this array first based upon the three number that I have defined here, three
[02:24] different rows will be created like row zero, row one, and row two.
[02:30] So this is a simple array
[02:32] and inside this simple array we are going to store three different elements at the position row zero,
[02:38] row one and row two.
[02:40] Now let's try to understand what is going to happen based upon the number four that we have defined
[02:46] as part of the second dimension.
[02:49] Like I said before, using two dimensional arrays we can represent that tabular data just like inside
[02:56] excel sheets how we have row numbers and columns.
[02:59] Very similarly as of now based upon these three we have created three different row numbers.
[03:05] Now based upon these four number, you can see inside each of my row number there is going to be another
[03:13] array which is capable of storing four different values.
[03:17] So this is a classical representation of array of array.
[03:22] So whatever you see inside green color it is my outer array or a simple array where it is going to have
[03:28] three different positions or indexes.
[03:32] And inside each index I'm trying to store one more array at the row number zero, I'm trying to store
[03:38] another array with the total length as four.
[03:41] That's why the same you can see under the row one and row two.
[03:44] I hope you are clear with these visualization.
[03:47] And whenever we are trying to create the 2D array or two dimensional array, you may have a question
[03:53] how can I know what is the length of my total array elements.
[03:58] So the formula it is going to be super simple.
[04:00] You just need to do the multiplication or the product of two lengths that you have like 3 * 4
[04:06] it is going to give you the total array length or the total elements that are going to be stored inside
[04:13] your two dimensional array.
[04:15] So here you can see we have total two positions at 12 indexes using which we can store two well into
[04:24] values.
[04:24] I hope you're clear.
[04:25] Now let's try to take an example of 2D array and try to visualize the same and how it is going to be
[04:32] stored behind the scenes, inside the memory.
[04:34] Like you can see here, I'm trying to create an two dimensional array.
[04:39] And during the declaration itself, I'm trying to assign the data into my two dimensional array.
[04:45] So here you can see this is my outer array
[04:48] whatever.
[04:49] you can see this red color curly braces.
[04:51] This is my outer array.
[04:53] So my outer array has three different arrays like 1, 2, 3.
[04:58] So that's why here
[05:00] the number of rows that we are going to store inside my two dimensional array is going to be three rows
[05:06] like row zero, row one, and row two.
[05:09] Now inside my each row I'm going to store another array which is capable of storing four int elements.
[05:16] You can see the very first nested array that we have.
[05:20] It is holding the elements 1, 2, 3, 4.
[05:23] So the same I need to mention like at column zero we need to mention one followed by two at column one,
[05:31] three at column two, and four at column three.
[05:34] The same applies for the second nested array and the third nested array.
[05:38] With this, I'm assuming you are clear on how the data is going to be stored inside an two dimensional
[05:45] array.
[05:45] The next question that you may have is how to access the data from a two dimensional array.
[05:52] It is going to be very easy.
[05:53] First you need to mention what is your row number.
[05:56] If I want to access this value two first I need to mention my row index which is zero, followed by
[06:02] column index, which is one.
[06:04] Let me show you another table structure, which is going to help you to understand on how to access
[06:10] the two dimensional array elements. Like you can see here
[06:14] if I want to access these one value, I need to use the index zero and zero because it is available
[06:21] at the row number zero and the column number zero.
[06:23] In a similar style, you can try to mention what is the row index number and the column index number
[06:29] to access the any element inside your 2D array.
[06:33] I hope you are clear with this quick introduction about that 2D array.
[06:37] In the next lecture, let's try to see the demo of these 2D arrays by writing a Java program inside
[06:43] IntelliJ.
[06:44] Thank you,
[06:44] bye.

----------------------------------------
