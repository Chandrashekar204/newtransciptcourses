# 2.24 — Type casting in Java

> Section 2: Primitive data types in Java

[00:00] Now, inside this lecture let me introduce a concept called typecasting in Java.
[00:05] So what is casting ?
[00:08] Inside Java whenever you are trying to assign a value of one primitive data type to another type, we call it as
[00:14] typecasting.
[00:15] For example, you can try to assign a float value to the int data type very similarly
[00:21] you can also try to assign an integer value to the float data type.
[00:25] So here what we are trying to do.
[00:27] We are trying to assign a value of one primitive data type to another type.
[00:32] So these kind of scenarios we call it as typecasting.
[00:35] So there are two types of casting available inside Java.
[00:38] The very first one is widening casting.
[00:41] And this one is going to happen automatically.
[00:44] That's why we call it as automatic casting or implicit casting.
[00:49] The Java compiler is not going to complain or throw an any error whenever these widening casting is
[00:55] happening.
[00:55] So what is widening casting?
[00:57] If you are trying to convert a smaller type to a larger type size, such casting, we call it as implicit
[01:04] casting or widening casting.
[01:06] Why this is done automatically is it is safe because there is no chance of losing data.
[01:12] Think like you are trying to assign a byte value to the short, so whatever byte is capable of storing
[01:18] short is also capable of storing.
[01:20] That's why byte to short will not have any chance of losing the data and similarly short to car, car to int,
[01:26] int to long, long to float, float to double.
[01:30] If you want to compare widening casting to some real life scenario, think like you're working in an company.
[01:35] Based upon your smart work,
[01:37] someone is trying to promote you to the next position.
[01:40] So in such scenarios, are you going to oppose?
[01:43] Off course not, because you will be more than happy to get promoted.
[01:47] So the same is going to happen here.
[01:49] The byte value is get promoted to the short
[01:52] or you can also promote an int value to the long data type or long value to the float data type.
[01:58] So in all these kind of scenarios, since there is no chance to lose data, the widening casting or
[02:04] implicit
[02:05] casting is going to be done by your Java compiler without any complaints.
[02:09] But if you try to do the other way, like converting a large type to a smaller size type, then we call
[02:16] that casting as narrowing casting or manual casting or explicit casting.
[02:21] Whenever you are trying to convert a large type to a smaller size type, then compiler will not accept
[02:27] because there is a chance of losing that data.
[02:30] Think like you have a float value, which is 3.14 if you're trying to convert that to a long or int,
[02:37] definitely you are going to lose that decimal values.
[02:40] You are simply going to get the whole number from the float value.
[02:44] So since there is a chance of loss of data in these kind of scenarios, the developer has to explicitly
[02:51] or manually, he has to perform the narrowing casting by following a syntax. With the narrowing casting
[02:57] syntax the developer is conveying to the Java compiler, I am fine to lose some data during the conversion
[03:04] from larger type to a smaller type, since the developer itself is fine to lose the data, the Java
[03:09] compiler is not going to complain anything.
[03:12] But if the developer is trying to simply assigning a large type value to a small size type value without
[03:18] casting, then compiler will throw an error.
[03:21] So we're going to see that in the demo.
[03:23] So narrowing casting is like a demotion.
[03:26] So someone is trying to demote you in such scenarios
[03:29] are you going to accept?
[03:30] Off course not.
[03:31] You will ask them what is the reason why you want to demote me?
[03:34] What mistake I have done?
[03:36] Only when you're satisfied with the reason, then only you're going to accept that decision.
[03:41] Very similarly, Java compiler also is not going to accept the narrowing casting by default until unless
[03:48] the developer is explicitly telling to the compiler, please do the narrowing casting and I'm fine to
[03:54] lose the data.
[03:55] I hope you are clear with these definitions.
[03:57] Now let me show you some examples.
[03:59] First, we can try to understand a implicit casting or widening casting or automatic casting.
[04:05] So here you can see first I have created an int variable with the value 16.
[04:11] This int variable I'm trying to assign to the double variable.
[04:16] And here I'm trying to promote my integer to the higher data type which is double.
[04:22] So since there is no chance of losing the data, my compiler is going to be more than happy to allow
[04:28] this automatic casting.
[04:30] You can see under the int variable we are going to have the data 16, whereas under the double variable
[04:36] we are going to have 16.0.
[04:38] So there is no loss of data.
[04:40] In fact we got some extra data under the decimal points.
[04:44] So this is one of the classic example of implicit casting.
[04:48] But please note that never ever try to convert your boolean to other data types.
[04:54] The casting of boolean to other data types is not allowed because whatever values that we
[05:00] hold inside boolean are not supported by other primitive data types.
[05:04] So inside boolean we saw we are going to store false and true, and these false and true are not going
[05:09] to be supported by any of the other primitive data types.
[05:12] That's why the casting of boolean to other data types is not allowed in Java.
[05:17] I hope you are clear on implicit casting example.
[05:20] Now let's see the explicit casting or manual casting or narrowing casting.
[05:25] So here the example is,
[05:27] first I'm trying to create an double variable with the 3.14 d.
[05:32] If I try to directly assign this double variable to the integer, my compiler is not going to accept,
[05:39] it is going to simply throw an error, because I may lose that decimal values if I try to convert this
[05:45] double number to the integer.
[05:46] So to convey to the compiler that I'm fine to lose these decimal values, I need to do the narrow casting
[05:53] or manual casting or explicit casting,
[05:56] by following this syntax.
[05:57] You can see whenever we are trying to assign a large value data type to the small size data type, we
[06:03] need to mention that what is the target type
[06:05] under the brackets. Here you can see this is a syntax, the same I'm trying to do here.
[06:10] Since I'm trying to convert this myDoublePiNum to int, I need to mention that int inside the
[06:16] brackets and the right hand side itself.
[06:18] And this is going to give an indication to the compiler that developer is fine to lose the data.
[06:25] And with that, the compiler is going to allow the casting from double to int.
[06:29] So here we are downgrading from double to int.
[06:32] So now if you try to print the myoublePiNum it is going to have original value which is 3.14.
[06:38] But if you see the value that we have inside myIntPiNum, which we assigned after explicit
[06:45] casting or implicit casting, the output is going to have only three because int cannot store the
[06:51] decimal values
[06:52] and with that there is a loss of data which is 0.14 inside your integer.
[06:57] Since there is a loss of data, we call this kind of casting as explicit casting or narrowing casting.
[07:04] I hope you are clear with this theory discussion.
[07:06] In the next lecture, let's see the demo of this type casting with the help of jshell.
[07:11] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
