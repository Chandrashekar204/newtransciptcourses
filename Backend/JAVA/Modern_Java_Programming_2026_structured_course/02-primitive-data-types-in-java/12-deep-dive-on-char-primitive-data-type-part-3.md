# 2.12 — Deep dive on char primitive data type - Part 3

> Section 2: Primitive data types in Java

[00:00] Now inside this lecture, let's continue that demo of char data type.
[00:04] This time I want to show you that demo of Escape sequence.
[00:08] Previously we discussed that whenever we want to define some special characters like tab space, next line,
[00:14] we need to use the backslash as an escape sequence.
[00:19] For example, whenever we want to assign a new line to the char data type, we need to use the
[00:26] \n.
[00:27] So let me try to create the same.
[00:29] For the same I'm going to mention char newLine,
[00:33] newLine is a variable name is equal to single quotes inside single quotes.
[00:37] I'm going to mention the backslash which is going to act as an escape sequence
[00:41] here.
[00:42] Post this I need to mention n. If I don't mention this escape sequence, which is backslash, then my
[00:48] n is going to be a simple character.
[00:51] So if I try to execute this, you can see I'm simply getting a n value.
[00:55] That's why whenever you have these kind of situations, always use backslash as an escape sequence.
[01:02] So now if I try to execute this you can see newLine variable has this value.
[01:07] If I try to print this newLine you will be able to see a new line has been printed on your screen.
[01:13] So let me try to print this variable.
[01:16] The variable is newLine.
[01:18] So if I try to print this you can see right now the space between these two statements is increased
[01:24] because a new line is printed.
[01:26] We cannot see that with our own eyes, but you'll be able to see the space between these two statements.
[01:32] Very similarly
[01:33] sometimes you may want to assign some special character to your char variable.
[01:37] For example, I want to create a variable x and to this x I want to assign backslash because I want
[01:46] to display backslash onto my screen.
[01:48] If I try to execute this, I'm going to get an error because there is a meaning for backslash inside
[01:54] the char data type.
[01:56] We're going to use this backslash in many places like whenever we are trying to define Unicode value,
[02:01] or whenever we are trying to create some special values like new line, backspace, tab space.
[02:07] So that's why my compiler has a confusion here.
[02:10] So in this kind of scenarios we should always use this escape sequence which is backslash.
[02:15] And if you really want to print the backslash itself then you need to give one more backslash here.
[02:21] And if you try to execute this you can see this value is going to be assigned to your char variable.
[02:27] If I try to print this I'm going to get only a single backslash.
[02:32] So that's the purpose of escape sequence or backslash inside char data type.
[02:37] So whenever you have this kind of special requirements always make sure you are mentioning the backslash
[02:43] followed by what is a special symbol that you want to assign to your char variable.
[02:48] As a next step, let's try a tricky example.
[02:51] For the same,
[02:51] I'm going to clean my console by pressing command K, inside window
[02:56] it is going to be CTRL+L.
[02:57] So here first I'm going to create a variable m and to this variable m I'm going to assign M itself.
[03:05] And post that I'm going to create one more variable num.
[03:09] And to this num variable I'm going to assign a character 2.
[03:13] So now I have two different characters.
[03:15] Sometimes in interviews or in some exams, people can try to trick you by asking a question like, can
[03:22] I try to print out these two variables by summing up?
[03:26] So that can be a question like here I'm trying to mention m plus and what is the second variable.
[03:32] So I'm trying to add two char variables.
[03:35] You may think this is not possible because we can't add a numeric value with the alpha value.
[03:41] But technically this is possible because inside char data type, each and every character is going to
[03:49] have a unique or decimal value.
[03:52] So those decimal values are those decimal positions will be considered by the Java compiler to add them.
[03:59] So that's why if I try to execute this, I'm going to get an output 127.
[04:04] So let's try to see how we are getting these 127.
[04:07] So if you go back to the Wikipedia Unicode characters website here we can look for what is a value
[04:14] that we have for M.
[04:16] So let me scroll down,
[04:17] scroll down for M the value is 77.
[04:22] Very similarly for 2 let's see what is a value.
[04:25] So for the digit 2 we have value as 50.
[04:29] So what is a sum of 77 and 50.
[04:32] It is going to be 127.
[04:35] The same we are seeing on the screen.
[04:37] I hope this is clear.
[04:38] As the last step,
[04:39] I want to introduce you to the special class available inside the Java library
[04:44] and this class is Character.
[04:47] So the class name is Character.
[04:49] Inside this Character, there are many static methods that we can use as a helper
[04:54] methods.
[04:54] Whenever we are trying to deal with the char data type values.
[04:57] For example, I have a variable
[05:00] which is M. If I want to check if this M variable has a capital value or a lowercase value, I can invoke
[05:07] a method which is isLowerCase().
[05:10] So you can see I'm just pressing the tab, and it is going to give all the methods which are going to
[05:16] start with the isLow().
[05:17] So the method that I'm interested here is isLowerCase().
[05:21] To this I'm going to pass the M variable.
[05:24] So what is the output that you're expecting.
[05:26] The output we can expect here is false because my M character that I have stored here has a capital
[05:34] value.
[05:34] Very similarly, if you want to convert this M character to a lowercase value, we can also do that
[05:40] with the help of a helper method available inside the Character.
[05:43] So let me try to invoke that method.
[05:46] The method name is going to be .toLower()
[05:50] So let me press tab and you can see the name completely populated.
[05:54] So to this method I'm going to pass the variable name which is M.
[05:59] So as of now my m variable has char value in the capital letter.
[06:03] If I try to execute this I'm going to get an output which in the small m.
[06:09] So as of now I'm not trying to assign the output from this method to any variable.
[06:13] That's why behind the scenes my jshell is trying to assign this value to a random memory location,
[06:19] but if needed, I can try to change this statement by mentioning char x is equal to Character.LowerCase()
[06:26] .
[06:27] And what is the variable name which is m.
[06:30] With this now my x variable is going to hold the lower value of m.
[06:35] Very similarly, we also have some methods which will help us to identify whether a given character
[06:42] is a number or not.
[06:43] To invoke those methods, we need to use the Character class.
[06:48] Inside this Character class there is a method with the name isDigit(), which is going to help us to
[06:55] identify whether a given char variable is a digit or not.
[06:59] So here I can pass m variable.
[07:01] So obviously we are going to get an output as false.
[07:04] Whereas if I pass the variable name as num I'm going to get true because under num we are trying to
[07:11] store the value 2 here, which is a digit.
[07:14] That's why whenever you have this kind of requirements where you want to execute some business logic
[07:20] on top of char variable, then first look for methods available inside the Character class.
[07:26] And if there is some method which is going to help you inside your business logic, you can always use
[07:31] that instead of writing your own business logic. We are going to discuss more about classes, methods
[07:37] in the coming sections, but I just wanted to give a quick introduction about these Character class.
[07:42] Since we are discussing about the char data type.
[07:45] With this, I'm going to conclude that discussion around the char data type.
[07:49] But my humble request is please try all the examples that I have demoed for you apart from these scenarios,
[07:56] please go and try some random scenarios based upon your own thoughts.
[08:01] This way you're going to be perfect at the Java programming language.
[08:05] I hope this is all clear to you.
[08:07] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
