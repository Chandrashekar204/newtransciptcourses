# 6.11 — Fetching a character at an index in String

> Section 6: Deep dive on String in Java

[00:00] By this time, it should be pretty clear for you that a String is a combination of multiple characters.
[00:06] For example, if I try to store Java String data inside a String object, my String is going to have
[00:13] multiple characters like j, a, v, a.
[00:16] Sometimes you may have a requirement to fetch a character or to find a character which is available
[00:23] at a specific index inside your String.
[00:26] So what is an index?
[00:27] Index represents the position of the character inside your String data.
[00:32] To fetch a character from a specific position within a String object, we can use the charAt() method.
[00:39] This charAt() method is a non-static method or an instance method, which we can invoke only by using
[00:46] the object of the String.
[00:48] Here you need to be aware about an important point inside String
[00:52] whenever we want to understand the position of a character, we should always start the index at the
[00:58] position from zero.
[00:59] But not the one.
[01:00] For example, like you can see here, I have a String object which is holding the Java word.
[01:05] If I try to understand what is the index or what is the position of each character, I need to start
[01:11] the counting from zero but not the one.
[01:14] So the J is going to be available at the index zero.
[01:17] The A is going to be available at one, the V is going to available at the position 2.
[01:23] And similarly the last A character is going to be available at the index 3.
[01:29] Always your last character is going to be available at the index position, which is equal to the length
[01:36] of the String -1.
[01:38] So what is the total length of this string?
[01:41] It is going to be four.
[01:42] So the last position here is going to be 4 - 1 which is 3.
[01:46] To this charAt() method we need to pass what is the index number or what is the position number that we
[01:53] want to consider to fetch a char.
[01:55] Since this charAt() method is going to return a character definitely on the left hand side, we need to
[02:01] accept that data by using the char primitive data type.
[02:05] Here is a simple example that you can see if you try to pass an invalid index or invalid position number
[02:12] to the carrot method, it is going to throw an exception which is StringIndexOutOfBoundsException.
[02:19] So here we know the index is going to start at 0 and it is going to end at 3.
[02:24] If I try to be oversmart and try to pass index as 4 or 5, then my program is going to throw this exception
[02:32] and it is going to terminate without running any further Java statements.
[02:36] As a next step, let's try to see the demo of this method by creating a sample program inside IntelliJ.
[02:43] I have created a class with the name charAt() Method demo, and inside this class I have created an empty
[02:49] main() method.
[02:50] Inside this main() method, first I'm going to create an object of String, and inside this object I'm
[02:57] going to store the data which is Java in all capital letters.
[03:02] Now if I want to fetch the first character, then I should pass the index number at the position number
[03:08] as zero.
[03:09] Because inside Java programming language, always the first position is going to start at zero, but
[03:15] not one.
[03:16] Let me try to fetch the first character inside my String object.
[03:20] First, I'm going to accept the output with the help of char data type.
[03:24] The name of the variable I'm going to give here is J.
[03:27] Now on the right hand side, first I want to use the String object.
[03:31] What is the String object?
[03:32] It is a java.
[03:33] Using this String object I want to invoke the charAt() method.
[03:38] So this charAt() method you can see it is going to accept the int as an input, which is going to represent
[03:44] your index or position.
[03:46] And the return type of this method is going to be char.
[03:49] Let me invoke this method.
[03:50] And to this I'm trying to pass zero.
[03:53] With that, we should get the first char value assigned to this char variable.
[03:58] So let me keep a breakpoint here and execute my program.
[04:02] As you can see, the j holds capital J and 74 is a Unicode position number.
[04:08] We are able to see both of them.
[04:10] This means our charAt() method is working without any issues.
[04:14] Let me release my breakpoint.
[04:15] This time I'll try to pass the index number, which is going to be invalid for my given String object.
[04:22] In the same process, I'm going to show you the exception that we may receive.
[04:26] So the same line of code.
[04:27] I'm going to copy paste inside the next line.
[04:30] And here I'm going to change the variable name to exception.
[04:35] And for the charAt() method I'm going to pass a index number four.
[04:39] Do you think index number four is valid,
[04:41] no.
[04:42] Because since the index number is going to start at zero, our Java object is going to have total three
[04:49] index like 0123.
[04:51] There won't be any char value at the index four.
[04:54] That's why we can expect an exception here.
[04:57] And keeping my breakpoint here.
[04:59] But my
[04:59] program is never going to reach my break point because just before my break point, I have a code which
[05:05] is going to throw an exception.
[05:07] Let me try to execute my program.
[05:09] You can see the breakpoint never stopped and I'm directly getting an exception which is StringIndexOutOfBoundsException
[05:16] StringIndexOutOfBoundsException.
[05:18] And here the reason is very simple index for out of bounds for the length four.
[05:23] So we have given a String which has a length of four.
[05:26] The last index obviously it will be four minus one which is three.
[05:30] I hope you are clear with this charAt() method.
[05:33] Thank you
[05:34] and I'll catch you in the next lecture bye.

----------------------------------------
