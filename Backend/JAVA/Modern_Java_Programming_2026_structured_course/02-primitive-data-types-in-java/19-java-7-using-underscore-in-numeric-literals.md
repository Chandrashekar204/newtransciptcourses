# 2.19 — [Java 7] Using underscore in numeric literals

> Section 2: Primitive data types in Java

[00:00] Inside this lecture, I'm going to show you under which scenarios we can use underscore special character
[00:07] while we are trying to define numeric literals with the help of int, float, double, byte, short, long.
[00:16] So regardless of whatever primitive data type that you are trying to use to declare numeric values in
[00:22] all such scenarios, we can use underscore to improve the readability of the code.
[00:29] So let's try to understand more details about this.
[00:31] In some scenarios we are going to mention very big numbers, which is very hard for the developers to
[00:38] read.
[00:39] Suppose if you have eight digit number or nine digit number, the developer has to count how many numbers
[00:45] are there inside your Java code manually by putting some efforts.
[00:49] So to improve the readability in these kind of scenarios, Java allows you to mention underscore in
[00:56] between your numbers, and your compiler is also not going to complain anything.
[01:02] So underscore is not a number and it is a special character.
[01:05] Your Java compiler will not throw an error. Behind the scenes
[01:09] your Java compiler is going to remove these underscore values by the time your Java code is converted
[01:15] into the machine code. Inside the Java source code, you will be able to see underscore, but the machine
[01:21] code will not have these underscore, because in between, the compiler is going to do the magic of
[01:27] removing these underscore value.
[01:29] So these underscore values is going to simply improve the readability of your variable declarations
[01:36] and initialization.
[01:38] Here you can see I'm trying to define a variable num of type int.
[01:43] If I don't mention these underscore values it will be very tough for other developers, including me
[01:49] also, to understand what is the total value of this number or how many zeros are there inside my number.
[01:55] So in future, whenever you see some developer using underscore values inside their numeric, please
[02:01] don't scratch your head by thinking like how this is possible, because this is a feature available
[02:07] inside the Java programming language. But there are some rules and regulations that we need to follow
[02:13] while you are trying to define this underscore value inside a numeric value.
[02:18] So let's try to understand what are those rules.
[02:20] The very first rule is the underscore value is not allowed at the beginning or at the end of a number.
[02:27] Suppose if we want to create a number six, we can't create a number underscore six and six underscore.
[02:34] And in the case of decimal numbers the underscore is not allowed adjacent to your decimal point, either
[02:42] before decimal point or after decimal point
[02:45] the underscore value is not allowed, and very similarly, when we try to create long numbers will mention
[02:52] the suffix as l, and for float numbers will mention the suffix as f, so the underscore is not allowed
[02:59] just after the suffix or just before the suffix value.
[03:03] And at last, when you try to represent your numbers using the string format using underscore values
[03:10] is not allowed.
[03:11] I know we are yet to discuss about what is string data type in the coming lectures
[03:15] we are going to discuss about it, but for now, please note that when you try to define your numeric
[03:21] values using String data type in such scenarios we are not allowed to use underscore value.
[03:27] I hope this is clear.
[03:28] Now let's see the demo of these underscore inside numeric values by going to the jshell.
[03:34] Here I'm going to create a variable with the name num of data type int.
[03:39] For this first I'm going to assign a value with one, and after one I'm going to mention some zeros.
[03:46] So in total I have mentioned seven zeros.
[03:48] So if you try to define this way you can see it is very hard for someone to read your value.
[03:54] Whereas if I try to change the same numeric value by mentioning underscore values at different places,
[04:02] then this is going to be super easy for other people to read my numeric value.
[04:07] So if I try to execute this, you can see by the time I get output, all the underscore values are being
[04:13] removed by the Java compiler.
[04:15] You may have a question
[04:16] can I use some other special character in the place of underscore?
[04:20] Let's try with comma.
[04:21] So if I try to use commas which is other than underscore, you can see we are getting a compilation
[04:28] error.
[04:28] That means we are allowed only to use underscore only.
[04:32] Now let's try to test some negative scenarios.
[04:35] For negative scenarios I'm going to mention underscore at the starting of the number which I'm trying
[04:42] to create here.
[04:43] So this is not allowed.
[04:45] And very similarly at the end of the number also it is not allowed.
[04:49] So let me mention the underscore at the end.
[04:52] This is also not allowed.
[04:53] Let me clean my console here.
[04:55] This time I will show for long variable.
[04:58] So for long variable
[05:00] we are going to mentioning underscore just before L is not allowed.
[05:05] Very similarly, just after L also is not allowed.
[05:08] As a next step, I'm going to create a flot to variable.
[05:12] And inside this float variable I'm going to store a number 3._6f.
[05:19] Do you think this is allowed?
[05:20] Off course this is not allowed because we are not supposed to use underscore adjacent to the decimal
[05:27] point.
[05:27] Even if I try to move these underscore before the decimal point, even this is also not allowed.
[05:33] I hope you are clear about these negative scenarios.
[05:36] Now let me show you an interesting demo, which is not known for many of the Java developers.
[05:43] Since you are my student, you're going to have the knowledge about the new demo that we are going to
[05:48] discuss.
[05:49] So previously we created a variable by mentioning these underscore value.
[05:54] Sometimes you may want more readability
[05:57] and you can mention underscore values like here I have mentioned three underscore values. Very similarly
[06:03] here
[06:03] also I'm going to mention.
[06:04] So do you think this is allowed or not.
[06:07] Off course
[06:07] please note this is completely allowed inside Java.
[06:11] So you can use any number of underscore values to improve the readability of your numbers.
[06:18] So these are secret where very few Java developers know.
[06:21] I hope you're happy and clear about all the scenarios that we have discussed.
[06:26] So please note about all the rules that we need to follow while we are trying to use underscore in the
[06:32] numeric literals that we are going to define inside Java programming language.
[06:37] Before we try to close this lecture, I want to highlight that these underscore feature is introduced
[06:44] inside JAVA 7, which means you can use this feature only with the JAVA 7 and above version,
[06:52] but not with the JAVA 6 or JAVA 5.
[06:55] Off course, these days there is no option for us to use JAVA 6 or JAVA 5, but I just want to let
[07:01] you know in case if someone asks you from which version this feature is introduced, you can answer
[07:07] them from JAVA 7.
[07:08] This underscore feature is introduced for numeric literals.
[07:13] I hope this is all clear to you.
[07:14] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
