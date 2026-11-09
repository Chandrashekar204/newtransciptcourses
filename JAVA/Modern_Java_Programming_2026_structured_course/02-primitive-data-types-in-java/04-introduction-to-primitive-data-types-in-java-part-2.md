# 2.4 — Introduction to Primitive Data types in Java - Part 2

> Section 2: Primitive data types in Java

[00:00] In the previous lecture, I gave a very quick introduction about the primitive data types that we have
[00:05] inside Java.
[00:06] Using these primitive data types, we can store simple data whenever we are trying to write some business
[00:13] logic with the help of Java programming language.
[00:16] Now, inside this lecture, let me try to answer your burning question why we have so many different
[00:21] data types, what kind of data that we can store using these primitive data types.
[00:26] So all these kind of questions I want to answer by giving the data about this primitive data types in
[00:32] the tabular format that you are seeing on the screen.
[00:35] The very first primitive data type that I want to discuss here is, boolean.
[00:39] What is the purpose of boolean primitive data type?
[00:41] Using these data type, we can store true or false.
[00:45] By default,
[00:46] whenever we are trying to create a variable using this data type, it is going to store the value as
[00:51] false.
[00:52] So what is the need of true and false inside Java programming language?
[00:56] Sometimes we may want to write some business logic based upon certain conditions.
[01:01] If so-and-so condition is true, or if so-and-so condition is false, then only execute these business
[01:07] logic.
[01:07] In all such scenarios, we are going to use boolean data type, and the size of this boolean data type
[01:13] is one bit, and there is no range of values for boolean data type because it is going to support only
[01:20] two different values, which is false and true.
[01:23] After boolean we have char data type.
[01:26] Using these char data type we can store the letters like I can store a letter A, B, C.
[01:33] So any single letter or any special characters like dollar value or asterisk or ampersand.
[01:40] So all such special characters
[01:42] also we can store with the help of these char data type.
[01:46] By default, the char data type is going to have the empty value.
[01:51] So whatever default value that you are seeing on the screen, that indicates empty value.
[01:56] So this is the Unicode representation of empty value.
[02:01] We are going to talk more about char data type in the coming lectures.
[02:04] And during the same discussion I am going to teach you about what are these Unicode characters.
[02:09] And the size of the char data type is 16 bits or two bytes.
[02:14] Inside computer we know one byte is equal to 8 bits.
[02:18] Since char has size of two bytes,
[02:20] we can also say the size of char is 16 bits as well.
[02:24] The range of values supported by char you can see on the screen.
[02:28] So these are the Unicode values.
[02:29] I am going to discuss more about them in the coming lectures.
[02:32] But here I want to share an very important information about char.
[02:36] Sometimes inside an Java interview you may face a question, which is why char is of two bytes instead
[02:43] of one byte.
[02:44] Because whenever we have a size of one byte, which means eight bits, it is going to support total
[02:50] 256 length of values.
[02:53] Why 256?
[02:54] because two power eight is equal to 256.
[02:58] Using these 256 size, we can easily store all characters available inside our keyboard.
[03:05] Then why?
[03:06] char data type is using two bytes, which is going to give the size of two power of 16.
[03:11] So what is the value of two
[03:13] power of 16?
[03:14] It is going to be somewhere more than 65,000.
[03:17] That means using char data type, we can store more than 65,000 different values.
[03:24] Why do we need such a big size for char
[03:26] data type is, usually
[03:28] there are many languages throughout the world.
[03:30] Inside keyboard we always use a global language which is English, but at the same time we also have
[03:36] many other languages and also there are many and many special characters are coming into picture day
[03:42] by day.
[03:43] Special characters like emojis,
[03:45] so there is a smiley face.
[03:47] There is a sad face, that we use in WhatsApp.
[03:50] So to accommodate all those special characters, along with all the other language alphabets, we have
[03:56] the char data type size as two bytes.
[03:59] With only one byte, we can only store a maximum of 256 values, whereas with the two bytes we can store
[04:07] more than 65,000 values.
[04:09] I hope you are clear.
[04:10] Now moving on to the next data type, which is byte.
[04:13] Using byte we can store numbers.
[04:16] When I say numbers, these numbers are going to be whole numbers without any decimal values.
[04:22] The size of byte is one byte itself, which means with the help of byte, we can store up to 256 values.
[04:30] So that's why the range you can see on the negative side it will go up to -128
[04:36] and on the positive side the value is 127 but not 128.
[04:41] Do you know the reason why?
[04:42] Because the positive side, the starting point is going to be zero.
[04:46] Always the positive side number is going to be one value less than compared to the negative side number.
[04:53] So if you try to count all the numbers between -128 to 127,
[04:59] it is going to give the count value as 256.
[05:03] So using byte we can store the range of whole numbers from -128 to 127.
[05:10] Very similarly, we also have short data type.
[05:14] So the size of the short data type is two bytes.
[05:17] That means we can store the total values of size two power of 16.
[05:22] So the range is going to be on the negative side
[05:25] it is going to be -32768.
[05:28] And the positive side it is going to be 32767.
[05:32] You don't have to remember these range values, but please remember the size which is like two bytes
[05:38] or 16 bits.
[05:39] So if someone asks you what is the size of short or byte, you can simply say one byte or two bytes.
[05:45] No one expects you to remember these values, but I'm going to show you how to identify the range,
[05:52] or the minimum or the maximum values of a particular data type using Java programming language in the
[05:57] coming lectures.
[05:58] For now, please remember the size only.
[06:00] You don't have to remember the range of values. After the short we have int.
[06:05] Using int data type, we can store up to four bytes.
[06:09] That means it is going to support the size of two power 32.
[06:13] You can see the range on the negative side and the positive side, even if this range is also not sufficient
[06:19] to store your particular number, then you can go to the long because long size is more, which is eight
[06:27] bytes or 64 bits.
[06:29] So the range that is supported by the long you can see on the screen.
[06:32] So it is going to support much higher and higher numbers compared to int, short, byte.
[06:39] And the default values for all these byte, short, int and long is zero.
[06:44] So using these byte, short, int, long we are going to store the whole numbers.
[06:50] Or the integer numbers or the numbers which is not going to have any decimal values.
[06:56] So here you may have a question like why do we need byte, short, int, long.
[07:01] Can't we use long itself.
[07:03] Because long is going to help me to store any kind of number, instead of byte
[07:08] I can use long itself.
[07:09] So why Java people introduce byte, short, int, long with the various sizes and with various ranges.
[07:16] So that's a very good question.
[07:18] So let me answer that question by taking a real life example.
[07:21] Think like you went to a soccer game or a football game,
[07:25] so few countries they call it as football and few countries they call it as soccer.
[07:29] So regardless of what you call think like you went to a game of soccer or football, and here we have
[07:35] various kind of data that happens inside any soccer game.
[07:38] The very first useful and important information that we may have inside soccer game is total number
[07:45] of goals done by a particular team.
[07:47] So if you want to store that total number of goals using your Java programming language, do you think
[07:53] storing them in long or int or short is going to make sense?
[07:58] Off course not, because the maximum number of goals that a particular team may have is maybe 10 or 20.
[08:05] or best case it may be 100.
[08:07] That's why to store the number of goals of a team byte data type is sufficient.
[08:13] If you go with the long, your Java is not going to complain anything.
[08:17] It is going to work very similarly
[08:19] but behind the scenes you are going to waste a lot of memory inside your computer.
[08:25] So if you store the number of goals information using long, you are unnecessarily assigning 64 bits
[08:32] to your variable to store a small number like 6 or 10 or 20 based upon the number of goals value.
[08:39] Very similarly,
[08:40] think like you want to store the total number of people watching the football game or soccer game in
[08:46] the ground.
[08:47] In such scenarios, the short data type is going to be sufficient, because usually the capacity of
[08:54] the grounds is going to be 20,000 or 30,000.
[08:57] So that's why short is going to be sufficient.
[08:59] But if you have a scenario where you want to store the data on how much money or the amount to spend
[09:07] by all the people in the ground to attend that particular football game or soccer game, then definitely
[09:13] you may need int or long to store that total amount of money spent by all the fans inside the ground.
[09:20] So I hope you are clear why we have so many different data types with the different sizes.
[09:25] So these four data types like byte, short, int and long, they are going to support us to store only
[09:30] the whole numbers or the numbers without any decimal values.
[09:33] How about the numbers that we want to store with a decimal value?
[09:38] Because sometimes we may want to store a decimal value, like what is the weight of a fruit?
[09:42] Like what is the weight of a person,
[09:44] or what is the bank balance of a person?
[09:47] So for all such scenarios we have primitive data type like float and double.
[09:52] So the default value for these primitive data type is going to be 0.0.
[09:56] The only difference between these two data types
[09:59] is the size.
[10:00] The float data type size is four bytes or 32 bits, whereas the double data type size is eight bytes
[10:06] or 64 bit.
[10:08] Like, if you want to store a number with more than eight decimal values, then you'll always go with
[10:15] the double, because double data type is going to support to store more decimals or more precision value,
[10:22] whereas float is going to support up to eight decimal values.
[10:26] We're going to discuss difference about float and double in detail in the coming lectures, but for
[10:31] now, please take a note of all the sizes and different data types that we have.
[10:36] So with this, I'm assuming you are clear what kind of data that we are going to store with the help
[10:42] of these primitive data types.
[10:44] And at the same time, I'm also assuming that you are clear about under which scenarios you need to
[10:49] use, which primitive data type.
[10:51] In the next lecture,
[10:52] let's try to understand how to use this primitive data types to store the data using Java programming
[10:59] language and its syntax.
[11:01] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
