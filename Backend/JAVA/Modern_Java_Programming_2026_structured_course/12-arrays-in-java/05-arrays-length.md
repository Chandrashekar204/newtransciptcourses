# 12.5 — Arrays length

> Section 12: Arrays in Java

[00:00] Sometimes
[00:01] once we created an array, and once we stored the data inside it at a later point of time
[00:07] inside your Java program, you may want to know what is the length of your array. To help you in these
[00:13] kind of scenarios.
[00:14] Every array object, they are going to have a public final instance variable with the name length.
[00:22] Whenever you try to access this length variable with the help of Array object, you will be able to
[00:27] know what is the length of your array.
[00:30] So let's try to understand how to do the same.
[00:33] To show you the demo around the length instance variable available inside array object, let me create
[00:40] a new class inside the main package, the class name I'm going to keep as ArrayLengthDemo.
[00:47] So inside this class first, as usual we need to create main() method and inside the main method I'm going
[00:54] to create an array with the name nums.
[00:58] And inside this array variable I want to store five different numbers.
[01:02] We can achieve the same by using the curly braces.
[01:06] And inside this curly braces we can try to mention 1, 2, 3, 4, 5.
[01:13] There is also one more syntax
[01:15] let me show you that.
[01:16] So this time I'll try to create a variable of type String and the variable name I'm going to mention
[01:24] as names.
[01:25] And after the variable name on the right hand side I'm going to mention new String of array.
[01:31] Now after this square brackets inside the curly braces, I can mention list of names that I want to
[01:38] store inside these names array.
[01:40] So first name I want to store is Madan.
[01:43] Then followed by second name I want to store is John, followed by the third name I want to store is
[01:50] Lucy.
[01:50] So if you want to understand what is the length of these two arrays at runtime inside your program,
[01:57] you need to invoke the length variable available inside your array object.
[02:02] By just looking at this data, we'll be able to know that the very first array length is five, whereas
[02:08] the second array's length is three.
[02:11] On the similar lines, let me try to create one more array variable with the name mobileNumbers.
[02:19] And to this I'm going to assign the size directly inside the square brackets.
[02:24] The size I want to assign is 116.
[02:27] So you can see
[02:28] for the third array we are just storing the default values of primitive type int.
[02:33] So all the elements inside my mobileNumbers array they are going to hold the default value zero.
[02:38] So now we have three different arrays which we have created with the three different styles.
[02:43] So for these three arrays let's try to understand what is the length of them.
[02:48] So first let me try to invoke the System.out.println() followed by I'm going to mention what
[02:54] is my first object name.
[02:55] So the first object name that I have is nums.
[02:59] So after the nums I need to mention the dot operator followed by length.
[03:04] So this length instance variable inside my nums object is going to hold the total length of the array.
[03:11] So this is a final object.
[03:13] That means once an array is created with with a given size, we will not be able to change the size
[03:21] of the array.
[03:21] So whatever we have created or committed while declaring and initialization of the array, the same
[03:27] is going to be final.
[03:29] So let me try to print the length of other array objects that we have, like for names
[03:35] also we can mention names.length.
[03:37] For mobile numbers we can mention mobileNumbers.length.
[03:40] So if I try to execute this program we will be able to see the output as 5, 3 and 116.
[03:47] So these are the lengths of our array objects.
[03:50] And the output is also like we expect. The very first array
[03:54] it has the length of 5 followed by 3 and 116.
[03:57] And like I said the length of the array is always fixed and static.
[04:03] For example, if I try to be oversmart and try to change the length of this num's to a different value
[04:09] by invoking nums.length = 6.
[04:14] You can see I'm getting an compilation error saying that cannot assign a value to a final variable length.
[04:21] So this confirms during the object creation of my array behind the scenes
[04:26] my Java is also going to create a length instance variable of type final.
[04:33] You can see we also have a definition of this length public final int.
[04:37] So the length is of type int.
[04:40] This should also give a clue to you on what is the maximum size that we can assign to a array.
[04:46] So the maximum size that we can assign to an array is, the maximum value that is supported by the inter
[04:53] primitive data type.
[04:54] Let's try to check the same.
[04:55] So this time I'll try to create a double array with the name
[04:59] rises and to this array I'll try to assign a size which is beyond the maximum value off int primitive
[05:08] data type.
[05:09] So how to know the maximum value supported by the inter primitive data type?
[05:13] With the help of Integer wrapper class, we will be able to invoke the max value.
[05:19] So you can see if I try to provide this max value as an input, it is accepting.
[05:24] But to this max value, if I try to add one more value, it will result into the overflow scenario that
[05:32] we have discussed previously.
[05:33] So let's try to check the same.
[05:35] So here I will try to take the System.out.println() and try to print the prices.length.
[05:41] So if I try to execute this program we can see we are also getting an RuntimeException which is negative
[05:48] array size exception.
[05:49] Why my number became negative since we added the plus one to the maximum value due to the overflow,
[05:56] the length value or the size value became the negative value.
[06:00] So that's why always make sure you are giving the size which is less than or equal to the max value
[06:05] supported by the into primitive data type.
[06:08] The next point that you need to be aware is, whenever you are trying to give such a huge value as an
[06:14] your size of your array, please make sure you have enough memory inside your System.
[06:21] For example, I'm using a 16 GB Ram laptop and to these IntelliJ or to my JDK program.
[06:28] I might have assigned only a fraction of 16 GB like 1 GB or 2 GB.
[06:33] So with these 1 GB or 2 GB memory, if I try to create an array of such a huge size, I may get
[06:41] an exception.
[06:42] For example, if I try to execute this program, you can see I'm getting an error saying that out of
[06:48] memory error.
[06:49] So these are RuntimeException that my Java is throwing because it is not able to create an array size,
[06:56] which is exceeding the memory that I have assigned to the IntelliJ or to the Java program, usually
[07:03] inside real projects
[07:04] also, we will not be able to create such a huge array, but if you're working on a rare scenario,
[07:10] please make sure you are providing enough space or memory to your Java program.
[07:16] So for now, I'll try to mention a value 1000.
[07:19] So this time if I try to execute this program, I will not get any runtime error because with the memory
[07:26] that I have provided to my Java program are to my intelliJ inside my laptop, it should be able to
[07:31] create an array of size 1000 very easily.
[07:35] Now this time let's try to understand what is going to happen.
[07:38] If I try to assign a negative value, maybe instead of 1000, I'll try to mention -123.
[07:45] So in this kind of scenarios also we are going to get a RuntimeException saying that negative array
[07:51] size exception.
[07:52] So this confirms negative numbers are not allowed as an input to the array length or array size.
[07:59] So let me revert back to 1000 if needed
[08:02] we can create an empty array with a zero size as well.
[08:06] Let me show you how to do that.
[08:08] So I'll try to create an array of type char and the array variable name is going to be grades to this
[08:15] grades array variable name.
[08:17] I'm going to assign the size as zero by just hard coding the size as zero
[08:22] like you can see. We also have other approach
[08:25] let me show you the same.
[08:26] So this time I'll try to create an array of type int and the variable name
[08:31] I'm going to keep it as empty array.
[08:34] So to this if I try to assign empty curly braces.
[08:38] So behind the scenes it is going to have zero size only.
[08:41] I can also confirm the same by printing out the length value of these two arrays.
[08:47] So let me copy the same statement and mention the variable name as empty array.
[08:53] Let me execute this program and you can see at the end we have output as 00, which confirms
[08:59] that we will be able to use the empty array as well.
[09:03] But in real projects these empty array is of no use because we will not be able to store any data inside
[09:11] them, but technically it is possible to create an empty array.
[09:15] I hope you are clear on how to know the length of an array, and how to assign a length to an array
[09:21] during the initialization process.
[09:24] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
