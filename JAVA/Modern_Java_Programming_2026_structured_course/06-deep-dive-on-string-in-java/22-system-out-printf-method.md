# 6.22 — System.out.printf() method

> Section 6: Deep dive on String in Java

[00:00] In the previous lecture, we discussed about the format() method available inside the String.
[00:05] Using this format() method, we can format a string by replacing the placeholders with the dynamic values
[00:12] at runtime.
[00:13] Here you can see I have an example with the help of String.format() method, where I have two placeholders
[00:19] %s and %d to this placeholders I'm trying to pass the name value and the age value.
[00:26] Once the String is formatted, I'm trying to print the result with the help of System.out.println() method.
[00:33] If I execute this program like you can see, we are able to print the formatted string on the console
[00:40] along with the dynamic values like what is the name and what is the age.
[00:44] Here the problem is my println() method always expects a well formatted string along with the replacing placeholders
[00:52] with that dynamic values.
[00:53] So whatever println()
[00:55] right now we are using,
[00:56] it has a limitation.
[00:57] It cannot format the string and it cannot replace the placeholders with the dynamic values.
[01:03] To overcome this challenge, we have a printf() method available inside Java.
[01:08] So how to invoke the printf() method?
[01:10] Let me show you that it is going to be very similar, like I'm going to mention first System post that
[01:15] I'm going to invoke out, and after the out, I need to invoke the printf() method and this printf() method
[01:23] first it is going to accept the format string
[01:26] like I can pass this entire content directly to the printf() method.
[01:30] With this, what is going to happen is, my printf() method behind the scenes
[01:34] first, it is going to format my string by replacing the placeholders with the dynamic values.
[01:40] Post that it is going to take care of printing the given string onto the console.
[01:45] I can show you the demo of this line as well by executing the program.
[01:49] Before that, let me comment these two lines of code.
[01:52] So to comment a block of code, I'm using a shortcut which is command option forward slash inside window
[01:59] it is going to be Ctrl + Shift + /.
[02:02] Now I have commented the code I can run this program.
[02:05] And here you can see I got an output like name John and age as 25.
[02:11] But the problem with the printf() method is once it printed a given method onto the console, it is not
[02:17] going to move the cursor to the next line.
[02:20] That's why you can see the next statement we are able to see immediately after our given statement.
[02:26] Whereas the println() method that we used to use before it has the ability to move the cursor to the next
[02:33] line once the printing of the statement is completed.
[02:36] So to resolve this issue, what we have to do is whenever we are using printf() method just at the end
[02:42] of your string, please provide %n, with the %n
[02:47] we are telling to the printf() method to move the cursor to the next line, so that my output is going
[02:53] to be clear on the console.
[02:54] Now let me run this program and this time you can see the statement is printed and the cursor also moved
[03:00] to the next line
[03:01] that's why we are able to see the statement in the next line.
[03:04] I hope this is clear.
[03:05] Now let me show you a few more examples with the help of printf() method.
[03:09] This time I want to display a price value with the help of printf() method.
[03:14] So let me copy this entire printf() statement.
[03:17] And here I'm going to update the string as Price :
[03:22] and I'm going to mention %f.
[03:24] So this is the statement that I want to provide to the printf() method.
[03:28] Since we have only one placeholder which is of type float, I'm going to provide a float number which
[03:34] is 19.99.
[03:36] So if I run this program you can see we are going to get the price value.
[03:41] But it is trying to show more accurate decimal points.
[03:44] So to fix this issue we have to follow the same approach like we discussed in the previous lecture.
[03:50] So just before f we need to mention point two.
[03:53] And one more issue that we have observed inside the console is the cursor is not getting moved to the
[03:59] next line immediately.
[04:00] So to overcome this issue we have to mention %n at the end of the String.
[04:06] So now if I try to print this statement this time they should not be any issues.
[04:10] Now let me show you an example how to display a char value with the help of printf() method.
[04:17] I'm going to copy the same statement and here in the place of price I'm going to mention grade.
[04:23] And whenever we want to display a char value, we need to use %c.
[04:28] That's what I'm trying to use here.
[04:30] And %n obviously we have to use to move the cursor to the next line.
[04:34] So the char value I want to display here is A.
[04:38] So someone got a grade A.
[04:39] .
[04:40] So that's what I'm trying to display onto the console with the help of printf() method.
[04:44] If I execute this program, you can see it is working like we expected.
[04:48] I can show you one more last example, and this time I'll try to print out a boolean value for the same
[04:54] I'm going to change the string value to Is Java fun ?, so I'll just put
[05:00] statement as a question, and instead of c, we need to mention b, because we are trying to display boolean
[05:05] value.
[05:06] And the argument that I need to pass here is true.
[05:09] So this true value is going to be considered in the place of placeholder that we have mentioned, which
[05:15] is %b.
[05:16] So let me try to execute this program.
[05:18] And this time you can see we are getting the expected output which is Is Java fun ? : true.
[05:24] .
[05:24] So whatever concepts that we have discussed as part of String.format() method, the same applies for
[05:30] the printf() method as well.
[05:32] So printf() method is a convenient method available inside Java which is going to take care of formatting
[05:39] your string.
[05:40] And at the same time it is also going to print your statement onto the console.
[05:44] If you try to achieve this with the help of String.format() method, first you need to format your
[05:49] string post that you need to use the println() method.
[05:52] So to avoid writing two lines of code, we can simply use printf() method.
[05:56] I hope you are clear about the printf() method.
[05:58] Before I try to close this lecture, let me explain you about a difference between the println() method
[06:04] and the print() method. For the same
[06:06] first I'm going to invoke System.out, and after the out I'm going to invoke the print() method
[06:12] not the println().
[06:14] So there are print() methods and also there are println() methods.
[06:18] So there is a minor difference between print() and println() methods.
[06:22] Let me show you that.
[06:23] Here I can invoke the print() method.
[06:25] And to this print() method I'm going to mention some sample string like saying that sample string value.
[06:33] Now using the same statement, I'm going to print one more second statement as well.
[06:38] This time I'll change the string value to another string value.
[06:42] If I try to execute this program.
[06:44] You can see the print() method is going to print whatever you are giving as an input, but it is not going
[06:51] to move the cursor to the next line.
[06:54] That's why the next string is displayed on the same line
[06:57] and at the end we have this statement as well.
[07:00] This is because the cursor is not getting moved to the next line.
[07:04] Whenever we are trying to display a content onto the console.
[07:08] So if you have a requirement to move the content to the next line and to see your output in an easily
[07:14] understandable format, then you should use the println() method.
[07:18] So if I try to execute the same statements with the help of println(), this time, you should be able
[07:25] to see that my cursor is getting moved to the next line.
[07:29] So let me execute my program.
[07:31] You can see these are the output that got printed from the print() method.
[07:35] The print() method is not going to move your cursor to the next line.
[07:39] That's why immediately we have another string from the println() method which is sample string value.
[07:45] And after printing this output, my println() method is going to move the cursor to the next line
[07:50] that's why we are able to see the next string in the next line.
[07:53] And after printing this string my print ln method again, move the cursor to the next line.
[07:58] That's why we are able to see the last statement in the next line.
[08:02] I hope you are clear.
[08:03] Please don't get confused why this sample string value is not moved to the next line, because the previous
[08:09] statement, which is executed with the help of print() method, it kept the cursor at this point only
[08:16] that's why whenever I tried to execute next statement, the statement is going to be displayed from
[08:22] this point of cursor.
[08:23] Most of the times developers they are going to use the println() methods, but inside interviews and
[08:28] inside some exams related to Java, they will try to confuse you by asking the difference between print()
[08:35] ln method and println() method.
[08:36] So there is nothing to confuse here.
[08:38] println() method always moves your cursor to the next line once the statement is printed, whereas print
[08:45] and printf methods they are not going to move the cursor anywhere.
[08:48] They are going to start the printing of the statements immediately from the same position where the
[08:54] cursor is right now present.
[08:56] I hope you are clear with all these concepts.
[08:58] Since we discussed about format method in the previous lecture, I thought it would be a wise decision
[09:03] to discuss about the printf() method immediately so that it is going to be more clear for you.
[09:08] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
