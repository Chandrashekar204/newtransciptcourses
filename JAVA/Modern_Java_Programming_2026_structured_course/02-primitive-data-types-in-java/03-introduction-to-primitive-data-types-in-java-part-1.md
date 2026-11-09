# 2.3 — Introduction to Primitive Data types in Java - Part 1

> Section 2: Primitive data types in Java

[00:00] Inside this lecture, I'm going to teach you about primitive data types inside Java programming language.
[00:07] Why should we use primitive data types?
[00:09] Usually any programming language it should capable of processing lot of data based upon our business
[00:16] logic.
[00:16] Suppose think like you have given two numbers to your programming language based upon your instructions
[00:23] are based upon your logic.
[00:25] It should be able to do addition, multiplication, division.
[00:28] So regardless of how complex the operation is going to be, your programming language should be capable
[00:35] of accepting the data, processing the data, and returning that data once the program is executed.
[00:41] Since we are going to provide lot of data to our programming language, we should use these primitive
[00:47] data types to store that data inside them.
[00:50] Inside Java anytime
[00:52] if you want to store data, there are two types of data types.
[00:56] One is Reference types, the other one is Primitive types.
[01:00] Inside this section, we are going to discuss in detail about all the Primitive data types available.
[01:05] Because these primitive data types are most basic and natural entry into the Java programming language.
[01:12] Using these primitive data types, only we can store simple data like numbers, whereas with the reference
[01:19] data types we can store complex data.
[01:22] Think like you want to store a details of a person, so the person will have a name, age, gender,
[01:29] address.
[01:29] So all such complex data you can store with the help of reference data types that we are going to discuss
[01:36] in the coming sections.
[01:37] But for now, since we started the Java journey just now, we should first focus and learn the primitive
[01:43] data types.
[01:44] Inside Java, there are eight primitive data types available.
[01:48] These eight primitive data types are boolean, char, byte, short, int, long, float, and double.
[01:57] So the same data type names,
[01:59] we have seen them as a Java keywords as well in the previous lecture.
[02:03] So each of these data type has a purpose.
[02:05] So they're going to help us to store different kinds of information.
[02:10] You may ask a question here,
[02:11] why do we need so many data types.
[02:13] Can't we have a single data type using which we can store any kind of data?
[02:18] That's a perfectly valid question, but let me give a real example to answer this question.
[02:23] Think like you went to a shopping mall and you're trying to buy drinking water, and at the same time
[02:28] you also ordered a pizza.
[02:30] So do you think both pizza and water, they're going to come in a similar packaging?
[02:35] Off course not.
[02:36] The water is going to come in a disposable plastic bottle, whereas pizza will be delivered in a tray
[02:42] or a paper cardboard.
[02:44] So if you see here the packaging requirements is going to be different for different items.
[02:49] Very similarly, we may have to store various kind of data using Java programming language.
[02:55] So if you try to store all kind of data in a single data type, it may bring inefficiency and it may
[03:02] also introduce some security issues or performance issues.
[03:06] That's why Java people decided to have eight different primitive data types.
[03:12] And in the coming lectures we are going to discuss about each of these data type.
[03:17] But before that, here you may have a burning question saying that why should I use primitive data types?
[03:23] or why should I store data with the help of primitive data types?
[03:28] So let me try to answer the same.
[03:30] Think of a scenario where one of your friend asks you to subtract two numbers.
[03:35] So he told the very first number as 30 and the second number as 10.
[03:39] Since you are an intelligent human, the way how you are going to process this information is you're
[03:45] going to store the first number as 30 inside your brain.
[03:49] And very similarly, you are also going to store the second number as 10.
[03:54] Like you can see here, you're going to store them at two different locations inside your brain.
[03:59] After storing these information,
[04:01] now as a next step you're going to perform the actual subtraction like 30 - 10, which is 20.
[04:09] If you by mistake store the numbers differently.
[04:12] Like under first number you are stored as ten and the second number
[04:16] if you store as 30, then definitely you're going to get a negative number as an output.
[04:21] So here it is very clear.
[04:23] Storing that data with the correct names is very important,
[04:27] otherwise we are going to get different results.
[04:30] And very similarly maybe after the subtraction your friend may ask you give me the answer by multiplying
[04:36] two numbers or give me an answer by doing a division.
[04:39] So then immediately you're going to refer to your brain memory and think of what is the first number
[04:45] and second number.
[04:46] And you're going to perform addition or multiplication or division based upon your friend request.
[04:52] So this is a scenario where whenever a human is involved.
[04:55] So very similarly we are going to give lot of instructions to the
[04:59] computer to process the data.
[05:02] Maybe inside a website, a customer might be entering his details on the HTML page where he's going
[05:08] to enter his name,
[05:10] what is his date of birth?
[05:11] So once the customer entered his details, you need to accept those details from the UI application
[05:17] and store them inside a database.
[05:19] And before you try to store them inside the database based upon the date of birth, you also want to
[05:25] calculate the age of the person.
[05:27] So how you're going to calculate the age of the person, you'll take the date of birth and you'll take
[05:32] the current date.
[05:33] And based upon these two dates you're going to calculate the age of the person.
[05:37] But whenever we're trying to give instructions to computer, we need to give accurate instructions.
[05:43] So think of the same scenario by referring to a computer programming language.
[05:47] So inside human scenario the person is able to store the information about the numbers in his brain.
[05:54] Very similarly, your Java programming language also need primitive data types to store that data that
[06:01] we are going to give.
[06:03] So here like you can see the first number is stored at a memory location inside the computer.
[06:08] And very similarly the second number also randomly stored inside a memory location.
[06:13] So this first number and second number are the variable names belongs to a particular primitive data
[06:18] type.
[06:18] After your computer store this data in a memory location based upon your instructions
[06:23] it is going to perform addition, subtraction, multiplication or division.
[06:27] So it is going to completely depend on your business logic that you have written.
[06:32] But working with computers is not going to be super easy.
[06:36] If you're trying to talk with a human, it is going to be super easy because you can very casually tell
[06:41] to your friend, first number is so and so second number is so and so,
[06:44] please do the addition.
[06:46] So even if you make some mistake while communicating with him, he should be able to understand because
[06:52] usually we humans are intelligent fellows.
[06:55] But coming to the computers, they are going to expect you to follow certain syntax.
[07:00] If you don't follow the syntax and rules of a programming language, then your computer cannot understand
[07:06] your data and business logic, and it is simply going to throw an error.
[07:10] Because programming language is a contract between a developer and a computer saying that we both are
[07:18] going to follow the so and so syntax, so and so rules.
[07:21] If you don't follow that contract, definitely whatever information we are going to give to the computer
[07:26] is not going to make any sense, and it is simply going to throw an error.
[07:30] So I hope you are now clear
[07:32] like why we need primitive data types.
[07:34] So let's try to understand more details about this primitive data types in the next lecture as well.
[07:39] Thank you
[07:40] and I'll catch you in the next lecture bye.

----------------------------------------
