# 2.22 — Demo of hexa number format in Java

> Section 2: Primitive data types in Java

[00:00] Inside this lecture,
[00:01] let's see the demo of Hexadecimal number format.
[00:04] Here I am going to create an int variable.
[00:07] The variable name is going to be myHexaNumber.
[00:12] And to this variable I'm going to assign an hex number.
[00:15] So what is the rule that we need to follow while we are trying to assign an hex number there should
[00:20] be a prefix which is 0X.
[00:22] The x can be in capital letter or in small letters,
[00:26] it's up to you.
[00:27] After this you can mention your hex number.
[00:29] So here I'm going to mention 1A3.
[00:32] So these are random number that I have selected.
[00:35] So if I try to execute this I'll get an corresponding representation of Decimal number value.
[00:40] So what is the Decimal number value for this, 419.
[00:42] Inside Hexadecimal format the valid values are 0 to 9 and a, b, c, d, e, f.
[00:50] Outside these digits and characters,
[00:52] if you try to use something else, then definitely you're going to get an compilation error.
[00:56] Let me show you that very quickly.
[00:58] Instead of a if I change this to H, then I'm going to get an error because H is not an valid value
[01:06] inside the Hexadecimal format.
[01:09] I hope this is clear.
[01:10] Now let's try to understand what are the steps that we need to follow whenever we want to convert an
[01:15] Hexadecimal number to normal decimal number value.
[01:18] I'm going to be your mathematics teacher again in the very first step, like we discussed previously.
[01:24] First, we need to identify whether the given number is a valid Hexadecimal number or not.
[01:29] So what are the valid values that are allowed inside hex digits?
[01:32] Inside the hex digits, 0 to 9 and letters A to F?
[01:36] The A to F can be in capital letters or in the small letters.
[01:40] So these eight f represents a value 10 to 15.
[01:43] So a means 10 b means 11.
[01:46] So the same mapping we need to be aware to calculate that decimal value from an Hexadecimal number.
[01:52] Once you identify whether you are given Hexadecimal number is valid or not, you can write down the
[01:57] power of 16.
[01:59] Why 16?
[02:00] Because inside Hexadecimal there are total 16 different digits or characters.
[02:05] That's why we need to write down the power of 16.
[02:08] So inside octal we followed eight, whereas in decimal it is going to be ten.
[02:12] In normal numbers we always have units digit which is ten power, zero which is one, and ten digit
[02:18] which is ten, power one, and 100 digits, which is ten, power two and thousands digit, which is
[02:24] ten power three.
[02:24] So this way in normal decimal number, we are going to represent the value with the help of ten, because
[02:30] inside normal decimal format total ten digits are allowed, which are from 0 to 9.
[02:35] But coming to the Hexadecimal, we need to make sure we are writing down the powers of 16.
[02:39] Once you write down these powers of 16 based upon the number of digits available inside your hex number,
[02:45] you can try to convert the Hex letters to that Decimal numbers.
[02:49] Like I said, whenever you see A, please consider that A as 10, B means 11, C means 12, D means
[02:56] 13, E means 14, f means 15.
[02:59] Once you convert your hex letters to decimal as a next step, you can try to multiply and sum all your
[03:06] 16 powers with the actual hex digits that you have inside your input.
[03:11] At last, you are going to get an output, which is going to be your Decimal number value.
[03:16] Here I have given an example for a sample hexa number which is 1A3, so three is at units place, a is
[03:23] in the tens place and one is in the hundreds place.
[03:26] That's why I'm trying to multiply them with 16 power zero, 16 power one and 16 power two.
[03:31] And at last, if you try to add all of them, you are going to get an output which is 419, which is
[03:37] in the format of Decimal number format.
[03:40] In the same we also saw in that Java as well, the same output we are getting, and this confirms our calculations
[03:45] are correct.
[03:46] I hope this is clear.
[03:47] Let's see the demo of binary format in the next lecture.
[03:52] Thank you.
[03:53] Bye.

----------------------------------------
