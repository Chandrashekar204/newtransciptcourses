# 12.18 — Addition of two matrices using 2D arrays

> Section 12: Arrays in Java

[00:00] Matrices are the very close concept to the two dimensional array.
[00:05] That's why inside this lecture, let's try to explore on how to perform the addition of two different
[00:11] matrices with the help of two dimensional array.
[00:15] Long back during our childhood days inside the mathematics subject, we studied about matrices.
[00:22] Performing an addition of two different matrices is going to be super simple.
[00:27] You just need to take the elements at the same position inside both the matrices, and you need to add
[00:33] them.
[00:33] For example, at the position 0 , 0 I have four here, and inside this matrix I have an element 3.
[00:41] So the addition of these four and three it is going to give the total value as seven.
[00:46] Similarly, if you try to perform addition of remaining elements you're going to get the desired output.
[00:52] So in order to perform these addition first we need to make sure we are representing both these matrices
[00:58] with the help of two dimensional array post that we need to iterate the arrays and perform the addition
[01:05] of each element inside the array.
[01:07] I have given the solution for you, but let's try to talk about it in detail by trying to build a Java
[01:14] program around this scenario.
[01:16] Inside my IntelliJ, I'm going to create a new Java class under the main package.
[01:21] The Java class name that I'm going to mention here is AddMatricesDemo.
[01:27] And inside this class first, as usual we need to create the main() method and post that
[01:31] first I'm going to create two different two dimensional arrays representing two different matrices.
[01:38] I have.
[01:38] Since the content of my matrices are int values, I'm going to create an two dimensional array by mentioning
[01:46] two square brackets.
[01:47] I'll mention the name of this array variable as array1 is equal to new operator along with the int
[01:55] data type, followed by two square brackets.
[01:58] Inside our matrices we have two different rows and three different columns.
[02:02] That's why we need to mention the length details as two and three.
[02:07] And with that, the total number of elements that my 2D array is going to hold will be six.
[02:12] But if I try to declare my array using this approach, I need to manually add the int value at each
[02:20] index by mentioning the row number and the column number.
[02:24] Instead, I'm going to show you another easy approach.
[02:27] First, I need to mention the curly braces.
[02:29] So these curly braces they are representing my outer array.
[02:33] Inside these outer array I want to store nested arrays.
[02:36] Let me try to mention the nested array details.
[02:39] So I'm trying to mention curly braces one more time
[02:42] and at the row number one I'm going to store three different int values like 4, 7, 9.
[02:49] Similarly I want to create one more nested array.
[02:52] This time I'm going to store the elements as 5, 7, 0.
[02:57] So this is my array1
[02:59] similarly, I also want to create the array2 which is going to represent my second matrix.
[03:05] So the elements we are going to store here is, 3, 8, 2.
[03:09] And under the second row we can store the elements which are 2, 6, 1.
[03:15] So now I have two different 2D arrays representing two matrices along with their input data.
[03:21] As a next step I want to perform the addition operation.
[03:25] So the output from the addition operation we want to store inside another array.
[03:29] That's why I'm trying to create another array with the variable name sumArray.
[03:35] So this one also should be two dimensional array.
[03:38] That's why I'm trying to mention square brackets two times and the size we need to make sure we are
[03:42] mentioning the same as array1 and array2.
[03:46] So what will be the size?
[03:47] It will be two and three.
[03:49] After this I'm going to write an outer for loop and inside this outer for loop
[03:54] first let me try to create an index variable representing the row numbers like int i is equal to zero
[04:01] colon i < array1.length followed by i++.
[04:08] So this is my outer for loop.
[04:10] Now inside this outer for loop let me try to write one more inner for loop.
[04:15] So inside the inner for loop I'll try to iterate the column values.
[04:19] So for the same I'm going to mention int j is equal to zero, followed by j < array1[i].length
[04:28] and after the length variable I need to mention j++.
[04:35] So if you observe these two outer for loops and nested for loop, they are looking very similar to what
[04:41] we have built in the previous lecture.
[04:43] So always the syntax at the structure is going to be the same to iterate two dimensional elements.
[04:50] Now I want to perform the addition of the elements present inside the two matrices and the sum value
[04:56] I want to assign back into the sumArray.
[04:59] So
[04:59] That's why
[05:00] first I need to mention some area with two square brackets
[05:04] and inside these two square brackets I need to mention i and j, and after mentioning i and j index
[05:11] values for the someArray variable I need to mention is equal to followed by
[05:18] array1[i][j].
[05:20] So this code will only assign the element inside the array1 into the someArray.
[05:26] But we want to perform the addition of the elements present inside the array1 and array2.
[05:31] So here what I can do is, I can simply copy this code and try to mention the same after mentioning plus
[05:37] symbol, but this time instead of array1, I'm going to mention array2, so we don't have to separately
[05:43] iterate the array2 elements, because whatever row numbers and columns that we are trying to iterate
[05:49] using the same index values, we should be able to access the element inside the array2 as well.
[05:55] So with this the addition operation is going to complete.
[05:59] But along with the addition, I also want to print the output into the console for the same
[06:05] I'm going to mention System.out.println().
[06:08] So instead of print l I'm going to mention only print and what I want to print here I want to print
[06:13] the content present inside the sumArray at the position i and j index values, and after that I also
[06:21] want to append the space value so that we can see the output in a readable format.
[06:27] With this statement, the entire content of sumArray is going to be displayed in a single line.
[06:33] So to avoid that we can try to mention System.out.println() in the outer for loop.
[06:39] Now if I try to execute this program, you will be able to see the output like 7, 15, 11, 7, 13,
[06:46] 1.
[06:47] I'm super happy that we got the desired output.
[06:49] I'm assuming you're also happy, so please try to understand what I have written inside this program
[06:54] and try to build a same program inside your intelliJ as well.
[06:58] In the same process, you will get to know how to initialize a two dimensional array,
[07:03] how to iterate a two dimensional array.
[07:05] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
