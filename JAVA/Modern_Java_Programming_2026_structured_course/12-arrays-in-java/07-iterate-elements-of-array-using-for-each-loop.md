# 12.7 — Iterate elements of Array using for-each loop

> Section 12: Arrays in Java

[00:00] When we are discussing about the loops inside Java, I told you that there is a for each loop available,
[00:07] which is an enhanced version of traditional for loop this for each loop we can only use with arrays
[00:14] and collections.
[00:15] Collection is an another advanced topic similar to arrays.
[00:19] But now let's try to focus on how to use this for each loop to iterate the elements of an array and
[00:26] how it is going to be a better version of traditional for loop.
[00:30] For each loop, which is also known as enhanced for loop, is a loop that is used to iterate over elements
[00:38] of an array or a collection.
[00:40] This is introduced in Java five to provide a simplified way to iterate through the elements of an array
[00:48] or collections.
[00:49] Whenever we are using these for each loop, we don't have to worry about how to use an index to iterate
[00:55] the elements.
[00:56] First, let's try to understand what is the syntax to use the for each loop.
[01:01] Like you can see here,
[01:02] whenever we want to use this
[01:03] for each loop, we need to mention the same for keyword followed by parentheses and curly braces.
[01:09] Inside traditional for loop, we will write three different kinds of expressions, whereas inside the
[01:14] for each loop we are going to write only two expressions, which are separated by colon.
[01:20] On the right hand side to the colon
[01:22] we need to give the variable of an array or the variable of an collection.
[01:27] In other words, to the right hand side of the colon, we need to mention what is the array, or what
[01:32] is a collection that we want to iterate with the help of for each loop, whereas on the left hand side
[01:39] we need to mention what is the data type of the elements that we stored inside an array or collection.
[01:46] For example, inside an array, if I store all elements of type int, I need to mention the data type
[01:52] as int followed by a temporary variable name.
[01:56] If you follow this syntax during the iteration, this for each loop, it is going to extract the element
[02:03] from the array one by one in each iteration, and during the same process, the value of the current
[02:10] element or the current iteration is going to be assigned to this temporary variable that you have mentioned.
[02:17] Using this variable only inside your
[02:19] for each loop, you can write the business logic.
[02:22] I can also show you an example here.
[02:24] Here you can see we have an array of type int.
[02:27] The array name is numbers.
[02:29] And inside this array we are storing five different int values.
[02:34] So whenever we want to use for each to iterate this array first we need to mention what is the array
[02:40] name.
[02:40] The array name is numbers and to the left hand side we need to mention what is the data type.
[02:45] The data type that we have considered during the declaration of numbers is, int the same I need to mention
[02:51] here.
[02:51] And what is the temporary variable name?
[02:53] So the temporary variable name that I have given is num.
[02:57] This temporary variable num is going to be used to refer to the current element in each iteration.
[03:04] And the same we can use as part of the business logic.
[03:07] If you see inside my for each loop, I have written a business logic which is to print each element
[03:13] inside my array.
[03:14] That's why I'm simply passing this num variable as an input to the println() method.
[03:19] Here you can see I'm nowhere worrying about the what is the length of my array?
[03:24] What is the current index?
[03:25] Since these for each loop is making our life easy, most of the developers on day to day work.
[03:32] They are going to use this for each loop, only to iterate over the elements of an array or a collection.
[03:38] Let me show you very quickly what is the difference between a traditional for loop and an enhanced
[03:43] For each loop. You can see the same input I have taken, like numbers, which is an array.
[03:49] In the case of for loop
[03:50] first we need to check what is the length of my array, and similarly we should start the index value
[03:57] at zero.
[03:57] By using this int i is equal to zero, and apart from initialization and this conditional check, we
[04:04] should also take care of updating the index variable after each iteration with the help of these i++
[04:11] and inside the business logic
[04:13] if you want to access the current element for the current iteration, you need to use this syntax,
[04:19] which is numbers.
[04:20] And inside the square bracket we need to mention the current index value which is represented by this
[04:26] i variable.
[04:27] Whereas with for each you can see how simple it is.
[04:30] We just have to mention what is the array variable and what is the data type of the element which is
[04:35] int and what is the temporary variable?
[04:38] Using this temporary variable, we can easily write the business logic inside the for each loop.
[04:43] So like I said, most of the times for each loop is a preferred approach for the developers to iterate
[04:49] the elements of an array.
[04:50] But that does not mean we don't have any use case to use the for loop.
[04:56] There are certain scenarios where using for loop is preferred approach
[05:00] compared to the for each loop.
[05:02] For example, think like inside your business logic
[05:05] you need to modify the array or collection elements during the iteration itself.
[05:11] So in this kind of scenarios we need to use the for loop.
[05:14] Because using for loop we should be able to know what is the current index number.
[05:20] After modifying the current array element value, we can update the same back into the current index
[05:26] number.
[05:27] The same we can't achieve with the help of for each loop, because inside for each loop, developers
[05:32] will not be able to get hold on to the current index number.
[05:36] I hope you are clear with this theory discussion.
[05:38] Let me show you an example on how to use for each loop very quickly. To demo you about the
[05:45] for each loop, I'm going to create a new Java class.
[05:48] The Java class name that I'm going to give here is
[05:51] ArrayForEachLoopDemo inside this class
[05:56] first, as usual we need to create the main() method, followed by
[05:59] I'm going to create an array of type int with the name numbers.
[06:05] And inside this array I'm going to store the values like 1, 2, 3, 4, 5.
[06:12] As a next step, let's try to use the for each loop to iterate these elements. For the same,
[06:17] first I need to mention for followed by what is the data type of my array elements.
[06:23] The data type is int followed by what is that temporary variable name that I want to give to the current
[06:31] element of each iteration.
[06:33] After providing the variable name, you can mention space followed by colon.
[06:37] After colon you can mention the space again and at last you need to provide your array as an input.
[06:43] Since our array is represented with the help of numbers variable, I'm trying to provide the same followed
[06:49] by curly braces.
[06:50] Now inside my
[06:52] for each loop, I'm going to use the num variable name to print each element available inside my numbers
[07:01] array during the iteration.
[07:03] So let me keep a breakpoint here.
[07:05] And if I try to execute this program, you can see during the first iteration the breakpoint stopped.
[07:11] And during the first iteration, what is the value stored inside the num,
[07:15] it is one because at the very first position we have the value one.
[07:19] If I try to keep debugging, the num variable is going to keep change to 3, 4, 5.
[07:25] During each iteration, the current focused element is going to be assigned to this variable.
[07:31] The same variable we can use inside the for loop to perform the business logic.
[07:37] So you can see inside our console we have the output 1, 2, 3, 4, 5.
[07:41] Let me do the same for one more array.
[07:43] For the same
[07:44] this time I'm going to define an array of type String, and inside the String I'm going to store three
[07:51] different names.
[07:52] The names are Madan followed by John, followed by Lucy.
[07:58] Now I have my names array ready, so let me use the for each loop by mentioning for followed by parentheses.
[08:05] After the parentheses, I can mention the curly braces. Inside the parentheses,
[08:09] this time I need to mention the data type as String and the temporary variable name as name, followed
[08:15] by what is the array variable name.
[08:17] So the array variable name is names.
[08:19] Now let me try to write the business logic inside this
[08:22] for each loop.
[08:23] The business logic is just to print the name value.
[08:27] If I execute this program, you will be able to see three names that are being displayed inside the
[08:32] console as well. As the next step
[08:34] let me show you under which scenarios we cannot use the for each loop.
[08:39] Suppose think like,
[08:40] I have a requirement to convert each of my name value to a completely capital letter.
[08:46] So in this kind of scenario, I want to first read the element from the array.
[08:53] Post that I need to current the element value into a complete capital value, and update back into
[08:58] the array.
[08:59] In this kind of scenarios, whenever we want to update a value back inside an array, we need to know
[09:05] what is the current index number, since for each loop is not going to provide you, what is the current
[09:10] index number during the iteration?
[09:12] We cannot use for each loop in this kind of scenario.
[09:15] So that's why I'm going to use the traditional for loop.
[09:19] Inside the traditional for loop, we are going to first mention int i is equal to zero, followed by
[09:25] a less than names.length, followed by i++ and post that inside the curly braces.
[09:33] I'm going to write a business logic, which is names followed by square brackets, and inside the square
[09:39] brackets I'm going to mention what is a current index number is equal to followed by names and inside
[09:46] the square brackets i and dot toUpperCase().
[09:51] So what do I get from these names off I I'm going to get a String object because my names array is going
[09:58] to hold the objects of String.
[09:59] So with the help of a String object, I can invoke the method toUpperCase(), which is going to convert
[10:05] the content of my String object into completely capital letter, the same I'm trying to assign back
[10:11] into my names array.
[10:13] So after executing this traditional for loop, all the names inside the names array is going to be converted
[10:19] into completely capital letters.
[10:21] We can also confirm the same by keeping a breakpoint at the end.
[10:24] Let me execute this method.
[10:26] You can see the breakpoint stopped at the line number 22, and the values inside the names are completely
[10:33] converted into uppercase letter.
[10:35] So when you have these kind of scenarios where you want to modify the elements of an array or a collection,
[10:41] in such scenarios, definitely you need to go with the traditional for loop, but not with the for each
[10:47] loop.
[10:48] Whereas if your scenario is only to process each element by having a business logic but not modifying
[10:55] or but not updating back into the array, then in such scenarios you can happily use the enhanced to
[11:02] for loop, which is for each for loop.
[11:05] I hope you are clear with this discussion.
[11:07] Thank you,
[11:07] bye.

----------------------------------------
