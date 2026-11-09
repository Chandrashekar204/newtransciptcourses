# 6.12 — Checking if a String is empty

> Section 6: Deep dive on String in Java

[00:00] Sometimes in the business logic that you are trying to write with the help of Java programming language,
[00:06] you may get a requirement, which is to check if a given String is an empty or not.
[00:12] If it is an empty string, please execute so and so business logic.
[00:15] Otherwise you want to execute other set of business logic.
[00:19] To handle these kind of situations, you need to know how to check if a given String object holds empty
[00:26] data or not.
[00:27] There are three different approaches inside Java to identify if a String does not contain any characters.
[00:34] Let's try to explore all these three options.
[00:37] The very first option is with the help of isEmpty() method.
[00:41] Inside String there is a non-static method or there is a instance method.
[00:46] This method name is isEmpty().
[00:48] We can invoke this method on top of a String object.
[00:52] If your String object holds empty data, this is empty.
[00:56] Method is going to return a boolean value as an output, and the boolean value is going to hold true
[01:02] value if the String is empty
[01:05] otherwise you're going to get false as an output.
[01:08] Before I try to reveal the second approach, I want to give you a hint.
[01:11] We already discussed about the length() method with the help of length() method
[01:16] can we identify if a given String is empty or not?
[01:19] Think about it when the length is going to be zero, if the given String is empty, or if the given
[01:25] String does not hold any character, then the length value is going to be zero.
[01:29] Using the same logic, we can easily identify if the given String is empty or not.
[01:36] You can see here I'm trying to invoke the length() method.
[01:39] If the output from the length() method is equal to zero, then that is an indication that your String
[01:46] object holds empty value.
[01:48] And the last approach is with the help of equals() method we already discussed equals() method as well.
[01:55] Whenever we want to use the equals() method to check if a given String is empty or not, we just have
[02:01] to provide two String objects to the equals(),
[02:04] one is your own String object.
[02:06] The other String object is the empty string itself.
[02:09] Here you can see
[02:10] first I have provided the empty String post that I'm trying to invoke the equals() method, followed by
[02:16] my String object, which is myString.
[02:19] My equals() method is going to return the boolean value as true if both the given string objects are holding
[02:26] empty value.
[02:27] Otherwise it is going to give the false value.
[02:29] So we have three different approaches, and you can use any of these approaches to check if a given
[02:35] string is empty or not.
[02:36] But here you may have a question which approach should I use or to which approach should I give priority?
[02:42] My request is always to give the priority to the third approach, which is with the help of equals() method.
[02:49] The reason why we should give preference to the equals() method approach is it is going to handle the
[02:55] null values as well.
[02:56] Suppose if you're trying to provide a null String object to the equals() method and try to compare it
[03:02] with an empty string behind the scenes, it is going to gracefully handle the null object as well.
[03:09] Whereas if you try to use the other two approaches with the null String object, you're going to get
[03:15] an NullPointerException.
[03:17] That's why always my recommendation is to go with the third approach.
[03:21] Can we see the demo of these three approaches inside IntelliJ.
[03:24] Let's go and create a new class.
[03:27] Inside this class I'm going to create public static void main() method.
[03:31] And here first I'm going to create an empty String object.
[03:35] The String object name is going to be myString.
[03:38] And inside this I'm trying to store an empty value.
[03:41] So how to store the empty value.
[03:43] We just need to mention that double quotes
[03:46] and within the double quotes we should not mention any char value, including the space value as well.
[03:52] As a next step
[03:53] let me show you the first approach that we have discussed .
[03:56] Here first, I'm trying to create an Boolean variable.
[04:00] The Boolean variable is going to be is empty.
[04:03] And the right hand side of this Java statement I'm going to first mention my String object.
[04:09] On top of that I need to invoke
[04:11] the method isEmpty().
[04:13] So this is empty method is not going to accept any input, but it is going to give the output as a boolean
[04:20] value.
[04:21] So let me invoke this.
[04:22] After this first approach, I'm also going to show you the second approach as well, which is with the
[04:27] help of length() method.
[04:29] Let me try to paste the same Java statement and the boolean name.
[04:33] I'm going to change it to isLengthZero.
[04:36] Now on top of my String object I'm going to invoke the length() method.
[04:42] If I simply leave like this, I'm going to get an compilation error because my length() method is going
[04:47] to give an integer value.
[04:49] But on the left hand side I'm trying to catch the boolean value.
[04:52] That's why since there is a mismatch, I'm getting a compilation error.
[04:57] To resolve this issue, I need to compare the output
[05:00] from the length method with the zero value.
[05:03] So how to compare with the help of double equal operator?
[05:07] So if the output from the length() method is zero, then I'm going to get a boolean value as true.
[05:13] Otherwise I'm going to get the value as false.
[05:15] Now let me show you the third approach to show you the third approach
[05:19] I'm going to copy the Java statement here and I will change this boolean name to isEqualEmpty.
[05:28] And inside the third approach we are going to use the equals() method.
[05:31] Whenever we are using the equals() method, we need to pass two String objects.
[05:36] The very first String object I want to pass is the hardcoded literal value of empty String.
[05:42] After mentioning this String value, I'm going to invoke the equals() method and to the equals() method
[05:48] I'm going to pass my String object, and with this we should be able to check if the given String is
[05:55] an empty string or not.
[05:57] If I try to execute this program, I should get true value for all the boolean variables that we have
[06:03] created.
[06:03] Let me try to execute this program.
[06:05] You can see all the three variables they are holding the true value.
[06:10] I hope this is clear.
[06:11] Let me release the breakpoint and this time let me show you the advantage of equals() method.
[06:17] Whenever we are dealing with the null string for the same, first I'm going to create an String object
[06:24] and the object name is going to be nullString
[06:27] and inside this nullString I'm going to hold the null.
[06:30] So inside Java what is null represent.
[06:32] It represents there is no data,
[06:34] there is no memory location that your object is referring.
[06:37] It just an orphan name that is just created.
[06:42] Now I'm going to copy this third approach code and mention here I'm going to mention isNullEmpty as
[06:50] a variable name and post that
[06:51] I'm going to mention the null String object here.
[06:54] If I execute this piece of code, I'm going to get the false value for the isNullEmpty because like
[07:01] we discussed previously, empty String is not same as null String.
[07:05] Even my intelliJ also is giving warning to me saying that you're always going to get false.
[07:11] Why you are trying to compare it.
[07:12] This is how intellIJ is going to help us by showing some warnings.
[07:17] But we should be fine with this warning because we are intentionally trying to test this scenario.
[07:21] Now, if I try to execute this program, you can see isNullEmpty
[07:25] is holding the false value.
[07:27] So I'm not getting any NullPointerException.
[07:30] If I use the other approaches I'm going to get a NullPointerException.
[07:34] Let me show you that as well.
[07:35] So what I'm going to do is I'm going to first copy the first approach.
[07:39] And here instead of my String I'm going to pass the null string.
[07:44] So we are trying to invoke the is empty method on top of the null string.
[07:48] And I'll change this boolean name to isEmptyNull.
[07:53] Now if I try to execute this program I should get an exception.
[07:56] You can see I got an exception which is NullPointerException and here it is also clearly highlighted
[08:03] Cannot invoke
[08:04] String.isEmpty() because null string is holding null value.
[08:08] Can we see the second approach as well?
[08:10] Let me show you that very quickly.
[08:12] I can simply copy this piece of code and mention here, but instead of myString I can use the null
[08:19] string.
[08:20] And this time also we should get a NullPointerException.
[08:23] So you can see we are getting NullPointerException.
[08:26] So that's why always please please use the equals() method.
[08:30] If you are not sure about the null presence inside your String data.
[08:34] Before I try to close this lecture, I want to talk about one more important method which is very similar
[08:40] to isEmpty().
[08:41] So if I open this isEmpty() method which is available inside the String.java.
[08:46] It is going to return true if and only if the length is zero.
[08:50] Otherwise you're going to get false just like isEmpty
[08:52] we also have another method which is isBlank().
[08:57] If I look for the isBlank() method, you can see here there is a clear difference between isBlank() and
[09:03] isEmpty() method.
[09:05] When you are using isBlank() method, it is going to return true.
[09:10] If the String is empty or contains only white space.
[09:14] That means if your String data contains white space or blank space, still your isBlank() is going to
[09:22] return a true value only if your string is holding other type of character other than white space or
[09:28] blank space, then only isBlank() is going to return the false value.
[09:33] I can also show you the demo of this method very quickly for the same
[09:37] what I can do is,
[09:38] first, let me comment this line of code, because with this code we are going to get NullPointerException
[09:44] here
[09:45] first I'm going to create a String object and the name of the object
[09:48] I'm going to give it as blank string.
[09:51] And inside this string I'm going to store lot of white spaces.
[09:56] You can see I have given lot many blank spaces.
[09:59] That's why you're able
[10:00] see the distance between the two double quotes.
[10:02] If we use the isEmpty() method, it is always going to give the value as false.
[10:09] Because this String is not empty, it has white space or blank space, whereas if you use the isBlank()
[10:15] method, it is going to return the true value because according to the isBlank() method, it is going
[10:21] to ignore the blank spaces as a valid character.
[10:24] We can see the demo of them very quickly.
[10:27] So let me copy this line of code.
[10:29] And here let me replace this myString with the blank string.
[10:33] And here I'll change the boolean name as isBlankEmpty.
[10:38] And very similarly, let me copy the same line of code and invoke the method, which is isBlank and
[10:45] the variable name I'm going to change this to isBlank.
[10:48] So now let me execute this program and you can see isBlankEmpty
[10:52] is returning a value false whereas isBlank variable holds a true.
[10:57] So if you have a scenario where you want to check if your String has only blank spaces, or if it is
[11:04] only empty, then you can always use isBlank() method.
[11:08] I hope you are clear with all these discussions.
[11:10] So always if you have any question, please always refer to the Java documentation available on top
[11:17] of your methods available inside the Java library.
[11:21] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
