# 22.3 — Problems with normal Java class constants approach

> Section 22: Enums in Java

[00:00] As of now, we are trying to solve our business problem with the help of Java constants.
[00:06] Like you can see here, I have created four different constants using the same.
[00:10] I'm trying to build a logic with the help of switch expression, but like I said before, there are
[00:15] some good amount of drawbacks with these constant approach.
[00:19] Let me try to explain one by one.
[00:21] The very first major or serious drawback whenever we are using Java constants is we cannot enforce restrictions
[00:29] during the compilation time itself.
[00:32] Here the expectation is to pass zero, one, two and three representing various priorities.
[00:38] But if someone is trying to send invalid data, then this default block is going to throw an runtime
[00:45] exception.
[00:45] But there is no restriction that we are enforcing during the compilation time itself.
[00:50] If you see inside this example class, we are able to send the ten as an int value and there is no compilation
[00:58] error.
[00:58] The developer will know about this invalid data only during the runtime, based upon the exception that
[01:03] we are trying to throw instead of ten, I can send some different value as well.
[01:07] So this is one of the drawback.
[01:09] To handle these drawback to some extent we have built these default block inside the switch expression.
[01:16] But this is more of a runtime exception handling.
[01:19] And it is not guaranteed that always you are going to use the switch expression.
[01:22] Sometimes you may build your logic with the help of if blocks, or by using some plain Java code.
[01:28] In all those scenarios, you may end up writing some dirty code to handle the invalid data.
[01:34] And believe me, in real projects you will have so many scenarios, and to handle all those scenarios
[01:41] you will have good amount of constants.
[01:43] As of now, we are trying to discuss a scenario which has only four different type of constants.
[01:49] But as you try to add more number of constants to your business logic, the dirty code that you need
[01:55] to write will also increase.
[01:57] So this is not a super proper solution.
[02:00] We should look for a proper solution, which will stop my other developers to sending the invalid data
[02:07] during the compilation time itself.
[02:09] So these are very first drawback of constants.
[02:12] The second drawback of Java constants approach is whenever you are trying to change this value, maybe
[02:18] from zero to some other value, in all those scenarios, you need to make sure you are compiling both
[02:25] the priority class and these task util class.
[02:28] If you compile only your priority class, but not the task util class, the latest values are not going
[02:34] to be reflected inside your switch expression.
[02:37] The reason is, during the compilation time, the JVM or the Java compiler is going to replace all these
[02:43] constants with zero, one, two, and three.
[02:46] So if you're trying to change some value inside the Java constants, then obviously you need to recompile
[02:52] both priority and task util.
[02:54] So this is another drawback.
[02:55] As of now I have only one class where I'm using these constants files.
[03:00] But if I have 100 different Java classes where I'm using these constants files, all of them needs to
[03:05] be recompiled.
[03:06] So this is a second drawback.
[03:08] The third drawback is as of now, you can see inside the priority Java class we have defined various
[03:14] constants like low along with inter representation like zero, one, two and three.
[03:19] So if someone is trying to store these constants inside a disc or inside a database, they will end
[03:26] up storing these values like zero, one, two and three.
[03:29] So they will not have any clue what is the zero, one, two and three represents until unless they look
[03:35] at these mapping that we have created inside the Java class.
[03:38] Of course, instead of zero you can also try to store low itself.
[03:43] We have this kind of workaround, but few developers they look for into values so that it is easy to
[03:49] manage and build the logic compared to the strings.
[03:52] Suppose instead of zero, if I store low, other developers may send input as low w or there can be
[03:59] some spelling mistakes can happen instead of o, they can press zero to avoid these kind of issues.
[04:06] Usually developers they prefer storing the integer values against to the Java constants, but with this
[04:13] we have other implications as well, which is people should always look for what is a mapping for zero,
[04:19] one, two and three.
[04:21] At the end of the day, when we try to store these constants into a discard database, only the values
[04:27] they are going to be stored.
[04:28] And for someone to get the meaning of those values, they need to look for the mapping inside the constant
[04:34] file and the similar lines.
[04:36] We also have next drawback, which is when someone is trying to print these constants like low, medium
[04:42] and high and adjacent, they're going to get the output as zero, one and two and three, which is not
[04:48] going to make any sense to end users.
[04:50] For example, inside this task priority constant demo, I can try to have a System.out.println.
[04:57] And here to this println method I can pass one of the.
[05:00] A constant which is urgent.
[05:02] If I execute this program for the last System.out.println.
[05:06] Like you can see, I'm getting the output as three, and this three is not going to make any sense to
[05:12] my end user.
[05:13] Instead, printing an urgent or high or medium or low, it is going to make more sense to achieve the
[05:20] same.
[05:20] Then we need to change the contents of these constants, which will bring other problems to handle by
[05:26] the developer.
[05:27] So this is one such drawback.
[05:29] The next drawback is around the maintaining the order for your constants.
[05:34] As of now, as a developer, I know low should be before the medium, and medium should be before the
[05:41] high and the high should be before the urgent.
[05:43] So since I know about these order of the constants, I have maintained or defined them in an sequential
[05:50] order.
[05:50] But there is a good chance in future if someone want to create a new constant inside this file, they
[05:56] may end up creating the new constant at the starting of the body or at the end of the body are at some
[06:02] random location.
[06:03] So with that, we are never going to maintain the order of our constants because the Java constants,
[06:09] they are not going to give you an option to maintain the order of your constants, whereas with enums
[06:15] internally it is going to maintain a order for each and every constant that you are going to define.
[06:21] When we discuss about enums, it is going to make more sense to you.
[06:25] The last drawback is think like someone is asking you what are the values supported by your Java constants?
[06:32] For priority we have four different constants and the values are zero, one, two, and three.
[06:37] So if someone asks you to provide the values supported by the priority constants, there is no quick
[06:43] or automatic way I need to provide them in an hardcoded format like zero, one, two, and three.
[06:49] And even for other developers, there is no way to query my priority constant file to know the values
[06:56] of my constants.
[06:57] Here we have only four constants, but in real projects we may have hundreds of constants.
[07:02] So if you have hundreds of constants and if someone is looking for the value supported by your constants,
[07:07] it is going to be a tedious process to share those values to the other developers, as there is no automatic
[07:13] for others to query your constants about their values.
[07:17] So these are all the drawbacks that you are going to face.
[07:20] If you are trying to build the constants with the help of normal Java class to overcome all these challenges,
[07:26] what should we do?
[07:27] We should build the constants with the help of enum data type.
[07:31] I hope you are clear.
[07:32] Whatever we discuss, along with the example and the drawbacks I have mentioned in these slides.
[07:38] For your reference, please refer them for more details from the next lecture.
[07:42] Let's try to leverage enums and make our life easy.
[07:46] And in the same process, we are going to overcome all the drawbacks that we have discussed inside this
[07:51] lecture.
[07:51] Thank you.
[07:52] Bye.

----------------------------------------
