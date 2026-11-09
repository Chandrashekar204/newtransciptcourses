# 2.20 — Other formats supported by integer & floating data types

> Section 2: Primitive data types in Java

[00:00] As of now, with the help of integer and floating primitive data types, we are storing the decimal
[00:07] format numbers.
[00:09] By default we humans use this decimal format to understand the numeric values, but apart from decimal format values,
[00:17] there are.
[00:17] other formats are also available inside the industry which will be used in various scenarios.
[00:23] That's why inside this lecture, let's try to learn how to store the other format numbers
[00:29] also, with the help of primitive data types available inside the Java.
[00:33] Like I said before, as of now we are using decimal number format.
[00:37] Apart from these formats, Java also supports Octal number format, Hexadecimal number format, and
[00:44] the Binary number format.
[00:46] Let me give you a very quick introduction about what are these formats. Inside the Decimal number format,
[00:51] each and every number is going to be represented from 0 to 9, whereas inside the Octal number format
[00:58] every number is going to be represented with the help of 0 to 7.
[01:02] So there will be total eight values.
[01:04] That's why we call it as Octal number format.
[01:07] Whereas in the scenario of Decimal number format there will be total ten numbers 0 to 9,
[01:13] that's why we call it as Decimal number format.
[01:16] Coming to the Hexadecimal number format, it is going to use total 16 different values 0 to 9.
[01:23] After nine it is going to use a, b, c, d, e, f.
[01:27] So using these total 16 characters, Hexadecimal number format is going to be representing a number.
[01:34] Whereas in the Binary number format we are going to represent each and every number only with the zero
[01:40] and one.
[01:41] That's why we call this format as Binary number format.
[01:44] So if you try to attend any Java interview, this can be one of the favorite topic that an interviewer
[01:50] can select to ask you questions around this.
[01:53] As of now, we are storing Decimal number format very normally.
[01:56] Like we just type two, three, four or five, three, six whatever we want.
[02:00] And Java is storing them as a normal decimal number format.
[02:04] This is the default behavior. But there might be some situations where you have to store the numbers
[02:09] in the Octal number format or Hexadecimal number format, or Binary number format.
[02:14] So let's try to understand how to store the numbers using these formats
[02:19] inside the Java. The very first format that we have is Octal number format.
[02:23] So whenever you want to store an Octal number we need to make sure there is a prefix zero.
[02:29] After the prefix zero, definitely there should be at least two digits.
[02:34] Then that number is going to be treated as Octal number.
[02:38] So here I have created one Octal number with the name 031.
[02:42] So when you try to convert this Octal number to the decimal value, the corresponding number is going
[02:48] to be 25.
[02:49] In the next lecture, I'm going to show you how to convert an Octal number format to the Decimal number
[02:55] format.
[02:55] But for now, please note that the rule that we need to follow whenever we want to define an Octal number
[03:00] is,
[03:01] we need to make sure there is a prefix zero.
[03:03] After zero, there should be at least two numbers to represent an Octal number.
[03:09] Now let's move on to the Hexadecimal number format.
[03:12] Like we discussed previously, Hexadecimal number format uses total 16 digits, or characters 0 to 9
[03:19] and A to F.
[03:21] The A to F can be in capital letters or in the small case letters.
[03:25] So whenever you want to store an Hexadecimal number format inside Java, you need to make sure you are
[03:31] mentioning a prefix value which is zero x.
[03:34] The x can be in small case or in the capital case.
[03:38] Regardless of the case sensitivity of the x, the compiler is going to treat that number as an Hexadecimal
[03:45] number.
[03:46] So here you can see I have given an Hexadecimal number which is zero x, which is the prefix that we
[03:53] need to follow post that I have mentioned 453f.
[03:57] So if you try to convert this into an decimal number, the output is going to be 17727.
[04:03] This conversion
[04:04] also, I'm going to show you in the next lecture on how to convert an Hexadecimal number format into
[04:10] a normal decimal number format.
[04:13] And at last we have Binary number formats, inside binary number format
[04:17] like I said, we are only allowed to use zeros and ones. For the Binary number format,
[04:23] the rule is we should use a prefix zero b.
[04:27] The b can be in small case or in the capital letter.
[04:30] After b, you can mention your binary number by using zeros and ones.
[04:35] So here I have mentioned a binary number which is 0B011.
[04:39] If you try to convert this Binary number into a Decimal number format, the output is going to be three.
[04:45] Here you may have a question under which scenarios these formats are going to be used.
[04:50] The very first format which is Decimal number format.
[04:53] We know it is used by humans and computers to store and process the data. But coming to the Octal number
[04:59] format,
[05:00] this is going to be used mostly inside the embedded systems.
[05:04] So whenever they want to give some instructions to the embedded systems, they are going to use this
[05:09] Octal number format.
[05:10] If you end up with a scenario where your Java program has to communicate with the embedded system,
[05:15] then there is a good chance that you will be asked to write your logic with the help of Octal number format.
[05:21] Coming to the Hexadecimal number format, the scenario where we are going to use this is.
[05:26] Most of the times we use this Hexadecimal number format to represent the color codes.
[05:31] Like we have so many flavors of colors inside the world, but each color there is a hex code assigned
[05:37] the same hex code we can use to display a particular color inside our web pages or inside our documents.
[05:44] So to store such kind of color codes, the Hexadecimal format is going to be used.
[05:49] And very similarly, Hexadecimal is also going to be used to store the memory details or the address
[05:55] details.
[05:56] We know behind the scenes all the data that we provide to the computer is going to store inside a memory
[06:01] location.
[06:02] So whatever memory location that my computer is going to use for storing the data for that memory location,
[06:09] the computer is going to assign a address value with the help of Hexadecimal number format and coming
[06:15] to the Binary number format,
[06:16] it is mostly used by the machines because machines can only understand zeros and ones.
[06:22] So whenever you are into scenarios where you want to provide machine learning instructions, in such
[06:27] scenarios, this Binary number format is going to be used.
[06:31] As a Java developer, you should learn about all these formats, how these formats are going to work.
[06:36] That's why I'm going to put some good amount of efforts inside this course to make you understand about
[06:41] this format.
[06:42] If you are attending an exam based upon Java, or if you're trying to attend an interview, they may
[06:47] give you an Octual number format as an input to the primitive data type.
[06:51] After that, they are going to ask a question saying that what is the output of this program?
[06:56] So you have to calculate what is the corresponding Decimal number format value, and the same you need
[07:01] to select as an answer.
[07:03] So all those details I'm going to share you in the next lecture on how to convert a specific number
[07:08] format to Decimal number format.
[07:11] But for now I'm assuming you are clear.
[07:13] What are the rules that we need to follow?
[07:15] While we are trying to define numbers with the various number formats that are supported by the Java?
[07:21] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
