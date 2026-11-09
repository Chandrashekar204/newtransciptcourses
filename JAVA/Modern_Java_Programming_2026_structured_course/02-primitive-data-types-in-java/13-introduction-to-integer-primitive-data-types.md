# 2.13 — Introduction to integer primitive data types

> Section 2: Primitive data types in Java

[00:00] Now let's try to understand what are the primitive data types available under the integer types.
[00:06] So what is an integer from Java perspective
[00:09] Integer means a whole number.
[00:11] It can be a negative or a positive number, but the number should not have any decimal values.
[00:17] It should be a simple negative or a positive number.
[00:20] So to store these kind of numbers inside Java variables, we need to use integer types available inside
[00:28] java under integer,
[00:30] there are four types of primitive data types available, and these data types are byte, short, int,
[00:36] and long.
[00:37] We already discussed on a high level what are these data types and when we should use them.
[00:42] But the new information that I want to share here is, whenever you are trying to declare and initialize
[00:48] a long variable, we need to make sure we are mentioning a uppercase or lowercase l value towards the
[00:55] end of the number that we are trying to assign to the long variable.
[00:59] Using these L value only the Java compiler can differentiate between an integer and long value.
[01:06] In few minutes
[01:06] I am going to share more details about why we should mention L character inside long variable values.
[01:14] Sometimes inside your interviews, people may ask you what is the maximum value or minimum value that
[01:20] is supported by a given integer primitive data type.
[01:24] It can be a byte, short or int or long.
[01:27] Regardless of what our primitive data type they may ask you
[01:30] question like what is the maximum value or the minimum value that a particular primitive data type is
[01:36] going to support?
[01:37] For this, we don't have to remember the minimum and maximum values.
[01:41] As long as you remember the size of this primitive data types, you should be good because we can easily
[01:47] identify what is a min value and max value based upon the corresponding classes available inside the
[01:54] Java library.
[01:55] For byte primitive data type, there is a Byte class.
[01:58] Very similarly, there is a Short class, for int
[02:01] the class name is going to be Integer, not int, and for long the class name is going to be Long.
[02:07] Using these classes only, we can invoke the static variables with the name MIN_VALUE and
[02:13] MAX_VALUE.
[02:15] And with that we can easily understand what is a min value and max value supported by a given primitive
[02:21] data type.
[02:22] You may have questions here,
[02:23] What is a static variable?
[02:24] don't worry for now.
[02:26] In the coming sections we are going to discuss about what are static methods and static variables.
[02:30] For now, please note that this min value and max value variables is going to be present in each of
[02:36] the classes of our primitive data type.
[02:38] So these classes like Byte, Short, Integer, and Long.
[02:42] The Character class that we have discussed in the previous lecture.
[02:45] And for Boolean also there is a Boolean class.
[02:47] So all these classes we call them as wrapper classes inside Java.
[02:52] The reason why we call them as wrapper classes is these wrapper classes provide a lot of functionality
[02:58] and helper methods to deal with the primitive data types like byte, short, int, long, char, boolean.
[03:05] We are going to discuss in detail about these wrapper classes in the coming sections, but for now I
[03:10] just want to give this quick introduction.
[03:13] So whenever you want to declare variables with the help of this primitive data types, the syntax is
[03:18] going to be same.
[03:18] But please make sure you are selecting the byte, short, int, and long based upon your size requirements.
[03:25] On top of that, whenever you are trying to create a long variable and you are trying to assign a number
[03:31] to it, please make sure you are mentioning the L or l at the end of the number.
[03:37] So here I have a number long num is equal to 456.
[03:41] After the 456,
[03:43] I'm trying to mention L.
[03:45] We can also use l, but my recommendation is always go with the L, because sometimes
[03:51] the other developers may confuse l with one.
[03:55] That's why always go with the L.
[03:57] I also want to show you a slide which will tell you under which scenarios you need to select which integer
[04:04] data type.
[04:05] We have four primitive data types under integer types, so the size and range of numeric values need
[04:11] to be considered while choosing one of the integer data types.
[04:15] With this picture, I'm trying to convey the same information.
[04:18] I'm assuming by seeing this picture
[04:20] you can remember this information for a long time.
[04:23] So you can see byte size is going to be one byte, and for short the size is going to be two bytes,
[04:30] for int is going to be four bytes.
[04:32] and for long it is going to be eight bytes.
[04:34] So based upon your business logic, if you have to store a very, very long number, then always go with
[04:41] the long.
[04:41] Otherwise you can always go with the int, short or byte based upon your business requirements.
[04:47] I hope you are clear with this quick introduction.
[04:49] In the next lecture, let's try to create some variables with the help of these integer primitive data
[04:55] types.
[04:55] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
