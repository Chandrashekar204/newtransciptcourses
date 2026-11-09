# 2.11 — Deep dive on char primitive data type - Part 2

> Section 2: Primitive data types in Java

[00:00] Are you ready for the demo of char data type?
[00:03] I know you're super ready, so let's right away jump into the demo.
[00:06] So first I'll try to show you how to create a variable of data type char and how to assign a character
[00:12] value inside it. For the same,
[00:14] the syntax is going to be very similar to other primitive data types.
[00:18] First we need to mention what is the data type, which is char here and post that
[00:22] what is your variable name?
[00:23] Usually the variables that we are trying to create with the help of char data type, they are going to
[00:29] hold a single character.
[00:31] So that's why most of the senior developers in the industry, they'll give a variable name which is
[00:36] a single character itself.
[00:38] For example, here I can say char m is equal to and what is the value that I want to store inside it?
[00:45] I want to store capital M inside these m variable.
[00:49] So there is no wrong here.
[00:51] You don't need to worry about the standards that we need to follow while we are trying to declare a
[00:56] variable name, because with this, anyone can easily understand that these m variable is going to hold
[01:02] a M character.
[01:03] But if you try to mention the name as y or x, which is something different compared to what we store,
[01:10] then definitely it's not a good practice because the other developers, they have to put some more efforts
[01:15] to understand what you have stored inside your char variable.
[01:19] I hope it is clear.
[01:20] Now let me execute this Java statement and you can see now I have a variable M created of char data type.
[01:28] And this variable has a value M inside it.
[01:31] We can also try to print the same with the help of System.out.println().
[01:35] And to this I'm going to pass what is a variable name?
[01:39] The variable name is going to be m.
[01:41] If I press enter
[01:42] here you can see I'm getting an output.
[01:45] Now let's see what will happen if I don't assign any value to my char variable.
[01:51] So here I will try to create a variable of name x.
[01:55] And to this I'm not going to do any initialization, I'm simply doing that declaration here.
[02:01] So with this a default value is going to be assigned to the x.
[02:06] So what is the default value.
[02:08] The default value is empty space.
[02:11] Inside Unicode
[02:12] the empty space is going to be represented with the help of these values.
[02:16] That's why it is showing this value here.
[02:18] But if you try to print these x variable inside your console, you should be able to see an empty space.
[02:25] You can see here there is an empty space that is displayed on the screen.
[02:29] I hope this is clear.
[02:30] Now let me try to create one more variable.
[02:33] This time I'm going to give the variable name as num and to this num
[02:38] I'm going to store the two value inside the single quotes.
[02:42] If I try to execute this statement, you can see a single value of two is stored inside the num variable.
[02:48] But if you forget mentioning the single quotes, then you're going to assign a Unicode value that is
[02:55] present at the position two inside the Unicode format.
[02:59] So let me try to execute this statement here you can see the Unicode value present at the position two
[03:04] is 002.
[03:06] The same is being displayed here.
[03:08] That's why always be cautious if you want to store a single digit with the help of char data type, mention
[03:13] them with the help of single quotes.
[03:15] So these are all happy paths.
[03:17] Like usually any Java developer inside his Java program, he will always try to store a single character
[03:24] which is available inside the keyboard.
[03:26] Most of the times we will try to store the characters which are available inside the keyboard, but
[03:31] sometimes we may end up with the requirement where we want to store some special character which is
[03:37] not available inside the keyboard.
[03:39] Maybe that special character belongs to a different language, or it can be a special symbol like smiley
[03:46] face.
[03:46] Then definitely in all such scenarios, we need to assign the Unicode value to the char variable.
[03:53] We know what is the format that we need to follow whenever we are trying to assign a Unicode value,
[03:57] but we don't know what is the exact Unicode value that we have to give for a specific special symbol
[04:04] or for a specific special character.
[04:06] So to understand more details about Unicode character, let me go to the browser. Inside the browser,
[04:11] I have opened Google and I'm trying to search list of Unicode characters inside Google
[04:17] and you can see I got the result. Inside the results,
[04:20] I'm going to open the page which is related to the Wikipedia.
[04:23] So let me open this very first link that I have here.
[04:26] Inside this page you will have all the Unicode characters.
[04:31] If you can scroll down here there is a table indicating what is a Unicode, what is a corresponding
[04:37] decimal value, what is a corresponding octal value, and what is the description of the character.
[04:42] You can see here these are all the Unicode values.
[04:45] If I can scroll down, you will be able to see the Unicode values which are familiar to us.
[04:51] For example, if I want to store these two value which is 2 , with the help of Unicode format
[04:58] I have various options,
[05:00] I can directly store two value inside my char variable r.
[05:03] I can also assign that decimal value.
[05:06] So what is the decimal value that we have here 50.
[05:09] So this is the position value that is maintained by the Unicode format for the 2.
[05:14] Here let me clean my console post that I'm going to create a variable x.
[05:19] And to this variable x I'm going to assign a numeric value which is 50.
[05:25] If I assign this 50 value to the x behind the scenes, my x is going to hold the two numeric value the
[05:32] same
[05:32] you can see here.
[05:33] That's why sometimes even if you assign some random numeric value behind the scenes, your char is not
[05:39] going to complain anything.
[05:41] But please make sure always you are assigning the numeric value, which is in the range of char data
[05:47] size.
[05:47] For example, if I try to assign some number which is not in the range of char data type, I'm going
[05:53] to get an error because this is not in the range of char.
[05:58] What is the range of char?,
[06:00] it is going to start from zero, and it is going to end at 65,535.
[06:06] Now let's go to the Unicode table one more time.
[06:08] This time I will try to print a special character which is not present inside my keyboard.
[06:15] So let me scroll down and look for some special character which is not available inside my keyboard.
[06:22] You can see here there is a symbol for pound sign.
[06:25] I don't have this pound sign inside my keyboard.
[06:28] Then how I can store and print this value with the help of char data type by assigning the Unicode format.
[06:34] Can I assign this Unicode value directly?
[06:37] I can't do that because Java have a different format that we need to follow.
[06:43] But before I try to use this Unicode value, let me try to give directly this decimal value.
[06:48] So here I will just give the decimal value as 163.
[06:52] And you can see I'm getting the pound symbol. Instead of number,
[06:56] we can also assign the Unicode value, in order to assign the Unicode value, we need to mention single
[07:03] quotes and inside the single quotes,
[07:05] first we need to mention \u.
[07:09] After mentioning this \u, you need to look for the Unicode value present inside the
[07:16] Unicode table.
[07:17] So you can simply ignore u
[07:18] and plus, by ignoring u under plus you can simply take the last four digit value which is 00A3.
[07:26] So let me mention the same here like 00A3.
[07:30] If I try to execute this, you can see I'm getting the same output which is the pound symbol.
[07:35] Are you seeing the power of Unicode and char data type?
[07:39] Most of the Java developers, they assume with the help of char data type, we can only store the simple
[07:44] characters and simple numbers, but they don't know the secret,
[07:48] now you know the secret and you will have some special edge whenever you go to and Java interview.
[07:54] And if they ask some questions around char you'll be able to answer any questions easily.
[07:59] As a next step, I want to add more fun to our demo.
[08:02] This time I want to display a smiley face. For the same,
[08:06] inside this page, please search for emoji and you can see there is an section for emoji.
[08:11] You can click on this emoji hyperlink.
[08:14] This will open a dedicated page related to the emoji Unicode symbols.
[08:20] Here there is a table showing you all the symbols and what is the corresponding Unicode value.
[08:25] Since we decided to display an smiley face, I'm going to look for a specific value.
[08:31] The specific value is going to have 263. Under the row 263X,
[08:37] there is a smiley face.
[08:39] So this face I want to display with the help of my char data type.
[08:44] Can I use this 263X.
[08:46] We cannot use this x because this x represents what is the column value inside this table.
[08:53] Inside this table under A we have this smiley face.
[08:57] So the value that I need to use is 2638.
[09:01] So let me create a variable with the name smiley.
[09:05] And to this smiley variable I'm going to assign a Unicode value.
[09:09] Whenever we want to assign a Unicode value.
[09:12] The prefix that we need to have is /u and post that
[09:17] what is the Unicode value. 263A is a Unicode value.
[09:21] So if I try to execute this command you can see I'm getting a smiley face inside my screen.
[09:27] I hope this brings smiles on your face.
[09:29] Let's try to continue this demo of char data type in the next lecture as well.
[09:33] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
