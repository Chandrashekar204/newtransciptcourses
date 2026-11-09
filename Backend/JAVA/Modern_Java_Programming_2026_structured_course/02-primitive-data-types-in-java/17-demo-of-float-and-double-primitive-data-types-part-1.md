# 2.17 — Demo of float and double primitive data types - Part 1

> Section 2: Primitive data types in Java

[00:00] Now inside this lecture let's see the demo of float and double data types.
[00:05] First I'm going to create a variable of type float.
[00:09] The variable name I'm going to give as piValue.
[00:13] Inside mathematics we have a pi constant.
[00:16] So what is the value of pi,
[00:17] it is 3.14.
[00:20] So if I try to mention this value directly I will get an compilation error.
[00:24] Because like I said before, by default all decimal numbers are real
[00:29] numbers are going to be considered as a double value.
[00:32] So to communicate to my Java compiler that these 3.14 should be treated as a normal float value, then
[00:40] I need to mention a suffix f.
[00:42] It can be in smallcase or uppercase.
[00:45] Once you mention the suffix, you should not get any compilation errors.
[00:49] You can see I'm getting a successful output.
[00:53] Now very similarly, whenever you want to create a variable of type double, you need to use double,
[01:00] and what is a variable name?
[01:02] So the variable name I'm going to use as piValue only.
[01:05] And this time I'm going to mention the piValue as 3.14 only without mentioning any suffix.
[01:12] And with this I should get a successful response.
[01:16] So this is pretty straightforward
[01:17] just like any other primitive data types, we can create variables or identifiers and assign data or
[01:25] literals to them.
[01:26] Now as a next step, let's see the what are the minimum and maximum values that are supported by the
[01:32] float and double.
[01:33] So there is a wrapper class for float data type.
[01:36] The class name is going to be Float only, but the first letter is going to start with capital letter.
[01:43] After mentioning this Float class name, you need to invoke the static variable which
[01:51] MIN_VALUE.
[01:52] So let me try to execute this statement.
[01:54] You can see this is the minimum value that is supported by the Float.
[01:58] This minimum value is represented with the help of exponential form.
[02:03] So the number is 1.4E-45.
[02:10] As a next step, let's try to see the what is the maximum value supported by the Float.
[02:15] So if I try to execute, if you see this is the maximum value supported by the Float, you'll be able
[02:21] to see there is a E to the power of 38.
[02:23] Since my jshell cannot display the power number, it is simply showing the 38 immediately after E, but
[02:31] ideally the number is a very higher number because it is going to multiply this number with E to the
[02:38] power of 38.
[02:39] As a next step, let's check the same minimum and maximum value for double as well.
[02:45] For the same, we need to use a class name which is Double, and inside this Double class we have minimum
[02:51] value and this is the MIN_VALUE
[02:54] You can see the power that we have to the E is -324.
[02:59] Now let's see the MAX_VALUE
[03:01] also, the maximum value that is supported by the Double is,
[03:05] this is the number where it has an exponential power of 308.
[03:10] I hope this is clear.
[03:11] As a next step, let me show you a demo which will give more clarity about the difference between the
[03:16] Float and Double data type.
[03:18] If you google for precise value of pi, Google is going to give you the precise value with up to 50
[03:25] digits.
[03:26] So let me copy this entire number the same I will try to use to assign to my Float and Double data types
[03:33] and post that you can see what is the difference between them.
[03:37] So first I'll try to create a variable of type float.
[03:40] To this I'll just do as piNum.
[03:43] After this variable name,
[03:45] I'm going to mention the complete pi value that we copied from the Google.
[03:49] Since we are trying to declare this as a float variable, we need to mention the suffix f, and if I
[03:56] try to execute this command, you can see we are getting an output and inside the output the float data
[04:03] type is only storing the decimals up to seven digits 1234567.
[04:09] Whereas if I do the same for double, you will be able to see that double is maintaining the precision
[04:17] of decimal numbers up to 15 digits.
[04:20] So you can see the precision maintained by the double is more accurate.
[04:25] So as a developer you have to decide if you are looking for a more precise values.
[04:31] Then always go with the double, especially if you are working on projects related to financial transactions
[04:38] that involves currency
[04:39] then always go with the double compared to float.
[04:42] Otherwise, if you are fine having a precise value up to seven decimal digits, you can always go with
[04:48] the float data type.
[04:50] One more important information that I want you to observe here is 3 is a very small number.
[04:55] Both float and double should be able to accommodate.
[04:59] So here
[05:00] size doesn't matter.
[05:01] What matters here is the accuracy of the decimal numbers that is going to provided by your float, and
[05:09] double float is going to provide the accuracy up to seven digits, whereas double is going to provide
[05:15] the accuracy up to 15 digits.
[05:18] That's why regardless of how small your number
[05:21] always consider the accuracy as well.
[05:24] Before you try to decide whether to use float or double data type with these examples and demo, I'm
[05:30] assuming that you are right now clear about when to use float and when to use double.
[05:35] Let's continue this discussion around float and double in the next lecture as well.
[05:40] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
