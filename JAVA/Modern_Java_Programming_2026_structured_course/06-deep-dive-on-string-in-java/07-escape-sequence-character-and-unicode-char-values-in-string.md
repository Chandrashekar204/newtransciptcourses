# 6.7 — Escape sequence character & Unicode char values in String

> Section 6: Deep dive on String in Java

[00:00] Whenever we want to store data with the help of String data type, we need to mention that data within
[00:07] the double quotes.
[00:08] What if you want to store the data along with the double quotes as well?
[00:13] In such scenarios, your compiler is going to throw an error.
[00:16] So how to handle this scenario?
[00:18] To handle this kind of scenarios, we have to use escape sequence character.
[00:23] Let me show you an example so that it is going to clear for you.
[00:26] Here I'm going to create a new Java class and the class name I'm going to keep it as EscapeSeq(indicates
[00:34] sequence)Demo.
[00:35] So these are class name inside this class.
[00:38] First I want to create a main() method.
[00:40] And inside this main() method I'm going to create an object of String.
[00:45] The name of the object is going to be name.
[00:48] And with the help of this object variable name, I want to store my name along with the
[00:54] double quotes.
[00:55] First, whenever we want to store data inside a String, we need to mention double quotes and inside
[01:00] the double quotes we need to type the name which is Madan.
[01:03] Apart from storing my name, I also want to surround my name with double quotes and the same I want
[01:08] to print on the screen.
[01:10] You may be thinking I can simply mention double quotes just around my name, but you can see my compiler
[01:17] is going to confuse with these syntax because according to my compiler, these two double quotes is
[01:23] one String, which is similar to empty string, and these two double quotes that we have at the end
[01:29] this also represent an empty String.
[01:31] In between there is some random text.
[01:34] That's why, since this is not matching with the syntax of Java compiler, I'm getting an compilation
[01:40] error.
[01:40] So how to resolve this issue?
[01:42] Like you said before, in these kind of scenarios we need to use escape sequence character.
[01:48] So what is a format
[01:49] to use the escape sequence character we need to use backslash.
[01:53] If you mention backslash at the two places where you have double quotes, then your compiler is going
[01:59] to be happy behind the scenes.
[02:01] these backslash double quotes is going to be considered as a double quote before my name.
[02:07] And very similarly, we also have one more backslash double quote after my name.
[02:12] So these two double quotes will be appended to my name.
[02:16] We can also confirm the same by trying to print out my name onto the console.
[02:21] So let me try to execute this program.
[02:23] You will be able to see my name in that
[02:26] double quotes.
[02:26] I hope you are clear
[02:27] what is the purpose of these escape sequence character which is backslash?
[02:32] The same kind of escape sequence character we also used as part of the char data type, as well.
[02:38] As a next step
[02:39] let me try to explain one more concept inside String.
[02:43] We know each character has an Unicode representation.
[02:47] While we are discussing about the char data type, we discussed about what are Unicode values.
[02:52] For example, here I am trying to create a object with the name m and to this m object I'm simply trying
[02:59] to store the value M.
[03:02] So if I try to print these output, I'm going to get the value whichever I have saved into this m object.
[03:09] Let me try to run this
[03:10] you can see I'm getting this m char value if needed
[03:14] you can also mention the Unicode representation of this 'M' .
[03:19] So what is our Unicode representation of 'M' value.
[03:22] First we need to mention \u.
[03:25] After that we need to mention the Unicode number which is 004D.
[03:32] So this is the Unicode representation of the capital M.
[03:36] Now if I try to execute the program I'm going to get the same output which is M.
[03:42] You can see I'm getting the same output.
[03:44] That means our String Java class is also capable of converting the Unicode characters into the corresponding
[03:51] alphabet representation value.
[03:53] I can also try to create one more object and show you one more example.
[03:57] So this time I'll try to create a variable with the name Unicode name, and to this variable I'm going
[04:05] to assign a combination of Unicode values and normal char values.
[04:11] First let me mention this value, which is Unicode representation of m and post that I will type my
[04:18] name, which is a d, a, n, and at the end I'm going to mention one more Unicode value, which is
[04:25] \u followed by 0021.
[04:30] Let's see what this value is going to be print out inside my console.
[04:34] So I'm trying to print out the String object which is Unicode name.
[04:38] If I execute this program you will be able to see an output which is Madan!.
[04:44] That means whatever Unicode value that I have mentioned just before the A char value, this represents
[04:51] M and whatever Unicode value I have mentioned after that N char this represent the exclamatory symbol.
[04:59] With this
[04:59] I'm assuming you are clear that String is capable of processing your Unicode values as well.
[05:05] Sometimes inside the interviews are inside the Java related exams
[05:09] they will try to confuse you or trick you by giving a String value with a combination of Unicode value
[05:15] and a normal character value.
[05:17] So don't worry about those scenarios.
[05:19] You can simply answer them.
[05:21] The Unicode value first is going to be converted as an normal char post, that only the entire String
[05:28] object is going to be created behind the scenes if needed.
[05:32] You can show these examples as well to convey your understanding to the others.
[05:37] The two concepts that we have discussed inside this lecture, which are related to the escape sequence
[05:42] character and Unicode char values.
[05:45] I have mentioned the details about them inside this slide for your reference.
[05:49] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
