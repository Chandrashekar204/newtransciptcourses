# 6.17 — Fetching Substring from a String

> Section 6: Deep dive on String in Java

[00:00] Using string
[00:01] we can store any amount of data.
[00:03] If you have a scenario where you want to extract a specific portion of your String data, then we can
[00:10] use substring concept that is available inside the String.
[00:15] So what is substring concept with the help of a substring() method which is available inside the String
[00:20] class, we can extract a portion of a String.
[00:24] With the help of this substring() method, we can create a new string that consists a specific range of
[00:30] characters from the original String.
[00:32] This substring method is available inside String class as an instance method, which means we can only
[00:39] invoke the substring method with the help of String object, and there are two overloaded methods of
[00:44] substring.
[00:45] The first form of substring is,
[00:47] I can mention what is the start index at the starting position that I want to be consider to extract
[00:54] that data from the original string.
[00:56] When I mention only the start index, my substring() method is going to extract the data from the start
[01:02] index towards the end of the string.
[01:04] So we are not telling what is the end index.
[01:07] That means my substring() method is going to assume that this fellow want to extract the entire String
[01:13] data, which starts from the given start index.
[01:16] But if you are looking to extract the String data in between two indexes, then you can provide start
[01:23] index and end index to the substring() method.
[01:26] But here you need to be aware of a important point, which is whenever we are mentioning start index,
[01:33] the substring() method is going to consider it as an inclusive, whereas the end index number is going
[01:40] to be exclusive.
[01:41] I'll show you what I mean here.
[01:43] In the screenshot I have mentioned a original string with the value hello comma, space world exclamatory
[01:49] mark that is the original string. From this original string,
[01:53] if I want to extract a portion of the data, I can use substring() method.
[01:57] In the second Java statement, I'm trying to pass the seven as a start index to my substring() method.
[02:04] So what is the character that is going to start at the seventh index?
[02:08] So please count from zero.
[02:10] If you start from zero the hatch is going to be at the position zero like 0123456.
[02:18] And at the seventh position the character w is going to start.
[02:23] So from this position or from this character, the entire string data is going to be extracted into
[02:29] the new String object.
[02:31] That's why here you can see the output we are going to get is world exclamatory mark.
[02:36] Here whatever start index that we are mentioning
[02:38] my substring method is considering it as an inclusive, which means the char present at the seventh position
[02:45] is also going to be considered when it is trying to extract the data.
[02:49] Whereas if you see the last statement where I'm trying to mention the start index and the end index.
[02:55] So here I have mentioned the start index as zero and the end index as five.
[03:00] Here inside this example, like I said before, end index is always going to be exclusive.
[03:05] That means my substring() method is going to extract only the data up to the index four.
[03:11] So if you count here like 01234 we are going to get the output as hello.
[03:17] We're not going to get the comma which is present at the index position five because the end index is
[03:24] exclusive.
[03:25] I hope you're clear.
[03:26] The other important point that you need to aware whenever you are using the substring() method is always
[03:31] please note that inside Java are inside strings
[03:35] always the index is going to start from zero.
[03:37] So the first character of a String is going to be available at the position or at the index zero.
[03:43] And the next important point here we have is for this substring() method.
[03:47] If you try to pass invalid index numbers like negative numbers or index number which which are out
[03:52] of the range of your String index values, then you are going to get an exception which is StringIndexOutOfBounds
[03:59] StringIndexOutOfBoundsException.
[04:00] And whenever we are using the substring() method, it is not going to modify the original string.
[04:06] Instead, you are going to get a new String value, which you can catch with the help of another string
[04:12] variable.
[04:13] If you want your original String to be modified, then you can reassign the output from the substring()
[04:18] method to the same original string variable.
[04:21] And the last point here we have is about the length of the substring that you are going to fetch with
[04:26] the help of substring() method.
[04:28] The formula to calculate the length of the resulting substring() is end index - start index.
[04:35] So here you can see the end index is five whereas the start index is zero.
[04:40] So five -0 is going to be five.
[04:42] That's why I got a substring which has a length of five.
[04:46] In the scenarios where you are passing only the start index, then you need to consider what is the
[04:50] last index number.
[04:52] From the last index number, you need to subtract the start index, and the resultant value is going
[04:58] to be the length of your substring
[04:59] value.
[05:00] So what is substring?
[05:02] Whenever we are trying to fetch a portion of the string data, we we call that concept as substring.
[05:08] Let's see the demo of this concept in the intelliJ.
[05:11] To see the demo of the substring() method inside String class I have created a new class inside our project.
[05:17] The class name is SubstringDemo.
[05:19] Inside this class I have created a main() method and inside the main() method you can see I have created
[05:25] a String object that is going to hold this string value, which is hello comma space world exclamatory
[05:32] mark.
[05:32] Using this original string variable, I want to extract a portion of data from the original string value.
[05:40] We can achieve the same with the help of substring() method.
[05:43] So let me try to create a String object, and the String object name is going to be substring1.
[05:49] After giving the object name, I am going to use the original string object, and with the help of this
[05:55] object, I'm going to invoke the substring() method.
[05:58] You can see there are two overloaded methods of substring().
[06:02] The very first one is where we can only pass the begin index to this method.
[06:07] If I pass the seven as an begin index, then my substring() method is going to calculate what is the character
[06:15] that is starting at the seventh position.
[06:16] So let's try to calculate 0123456.
[06:22] At the seventh position the char W is there.
[06:25] So from this position all the entire remaining data is going to be copied into the new substring() variable
[06:33] that we have created.
[06:35] Now very similarly I want to use the other overloaded method available.
[06:39] Before that let me rename this substring1 to substring2.
[06:43] This time I will pass the start index as zero and the end index as five.
[06:49] If I pass these index values, my substring is going to consider the start index as an inclusive and
[06:56] the end index as exclusive.
[06:58] That's why it is going to copy the data only up to the fourth index.
[07:02] So what do we have up to fourth index 01234.
[07:07] That means we are only get the hello word copied into this substring2.
[07:12] Let me execute this program and show you the values at runtime.
[07:16] You can see under the subString1 we have the output which is world exclamatory mark, whereas under
[07:23] the subString2 we have the word hello.
[07:25] And the output here is like we expected.
[07:28] So always use the substring() method whenever you are in the scenarios where you want to extract a portion
[07:34] of data from your String object.
[07:37] I'm trying to put lot of efforts explaining all the important methods available inside the String class.
[07:43] The reason is all these methods
[07:45] they are going to be super savior for you inside your real projects until.
[07:49] Unless you know there is such method, you cannot use them.
[07:53] And when we use these methods, we should be careful about various important concepts.
[07:58] For example, for the substring() method, you need to know that starting x is inclusive and the end index
[08:04] is exclusive.
[08:05] Otherwise, you're going to get super confused with all these reasons.
[08:09] I want to explain string in detail because string is a special data type inside Java.
[08:15] I hope you are enjoying the discussion around the String methods.
[08:19] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
