# 12.20 — Three-Dimensional or 3D Arrays

> Section 12: Arrays in Java

[00:00] Let's try to understand how to build a three dimensional or 3D arrays in Java.
[00:05] So what are these 3D arrays?
[00:07] These 3D arrays are just an extension of lecture 2D arrays.
[00:11] Because they just add a dimension to the help of a 2D array, where this 3D array of a can be
[00:19] visualized as a collection, and a 2D arrays are display where each two and array is an account of your
[00:26] an 3D array or it might be confusing concept going to share you an example in few seconds, then it
[00:32] is going to to run super sense to you this time.
[00:34] Before I try to share my example, let me share the syntax that we need to know
[00:38] while we are used to declare a as dimensional array, enter two dimensional array and we are going to
[00:44] mention input square brackets for three dimensional
[00:47] array
[00:47] obviously
[00:47] we are in a mention
[00:49] three square brackets . So that's why you can see during the declaration and
[00:53] initialization I'm trying to mention what is data type followed by three square brackets follwed by
[00:59] by what is array variable name and after this variable name on the right hand side
[01:04] I'm trying I to mention new data type and inside the three brackets
[01:09] I need to
[01:10] mention the size1 and size2 and size3 indicating the total size of my 3D array.
[01:17] For example
[01:18] here am trying to create an array with a variable name as 3D array.
[01:23] Here I have given the size details as 3, 4, 5.
[01:27] So with this was going to happen is, first you are going to have an array with three different rows.
[01:33] And inside these three different rows you're going to have three different 2D arrays.
[01:39] And each 2D array it is going to have the size of four and five.
[01:43] So let's try to visualize this 3D array like you can see here
[01:47] since the very first size we have mentioned as three, we are going to get the outer array with the
[01:53] length as three like row zero, row one, and row two.
[01:56] Inside these each rows we are going to store two dimensional arrays with the size of four and five.
[02:04] You can see here I have a two dimensional array here.
[02:07] And each two dimensional array it has four rows followed by five columns.
[02:13] The same applies for row one and row two as well.
[02:16] So this is how a 3D array is going to be created behind the scenes.
[02:20] In simple words we can say a 3D array is a array of 2D arrays.
[02:25] So you can see I have an array inside my array
[02:28] the elements are 2D arrays, whenever we want to access the element from 3D array
[02:33] obviously, we need to pass by different types of index value, the very first index value
[02:40] represent which row or which element of outer array you want to access. Post that we need to mention
[02:47] second index followed by third index.
[02:49] The second index indicates what is the row number of your 2D array
[02:54] that is stored at a particular row number and at last to the last index represent the
[02:59] column value of your 2D array.
[03:02] So let's try to take an example on how to create a 3D array and store the data inside this
[03:08] 3D array.
[03:09] You can see I have an example
[03:11] the requirement that I have is, I want to store the marks of a students in various subjects covering
[03:17] all the semisters.
[03:19] So inside each semister a student going to learn and write exams covering four different subjects.
[03:27] This way throughout the course the student is going to have total five semesters.
[03:32] So if I want to represent these kind of data I need to create the three dimensional array.
[03:37] You can see here I'm trying to create an three dimensional array with a variable name as student array.
[03:43] The very first length value I'm trying to mention is noOfStudents.
[03:47] So since I have mentioned the noOfStudents as 2, I'm going to get an outer array with
[03:52] the length as 2 where I can store student zero details and student one details.
[03:57] So here I have row one.
[03:58] I'm going to update these to
[04:00] student1 post this lecture.
[04:02] So don't worry about this type of for now.
[04:04] The second length details I'm trying to mention is, subjects like how many subjects my student is going
[04:10] to learn in a semester.
[04:12] So since I have mentioned the subjects as four, I'm going to get a 2D array inside my outer array with
[04:20] the total four number of rows covering subject zero.
[04:24] subject2, subject3 and at last
[04:26] I'm trying to mention the total semester input.
[04:29] Since I have mentioned the semesters as five, I'm going to get five different columns inside my 2D
[04:35] arrays with the values like semester zero, semester one, semester two, and semester three and semester
[04:41] four.
[04:42] With that, you should be clear how a 3D array is going to be created.
[04:45] As a next step, let's try to understand how to assign the data into a 3D array. Like you can see here
[04:52] first, I'm trying to create a 2D array with the variable name as student1 and student2.
[04:58] So inside this 2D array
[05:00] I have created four different arrays and these four different arrays, indicating the four different
[05:07] subjects. Under the each subject
[05:09] I'm trying to mention the marks that a student got under five semesters.
[05:14] So that's why under each array I have five different marks values the same repeated for student2
[05:21] as well.
[05:21] At last, I can try to assign these 2D arrays at the index value zero and one for my 3D array that I
[05:28] have created here with the variable name as studentArray.
[05:32] So you can see I'm trying to assign the 2D array like student1 and student2 at the index position
[05:37] zero and one of 3D array.
[05:40] That's why at the index zero, all the marks related to the student1 is going to be stored, whereas
[05:47] at the index one all the marks of student two are going to be stored.
[05:51] Can we see the demo of this inside the intelliJ?
[05:53] Let's try the same,
[05:55] let's go
[05:55] why not. Inside my IntelliJ,
[05:57] first I'm going to create a new Java class.
[06:00] The class name is going to be ThreeDArrayDemo.
[06:05] First let me create a main() method followed by
[06:08] I'm going to create a multiple variables representing that total number of students, subjects and semesters.
[06:15] So just to save some time I'm trying to paste the code here.
[06:19] You can see I have created three different variables with the name, noOfStudents, subjects,
[06:24] and totalSemesters.
[06:26] And inside these variables I'm trying to store various int values like two, four, five.
[06:31] As an excerpt, let me try to create a three dimensional array with the help of these three different
[06:38] lengths that I have.
[06:39] For the same, I need to mention three square brackets after my data type, so let me mention the same
[06:45] after that, I'm going to mention the array name as studentArray, and after this, on the right hand
[06:52] side, I'm going to mention the size details.
[06:54] The very first length I want to mention is noOfStudents, followed by subjects, followed by totalSemesters
[07:01] .
[07:01] With this I have a three dimensional array created as a next step
[07:06] I want to populate the data into these three dimensional array.
[07:09] So what is a three dimensional array?
[07:11] It is an array of 2D array.
[07:13] That's why first I need to create 2D arrays with the size as four and five.
[07:18] So let me try to create couple of 2D arrays along with the student to subject to mark details.
[07:24] I'm going to paste few lines of code here.
[07:26] Like you can see, this is not a super complex.
[07:28] I just created two 2D arrays with the name student one and student two.
[07:33] Inside these 2D arrays, I'm trying to store four different subject marks across five different semesters.
[07:41] So the same I have done for student2 as well. As a next step
[07:45] I want to store these 2D arrays inside my 3D array.
[07:48] So how to do the same?
[07:50] First we need to invoke the 3D array variable name followed by
[07:53] we need to mention the index as zero.
[07:56] And at this position we want to store the student1
[08:00] details.
[08:00] Similarly, let me try to store the student2 details at the index, one by assigning these student2
[08:09] 2D array that I have created previously.
[08:12] So now we have a complete proper 3D array available.
[08:16] Let's try to print out the same with the help of Arrays.deepToStirng() and to the same
[08:23] I'm going to pass studentArray as an input.
[08:26] If I execute this program, you will be able to see a three dimensional array.
[08:31] That's why you are able to see three square brackets here.
[08:34] So these are all the subject to marks of my student1 covering five different semesters.
[08:41] And very similarly these are the marks of student2 covering five different semesters.
[08:47] I hope you are clear how the three dimensional arrays they are going to work by this time
[08:52] it should have been pretty clear for you.
[08:54] As we try to add more dimensions to our arrays, the complexity is going to increase.
[09:00] That's why in real projects also at a max, developers will end up using 2D arrays or 3D arrays.
[09:06] So please make sure you are clear with all the concepts of multi-dimensional arrays that we have discussed
[09:12] so far.
[09:12] Because if someone tried to test your knowledge inside an interview around arrays, these are the toughest
[09:18] concept or questions that they can ask to put you in a tough situation.
[09:23] But with the discussions that we have done so far, you should be able to clear any question around
[09:28] the multi-dimensional arrays.
[09:30] I have a humble request here
[09:32] there can be a numerous examples around multi-dimensional arrays.
[09:36] I can't explain all of them.
[09:38] As an instructor, I can only teach you around the syntaxes and with a couple of examples and the responsibility
[09:45] of practicing lot many examples is going to be yours.
[09:49] That's why
[09:50] please search inside the web and try to practice multiple examples around any concept that we are going
[09:57] to discuss throughout the course that is going
[10:00] to make you as a better developer day by day.
[10:03] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
