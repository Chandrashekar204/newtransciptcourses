# 6.14 — Converting values as String

> Section 6: Deep dive on String in Java

[00:00] Sometimes you may have scenarios inside your real projects where you want to store an int number or
[00:07] a float number or a boolean value, or a given char in an String format.
[00:13] To handle these kind of scenarios, we need to understand how to convert a given input data as a String,
[00:20] inside a String class, we have a static method with the name valueOf().
[00:24] To this value of static method, we can pass any kind of data like I can pass into value, double value
[00:32] or boolean value or char value.
[00:34] The output from these valueOf() method is going to be the String representation of given input data.
[00:41] Imagine these valueOf() method as a magic box.
[00:45] You can put any kind of data inside this magic box.
[00:48] By the time you open this magic box, you're going to see the String representation of the data here.
[00:55] First you can see I have created int value, double value, boolean value with their respective primitive
[01:00] data types.
[01:01] The requirement that I have here is to convert these data values into the String representation.
[01:07] For the same I can use the value of static method.
[01:10] Since the value of is a static method, we can invoke it directly with the help of String class name.
[01:16] You can see I'm trying to invoke String dot valueOf(), and to this I'm trying to pass the variables
[01:21] that I have created like int value, double value and boolean value.
[01:25] By the time my valueOf() method is executed, this is how the output is going to be 42 3.14 and true,
[01:33] they're going to be converted as a String data.
[01:36] That's why you're able to see the double quotes around the data.
[01:39] There is also one more easier approach to convert your data into String.
[01:45] And this approach is with the help of concatenation operator, which is plus symbol that we have discussed
[01:51] previously.
[01:52] Whenever you have a String already in your hand, and if you try to append the new data, maybe it can
[01:58] be an integer or float or it can be a boolean.
[02:02] You can simply mention that new data just after the plus symbol, and by the time the concatenation
[02:09] operation completed, the new data that you are going to get will be completely inside the String format.
[02:15] So here you can see I'm trying to create a variable first age which is of primitive data type int.
[02:22] And inside this I'm trying to store that value post that.
[02:26] I'm trying to create a String object which is String message is equal to.
[02:30] And I have mentioned some String literal value, which is my age is semicolon
[02:36] and after this String object I am trying to append the new data.
[02:41] That's why I'm using this plus symbol.
[02:43] And the new data can be a another String, or it can be another data value as well.
[02:49] Here I'm trying to pass the age variable which is of type int, but my compiler is not going to complain
[02:55] anything
[02:55] it is simply going to convert the int value into the String the same
[03:01] you can see inside the next line as well.
[03:03] I am trying to create a String object with the name pie value, and here my requirement is simply to
[03:09] convert the 3.4 into the String.
[03:11] I can use valueOf() method, or I can try to append this 3.4 with the help of plus symbol by using an
[03:19] empty string.
[03:19] So this is one of the shortcuts you can use if you don't want to use the valueOf() method.
[03:25] There is no better or bad inside these two approaches.
[03:29] Based upon your convenience, you can use any of these approaches.
[03:33] Can we see this in the demo?
[03:34] Let's create a Java class inside our intelliJ.
[03:37] To show you the demo, I'm going to create a new Java class here.
[03:41] The class name is going to be ConvertStringDemo.
[03:45] And inside this class I'm going to create the main method inside the main() method
[03:50] first I'm going to create some variables which are going to hold the data other than String.
[03:56] So first I'm going to mention the variable name as into value and inside this into value I'm going to
[04:02] store 42 number post that.
[04:05] Very similarly I'm going to create double value
[04:09] and inside this double value I'm going to store 3.14 decimal number.
[04:15] Very similarly using boolean primitive data type
[04:18] let me save a boolean value which is none other than true.
[04:24] Now using the valueOf() method, I will try to convert all these data into the String format.
[04:30] So for the same, let me create the String object with the name str one and post that I'm just typing
[04:36] the class name of String, which is String, and after that I'm going to mention dot operator and type
[04:42] for valueOf().
[04:44] You can see there are so many valueOf() methods you need to invoke the value of method that accept your
[04:52] respective data.
[04:53] So first I want to pass the int value.
[04:56] That's why I need to invoke the very first method which is accepting
[05:00] the int as an input.
[05:02] Like we discussed previously, inside Java, we can have multiple methods with the same name
[05:07] as long as the method signatures are different.
[05:10] My JVM should accept multiple methods with the same method name.
[05:14] So this concept we call it as method overloading.
[05:18] We are going to discuss about these in detail in the coming sections.
[05:22] But now let's invoke the valueOf() method that is going to accept int as an input.
[05:27] And the output from this method is going to be String object.
[05:31] So let me invoke this.
[05:32] And to this I'm going to pass the variable which is int value.
[05:36] Very similarly I'm going to paste this line two times and change the variable names to str2 and
[05:43] str3.
[05:43] In the second line I'm going to pass double value, and similarly in the third line I'm going to pass
[05:51] bool value.
[05:52] If I try to execute this program, we can see the String representation of these data that we have passed.
[05:58] So let me execute this program.
[06:00] And you can see the str1 has 42
[06:03] but in a String data. How I know it is a String data, because we are able to see the double quotes around
[06:09] the 42 value.
[06:10] The same you can see for str2 and str3.
[06:14] Let me release this breakpoint if needed
[06:16] we can also pass the char value as well.
[06:19] I can show you one example by creating an object str4, and I'll pass the char value directly
[06:26] here I'll just mention the value as M with this
[06:29] if you try to execute the program, the str4 is going to hold the string representation of M.
[06:35] That's what we are able to see here.
[06:37] Let me release this breakpoint and show you another approach that we have discussed with the help of
[06:42] concatenation operator.
[06:44] Here first I'm going to create a variable of type int
[06:47] and it is going to hold the 30 value and post that
[06:52] I'm going to create a variable with the name message of type String.
[06:57] And to this message variable I need to assign the String value.
[07:02] The String value that I want to assign here is " My age is : space, and with this I'm going to have
[07:10] this String whatever I have typed here.
[07:12] But I want to append the age data as well.
[07:15] So what I can do here, I can type plus and post that
[07:19] I can pass the age variable which is age
[07:22] and with this you can see there is no compilation error.
[07:25] Though we are trying to append the inter data to the String.
[07:28] My compiler is not complaining because my concatenation operator behind the scenes
[07:33] it is going to convert this age data into the String before it is tried to append to the first String.
[07:38] Let me show you other example as well.
[07:41] So here I'm going to create a String object with the name piValue.
[07:45] This time I will simply mention empty String and to this empty String I'm going to append 3.14, which
[07:52] is a double number.
[07:53] So this is a shortcut that we can use to simply convert a data into a String without using the String.valueOf()
[08:00] method.
[08:01] So if I try to execute this method, the output should be like we expect.
[08:06] You can see under the message we have a complete sentence, which is My age is : 30, and
[08:12] the pie value is going to have 3.14 in a String format.
[08:16] I hope you are clear with this discussion around the value of method and concatenation operator.
[08:22] So whenever you are into the situations where you want to convert a given data into a String representation,
[08:29] then always feel free to use these approaches.
[08:32] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
