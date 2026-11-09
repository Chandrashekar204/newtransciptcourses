# 12.17 — Two-Dimensional or 2D Arrays - Demo

> Section 12: Arrays in Java

[00:00] Let's see that demo of 2D array inside this lecture.
[00:04] To demo you the same
[00:05] I'm going to create a new Java class inside my main package.
[00:09] The class name is going to be TwoDArrayDemo.
[00:15] I can't use the numerical value as the very first value inside my class name.
[00:20] That's why instead of numeric value, I have mentioned that spelling of two here.
[00:24] So let me create this class.
[00:25] Inside this class, as usual, I want to create first main() method.
[00:30] The data that I want to store with the help of 2D array is,
[00:33] I want to store the academic max details of given number of students.
[00:39] So let me show you how to achieve the same with the help of 2D array.
[00:43] So first I'm trying to create a variable with the name totalStudents.
[00:48] So this variable will tell me how many students marks details I want to store inside my 2D array.
[00:55] For now, let's assume we are trying to store marks of three different students, and when you are trying
[01:01] to store the marks of a student, the student might have studied in various subjects.
[01:07] That's why we should also consider how many subjects each student studied and attended an exam to indicate
[01:14] that total number of subjects.
[01:16] Here I'm trying to create a variable name, which is totalSubjects, and let's assume we have total
[01:23] six subjects that each student is going to write an exam.
[01:27] Now I'm going to create an two dimensional array.
[01:31] The syntax is we need to mention two square brackets followed by what is the array variable name.
[01:37] The array variable name that I'm going to give here is, studentMarks to this array variable
[01:43] I'm going to assign the size as three and six because I want to store max for three different students.
[01:52] And each student is going to have marks across six subjects.
[01:55] So total we want to store 18 elements.
[01:59] That's why I'm trying to mention here three and six.
[02:01] The product of three and six is going to be 18, which is matching to our expected total number of marks
[02:09] that we want to store inside these 2D array.
[02:12] Now as a next step I want to assign the values into this array.
[02:17] So let's try to understand how to assign the same.
[02:20] So first I'm trying to assign the values to the very first student.
[02:24] So that's why I need to mention the first index value as zero followed by the first subject marks.
[02:31] So that's why I'm trying to mention zero and zero in both the index.
[02:35] So think like in the very first subject, the very first student he got 89 marks.
[02:42] So the same I have to repeat for the remaining subjects like I have total six subjects.
[02:47] So let me update the second index number like one, two, three, four and five.
[02:53] So total six subjects
[02:55] and for each subject I'm trying to update the marks like in the second subject 76, followed by 55,
[03:01] followed by 92 followed by 100.
[03:05] And at last we can mention 78.
[03:08] So these are the marks secured by student one.
[03:12] If needed, we can also store the student name to make it more clear.
[03:17] What I can do is I can try to increase this six number to seven so that we can store the student name
[03:23] as well.
[03:24] So let me copy this and mention zero comma zero again.
[03:28] And here I want to store the name of the student.
[03:31] Maybe I can mention the name as modern.
[03:34] But as soon as we try to assign a name to the student, we're getting an error because we have mentioned
[03:40] the array data type as int.
[03:41] So to resolve this issue, I can try to convert these data type as String.
[03:46] Let me mention on the right hand side as well.
[03:49] With that I'm going to get compilation error at multiple other places.
[03:53] So let me remove these 0, 0 index code.
[03:56] And now I'm going to mention all these marks as a String value so that the compilation error is going
[04:03] to be resolved.
[04:05] At last I want to define the sixth subject marks as well by using the index six.
[04:11] Maybe this time I'll mention 83 as a number of marks.
[04:15] So you can see we have hardcoded the length values.
[04:18] Maybe what we can do is, we can try to mention the variables that we have declared on the top, like
[04:23] totalStudent.
[04:24] And I will mention totalSubjects plus one, because I also want to store the name of the student.
[04:31] Very similarly
[04:32] now I can try to store the data of the second student.
[04:36] In order to update the marks
[04:37] for the second student, we need to update the first index as one
[04:40] in all the places like you can see here, I'm trying to update the index to one.
[04:45] Post that I will change the name of the student to John, followed by
[04:50] I'm going to mention some mark for the student as well.
[04:54] Let me mention all of them.
[04:56] Now I have mentioned the marks for the second student as well as a next step
[05:00] let me do the same for our third student as well.
[05:03] But the third student, the index number is going to be two because inside array the index always starts
[05:10] from zero.
[05:11] So the name that I'm going to give for the start student is Lucy.
[05:14] And for her also I'm going to assign some marks.
[05:18] So let me do that very quickly
[05:20] behind the scenes. You can see I have updated the marks for Lucy as well.
[05:24] Now we have our 2D array populated with all the required data.
[05:29] Let's try to understand how these data is going to look like by trying to print the content of this
[05:35] two dimensional array.
[05:36] So how to print the content of this two dimensional array?
[05:39] First we need to convert this two dimensional array into an String value.
[05:44] So first let me mention System.out.println().
[05:47] Here
[05:47] inside this println() method I'm going to mention Arrays.toString().
[05:52] Let's see what is going to happen if we invoke that toString() method and pass the two dimensional array
[05:59] as an input.
[06:00] So if I execute this program, you can see I'm going to get the output
[06:04] like you can see here. There are three students data
[06:07] and each student data is again another array.
[06:11] So that's why we are getting these kind of data.
[06:14] Like I said before, whenever we are using multi-dimensional array, the method that you need to invoke
[06:20] is deep toString() method, which will convert all the content of your two dimensional array into a
[06:27] String representation.
[06:28] So let me execute this program
[06:30] this time
[06:31] you can see there is an outer array.
[06:33] Inside the outer array there are three different arrays.
[06:37] Like you can see the Person, Madan
[06:39] he got so and so marks the same kind of data you will be able to see for John and Lucy as well.
[06:45] I hope you are clear and how to build a two dimensional array.
[06:48] Now let me show you very quickly on how to iterate multi-dimensional arrays.
[06:53] Since we built a two dimensional array, then we need to create a nested for loop.
[06:59] Let me show you how to do the same.
[07:00] First I'm going to create the outer for loop, and inside this outer for loop I'm going to mention int
[07:07] i is equal to zero, followed by i less than studentMarks.length, followed by
[07:15] i++.
[07:16] You might be thinking the value that we get from this length variable is 3 * 7, which is
[07:23] 21, but that's not the case.
[07:25] Whenever we try to invoke the studentMarks.length, it is always going to give what are the total
[07:31] number of rows that you have inside your two dimensional array?
[07:35] In this case, since we have three different students, the length is going to be three.
[07:40] I can also confirm you the same by trying to print out the value of length using the
[07:47] System.out.println().
[07:48] If I try to execute this program, you'll be able to see the length as three.
[07:52] That means my outer for loop
[07:53] it is going to iterate three different times, covering three different students.
[07:58] Since we are starting the index at zero.
[08:01] That's why I have mentioned the condition as I less than three.
[08:05] Now we have an outer for loop to iterate the rows.
[08:08] As a next step, I want to access the nested array inside each row and using the same nested array,
[08:15] I want to iterate all the elements and print the same.
[08:19] So that's why I have to write a nested for loop
[08:22] and this time I'm going to mention the variable as integer a is equal to zero, followed by j less than
[08:30] studentMarks[i].length.
[08:35] And after this length I need to mention j++.
[08:39] .
[08:39] I'll explain you in few seconds why I have written all these expression.
[08:43] So if you see what is happening here is,
[08:45] I know there is an inner array inside each row.
[08:49] That's why I'm trying to access the length of the inner array.
[08:53] So how I can know what is the length of an inner array by fetching the actual array at a given row.
[08:59] Since the row numbers are represented with these I index, which you have declared as part of the outer
[09:05] for loop.
[09:05] Whenever I'm mentioning studentMarks of index i, it is going to give me the array that is available
[09:12] at a particular row.
[09:13] After that, I'm trying to invoke this length variable.
[09:16] So this is going to give me the total number of elements that I have inside my nested array available
[09:23] at a particular row.
[09:24] So this nested for loop that we have defined just now, it is going to be executed multiple times based
[09:30] upon the number of elements that you have inside your nested array at a particular row.
[09:36] So what we want to do inside this nested array, we want to print the content of the nested array.
[09:42] So let me try to do the same by using the System.out .println() and how to access the values inside
[09:49] the two dimensional array.
[09:50] You need to mention what is the array name, which is studentMarks followed by two square brackets
[09:57] inside the first square bracket you need to mention
[09:59] what is the row number?
[10:01] The row numbers are represented with the help of this i variable.
[10:05] Very similarly we need to mention what is the column number.
[10:08] So the column numbers are represented with the help of J.
[10:12] That's why I'm trying to mention the same here.
[10:14] Before I try to execute this program.
[10:15] First let me comment
[10:17] this code that we have, which is going to print the student Marks array with the help of deepTwoString().
[10:23] So let me comment this code.
[10:24] Now if I try to execute this program you can see I'm getting what is the name of the student and what
[10:31] are the marks of this student in each subject.
[10:34] If needed, I can optimize this further.
[10:36] Let me do the same.
[10:37] What I can do is I can try to remove these ln
[10:41] I will simply use the print statement.
[10:43] What I'm trying to achieve here.
[10:45] I'm not going to print the marks and the student details in multiple lines.
[10:50] I will try to display the student details along with the marks details in a single line.
[10:55] If I try to go with this code, all the student details are going to be printed in a single line.
[11:02] That's why whenever my nested for loop is executed completely for a given row, I want to break into
[11:09] the next line.
[11:09] So how I can do that?
[11:11] I can try to mention the System.out.println().
[11:15] So this println code
[11:16] it is going to move the cursor to the next line.
[11:20] As soon as we are done with the current execution for a given row.
[11:24] So if I try to execute this program this time, you can see the marks are displayed in three different
[11:30] lines.
[11:30] But the problem I have here is, all the values
[11:33] they are appended continuously without a space value.
[11:37] So I can try to include the space.
[11:40] So to include the space, I can simply mention place and a String value which is going to have a space
[11:47] value.
[11:48] Now if I try to execute this program this time, we should have a decent output.
[11:52] You can see we are able to display the student name along with his marks details.
[11:58] I hope you are clear on how to create that two dimensional array, and how to store the data with the
[12:03] help of two dimensional array, and how to iterate the data of two dimensional array.
[12:09] My humble request here is to practice this program by increasing the size of this two dimensional array.
[12:15] Maybe you can try to mention the totalStudent size as six.
[12:19] So try to populate the data for remaining students and see how this program is behaving by executing
[12:26] the same logic inside your intelliJ as well.
[12:29] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
