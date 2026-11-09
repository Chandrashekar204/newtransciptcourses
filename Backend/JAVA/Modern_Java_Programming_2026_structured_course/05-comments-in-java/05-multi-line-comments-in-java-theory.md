# 5.5 — Multi line Comments in Java - Theory

> Section 5: Comments in Java

[00:00] In this lecture let's try to talk about the multi line comments approach in Java.
[00:05] Whenever we want to write multi line comments inside Java we should always start with /
[00:11] immediately followed by an asterisk mark.
[00:13] Once you have mentioned these forward slash followed by asterisk mark you can define any number of lines
[00:19] of comments.
[00:20] Once you have mentioned all your lines of comments at the end, you need to close the comments with
[00:26] the help of asterisk followed by forward slash.
[00:29] So anything that you are going to write in between the starting and the ending of your multi line comment
[00:35] symbols is going to be considered as a comment by your Java compiler, and all the content that you
[00:41] have written inside these comments will be ignored by the compiler.
[00:45] Here you may have a question which is if we already have single line comments, why do we need to follow
[00:51] the multi line comments approach?
[00:52] Let me try to answer the same.
[00:54] In some scenarios, we may not be able to explain the complexity of our Java code within a single line
[01:01] of comment.
[01:02] In this kind of scenarios we can use multi line comments approach.
[01:06] Apart from explaining complex code of logic, we can also try to document a purpose of a class, a purpose
[01:12] of the method with the help of multi line comments.
[01:16] Apart from documenting, we can also comment multiple lines of code at a time.
[01:21] For example, if you want to comment out entire method, you can comment out with the help of multi
[01:26] line comments.
[01:27] When I say comment you want to temporarily disable or temporarily ignore certain lines of Java code.
[01:34] So that process we call it as comment.
[01:36] In the previous lecture, when we were discussing about the single line comment, we were able to comment,
[01:41] method invocations or a single line of Java code, but with the help of multi line comments, we can
[01:47] comment multiple lines of Java code at a time.
[01:50] Let's try to understand few examples here around the multiple line comments like you can see here
[01:56] I have a class Customer.
[01:58] If I want to explain the purpose of this class to other developers, or if I want to document the purpose
[02:04] of this class for my future reference, I can achieve that with the help of multi line comments.
[02:09] So to mention multi line comments like we discussed
[02:12] first we need to start the comment with the help of forward slash followed by asterisk mark.
[02:17] After that you can define your multi line comments here
[02:20] I'm trying to mention multiple lines of comments saying that this class represents a customer in bank
[02:26] app.
[02:27] It contains information such as firstName, lastName, dateOfBirth, address and accountDetails.
[02:34] Once I'm satisfied with my lines of comments, I need to terminate our closer multi line comments with
[02:40] the symbol asterisk followed by forward slash.
[02:44] Very similarly, you can also try to document the purpose of a method.
[02:48] So here you can see I have a method with the name calculate rectangle area.
[02:53] I tried to explain the purpose of this method with the multi line comments.
[02:57] So this method is going to accept two method input parameters by multiplying these two input parameters
[03:03] I'm going to return the output which is going to be the total area of the given rectangle.
[03:09] So that's what I tried to document with the help of multi line comments.
[03:13] Just like how we are trying to document the purpose of a class, method
[03:18] very similarly, we can also try to document a purpose of a variable with the help of multi line comments.
[03:24] So here I'm trying to create a variable MAX_RETRY_ATTEMPTS.
[03:28] In the previous lecture, with the help of single line comments, I explained on a high level using
[03:33] a single line of command.
[03:34] Whereas whenever I want to share more details or whenever I want to be more expressive in such scenarios,
[03:41] I can use multi line comments like you can see.
[03:44] This way we can document a Java class, a Java method or a Java variable with the help of multi line
[03:51] comments.
[03:51] Let's try to understand more details about multi line comments like I was telling before.
[03:56] With the help of multi line comments, we can comment multiple lines of Java source code. like you can
[04:02] see here
[04:03] I'm trying to comment entire method.
[04:05] So here I have a method with the name sum().
[04:08] If I want to disable or if I want to ignore this method temporarily, I can use multi line comments
[04:15] to comment the code off entire method.
[04:17] Very similarly, we can comment entire class or multiple lines of code by following the same syntax.
[04:24] Sometimes you may see few developers
[04:26] they try to achieve the multi line comments with a single line comments.
[04:31] For example, you can see first I have a multi line comment where I'm trying to mention an example of
[04:36] a multiple line comment.
[04:38] The same multi line comments
[04:39] we can also try to achieve with the help of single line comments.
[04:43] So how the developer is achieving here?
[04:45] He's trying to mention the single line comment symbol at every line of comment.
[04:50] So you may see this kind of strategy as well by few developers.
[04:55] And these strategy may work only for certain limited number of lines of comments.
[05:00] If you have more lines of comments like five lines or ten lines, then always the easiest and recommended
[05:06] approach is to follow the multi-line comments
[05:09] instead of mentioning the single line comment syntax before each line of comment.
[05:13] I hope you are clear why we should avoid single line comment when you are trying to define multi-line
[05:19] comment.
[05:20] The last point that I want to discuss here is, we can write multi-line comment in the middle of a Java
[05:27] code.
[05:27] This may be surprise for you because for single line command we saw that it is a limitation whenever
[05:33] we try to use a single line comment in the middle of a Java code, it is going to throw a compilation
[05:39] error, whereas a multi-line comment can be written or inserted in the middle of a Java code.
[05:45] Here you can see I have an example where I'm trying to define a constant variable with the name
[05:51] MAX_RETRY_ATTEMPTS = 3, but in between my Java code I have a multi-line comment syntax,
[05:58] and with this my Java compiler is not going to complain anything because inside multi-line comment
[06:04] my compiler always know what is the starting point,
[06:07] what is the ending point. In this variable declaration,
[06:10] whatever multi-line comment I have mentioned, my compiler is going to ignore by ignoring these multi-line
[06:16] comment, my Java statement is going to be a valid statement, but in the scenario of single line comment,
[06:22] this is not possible because whenever we are trying to use a single line comment, we can only mention
[06:27] the starting point.
[06:28] There is no ending point.
[06:30] Whatever we have mentioned after the single line comment syntax, all that piece of characters are going
[06:36] to be considered comments because there is no termination for the single line comment in the same line.
[06:43] I'm assuming you are clear why we are able to write multi-line comments in between the Java code, but
[06:49] not the single line comment.
[06:51] Though it is technically possible to define a multi-line comment in the middle of a Java code, it is
[06:57] not recommended to use this because that is very bad way of writing comments, and it is going to reduce
[07:04] the readability of your code.
[07:06] With this, I'm assuming you're clear about what is multi-line comments.
[07:10] The summary is very simple.
[07:12] If you want to be more expressive inside your documentation or inside your comments, always use multi-line
[07:18] comments.
[07:19] Whereas if you can explain a piece of logic within a single line comment, you can always go with the
[07:24] approach that we have discussed in the previous lecture.
[07:27] Let's try to create some examples to understand more about multi-line comments in the next lecture.
[07:33] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
