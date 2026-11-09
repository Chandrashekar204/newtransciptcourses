# 12.14 — Filling an Array

> Section 12: Arrays in Java

[00:00] Sometimes we may have a requirement to populate the elements of an array with a default value.
[00:07] As of now, whenever I try to create an array of type int, I'm going to get a default value zero.
[00:14] But if I have a requirement to populate a different default value for all my elements during the initialization
[00:21] process, then I can use the fill method available inside the arrays.
[00:26] You can see here
[00:27] first, I'm trying to create an array with the name scores, and it is of type int with a size of ten.
[00:34] If I use these Arrays.fill() method by passing the array name and what is the default value to be
[00:41] filled?
[00:42] All the elements inside the scores array
[00:45] they are going to be replaced with the 100 value.
[00:48] Similarly, we also have set all method which is going to accept your array name and a lambda expression
[00:56] or a lambda function.
[00:57] So we are ready to discuss about lambdas.
[00:59] So that's why I'm not going to focus a lot about the setAll() method.
[01:03] So I'm going to give you a small demo.
[01:05] My humble request is once we discuss everything about the lambda expressions then this setAll() method
[01:12] example.
[01:13] It is going to make sense for you.
[01:14] So please revisit the same after that Lambda expressions discussion.
[01:18] For now, let's see the demo of these methods inside IntelliJ.
[01:22] Inside IntelliJ
[01:23] I'm going to create a new Java class with the name FillDemo inside this class
[01:29] First, as usual, we need to create the main() method and inside the main() method I'm going to first create
[01:36] an array of type int with the variable name as course and to this I'm going to assign the length as
[01:44] ten.
[01:45] Now my array is going to hold that ten different elements with a default value as zero.
[01:52] The same I can confirm by invoking Arrays.toString() and passing my array name to these toString() method.
[02:00] So if I execute this program, the content is going to be displayed in a string format.
[02:05] Right now I have all the values as zero.
[02:08] Think like I have a requirement to populate the default score value as 100 inside my array.
[02:15] So in this kind of scenarios, we just need to invoke the Arrays.fill() method.
[02:22] And to this fill() method we need to pass your array name, which is score followed by what is the default
[02:29] number that you want to fill.
[02:31] Since I want to fill 100 in all the positions, I'm trying to mention the same number.
[02:38] Now if I try to execute this program this time, you can see my array has all default elements populated
[02:45] with the help of fill() method.
[02:47] Very similarly, let me show you the demo of setAll() method for the same
[02:52] I'm going to create an array of type int with the name as indices.
[02:58] This one I'm going to create with a length of five post that I'm going to invoke Arrays.setAll()
[03:07] followed by what is my array name?
[03:09] And after giving the array name, I'm trying to mention a lambda expression I followed by lambda expression
[03:16] symbol followed by i.
[03:17] So with this lambda expression, what I'm telling is, please take the index value from the current iteration.
[03:24] The same index value I want to store as the element value.
[03:30] So when I execute this program, you will be able to see that data 1, 2, 3, 4, 5.
[03:35] So let me replace this course with indices.
[03:38] And if I try to execute this program you can see we are getting the output as 0, 1, 2, 3, 4.
[03:43] Previously I said 1, 2, 3, 4, 5.
[03:45] I was wrong because I forgot the index is always going to start from zero.
[03:50] So how we got this output we mentioned inside the lambda expression that please take the index value
[03:57] that I'm going to get based upon the current iteration.
[04:01] The same value set as an element value as well at the same position.
[04:06] That's what we are telling.
[04:07] For example, if I try to multiply two to this index number, then you'll be able to see the output
[04:13] as 0, 2, 4, 6, 8, because for each index value we are trying to multiply two and the output from the expression
[04:22] we are trying to store inside the array.
[04:24] I hope you are clear on how to use this fill() and setAll() method.
[04:28] If something is not clear about this lambda expression, don't worry.
[04:32] It is a very advanced topic and a beautiful concept inside Java, which we are going to discuss in the
[04:38] coming sections.
[04:40] I hope you are clear,
[04:40] thank you,
[04:41] bye.

----------------------------------------
