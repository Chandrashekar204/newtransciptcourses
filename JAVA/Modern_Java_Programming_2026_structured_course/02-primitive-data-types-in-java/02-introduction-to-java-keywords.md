# 2.2 — Introduction to Java Keywords

> Section 2: Primitive data types in Java

[00:00] As of now, we are done with the very initial baby step towards the journey of Java.
[00:06] What is the baby step that we have completed already?
[00:08] We said hi to Java and completed the installation inside our local system.
[00:14] Very similarly, we are going to take multiple baby steps while we are trying to learn the Java because
[00:19] as of now, I'm assuming you are completely beginner.
[00:22] With that reason, I'm going to explain all the basics of Java by taking some initial baby steps.
[00:27] Once you are familiar with all the basics, then definitely
[00:31] I'm going to discuss more advanced topics throughout this course.
[00:35] Now, as a next baby step, I want to explain about the keywords in Java.
[00:40] So what are keywords in Java?
[00:42] In Java, a keyword is a reserved word that has a specific meaning and purpose in the programming language.
[00:50] Just like in English, we have so many words like if I say Apple, we know that is the name of the fruit.
[00:57] And if I say dog, we know it's a name of the animal.
[01:00] Very similarly, in Java, there are some keywords which have some predefined meaning.
[01:05] Since these keywords have some predefined meaning, you should not use these keywords as variable names
[01:11] and method names in the code that you are going to write inside your projects.
[01:16] So in the coming lectures, I'm going to show you why we should create variables.
[01:21] So variables will help us to store the data.
[01:23] And very similarly inside the Java methods we can write our business logic or the logic that we want
[01:29] to be executed using a Java program.
[01:32] So these variable names and method names should not have Java keywords.
[01:37] Because if you use these Java keywords as your method names and variable names, then your Java compiler
[01:43] is going to be confused and it is going to throw an error.
[01:47] So that's why
[01:48] please don't use any keywords as a method names and a variable names.
[01:53] So let me show you a few keywords that we have inside Java.
[01:56] So like you can see these are all the keywords which are available in Java.
[02:01] And they have different, different meaning.
[02:03] For example there is a keyword with the name
[02:05] 'if', so this if I'm going to use to build some conditional logic inside my Java program.
[02:12] Very similarly, we have try, catch, finally, throw, throws which we are going to use while handling errors
[02:19] and exceptions inside our Java program.
[02:23] So this way there are good amount of Java keywords.
[02:26] Right now
[02:26] you don't have to memorize all of them, and you don't have to understand what is the purpose of each
[02:32] of these keyword.
[02:33] Because throughout this course I'm going to teach about all these keywords.
[02:37] And by the end of this course you will be familiar with all these keywords.
[02:41] And very similarly, as you are doing more and more practice by writing Java programs, you will be
[02:48] familiar with all these keywords.
[02:49] But the key takeaway that I want you to be consider here is, Java keywords
[02:54] have some special definition, a special meaning inside the Java language, so please don't use them
[03:00] as your variable names and method names.
[03:02] Like we discussed previously inside Java, everything is going to be case sensitive.
[03:07] For example, we have a first keyword here with the name public.
[03:11] So all are in lower case letters.
[03:14] So this public with all lower case is not going to be equivalent if you use P as capital letter.
[03:21] Because since Java is a case sensitive, even if you change the case sensitivity of a single character,
[03:28] it is going to bring a different meaning for your Java compiler.
[03:32] That's why always take care of case sensitivity inside your Java programs.
[03:36] And if you observe all our keywords here, all these are using pure lower case letter.
[03:42] There is no single Java keyword with a capital letter.
[03:46] I can also show you the full list of Java keywords by going into the Oracle official website.
[03:52] So this is the URL which you need to navigate to see the full list of Java keywords.
[03:57] The same URL I have mentioned inside the GitHub repo under the important links.
[04:03] If you go to the GitHub repo of this course, which I have highlighted at the starting of the course,
[04:08] you will be able to see all the important links that I'm going to discuss throughout this course.
[04:13] So whenever you have some question around the URL or the website that I am trying to access, you can
[04:18] come to this GitHub repo and access them without any issues.
[04:22] Now let me go to the Oracle website.
[04:24] So here we have a full list of Java keywords.
[04:28] And each keyword has a meaning.
[04:30] For now
[04:30] please don't worry about the meaning of each of these keywords.
[04:33] So here you can see most of the keywords are introduced on the day one of Java itself only there are
[04:41] few Java keywords which are released later on.
[04:44] For example, you can see the Java keyword with two asterisk,
[04:48] it is introduced in 1.2 version of Java.
[04:51] So what is that keyword?
[04:52] So this is the keyword which is strictfp.
[04:55] And very similarly the keyword with a three asterisk is introduced in
[05:00] 1.4.
[05:01] So what is that keyword?
[05:02] assert is the keyword which has three asterisks and the keyword which is enum,
[05:07] this is introduced in the Java 5th version.
[05:09] So this also gives some confidence to you.
[05:12] Java is not going to change a lot as new versions are trying to be introduced.
[05:17] Only the enhancements are the better features will be introduced in the new versions of Java.
[05:23] And you can also see there are some keywords which are not used anywhere inside Java programming language.
[05:29] One such keyword is goto.
[05:32] So this goto and 'const' constant keyword
[05:36] they are not right now being used anywhere inside the Java programming language.
[05:41] They are simply created and reserved for future usage.
[05:45] So in future if Java development team, if they have some requirement around these keywords, then they
[05:51] are going to use them inside the Java library.
[05:54] As of now, they are not being used anywhere inside the Java library.
[05:57] So now we are clear about what are keywords in Java.
[06:01] Before I try to close this lecture, I want to show you a quick demo.
[06:04] What will happen if I try to use one of the keyword as a variable name. For the same,
[06:09] let's pick a keyword.
[06:10] Maybe
[06:11] here I'm going to use the keyword, which is 'this'.
[06:14] So let me go to the jshell.
[06:16] I came to my terminal and inside my terminal to activate jshell I need to type the command which is
[06:22] jshell.
[06:22] And this is going to open a new session with my jshell.
[06:26] As of now, we only know on how to print our own name with the help of System.out.println().
[06:32] So let me try to execute the same command one more time.
[06:36] For the same, I'm going to type the Java code, which is System.out.println(), and I'm going
[06:43] to mention my name which is Madan.
[06:45] So with this we know what is output we are going to get.
[06:48] As of now you can see I'm trying to hardcode my name.
[06:52] So what is the meaning of hard coding?
[06:54] Whenever we try to mention a value directly inside your Java business logic or Java statements, then
[07:01] such code we call it as hard code.
[07:04] The spelling of hard code is h, a, r, d, c, o, d, e.
[07:08] So there are some disadvantages if you try to mention the values with the help of hard code approach.
[07:14] Think like I'm trying to print my name inside my Java program at multiple places.
[07:20] In all those places, if I try to mention my name using the hard coded value in future, if I want to
[07:27] change my name from Madan to some other name, then I need to visit all the lines where I have mentioned
[07:33] the hard coded value of Madan.
[07:35] Instead of hard coding the values, we should always follow certain standards, like storing the name
[07:41] into a variable and that variable which is holding my name
[07:44] we need to pass to the System.out.println().
[07:47] So let me try to show you how to do that.
[07:50] So in order to create a variable that is going to hold my name, I need to use a class available inside
[07:56] the Java library.
[07:57] And this class name is String.
[07:59] Inside Java
[08:00] anytime we want to store some alpha numeric values, we are going to use this String class.
[08:07] After mentioning the String class, I need to give space and what is a variable name?
[08:11] So I'm going to discuss in detail about what are variables, how to give the names to them.
[08:16] So in the coming lectures I'm going to discuss in detail about them.
[08:20] But for now think like I'm trying to create a variable where I can store my name, the variable name
[08:26] I'm going to give as myName, and what is my name value.
[08:31] The name that I want to give here is Madan post that I'll give colon,
[08:35] I'll press enter.
[08:36] As of now you can see my jshell is telling,
[08:38] there is a variable created with the name myName and inside this variable there is a value called
[08:43] Madan.
[08:44] Now if I try to pass the same to the System.out.println(), whatever value that I have mentioned
[08:50] inside my variable is going to be printed on the output.
[08:53] So how to pass the variable name to the System.out.println().
[08:57] You can directly mention your variable name.
[08:59] So the variable name that I'm going to mention here is my name.
[09:03] So please note that here we should not use the double quotes because we are trying to pass the actual
[09:09] variable name.
[09:09] And with this, my Java is going to look for the variable which is created previously, inside the same
[09:16] variable
[09:16] we have the data which is Madan.
[09:18] So if I try to execute this we are getting the same output.
[09:21] So this is the purpose of variables with this,
[09:24] in future if I have to change my name, I can directly change the name inside my variable.
[09:30] I don't have to revisit all the Java statements where I'm trying to print my name with the help of
[09:37] System.out.println().
[09:38] So that's the power of variables.
[09:41] That's why please, please never hardcode values inside your Java code.
[09:47] So this is one of the Java standard that you should know as a Java developer.
[09:51] Whenever you hard code lot of values inside your Java code, it shows that you are not an experienced
[09:56] developer.
[09:57] So throughout the course I'm going to teach you all these
[10:00] type of techniques. Now coming to the topic of keywords,
[10:03] previously I said we cannot use the keywords as a variable names.
[10:08] So as of now we have variable name with the name my name.
[10:11] So this time let me try to create one more variable name.
[10:14] So to create one more variable where I can hold a different name I'm going to use String again.
[10:20] After String I'm going to mention the variable name as this.
[10:24] But 'this' is a keyword in Java.
[10:26] So let's see what is going to happen after this I'm going to give equal to
[10:31] and here I'm going to mention Saanvi and post that I'm going to press enter.
[10:36] You can see my compiler is shouting at me.
[10:39] Don't you know that 'this' is a Java keyword?
[10:42] Why are you trying to use that as a variable name.
[10:45] So it is trying to give all those details.
[10:47] So this confirms that we cannot use keywords as a variable names and method names.
[10:52] Now let me try to change this this to some different value by making s as a capital S, and I as capital
[11:00] I.
[11:01] So this time we should not get any error because here I have used different case sensitivity,
[11:07] like I said before, in Java the compiler is going to consider case sensitivity very seriously.
[11:14] So for my compiler this with all lower case letter is not going to be same as this which has two letters
[11:22] in capital letters.
[11:24] So these two words are not going to be equal in terms of my compiler.
[11:28] That's why it is not throwing me any error.
[11:31] So if I try to execute System.out.println() using the variable thIS, I'm going
[11:39] to get my output which is Saanvi. With this,
[11:42] I'm assuming your super clear about what are keywords, but don't worry why we have so many keywords,
[11:47] what is the purpose of them?
[11:48] I'm going to teach all of those keywords one by one
[11:52] throughout this course.
[11:53] Whenever we are trying to discuss a particular topic related to that keyword.
[11:57] I hope you are enjoying the course,
[11:59] thank you and I'll catch you in the next lecture bye.

----------------------------------------
