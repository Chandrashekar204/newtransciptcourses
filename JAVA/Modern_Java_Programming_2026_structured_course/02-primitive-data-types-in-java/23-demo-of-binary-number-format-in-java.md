# 2.23 — Demo of binary number format in Java

> Section 2: Primitive data types in Java

[00:00] Let's see the demo of Binary number format for the same
[00:05] I came to my jshell and here I'm going to create a variable of data type int with the variable name
[00:11] as myBinaryNumber.
[00:14] To this I want to assign a binary number value.
[00:17] So what is the rule that we need to follow
[00:19] while we are trying to assign a binary number, it should have a prefix 0B, and the B can be in
[00:25] capital letter or in the small letter.
[00:27] After this prefix value you can mention your actual binary number.
[00:32] So here I want to mention a binary number 1101.
[00:36] And if I try to execute this command you can see I'm getting an output which is 13.
[00:41] So 13 is a decimal number value for the given binary number.
[00:45] So inside the binary numbers we know only zeros and ones are allowed, which means only two digits are
[00:52] allowed inside your binary number format.
[00:55] If you try to be oversmart and try to assign a value which is outside zero and one, you're going to
[01:01] get an compilation error.
[01:03] So let me try to assign some number here in the place of one,
[01:07] I'm going to mention three.
[01:08] And with this you should get an compilation error.
[01:11] I hope this is clear.
[01:12] As a next step, let's try to understand how to calculate a decimal number value from a given binary
[01:18] number.
[01:19] The steps are going to be very similar.
[01:21] In the very first step you need to identify your binary digits.
[01:24] Please make sure you have only zeros and ones.
[01:27] After that, you need to write down the powers of two, because inside the binary digit format, only
[01:33] two digits are allowed, which are zero and one.
[01:36] That's why we need to write down the powers of two for all the positions, or for all the numbers that
[01:42] you have inside your given binary number.
[01:45] Once you written down the powers of two, the very next step is to multiply and sum all the numbers
[01:51] to calculate the decimal value.
[01:54] Like you can see here, I have taken the same value which is 1101 is a binary number.
[01:59] Since we have four numbers, we need to write down four two powers like two power zero two, power one
[02:05] two power two, and two power three.
[02:06] To these two power values, we need to multiply with the digits present inside your binary number.
[02:12] So whatever you see inside the units, place that will go with that two power zero followed by two power one,
[02:18] two power two, two power three.
[02:20] And at last, if you sum all these numbers, you are going to get an output, which is an decimal representation
[02:26] of your binary number.
[02:28] The same
[02:29] we also validated with the help of Java code as well.
[02:32] With this, I'm assuming you are completely clear about what are the number formats that are supported
[02:38] by Java?
[02:39] What are the rules that we need to follow to represent various number formats, and what are the steps
[02:44] that you need to follow?
[02:45] Whenever someone asks you to convert a given number format to the default decimal number format, I'm
[02:52] assuming you're having fun.
[02:53] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
