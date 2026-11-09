# 2.6 — Demo of declaring primitive data types & store data using them

> Section 2: Primitive data types in Java

[00:00] Now inside this lecture, let's try to create the variables with the help of primitive data types and
[00:06] post that we can also save some data inside them.
[00:09] So the very first demo that I want to do is with the help of boolean data type.
[00:15] So what is a boolean primitive data type, boolean itself.
[00:18] So we need to type boolean in all lowercase letters.
[00:23] Post that you can give a name to your variable.
[00:26] So the name that I want to give here is b.
[00:29] So this b we can also call it as a variable or identifier.
[00:33] After this we need to mention is equal to followed by,
[00:36] what is a value that you want to assign to these b variable.
[00:41] So the value that I want to assign here is, false.
[00:44] And at last I need to mention semicolon.
[00:46] Even if you don't mention semicolon in jshell it is going to work perfectly.
[00:51] So let me try to execute this.
[00:52] So you can see here my jshell created a variable with the name b and it has a data false inside it.
[01:00] I can also confirm this by running System.out.println() and to this println.
[01:07] I can pass the variable which is b.
[01:09] So here I'm not hard coding any value which is false directly.
[01:14] I'm simply passing the variable name and behind the scenes my Java is going to look for the memory location
[01:21] where the b variable is stored.
[01:23] Once the memory location is identified, it is going to look what is stored inside that memory location.
[01:29] Since we stored the false value, it is displaying the same.
[01:33] Now as a next step, let me try to create a variable of int primitive data type.
[01:38] For the same I need to mention int and what is the variables that I want to create.
[01:44] This time I'm going to create two variables i, j and post that I'm going to mention is equal to,
[01:51] after is equal to
[01:52] I'm going to mention 8.
[01:54] With this you can see here I'm doing only declaration for the i value, whereas I'm doing both declaration
[02:02] and initialization for the j variable.
[02:05] So what is the value that i is going to hold,
[02:08] i is going to hold the default value which is zero, whereas j is going to hold the the initialized
[02:15] value that we have provided, which is eight.
[02:17] So let me execute this.
[02:18] You can see I have two variables right now which is i and j, i has zero value and j has eight value.
[02:26] So I can also confirm that by executing System.out.println() with i and post that I'm also going
[02:33] to run the same command with the j.
[02:35] So this confirms my Java statement is perfect.
[02:38] Very similarly, let me try to create a variable for that double data type.
[02:43] After double, I'm going to mention the variable name as num and for the num I'm not going to do any
[02:49] initialization, I'm simply going with the declaration only.
[02:53] So let me give a semicolon and press enter.
[02:55] You can see the num variable right now holding the default value of double, which is 0.0.
[03:02] Very similarly, I can also create a variable of data type char. For the same,
[03:07] I need to mention char space,
[03:09] what is the variable name that I want to give for my char?
[03:13] So the variable name I can give as m and post that I'll just give is equal to.
[03:18] And whenever we want to assign a value to the char variable, we need to use single quotes (' ').
[03:23] And inside the single quotes we can mention what is a char value that we want to store.
[03:28] So here I'm going to store the capital 'M'.
[03:32] So let me give semicolon and press enter.
[03:34] And you can see now my m char variable has a value capital 'M' mentioning semicolon at the end of the
[03:42] Java statement
[03:42] inside jshell is completely optional.
[03:45] If you want, you can test one more time.
[03:47] I can remove the semicolon and execute it.
[03:51] You can see the statement is getting executed without any issues.
[03:55] So as of now we tested all positive scenarios.
[03:58] Let me show you some negative scenarios as well.
[04:01] For the same, let me clean the console of jshell.
[04:04] So to clean the console of jshell regular clear command in mac is not going to work.
[04:10] And similarly inside windows we used to use cls.
[04:13] It is also not going to work because right now we are inside the jshell session, but not in our operating
[04:19] system terminal.
[04:20] So then what is the command that we need to use to clean the jshell console.
[04:25] So it is going to be different for macOS and windows operating system.
[04:29] So to clean the console of jshell we are going to use a shortcut.
[04:33] And this shortcut is going to be different for macOS and windows operating system.
[04:38] The same I have mentioned inside our GitHub repo.
[04:41] Under shortcuts, you can see to clean console inside windows we need to press CTRL+L, whereas
[04:49] inside the mac we need to press command and K. For Linux and Unix based
[04:55] whatever shortcut we have for macOS, the same should work.
[04:59] If not, please let me know what is a shortcut that is working for you so that I can update that information
[05:05] here under the shortcuts.
[05:07] So since I'm using macOS, I'm pressing command K.
[05:11] If you are using windows, please press Ctrl+L.
[05:15] So with this my jshell is clean right now.
[05:17] Now let me show you some negative scenarios.
[05:19] For the same I'm going to use the inter primitive data type.
[05:23] After mentioning this data type I'm going to give a variable name which is one of the Java keyword.
[05:29] So here we have a list of Java keywords.
[05:31] You can select one of the Java keyword
[05:34] here I'm going to mention the name of my variable as if and see what is going to happen.
[05:39] So here I'm mentioning if is equal to and after the is equal to I'm trying to assign some value which
[05:45] is five.
[05:46] So if I try to execute this you can see I'm getting a big error.
[05:49] This indicates that we are not supposed to use the Java keywords.
[05:55] Every keyword inside Java has a meaning.
[05:57] So if you try to use those keywords as our variable names, the Java compiler is going to be confused
[06:03] and it is going to throw an compilation error.
[06:06] So let me clean the jshell by pressing command K.
[06:09] For windows it is going to be control L.
[06:12] The next negative scenario that I want to discuss here is case sensitivity is very important for your
[06:18] variable names.
[06:19] So think like I'm trying to create a variable with a name num
[06:24] and to this I'm trying to assign a value five.
[06:27] If I try to display that data inside the num variable, I need to use the exact same word with the same
[06:35] case
[06:36] sensitivity letters.
[06:37] If I try to mention some capital letters, then it is not going to work because my Java compiler is
[06:44] going to complain that I have never created a variable with the name num, where M is capital.
[06:51] I hope this is clear.
[06:52] Now let's try to test one more negative scenario.
[06:55] Think like I'm trying to assign an invalid value to the one of the primitive data type in such scenarios
[07:02] also, my compiler will throw an error.
[07:05] For example inside boolean I'm trying to store a numeric value.
[07:11] So here I have mentioned boolean b = 1.
[07:14] So if I try to execute this command, you can see I'm getting an error saying that, " int cannot be converted to a boolean ".
[07:21] .
[07:22] Very similarly let me try to assign some char value for Integer data type.
[07:27] So here I'm going to mention int num is equal to and I'm going to assign 'M' char,
[07:34] if I try to execute this you may expect a compilation error
[07:38] but we're not going to get compilation error.
[07:40] Instead we're going to get an output 77.
[07:43] So this is a tricky situation.
[07:45] I'm going to talk more about this when we are trying to discuss about char data type in the coming lectures.
[07:50] But what is happening here is char though it is going to accept the char values behind the scenes, it
[07:56] is going to store each char value using a numeric value.
[08:00] So for capital 'M' behind the scenes it is going to store as a 77 numeric value.
[08:05] That's why we are seeing the 77 numeric value assigned to the num variable here.
[08:09] So Java is very interesting.
[08:11] There are so many tricky scenarios which we need to be aware.
[08:15] So I'm going to teach you as many tricky questions as possible so that it is going to help in your projects
[08:21] or in your interviews.
[08:22] But since it is not possible for me to teach each and every possible tricky scenario, my request is
[08:29] to always try to make lot many mistakes so that you can try to understand why a particular Java statement
[08:36] is working.
[08:37] If it is not working, then you can focus to understand why it is not working.
[08:41] With this, I'm assuming at least you have some basic understanding on how to store data with the help
[08:47] of primitive data types inside Java programming language. Like you can see here, we are taking baby
[08:53] steps
[08:54] here we are trying to learn concept by concept slowly.
[08:57] And all these concepts are very basic.
[09:00] If you are comfortable with all these basics, my request is to watch the lectures at a faster speed,
[09:06] so that you can quickly move on to the sections where you are more interested.
[09:10] But please don't skip any lecture because regardless of how much you learnt in Java, there will be
[09:16] always new information.
[09:17] So there might be some new information for you in all these lectures, even though you are familiar
[09:22] with the particular topic.
[09:23] That's why I will not recommend you to skip the complete lecture.
[09:26] Instead, please watch the lectures at a faster speed.
[09:29] I hope you are clear,
[09:31] thank you and I'll catch you in the next lecture bye.

----------------------------------------
