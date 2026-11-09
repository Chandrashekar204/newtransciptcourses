# 2.16 — Introduction to floating data types

> Section 2: Primitive data types in Java

[00:00] As of now, we discussed about the primitive data types that are going to help us to store the whole
[00:05] numbers.
[00:06] But how about real or decimal numbers?
[00:09] To store the real numbers
[00:10] we have two primitive data types under the name floating point.
[00:14] So with the help of the data types available inside the floating point, we can store real or decimal
[00:20] numbers in Java.
[00:22] So there are two primitive data types that are going to support under this floating point.
[00:27] The very first data type is float and the second one is double.
[00:30] So there is some difference between this float and double.
[00:33] Just like how we have size difference in between int and long.
[00:37] Very similarly, in between float and double we have a size difference.
[00:41] The size of float is four bytes, whereas the size of double is eight bytes.
[00:45] Apart from the size and range of numbers supported by this data types, there is also one more difference,
[00:51] which is precision.
[00:52] We know inside fractional numbers or decimal numbers.
[00:56] We can have the decimal value even up to the 50 numbers.
[01:00] So if you are looking for a lower precision up to seven decimal digits, then you can always go with
[01:06] the float data type.
[01:08] Otherwise, if you are looking for more precision with more number of decimal values, then you can
[01:13] go with the double.
[01:15] Double is going to support that decimal values up to 15 digits, just like how other primitive data
[01:21] types hasMIN_VALUE and MAX_VALUE constants.
[01:24] Very similarly, the wrapper classes of float and double data types also have these static variables,
[01:31] which we can use to understand what is the minimum value and the maximum value supported by the float
[01:38] and double data types. Inside whole numbers,
[01:41] by default, every number that you are going to write is going to act as an int value.
[01:46] If you want a specific whole number to be acting as an long value, then we need to mention the suffix
[01:53] of l, very similarly inside that decimal values
[01:57] also, by default, all your decimal values are going to act as a double data type.
[02:03] But if you want to treat a specific decimal number using float data point, then it is mandatory to
[02:10] mention the suffix f either in small case letter or in the capital case letter after your decimal number.
[02:17] Mentioning d suffix value
[02:19] for the double numbers is completely optional, even if you don't mention your Java compiler by default
[02:26] is going to consider all your decimal numbers as double only.
[02:30] In the case where you want your compiler to consider a specific decimal number as a float, then you
[02:37] should definitely mention the suffix as f after your decimal number.
[02:42] So let's try to see the examples on how we can declare floating point variables and values.
[02:48] So here you can see I'm trying to declare a variable f of type float.
[02:54] Since I want my decimal number to act as a float value, it is mandatory to mention the f suffix value
[03:02] at the end of the decimal number value.
[03:04] Very similarly, in the next variable where I'm trying to use d, I'm trying to mention the suffix with
[03:09] the capital letter F, so regardless you use small letter or capital letter, the effect is going to
[03:15] be same.
[03:16] But coming to the double, you don't have to mention any suffix, because by default all the decimal
[03:22] numbers are real
[03:23] numbers are going to be considered as a double.
[03:25] So inside all my presentations I'm not going to follow the naming standards for my variables.
[03:31] So here you can see I have used a simple variable names like f, d, a.
[03:36] Whereas when I try to give the actual demo, I will follow the naming standards because I want to keep
[03:42] my presentation as simple as possible.
[03:44] If I try to use bigger numbers sometimes it may take a lot of space inside the presentation.
[03:50] That's why please ignore the naming standards that I'm following inside my presentation.
[03:54] Please always follow the naming standards that I'm going to use inside the demos.
[03:59] I hope this is clear.
[04:00] So with the help of float and double, we can define decimal numbers, but sometimes we may need some
[04:07] more precision beyond 15 decimal digits.
[04:11] For such scenarios, we have a Big Decimal available inside the Java library.
[04:17] In the scenarios where you are looking for more precise values for any scientific calculations or currency
[04:23] calculations, it is always recommended to use BigDecimal, which is one of the class available inside
[04:29] the Java library.
[04:30] We are going to discuss about these in the coming sections, but for now let's focus on simply on float
[04:36] and double only.
[04:38] Let's go to the next slide where I want to show you the difference between float and double by using
[04:44] a picture.
[04:45] So here you can see whenever you have a confusion on which data type to use to store a decimal number.
[04:52] Always remember this image.
[04:54] You can see float is capable of providing a smaller precision up to
[05:00] 7 digits, whereas double is capable of providing more precision up to 15 digits.
[05:06] In general, using double is a better choice than float because it is going to provide higher precision.
[05:13] A wide range of values and a greater accuracy.
[05:17] I hope you are clear with these discussion.
[05:19] In the next lecture, let's see the demo of float and double data types by using jshell.
[05:25] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
