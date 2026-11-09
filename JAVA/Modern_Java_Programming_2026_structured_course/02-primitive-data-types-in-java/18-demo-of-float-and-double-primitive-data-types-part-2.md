# 2.18 — Demo of float and double primitive data types - Part 2

> Section 2: Primitive data types in Java

[00:00] Inside this lecture, I'm going to take some tricky scenarios and give more details about the same,
[00:06] so that these tricky scenarios is going to help inside your interviews.
[00:10] Using float or double, we can create a positive zero and negitive zero.
[00:15] So let me show you what I mean here.
[00:17] For the same,
[00:17] first I'm going to create a new variable and this variable name
[00:21] I'll just keep it as positiveZero. To this positiveZero variable
[00:26] I'm going to assign a positive zero which is 0.0f.
[00:32] And with this this value is going to be assigned to my positiveZero.
[00:36] Very similarly
[00:37] this time I'm going to create negitive zero.
[00:40] So the variable name is going to be negitiveZero.
[00:43] And the value I'll mention as -0.0 f.
[00:47] So if you see here the output we got is different.
[00:51] But if you try to compare both these two numbers are these two variables
[00:55] they are equal.
[00:56] So inside Java whenever you mention 0.0 or -0.0, it is always going to be treated as a 0.0 itself.
[01:05] I can also show you the output by trying to compare these two variables.
[01:10] To compare two variables, you can always use double equal symbol (==) using the same,
[01:16] I'm trying to compare here.
[01:18] So the first variable name that we have here is positiveZero.
[01:21] Let me copy this and paste it here and post that I'll mention two double equal.
[01:26] And after that I'm going to mention the second variable name which is negitiveZero.
[01:30] So if I try to execute this Java statement you can see I'm getting an output which is true.
[01:36] That means both these numbers are being treated as a same numbers by the Java compiler.
[01:42] The same applies for double as well.
[01:45] Let me show you that very quickly.
[01:47] For the same first I'm going to create a first variable which is double positiveZero.
[01:52] For double, we don't have to mention the suffix I'm deleting this and creating this variable
[01:57] and after this I'm going to change this variable to negitiveZero.
[02:03] After changing this to negitiveZero I'm going to mention minus here and execute this command.
[02:09] Now I'm going to run
[02:10] the positiveZero == negitiveZero.
[02:14] And this is also going to give true as an output.
[02:18] I'm going to discuss various operators that we have inside Java in the coming sections.
[02:22] But for now please note that using two equal symbols, we can always compare two variables and two numbers,
[02:29] whether they are equal or not.
[02:31] Now let's go to the next scenario for the same
[02:34] let me clean my console.
[02:36] This time I'm going to show you a demo.
[02:38] What is going to happen if I try to divide a float or double number with 0.0.
[02:44] So let's try to see what is going to happen.
[02:46] For the same, I'm going to give a float data type, and the variable name I'll give is positiveInfinity.
[02:54] To this variable,
[02:55] I'm going to pass one float value which is like 1.5 f.
[03:00] This float value I'm going to divide with 0.0f.
[03:05] So let's see what is going to happen.
[03:07] So to divide a number inside Java we can use this forward slash.
[03:12] So if I try to execute these statements you can see I'm getting the infinity which is like a positive
[03:19] infinity as an output.
[03:20] If I try to execute the same with -0.0f, this time I'm getting negative infinity.
[03:29] Now let's try to see what is going to happen
[03:31] if I try to mention 0.0 both in numerator and denominator.
[03:36] So here I'm going to mention 0.0 inside numerator and denominator.
[03:43] This time the output is going to be NaN.
[03:46] So what is the meaning of NaN inside Java NaN means Not a Number.
[03:51] So this is the output that you can expect for this scenario.
[03:54] The same applies for double data type as well.
[03:58] You can test these three floors by using double value.
[04:02] So please don't mention f suffix.
[04:04] And with that you should be able to see the same output.
[04:08] So please pause the video and try the same if you are interested.
[04:11] Sometimes whenever you want to compare a particular arithmetic expression resulted in an positive infinity
[04:19] or negative infinity or a Not a Number.
[04:21] So for such comparison scenarios, float and double wrapper classes have some variables.
[04:28] Let me show you those variables. For the same,
[04:30] first I'm going to invoke the Float class.
[04:32] After this Float class, I'm going to invoke the constant which is POSITIVE.INFINITY.
[04:38] So this is going to give what is a positive infinity value.
[04:42] So using this variable you can always compare whether a given output is equal to positive infinity or
[04:48] not.
[04:49] Very similarly we also have negative infinity inside the Float class.
[04:54] And this is going to give the negative infinity as an output.
[04:58] And at last we also have a constant.
[05:00] With the name NaN.
[05:03] So this is going to give the output as not a number.
[05:07] So these three constants are also available inside the Double class as well.
[05:11] So these are the some tricky questions you may face inside the interviews.
[05:15] If you want you can validate the constants available inside the Double class.
[05:20] Now let me clean the console by pressing command k.
[05:23] And now I'm going to show you the next scenario.
[05:27] This scenario is going to be super interesting.
[05:30] Think like I'm trying to create two numbers.
[05:32] One is of type float,
[05:34] the variable name here I'm going to give as num1.
[05:37] And for this variable I'm going to assign the value which is 3.14f.
[05:43] As a next step I'm going to create the next variable with the name num2.
[05:47] And this time the num2 data type is going to be double.
[05:51] And the value that I want to assign here is the same value like 3.14.
[05:55] If you observe the output from the both statements, they are looking like very similar, like 3.14
[06:02] here and 3.14 here.
[06:04] If I try to compare these two numbers, you may think like we are going to get true as an output because
[06:11] they both are looking very similar.
[06:13] Let's see what is going to happen.
[06:15] So I'll just do num1 == num2.
[06:19] So with this I'm trying to compare whether the num1 is exactly same as num2.
[06:25] And you can see I'm going to get an output which is false.
[06:29] That means they are not same.
[06:31] So why this is happening.
[06:33] Because behind the scenes the way float and double they stored the number is going to be different.
[06:39] That's why they will always some difference between them.
[06:43] That's why inside Java always don't try to compare double and float numbers with each other.
[06:50] By assuming the content is same, they should give a proper true output.
[06:55] It is never going to happen.
[06:56] You should always use greater than or less than symbols to compare float and double values.
[07:03] If you try to build some looping logic inside Java, that is going to run continuously until your float
[07:10] and double numbers are going to become equal, then you will end up running your code continuously.
[07:17] Your loop is never going to stop.
[07:20] So what is a loop inside Java?
[07:22] Using loops inside Java, we can continuously run a business logic until a specific condition met.
[07:28] If you define the condition as that your float and double number has to be equal, then your loop is
[07:35] never going to stop.
[07:36] You are going to run it infinitely.
[07:38] We're going to discuss about loops in the coming sections, but for now, I'm just trying to give you
[07:43] some details about this scenario.
[07:45] I hope this is clear.
[07:46] Now let me give the last demo as part of this lecture.
[07:50] We know inside integer data types any whole number that we define
[07:55] by default it is going to act as integer.
[07:58] Very similarly, inside the real numbers or inside the decimal numbers
[08:02] by default, every number is going to act as a double data type value.
[08:07] So inside interviews people may ask you what is going to happen if I try to multiply a double number
[08:14] with a integer value?
[08:16] So let's try to understand more about this scenario.
[08:19] So here I'm going to create my first variable of data type double.
[08:24] The variable name is going to be myDoubleNum.
[08:28] And the number that I'm going to mention here is 10.0.
[08:32] After mentioning this number I'm going to create an int variable and the int variable name is
[08:39] going to be myIntNum and to this integer variable I'm going to assign a number which is 9.
[08:46] So there is no issue like we declared and initialized double and int variables independently.
[08:53] Now the question is what should be the output?
[08:56] If I try to multiply these two variables?
[08:59] First, let me try by using int as an output.
[09:03] So here I'm trying to create a variable as int result.
[09:06] To this result variable I will try to pass the output, which I'm going to get after multiplying the
[09:13] two variables that I have created here.
[09:16] The very first variable is my double number and the symbol that we need to use inside Java to multiply
[09:22] two numbers is asterisk (*).
[09:24] And what is the second variable that we have here?
[09:26] myIntNum
[09:27] So let me mention the same and post that
[09:30] if I try to execute this command, you can see I'm getting an output because based upon this multiplication
[09:38] I'm going to get the output as 90.0.
[09:41] If I try to assign that to the integer result, I'm going to lose some decimal values.
[09:46] Think like
[09:47] I have mentioned the double number as 10.2.
[09:50] In such scenarios the output is going to be 90.2, and if my compiler allowed this conversion
[09:56] to the result, I'm going to lose that decimal value
[10:00] and my output is going to be 90 only, which is not correct.
[10:04] That's why Java Compiler is simply throwing an compilation issue.
[10:09] Now, as a next step, I can try to change this result to the data type double and this time see what
[10:15] is going to happen.
[10:16] We are going to get the successful response which is 90.0.
[10:19] This means always if you try to multiply a double with int or float with the int, please make sure
[10:27] you are trying to catch that result with the help of double or float.
[10:33] Otherwise, your compiler is not going to accept because you're going to lose the decimal values present
[10:40] inside your output.
[10:41] There are certain approaches on how to communicate to compiler to allow these kind of operations, like
[10:48] for your business logic, if you're not going to consider your decimal values, then you can communicate
[10:53] to the compiler.
[10:54] Please allow these conversion from double to int by following a process called casting.
[11:01] So we're going to discuss about that casting in the coming lectures.
[11:04] But for now please note about this scenario and please answer any questions that you may face around
[11:09] this scenario inside your interviews.
[11:12] I hope you are clear about all the scenarios that we have discussed inside this lecture.
[11:17] For your reference, I also mentioned all the details that we have discussed inside these slides.
[11:22] In this slide, I discussed about the positive infinity negative infinity, not a number.
[11:27] Whereas in the next slide I discussed about the what will happen if you try to compare double and float
[11:34] values inside a loop.
[11:36] And at last I also mentioned the last scenario details, where we are trying to multiply a double number
[11:42] with the int number, so please have them as a reference.
[11:45] I hope this is all making sense to you.
[11:47] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
