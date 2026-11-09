# 12.3 — Declaring & initializing Arrays - Part 1

> Section 12: Arrays in Java

[00:00] Let's start the journey of Arrays.
[00:02] Since we are into a new section, I have created a new Java project with the name
[00:08] section_12,
[00:09] inside this Java project you can see as of now I have an empty source folder.
[00:14] As a first step, let me try to create a new package inside my source folder.
[00:19] The package name that I'm going to give here is, com.eazybytes.main.
[00:25] So inside these package I'm going to write all classes which are going to have main method to execute
[00:32] them.
[00:32] So that's why I have given these meaningful name.
[00:34] Now inside this package I'm going to create a new Java class.
[00:39] And the class name I'm going to mention as ArraysBasics inside this class,
[00:45] first, let me try to create the main() method before I try to show you how to create the arrays and how
[00:50] to store data with the help of arrays.
[00:53] First, let me try to show the problem that we may face if we don't use arrays inside the real projects.
[00:59] Think like you have a scenario where you want to store all your friends mobile numbers for the same
[01:07] if you don't know arrays, you will end up creating variables for each of your friend.
[01:12] mobile number.
[01:13] For example, I can declare variables of type into primitive data type and the variable names I'll mention
[01:20] as mobileNumber1
[01:22] and similarly I can keep mention these variable name saying that mobileNumber2,
[01:28] mobileNumber3.
[01:30] So if I have three different friends, if I want to store all their mobile numbers, I need to create
[01:36] three different variables like this.
[01:38] But what if you are a super social person and if you have more than 1000 friends, are you going to
[01:45] create the variable names of primitive data type int for all your 1000 friends?
[01:51] Off course, that's not a feasible option.
[01:54] We should not go for such a basic solution, because the basic solution of creating 1000 different int
[02:01] variables is super cumbersome and difficult to maintain.
[02:04] So for these kind of scenarios only we have arrays.
[02:08] So let's try to understand how to handle the same scenario with the help of arrays.
[02:13] So whenever you want to store a group of data which belongs to a data type, then you need to create
[02:18] a variable of type array.
[02:20] So let me show you how to do the same.
[02:22] So first you need to mention what kind of data you want to store inside your array.
[02:28] Since we want to store data of type int, I'm mentioning that int as a data type post that we need to
[02:35] mention opening and closing square brackets.
[02:38] After this you can give a name to your array, so I'll just give the variable name as mobileNumbers.
[02:47] With this, we successfully created an array variable which is capable of storing into primitive type
[02:54] elements.
[02:55] So if you see the difference between a normal variable declaration and array variable declaration is,
[03:02] we just have to mention the square brackets just after your data type.
[03:07] We also have other approach.
[03:09] The other approach is first you can mention what is your data type followed by what is the variable
[03:16] name of the array.
[03:17] This time I can give the variable name as mobileNums.
[03:22] After the variable name, you can try to mention the square brackets like you can see open and closing
[03:28] square brackets followed by semicolon.
[03:30] So this is another style of array declaration.
[03:33] Even if you try to mention this square brackets just before the variable name, it is still is going
[03:40] to work.
[03:41] So these are all the three different flavors of creating a variable of type array.
[03:46] But most of the times inside real projects people will use the very first approach.
[03:52] So that's why I would also encourage you to use the same to declare an array variable.
[03:57] Similarly, let's try to create arrays of different data types.
[04:02] For example, if I want to store the list of prices, I can use double as a data type followed by square
[04:10] brackets space
[04:11] and after this I'm going to give the array variable name as prices.
[04:16] Similarly, let me try to create one more array.
[04:19] This time I'm going to mention char as a data type, followed by what is the array variable name.
[04:24] So I'll just mention grades as a name in case if you want to create an array that is capable of storing
[04:31] the group of objects, you can also follow the same syntax.
[04:35] For example, if I want to store the group of String objects, I can first mention what is the data
[04:42] type, which is String followed by square brackets and post that
[04:45] I can try to mention the variable name as names.
[04:48] Similarly, we can also try to create an array that is capable of storing the objects of a custom class
[04:56] or a custom data type like person for.
[04:59] Example, if I want to create a array that is capable of a group of person objects, then first I need
[05:06] to make sure I have Person class inside my section 12 project.
[05:10] So let me try to create one more package.
[05:13] So the package name this time I'm going to mention as com.eazybytes.model.
[05:19] So inside this model package I'm going to create a empty class with the name Person.
[05:24] For now, let's not worry about what to write inside this Person class, since I want to show you how
[05:30] to create an array of custom data type, I just created this Person class.
[05:35] First we need to mention that data type name, which is Person followed by square brackets.
[05:41] After the square brackets I can give space followed by the variable name which is persons.
[05:46] As of now, with all these declarations, we only declared the array variables, but we didn't define
[05:54] anywhere how many elements or how many objects we want to store inside these arrays.
[05:59] For example, I have a mobile numbers array with this declaration, I'm not giving any information to
[06:06] my Java
[06:07] on what is the size of mobile numbers that I want to store inside these arrays
[06:12] object.
[06:12] Until you define a size for your array, you can't store the data inside them.
[06:18] That's why, as a next step, let's try to understand how to define size to an array for the same
[06:24] just after this mobile numbers,
[06:26] let's try to delete the semicolon and mention is equal to followed by new operator.
[06:32] After mentioning the new operator, you need to mention what is the data type that you have used on
[06:38] the left hand side.
[06:39] So what is the data type that we have used?
[06:41] We have used int.
[06:42] That's why we need to mention the same here as well.
[06:45] And this time also on the right hand side we need to mention square brackets after the int.
[06:50] And inside these right hand side square brackets we need to mention the size.
[06:55] For example, if I want to store five different mobile numbers, I can mention the five as a size and
[07:01] post that I can mention the semicolon.
[07:04] So if you try to see this line of code, I'm trying to do the initialization of my array.
[07:10] So I have created a array with the variable name as mobile numbers, which is capable of storing five
[07:17] different elements of int data type.
[07:20] What is the default value for int primitive data type,
[07:23] it is zero.
[07:24] That's why if you try to debug this program by mentioning a breakpoint at line number ten and starting
[07:31] this program in a debug mode at runtime, you will be able to see what is present inside this mobile
[07:38] numbers array.
[07:39] So my breakpoint stopped.
[07:40] So let me execute line by line.
[07:43] You can see at runtime my mobile numbers array is holding five different elements with the default values
[07:50] like 00000.
[07:53] Because we define the length of an array as five.
[07:57] Let me release this breakpoint.
[07:59] I hope you are clear on how to create a array variable, and how to declare and initialize an array
[08:06] variable with required length.
[08:08] Let's try to continue this discussion in the next lecture as well.
[08:11] Thank you,
[08:12] bye.

----------------------------------------
