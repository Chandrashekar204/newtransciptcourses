# 16.7 — Autoboxing and unboxing - Theory

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] As of now, we are performing the boxing and unboxing manually with the help of the methods available
[00:06] inside the wrapper classes.
[00:08] For example, we are leveraging the valueOf() method to perform the boxing, whereas to perform the unboxing
[00:15] with the help of the wrapper objects, we are invoking the instance methods like intValue(), doubleValue(),
[00:21] and longValue().
[00:22] But here you may have a question which is boxing and unboxing seems to be a very most common scenario
[00:30] inside Java.
[00:31] Is there any better approach or is there any automated way of boxing and unboxing?
[00:36] It's a very great question and a valid question as well.
[00:39] When Java introduced the collections very first time Java team, they made these boxing and unboxing
[00:45] as manual process, which means that Java developers, they have to perform the boxing and unboxing
[00:52] manually with the help of these methods.
[00:54] But in the Java five version, the Java team, they made these boxing and unboxing automatic.
[01:02] So that's why from Java five there is a new concept came into picture which is auto boxing and auto
[01:08] unboxing.
[01:09] So let's try to understand how these boxing and unboxing is going to happen automatically.
[01:14] Like I said before, the Java is capable of performing automatic boxing and automatic unboxing from
[01:21] Java5 version.
[01:22] That's why these concept is commonly known as auto boxing and auto unboxing.
[01:28] First, let's try to understand how to perform the boxing automatically. Like you can see here,
[01:33] first, I have created the inter primitive data type variable with the name num and to the same variable
[01:39] I'm trying to assign the numerical value, which is 16.
[01:43] As a next step, I'm trying to assign this num variable directly to the object of Integer wrapper class.
[01:50] So this is auto boxing.
[01:51] So whenever I'm trying to assign a direct int literal value or a variable
[01:57] in such scenarios the boxing is going to happen automatically behind the scenes.
[02:02] We don't have to manually invoke the valueOf() method.
[02:05] So this is auto boxing.
[02:07] Whereas coming to the unboxing even this is also work very similarly.
[02:12] You can see first I'm trying to assign the 16 directly to the wrapper object of Integer.
[02:17] So at the very first line auto boxing is going to happen.
[02:21] Whereas in the second line I'm trying to assign these num object to the primitive data type variable
[02:28] which is num.
[02:29] So at the second line the unboxing is happening automatically.
[02:34] Did you see how easy it is with this auto boxing and unboxing?
[02:38] We never have to do the boxing or unboxing manually with the help of valueOf() method or intValue(), doubleValue().
[02:45] .
[02:46] or longValue() methods.
[02:47] We can use this auto boxing and unboxing feature only from the Java5 version.
[02:53] Do you know when Java five released?
[02:55] Java5 released a long back in 2004.
[02:58] In 2004, most of us might be in school, which means this feature is introduced long back, and right
[03:05] now we can happily use the auto boxing and unboxing without any manual code.
[03:11] Let's try to understand more details about auto boxing and unboxing these auto boxing and unboxing
[03:17] it is going to be performed when we compile the code.
[03:20] The JVM is completely clueless of the boxing and unboxing performed by the compiler, which means when
[03:27] we try to assign a primitive data type value to the wrapper class object, the auto boxing is going
[03:33] to happen behind the scenes.
[03:34] So by the time my JVM is trying to execute the bytecode of my Java program behind the scenes, the compiler
[03:41] will use the valueOf() method to convert that primitive data type value into the wrapper class object.
[03:47] The same applies for the unboxing as well.
[03:49] Here I want to share a very important note.
[03:52] So as of now everything seems to be good.
[03:55] Like you might be liking these auto boxing and unboxing a lot, but you need to be very careful whenever
[04:01] you're trying to use these auto boxing and and unboxing feature.
[04:05] While you are trying to deal with the null values. Like you can see here
[04:09] first, I have created an object of Integer wrapper class, and to the same I'm trying to assign the
[04:15] null value later on.
[04:17] If I try to assign this wrapper class object directly to the primitive data type variable, I'm going
[04:23] to get a NullPointerException.
[04:24] Do you know why?
[04:25] Because behind the scenes the compiler is going to write a code which is with the help of these n wrapper
[04:32] object
[04:32] it is going to invoke the intValue() method available inside the Integer wrapper class.
[04:38] So anything that we try to invoke on top of the null object, what do we get?
[04:43] We get our favorite exception which is NullPointerException.
[04:48] That's why whenever you are trying to deal with the wrapper objects that have null values, please do
[04:53] enough null checks and do enough unit testing to avoid these kind of surprises.
[04:58] I hope you are clear about the
[04:59] process of autoboxing and unboxing how it is going to work.
[05:03] As of now, we just discussed this concept using the slides.
[05:07] In the next lecture, we can try to write a Java program, and in the same program I'll show you how
[05:12] these autoboxing and unboxing is going to happen automatically.
[05:16] I hope you are fine with the plan.
[05:18] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
