# 2.10 — Deep dive on char primitive data type - Part 1

> Section 2: Primitive data types in Java

[00:00] Now, inside this lecture, let's try to discuss in detail about the char primitive data type.
[00:06] We already know on a high level, using char data type we can store a single character.
[00:11] For example, using single quotes I can store a character M.
[00:16] We also learned that the size of the char data type is two bytes or 16 bits.
[00:22] With this 16 bit size, my char data type can store up to two power of 16 different characters.
[00:30] If you try to convert that two to the power of 16, it will come around the 65,536.
[00:37] But since inside Java, the counting is going to start from the zero, you're able to see a number here,
[00:42] which is 65,535.
[00:44] And here you may have a question like why char data type need two bytes are 16 bits.
[00:50] Can't it store all the elements on the keyboard with the help of a single byte or eight bits?
[00:56] Off course it can store if you go with a single one byte size for the char data type, it can store a
[01:01] maximum elements of two power of eight are 256 elements, and within that 256 element, it can easily
[01:08] accommodate all the elements that we have on the keyboard.
[01:12] Then why Java team assigned a size of two bytes to the char data type.
[01:16] So this is going to be a famous interview question for you.
[01:19] The reason why Java team decided to go with the two bytes as 16 bits for the char data type is, they want
[01:26] to accommodate all kind of languages, all kind of special characters
[01:31] with the help of this char data type, I'm going to show you a demo in few minutes.
[01:36] Then it is going to make sense more to you.
[01:38] And whenever we are using char data type inside Java internally it is going to use the Unicode format.
[01:45] So what is Unicode universal International standard character encoding.
[01:50] So this Unicode format is capable of representing most of the written languages that are available in
[01:57] the world.
[01:58] For example, if you take English in English we have 26 letters.
[02:02] With these 26 letters only all the words present inside the English is going to be formed. Very similarly
[02:09] there can be other languages like Hindi is one language, German, Spanish, French.
[02:15] So there are many languages available and each language will have their limited set of alphabets.
[02:21] So all those alphabets of different languages, along with the special characters, are accommodated
[02:27] with the help of these Unicode format.
[02:29] That's why Java also is going to use this Unicode format.
[02:33] Apart from Unicode format there are Ascii format ISO format.
[02:37] They have some disadvantages.
[02:39] That's why most of the programming language they are going to use the Unicode format.
[02:43] I'm going to show you a few details about the Unicode format in few seconds.
[02:47] So please brace yourself for that information.
[02:49] But before that, I want to quickly show you how we are going to declare variables with the help of
[02:55] char data type. Like you can see here
[02:57] if I want to store a single char like 2 or M, I can create the variables with the syntax like char
[03:04] name is equal to two or char x is equal to m.
[03:06] And whenever you are not initializing any value for your char variable behind the scenes, it is going
[03:12] to hold the empty value.
[03:13] So that's what
[03:14] here you can see
[03:15] I'm simply trying to declare char y, but I'm not trying to initialize with any value.
[03:20] So behind the scenes y is going to hold the empty value.
[03:24] Most of the times we are simply going to assign our required character to the char variable.
[03:29] But sometimes we may want to assign a special symbol like a smiling face, which is smiley emoji.
[03:36] So all such kind of variables
[03:37] if you want to assign to a character, then you can't type that with the help of keyboard.
[03:42] That's why in such scenarios, either you can give the Unicode format by following a format called
[03:49] \u or you can also directly assign the decimal value of that special character inside the Unicode format.
[03:56] So that's what you can see here
[03:58] I'm trying to create two variables, which is char x1 one with an Unicode value.
[04:03] And very similarly for char z I'm trying to assign a number.
[04:06] So what is going to happen with these assignment is, behind the scenes
[04:09] the Java is going to look for what is the character that is going to be represented by that specific
[04:14] number or by that specific Unicode value.
[04:17] The same is going to be stored inside the char variable.
[04:21] So when I show you this in the demo it is going to make sense to you.
[04:24] But before we try to go and look at the demo, let me show you the next slide as well.
[04:29] I was telling before, Java also supports Unicode format whenever you want to assign some data to a
[04:36] char variable.
[04:37] So whenever you want to follow the Unicode format, you should make sure that your character is always
[04:43] starting with \u
[04:46] indicates Unicode post that you need to mention what is the value of that character inside the Unicode
[04:54] table.
[04:54] For example, inside the Unicode table, the value for the 2 character is 0032
[05:00] .
[05:00] If I try to assign this 0032 to the x1 variable behind the scenes, my char variable is going to hold
[05:08] the character, which is two.
[05:09] But like I said, if you want to simply use a simple character like 2 or A or M which is available
[05:16] inside the keyboard, always go directly mentioning that specific character.
[05:20] Only use this Unicode format in a scenario where you can't type that character with the help of your
[05:27] keyboard, and apart from normal characters, char data type also supports various spacing related characters.
[05:34] Like using char
[05:35] you can store a new line tab space or if needed, you can also store special characters like backslash.
[05:42] So to store a tab space inside char, then you need to use \t, whereas if you want
[05:50] to store an empty value, then you can mention \000.
[05:54] And very similarly if you want to store the backslash value inside char data type, then you need to
[06:00] mention two \\ inside your char variable.
[06:04] And sometimes if an interview person he wants to trick you, he may ask you a question like what happens
[06:10] if I try to add two character variables?
[06:13] We know using char we can only store the different characters, but can we add those two characters?
[06:19] Off course, from a normal common man perspective, we cannot add it to different characters.
[06:24] Here you can see I'm trying to create two variables x and x1, inside x I'm trying to store M, whereas
[06:31] inside x1 I'm trying to store 2.
[06:33] Can I add M plus 2?
[06:35] Off course it is not possible, but if you try to add these two variables behind the scenes, Java compiler
[06:42] is going to give you a proper output without throwing an error, because this M behind the scenes is
[06:47] going to have some numeric value assigned.
[06:50] We all know the size of char data type starts from 0 to 65,535.
[06:55] In that range, M is going to have one number assigned, and similarly two also is going to have some
[07:01] number assigned to it.
[07:02] So if you try to add these M and 2 behind the scenes, my Java compiler is going to add the numeric
[07:09] values that are represented by these characters in the char data type range.
[07:14] I hope this is clear.
[07:15] If something is not clear, don't worry,
[07:17] when I show you the demo it is going to be make sense to you.
[07:20] And at last I also want to highlight you that inside Java there is a class called Character.
[07:26] So for char data type we have a Character Java class.
[07:29] Inside this Java class there are number of static methods are available that we can use inside our business
[07:36] logic.
[07:37] For example, if you want to identify if a given character is a digit or not, then there is a function
[07:43] or a method with the name isDigit()
[07:45] available inside the Character class?
[07:48] And very similarly, if you want to identify a particular character is available in a lower case, then
[07:55] you can use a method called isLowerCase().
[07:58] And if you have a requirement to convert that lower case letter to a uppercase, there is a method called
[08:03] toUppercase().
[08:04] This way there are many methods available inside Character class.
[08:08] I'm going to show you a quick demo about these methods as well in the coming lectures, but as of now,
[08:13] I know we have not discussed about what is a Java class,
[08:16] what is a Java method?
[08:18] It is going to be make more sense to you when we start discussing about these advanced concepts like
[08:23] Java class and Java methods in the coming sections.
[08:26] I also mentioned for your reference, what are the various escape sequences that we need to use to represent
[08:33] various values with the help of char data type?
[08:35] For example, here, if you mention \b, it is going to hold the backspace value inside your
[08:42] char variable.
[08:43] Very similarly, we can use horizontal tab, new line, form field, carriage return, double quote, single quote
[08:50] backslash.
[08:51] So all these kind of special values we can easily store with the help of escape sequence inside char
[08:58] data type.
[08:58] So what is the escape sequence.
[09:00] Whenever we are starting a element with a backslash value it is going to act as a escape sequence.
[09:08] For example, if you see for backspace, if I simply mention b, then my Java compiler does not know
[09:14] whether it has to go for the backspace or a normal b character.
[09:18] So to avoid such confusion, if I mention the escape sequence which is backslash, and with that to
[09:25] my compiler, it is going to be super clear that it has to hold a backspace value.
[09:29] I hope this all clear to you, if there are some questions
[09:32] don't worry,
[09:33] when we see the demo of all the scenarios in the next lecture, it is going to make more sense to you.
[09:38] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
