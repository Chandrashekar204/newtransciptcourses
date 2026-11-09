# 6.28 — Converting String to primitive data type values - Demo

> Section 6: Deep dive on String in Java

[00:00] Here I have created a class with the name ParsingDemo, and inside this class we have a main() method.
[00:06] Inside this main() method,
[00:07] first I'm going to create a String object with the name strInt.
[00:12] And inside this String object I'm going to store the int number which is 456.
[00:18] As of now you can see this is a String object which is holding my int value.
[00:22] With the help of parsing, I want to convert this String data into the int primitive value.
[00:27] So what is the process?
[00:29] First we need to mention int followed by what is the variable name?
[00:33] I'll just mention the variable name as num.
[00:36] After this num, I'm going to invoke the wrapper class of int.
[00:40] So what is a wrapper class?
[00:41] It is Integer.
[00:42] Using this Integer class, I'm going to invoke the static method which is parseInt().
[00:49] So to this parseInt() method, I'm going to pass the object of String.
[00:53] And with that this value is going to be converted into the int primitive value.
[00:59] Now let's do the same for other primitive data types as well as a next step I'm going to create the
[01:05] variable as strDouble.
[01:08] And inside this strDouble I'm going to store that double number which is 3.14.
[01:14] And post that I'll change this into double and variable name to num1.
[01:19] After that I'm going to invoke the double class, and from the double class I'm going to invoke the
[01:25] pass double method.
[01:26] Very similarly we can also do for float.
[01:29] So let me copy this value and paste it here.
[01:32] For the float I'm going to save a number which is 2.718
[01:37] and the variable name I'll change it to strFloat.
[01:41] After this I will replace this double with float and rename this variable name to num2, followed
[01:48] by what is the wrapper class of float and what is the parse method of float which is parseFloat().
[01:54] And for this I'm going to pass the stringFloat object.
[01:58] Here also, we need to pass the correct object, which is strDouble I forgot previously, let me correct
[02:04] it after the float conversion,
[02:06] this time I'm going to do the long conversion.
[02:09] So the variable name is going to be strLong.
[02:13] And the value that I want to store inside this strLong is 3476543210.
[02:22] It can be anything
[02:23] I'm just typing some random number and the variable name
[02:25] I'll change this to num3 and I'll replace this float with the long.
[02:30] And after that I need to invoke the wrapper class of Long, which is long followed by parse method of
[02:37] long, which is parseLong().
[02:40] And the object that I need to pass here is strLong.
[02:43] As of now here I'm showing the demo of int, float, double and long.
[02:48] You may have a question here like how about byte and short?
[02:51] Even for byte and short
[02:53] also the process is going to be the same, like there is a byte of wrapper class.
[02:57] And inside this Byte of wrapper class we have a parseByte()method.
[03:01] Very similarly
[03:02] for short, we have a Short wrapper class, and inside that we have a parseShort() method.
[03:07] So please use them based upon your requirements.
[03:10] Now let me show you how to perform the parsing for the boolean value for the parsing of Boolean value.
[03:17] First I'm going to create a String object with the name strBoolean.
[03:21] And inside this I'm going to store a value, which is true.
[03:25] After this line of code, I'm going to create a variable of type boolean and the variable name is going
[03:32] to be is true to this variable
[03:34] I'm going to assign the output that I am going to get from the Boolean.parseBoolean() method.
[03:40] So here I'm trying to pass strBoolean object as an input to the parseBoolean() method.
[03:45] Let me also show you what will happen if I try to send the invalid boolean values, like here.
[03:52] I'll try to send my name and I'll change this strBoolean to str Name.
[03:58] And I'm going to send the same here.
[04:00] And I'll change this boolean variable name to isName.
[04:04] When we are running this program, we are going to clearly see this is name is going to hold the false
[04:10] because like we discussed, anything that we are trying to send other than true and false, we're always
[04:15] going to get the false as an output.
[04:17] Now we are done with the boolean.
[04:19] As a next step, let's try to do the conversion for char as well. For the char
[04:23] like we discussed, there are two approaches.
[04:25] First, let me create a hello String object with the content as Hello itself and post that I'm going
[04:32] to create a char variable with the name firstChar.
[04:36] And this time we should not use the wrapper class of Char.
[04:40] There is a wrapper class for the char which is Character, but inside this there is no parse method.
[04:46] That's why we discuss other approaches, which is with the help of this hello String object, we can
[04:52] invoke the method which is charAt(), and we can pass the index value.
[04:56] So if I pass here zero I'm going to get the firstChar.
[04:59] As an output, and the same is going to be saved into these firstChar variable.
[05:04] Let me show you the other approach as well.
[05:06] The other approach that we discussed is with the help of toCharArray() method.
[05:11] So using your string object you need to invoke toCharArray().
[05:15] Whenever we are invoking this toCharArray() method you're going to get the output as char [].
[05:21] That's what you can see here inside that definition of the method.
[05:24] So on the left hand side I need to mention char [] and
[05:30] the variable name
[05:31] I can change this to charArray.
[05:33] Now from this charArray variable which is an array object.
[05:37] I can try to fetch any character inside my array.
[05:40] So if I want to fetch the second character, then I need to mention the second index number, which
[05:47] is one inside the square brackets by using these charArray object name.
[05:51] So the output from this is going to be the char data type.
[05:55] So let me catch the same on the left hand side with the variable name as secondChar.
[06:00] With this we have done all the required code changes.
[06:03] Let me keep a breakpoint at the starting of the main() method, and I'm going to start the program in
[06:09] a debug mode.
[06:10] Now I can try to execute my program line by line with the help of this button, which is step over.
[06:17] So instead of pressing this button every time, I can use the shortcut which is F8.
[06:21] So let me use the shortcut F8.
[06:24] First I'm going to execute the very first statement
[06:26] and you can see the strInt has a value 456 in the format of string.
[06:32] If I execute the next line, my num is going to hold a int value which is 456.
[06:38] The same is going to happen for other parsing
[06:41] also the num1
[06:42] right now it is holding a double value which is 3.14, the same inside the num2.
[06:47] You can see we are holding a float number which is 2.718.
[06:51] After that, if you try to run the code related to the parseLong(), you can see num three is going to
[06:58] hold the long value.
[06:59] Now let's try to execute the code related to the boolean.
[07:02] Here my isTrue() is going to hold the true value.
[07:05] Now coming to the ease name, it is going to hold the false value because we are trying to send an invalid
[07:11] boolean value.
[07:12] After this we have the code related to the char.
[07:16] So let me try to execute this code as well.
[07:18] The first char is going to hold the H value and now I'm trying to execute the toCarArray() method.
[07:25] Here you can see the char [] array object has a list of elements.
[07:29] The first element is h followed by e, l, l and o.
[07:34] So it is an array of char elements.
[07:36] Now if I try to execute the last line of code, the second char is going to hold the value which is e.
[07:43] With this we have executed the entire program.
[07:46] Let me release this breakpoint.
[07:48] I hope you are clear with all the parsing concepts that we have discussed.
[07:51] So always remember these methods.
[07:54] They are going to be very very useful in your real projects.
[07:58] Many times you will end up into these kind of scenarios thousands of times inside your career, like
[08:04] converting a String data into a primitive data type or converting a primitive into the String.
[08:09] So these are like daily requirements for you whenever you are trying to build business logic with the
[08:14] help of Java programming language.
[08:16] I hope you like the demo and you are enjoying the course.
[08:19] Thank you and I'll catch you in the next lecture bye.


########################################
