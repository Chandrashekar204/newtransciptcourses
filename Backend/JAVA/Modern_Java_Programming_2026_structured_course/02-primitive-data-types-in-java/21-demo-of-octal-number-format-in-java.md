# 2.21 — Demo of octal number format in Java

> Section 2: Primitive data types in Java

[00:01] Let's see the demo of various formats that we have discussed in the previous lecture.
[00:06] The very first format demo that I want to do is with the help of Octal number format.
[00:11] So let me try to create an Octal number which is of type Integer.
[00:16] So here I'm going to mention int and the variable name is going to be myOctalNumber.
[00:24] And to this I'm going to assign an Octal number.
[00:27] So what is the rule that we need to follow.
[00:29] Whenever we want to assign an Octal number we should make sure there is a zero as a prefix post that
[00:36] there should be at least two numbers inside the Octal number.
[00:40] So here I'll give a number which is 346.
[00:43] So this is a valid Octal number.
[00:45] If I try to execute this you can see I'm getting the output two 230.
[00:49] So why this is because in Java by default Decimal number format is going to be used by your compiler.
[00:56] So that's why even though we are giving an Octal number as an input, we are getting the Decimal number
[01:01] as an output. In few seconds
[01:03] I'm going to explain you how this Decimal number is calculated from this Octal number.
[01:08] But before that let me show you other demos here.
[01:11] We know that inside Octal number format there are going to be eight digits 0 to 7.
[01:18] Anything above seven
[01:19] if you try to use inside your Octal number, it is going to be treated as an invalid number and your
[01:25] compiler is going to throw an error.
[01:27] So let me try to be oversmart here and I'll mention something like 348.
[01:32] So here three is a valid number, four is a valid number, but eight is not a valid number
[01:37] inside Octal format only 0 to 7 are the allowed values.
[01:42] So if I try to execute you can see I'm getting an compilation error.
[01:46] And the other rule that I have mentioned previously is after zero
[01:50] we should make sure there are at least two digits inside your Octual number, but in some scenarios
[01:56] your compiler may accept even with one digit
[02:00] also, after zero.
[02:01] Let me show you what are those some scenarios.
[02:03] So here, if I try to assign only zero three, there is no problem,
[02:07] you will get an output because up to the number seven both Octal numbers and Decimal number format,
[02:14] they are going to represent the same number.
[02:16] So here I'm going to mention again zero seven.
[02:19] It is going to work perfectly.
[02:20] But the moment I try to mention zero eight this number is going to be invalid because inside Octal number
[02:28] format eight is not allowed.
[02:30] This is one of the interesting question that you may face when you are dealing with the Octal number
[02:34] format.
[02:35] Though it is technically possible to use only one number after zero, but this is only allowed up to the
[02:41] number zero seven only.
[02:43] But beyond that, always you should make sure there are at least two digits inside your Octal number
[02:49] format.
[02:50] I hope this is clear.
[02:51] Now let's try to understand how this Octal number value is being converted into a Decimal number value.
[02:57] I'm going to take the same example, and I'll show you the list of steps that we need to follow whenever
[03:03] we want to convert an Octal number to the Decimal.
[03:06] The same steps is also followed by your Java compiler.
[03:09] In the very first step, we need to identify whether you are given number has Octal digits or not.
[03:15] So how to identify your number is going to start with a prefix of zero, and your number is also going
[03:20] to have numbers from 0 to 7 only.
[03:23] So please identify all the digits available inside your Octal number.
[03:28] After that, we need to write down the power of eight.
[03:32] Inside Octal number we have eight numbers.
[03:35] That's why each position value is going to be derived with the help of eight power.
[03:41] So first we need to start with eight power of zero, eight
[03:44] power of one, eight power of two.
[03:46] So if you have three digits you're going to write only eight, power of zero, eight power of one and
[03:51] eight power of two.
[03:52] So based upon your numbers inside your Octal number, you need to write corresponding number of eight
[03:57] power positions.
[03:59] Once you have written down all these powers of eight, you can try to multiply the given Octal digit
[04:05] with the corresponding eight power position.
[04:08] And at last you need to sum all those numbers.
[04:11] So let me show you an example here.
[04:13] So here you can see we have an Octal number which is 346.
[04:18] Inside Java we have to represent as 0346.
[04:21] But in traditional mathematics we are going to represent as 346.
[04:26] And we are going to put eight in that down.
[04:28] So how to convert this into a Decimal number.
[04:31] First you can see I have written eight power of zero, eight power of one and eight power of two
[04:36] because I have only three digits.
[04:37] Now at the units place we have the number six.
[04:41] So we need to take that six and multiply with the eight power zero.
[04:45] Similarly, in the tens place we have four,
[04:47] that's why we need to multiply that with eight power one followed by in the hundreds place we have three.
[04:53] We need to multiply that with eight power two.
[04:55] So this way you need to keep on adding and multiplying based upon your number of digits
[05:00] inside your Octal number.
[05:02] And at last, if you perform the sum of all the numbers, you are going to get the Decimal number value.
[05:08] So what is the Decimal number value for 346 of Octal number it is 230, the same we saw previously with
[05:15] the Java code as well.
[05:17] So right now I'm acting as your mathematics teacher.
[05:20] Apart from teaching you Java, I'm also right now teaching you mathematics.
[05:25] Hope you liked your new mathematics teacher.
[05:27] I'm assuming this is very clear to you.
[05:29] Like how to represent an Octal number and how to convert that into a Decimal number value.
[05:34] Please have this information always handy so that you can easily answer the questions related to these
[05:40] concepts, like Octal to Decimal.
[05:42] I hope this is clear.
[05:43] In the next lecture, let's continue with the demo of Hexadecimal format.
[05:48] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
