# 16.9 — Caching with valueOf() methods

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] Inside this lecture, I'm going to show you a demo of a scenario which is super tough to understand,
[00:06] and I'm sure most of the senior Java developers also they don't know about these scenario.
[00:11] This scenario can be your most toughest question inside your Java interviews.
[00:16] But since you are my student, I want to teach about these most to complex scenario around the wrapper
[00:22] classes.
[00:23] This scenario revolves around the caching mechanism that wrapper classes follows.
[00:29] To show you the demo of this scenario, I'm going to create a new Java class.
[00:34] The class name is going to be WrapperObjectsCaching
[00:38] behind the scenes few of the wrapper classes
[00:42] they are going to have some caching mechanism.
[00:44] So there are certain advantages with this caching mechanism.
[00:48] Before I try to show you the demo of this caching mechanism, let me highlight you that whatever caching
[00:53] mechanism that we are going to discuss right now, it is only applicable for the numeric wrapper classes.
[01:01] So there are four numerical wrapper classes inside Java, each representing the numeric primitive data
[01:07] types.
[01:08] So inside we have four numeric data types byte, short, long and int.
[01:14] Using these primitive data types, we can store normal numerical values, whereas float, double they
[01:21] come under the decimal format.
[01:23] That's why whatever caching that we are going to discuss, these are applicable for the objects that
[01:28] we are going to create with the help of wrapper classes like Integer, Byte, Short and Long.
[01:35] I hope it is clear.
[01:36] Now let me create the main() method inside the main() method
[01:40] first, I'm going to create the wrapper objects with the help of autoboxing feature.
[01:45] So let me try to create the object of Integer wrapper class with the object reference name as obj1.
[01:53] To this, I'm going to assign the value 16.
[01:56] Next, I'm going to copy the same code and create that different object of Integer.
[02:01] And inside this I'm going to store the same value 16.
[02:05] As a next step I'm going to repeat the same with the different objects like obj3 and obj4.
[02:12] So this time I'm going to store a different value.
[02:15] Maybe I'll try to store 161.
[02:18] So you might be expecting there will be total four objects will be created inside the heap memory.
[02:24] obj1, obj2, obj3 and obj4.
[02:28] So let's try to validate our understanding.
[02:30] To validate the same.
[02:32] I'm going to compare the memory locations of these objects.
[02:36] We are expecting four different memory locations for these four different objects.
[02:41] Let's see what is going to happen.
[02:42] So how to compare the memory locations inside Java with the help of double equal to operator ( == ) , we can
[02:50] compare the memory locations. Whenever you are trying to use these double equal to operator in between
[02:56] the object references, then it is going to compare the memory locations.
[03:00] So now let me copy the same line.
[03:03] And this time let me try to compare obj3 and obj4.
[03:08] You might be expecting false and false.
[03:11] Let's see
[03:12] you're going to have a surprise here.
[03:13] Did you see we are getting true for the first statement
[03:17] whereas for the second statement we are getting the false.
[03:20] Why we are getting true for the first statement and false for the second statement.
[03:24] We followed the same approach, but we are getting a different output this time
[03:28] maybe what I can do is, I'll try to change this number to 121.
[03:32] Let me change the same inside obj4 as well.
[03:35] If I try to execute this program, we are getting true in both scenarios.
[03:39] What is happening here?
[03:40] We are getting some random output so it is not a random output.
[03:44] There is a logic behind it.
[03:45] So let's try to understand the same logic.
[03:48] Then it is going to be very clear for you, and you're going to answer pretty confidently to make you
[03:52] understand around this scenario.
[03:54] First, let me open the Integer wrapper class.
[03:57] Here inside this class I'm going to search for cache.
[04:00] Let's keep searching for cache and you'll be able to see a inner class with the name IntegerCache.
[04:07] If you try to read these documentation on top of this class, you will be able to clearly understand
[04:12] there is a cache to support the objects identity semantics of autoboxing for values between -128 to
[04:21] 127.
[04:22] That means for all the objects that you are going to create with the help of the wrapper classes like
[04:28] Integer, Byte, Short, and Long.
[04:30] If you're trying to assign the same value to the different wrapper objects like obj1 and obj2,
[04:37] and if this value is present in between -128 and 127, and you can see the boundaries are also inclusive.
[04:46] So if your number falls between -128 and 127 inclusive, then in such scenarios behind the scenes JVM
[04:54] is not going to create multiple different objects.
[04:58] Instead it is going to create
[04:59] a single object and both your references like obj1 and obj2, they are going to point to the same
[05:07] object inside the heap memory.
[05:09] That's why since 16 is less than or equal to 127, we are getting the output as true here.
[05:16] Since obj1 and obj2, they are pointing to the same object.
[05:21] But if you try to give a number like 128 which is just above 127, this time you will be able to see
[05:28] the output as false.
[05:30] The reason is obviously the Integer cache that we discussed.
[05:34] It is only going to work up to the number 127, whereas for the negative numbers it is going to work
[05:39] up to -128.
[05:41] Since our number is just above 127, this obj3 and obj4 will be created as two separate objects
[05:49] inside the heap memory.
[05:50] So why Java is doing this?
[05:52] The reason is very simple.
[05:53] According to the Java team, most of the times Java developers end up creating the objects with small
[06:01] numerical values, which may fall in the range of -128 to 127.
[06:06] So to improve the performance or to save some heap memory, they have built these Integer cache.
[06:12] And very similarly you will be able to see the same kind of cache inside the Long as well.
[06:18] So let me search for cache.
[06:20] You can see there is a inner static class with the name LongCache.
[06:24] So this also follows the same kind of approach.
[06:27] The same applicable for other wrapper classes like Byte and Short.
[06:31] Anytime inside Java interviews or inside Java exams, they will ask you these kind of questions.
[06:37] What is the output that I am going to get in this kind of scenario?
[06:40] So first check what is the numerical value that they are trying to assign.
[06:44] If it is falling in the range of cache, then you are always going to get the same object regardless
[06:49] of how many objects you are trying to create, like obj1, obj2, obj3.
[06:54] You can create any number of object references, but all of them they are going to point to the same
[06:59] memory location inside the heap memory.
[07:02] Whereas if your number is outside the cache boundaries, then obviously you are going to get multiple
[07:09] different objects for each of your object references like obj3 and obj4.
[07:14] Here you can see we are doing the autoboxing.
[07:18] So whenever the autoboxing is happening behind the scenes, my JVM is going to consider valueOf() method
[07:24] that is available inside the Integer or any other wrapper class.
[07:28] So this caching is going to work only when you use valueOf() method.
[07:32] So when you end up using auto boxing, or when you end up using value off methods manually to convert
[07:39] your primitive data type values into the wrapper object.
[07:42] In both these scenarios, this caching mechanism is going to come into picture.
[07:46] Whereas if you try to create the wrapper objects with the help of deprecated constructor approach,
[07:53] then in that scenario, regardless of what kind of value you are trying to store, you're always going
[07:58] to get a fresh new object.
[08:00] I can also confirm you the same.
[08:02] Maybe what I can do is I can try to create an object of Integer with the name obj5.
[08:10] To this, I can try to assign the constructor of Integer with the help of new Integer, and to this
[08:17] constructor I can pass the value 16.
[08:19] I can try to copy the same code, and this time I'll mention the object reference name as obj6.
[08:26] Post that I can try to compare the output of obj5 and obj6.
[08:32] So let me compare the memory locations of obj5 and obj6.
[08:37] As per our discussion, we should get the output as false.
[08:40] Let's see
[08:41] you can see we are getting false.
[08:42] So this confirms whenever we are using the constructor approach to perform the boxing, we are always
[08:48] going to get the fresh object or a different object,
[08:51] there won't be any caching involved.
[08:53] Whereas if you are trying to implement autoboxing or if you're trying to use the Integer.valueOf(),
[08:59] method or value of methods inside other wrapper classes like Long, Byte and Short.
[09:05] In those scenarios, always JVM is going to check what kind of data you're trying to store.
[09:10] If the data that you are trying to store is falling between -128 to 127, then JVM is not going to create
[09:18] multiple object.
[09:19] Instead it is going to create a single object.
[09:22] The same is going to be referred by all your object reference variables.
[09:27] I hope you are clear and you are pretty confident around this scenario.
[09:31] Maybe you can try to trick one of your friend by asking this question.
[09:35] I'm sure 90% of the people they will scratch their head to answer this question.
[09:41] Everything that we discussed around the caching inside this lecture I have mentioned inside this slide
[09:46] for your reference.
[09:47] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
