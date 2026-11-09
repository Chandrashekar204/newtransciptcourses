# 2.14 — Demo of byte, short, int and long primitive data types

> Section 2: Primitive data types in Java

[00:00] Inside this lecture, let's see the demo of integer primitive data types.
[00:04] The very first data type that I want to use here is byte.
[00:08] Using byte we can store a maximum of 256 numbers.
[00:13] So the range is going to be -128 to 127.
[00:18] I already explained you previously how this min value and max value is derived for any integer base
[00:24] two primitive data type.
[00:26] If you have any questions, please rewatch the lecture where I introduce about the primitive data types
[00:32] very first time.
[00:33] Here first, I'll try to mention what is a primitive data type, which is byte and post that I'm going to
[00:39] create a variable which is age.
[00:41] So for age I know maximum number always is going to be 100 at max it can be 120.
[00:48] I know there are no scenarios where a person can live more than 127 years.
[00:53] That's why I'm trying to use byte here to store the age details of a person. If needed
[00:59] if you want to provide more context like whose age it is, is it related to a person or an animal?
[01:05] In such scenarios, you can mention age of person is equal to,
[01:10] I'll just mention some random age which is 30.
[01:13] So if I try to print this statement, you can see I'm going to get a variable which is going to hold
[01:19] the byte value, which is 30.
[01:21] What happens if I try to assign a number which is outside the range of byte. For the same,
[01:28] let's see what is going to happen.
[01:30] Obviously you can expect a compilation error.
[01:32] So I'm just going to mention 128 which is outside the range of byte.
[01:37] You can see I'm getting a compilation error here.
[01:40] I also mentioned you previously.
[01:41] There is an option inside Java to understand what is a min value or max value of a particular integer
[01:48] primitive data type.
[01:49] So what is that option with the help of wrapper class?
[01:52] So for byte data type, what is a wrapper class.
[01:55] It is going to be Byte only but the B is going to be capital.
[02:00] So this is the class name.
[02:01] Inside this class I have a variable with the names min value and max value.
[02:07] So first let me try to invoke MIN_VALUE.
[02:10] So after typing min I'm just going to press tab.
[02:14] And you can see automatically it is populating the entire variable name.
[02:18] So if I try to execute this statement you will be able to see what is the minimum value that we can
[02:24] store with the help of byte.
[02:25] So here what is the minimum value -128.
[02:29] Very similarly we can invoke the next constant which is MAX_VALUE.
[02:35] And this will show you what is the maximum value that we can store.
[02:38] The maximum value that we can store is 127.
[02:41] Don't worry about these $103, $102.
[02:45] So these are the memory locations where my jshell is trying to save this information of min value and
[02:51] max value, because I'm not trying to assign this value to any other variable.
[02:56] That's why internally jshell is trying to assign them to the memory locations like $102,
[03:02] $103.
[03:03] So now very similarly we can create variables for short as well.
[03:08] So for short this time I'm going to consider a variable which is totalStudents I want to store.
[03:16] What are the total number of students that are studying in a particular school or a college?
[03:22] Since I am sure that a school or a college may not have more than 30,000 active students, that's why
[03:28] I'm using short here.
[03:30] So let me try to assign some value here.
[03:32] Maybe I'll just assign some 1234.
[03:35] And if I try to execute this you can see I'm getting an output.
[03:38] And just like how we saw min value and max value for byte, very similarly we can see for short as well.
[03:44] For the same we need to use a Short of wrapper class.
[03:46] The S is going to be capital.
[03:48] So first we need to mention what is the Java class name and post that
[03:52] what is our static variable available inside this Short class.
[03:56] So I'm trying to press enter here.
[03:58] And you can see this is a minimum value.
[04:00] And very similarly if you want to understand what is the maximum value, you can also find it with the
[04:06] help of this max variable available inside the Short class.
[04:10] Now let's try to jump on to the int primitive data type.
[04:13] Before that let me clean my jshell.
[04:16] So here I'm going to create an integer variable with the name total audience.
[04:23] So I just wanted to store how many audience are seeing a particular game inside a stadium.
[04:28] Since there is a very good chance the audience can be more than 32,000, which is going to be outside
[04:35] the short variable range, I need to use int here.
[04:38] That's why with the help of this int, I'm going to store some random number to indicate how many audience
[04:45] are watching the game live inside the ground.
[04:47] So the same is going to be assigned to this variable.
[04:50] If you want to check what are the min and max values, we can use the wrapper class of int.
[04:55] So what is a wrapper class of int?
[04:57] It is going to be Integer, not int.
[04:59] So we need to invoke the class which is Integer.
[05:03] I is going to be capital letter.
[05:05] And inside this class we have variables which are MIN_VALUE.
[05:10] I press shift tab by mistake.
[05:12] So let me press tab this time by just mentioning MIN.
[05:16] And you can see the variable name populated automatically by jshell.
[05:20] So you can see this is the minimum value.
[05:22] Very similarly we can try to identify what is our maximum value.
[05:26] So this is the maximum value.
[05:28] Always please note that the positive number is going to be minus one off negative number.
[05:35] Because the positive number range is going to be started from zero.
[05:39] Now let me try with some negative numbers.
[05:41] As of now we are only trying with positive numbers.
[05:44] We can also store negative numbers inside the int, byte, short and long.
[05:49] For example, I can try to create a variable with the name negative num and to this variable I can randomly
[05:58] assign some negative number and you can see in the output
[06:02] also I'm getting the same negative number.
[06:04] With this, we explored enough examples on the int data type as well. As a next step
[06:09] let's try to see the demo off long data type as well.
[06:13] For the same, I'm going to create a long variable here.
[06:17] The long variable name that I'm going to give here is totalNumOfTrees.
[06:22] So I want to assign total number of trees available on the earth to this variable.
[06:28] First let me start with some small number which is within the range of integer number.
[06:33] So here I'm going to give some number.
[06:35] And this number should be within the range of integer.
[06:39] If I try to execute this command you can see it is working fine.
[06:43] That means I'm able to assign a number to my long.
[06:47] Now let's try to assign a number which is outside of the range of integer.
[06:52] This time I'm going to execute the same command, but I will take the maximum value of integer.
[06:58] And to this I'm going to add one.
[07:00] That means the number is going to become 648.
[07:04] If I try to assign this number, you can see I'm getting an error integer number too long.
[07:09] But if you see here on the left hand side I have given long, my long should be able to accept this
[07:15] number.
[07:16] Then why we are getting this error.
[07:18] This is because in Java by default, all the whole numbers without any decimal values will be considered
[07:25] as int data type values.
[07:27] So since compiler is treating this number as int data type value, it is also trying to convert this
[07:34] number total number of trees to into data type variable to save some memory on the system.
[07:41] So the solution for this is
[07:42] we need to make sure we are appending the l as a suffix towards the end of the number to convey that
[07:50] I want to store a long number.
[07:52] So please treat my total number of trees variable as a long data type only.
[07:58] So let me clean my console post that I'm going to run the same command, but this time I'm going to
[08:04] give the suffix which is L.
[08:06] It can be a L or l as well, but if I type small l it is going to look like a one.
[08:13] So since it is going to create a confusion to other developers, I will always advise you to use
[08:19] L.
[08:19] So let me execute this.
[08:20] This time you should not get any error because we are clearly telling to the compiler this is going
[08:27] to be a long number, otherwise it is always going to treat it as int data type.
[08:33] As a next step, can we see the minimum value and maximum value supported by long?
[08:37] Let's do that.
[08:38] So what is the class name of long.
[08:40] So the class name of long data type is Long itself.
[08:43] But the L should be in capital.
[08:46] So every class name inside Java always starts with a capital letter.
[08:50] So this is a information that I want to share.
[08:52] I know we are yet to discuss about classes, but I'm trying to leak some information here because we
[08:58] both are friends.
[08:59] After mentioning these Long class name, I need to mention dot and what is the variable name that I
[09:05] want to invoke?
[09:06] The variable name is going to be same in all classes, so the minimum value variable is MIN_VALUE.
[09:12] So if I try to invoke this you can see this is the minimum value.
[09:16] It is such a big number which can handle any kind of data inside your business applications.
[09:22] Very similarly let's look for maximum value
[09:24] also you can always expect what is the maximum value.
[09:28] It is always going to be one minus with this minimum value.
[09:32] That's why we are seeing here 807.
[09:35] With this we saw the demo off all the primitive data types that are available under the Integer type.
[09:41] Before I try to close this lecture, I want to show you a slide which I have prepared with the details
[09:46] about the importance of L suffix that we need to follow while we are trying to create long variables.
[09:53] So whatever we have discussed, I have mentioned the same inside this slide for your reference so that
[09:58] in future when
[09:59] you are trying to brush up your knowledge,
[10:02] this information is going to be available at your hand.
[10:05] I hope you are enjoying the course.
[10:07] I'm also enjoying this course a lot because I'm able to share lot many information to you, and I'm
[10:13] playing a part inside your Java journey.
[10:15] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
