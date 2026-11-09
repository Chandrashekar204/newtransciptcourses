# 9.8 — The great java.lang package

> Section 9: packages in Java

[00:00] Based upon our previous lecture discussion, you may have a burning question or million dollar question,
[00:07] which is in all the previous sections we created lot many objects of String.
[00:12] So String is a class which is present inside a package of JDK library.
[00:18] Then why we have not used any import statement while we are trying to access something from the JDK
[00:25] library.
[00:25] So you may have this question running behind the scenes.
[00:29] That's why let me provide a clarity around this inside this lecture.
[00:33] First, let me create the object of the String class inside the class that I have created in the previous
[00:39] lecture.
[00:39] So to create the object of the String, I'm going to first access String and post that
[00:45] I'm going to mention the object name as input, followed by new of String, and inside the constructor
[00:52] parentheses I'm going to pass an input, which is
[00:56] hello.
[00:56] So here I have created a String object which contains the data
[01:00] Hello.
[01:01] If I open this String class you can see this is present inside a package which is java.lang.
[01:08] But inside my Main class I have not mentioned any import statement.
[01:13] Do you know how this is working
[01:15] even though we are not mentioning any import statement of String, this is because all the classes that
[01:22] are present inside the base package java.lang.
[01:26] For these classes, you don't need to mention any import statement specifically inside your own Java
[01:34] code.
[01:34] So this java.lang package has all the important classes that are required by the developers on their
[01:43] day to day job.
[01:44] Similarly, we have other kind of classes.
[01:47] For example, I can look for the Integer wrapper class.
[01:51] So this Integer wrapper class also is available inside the java.lang package.
[01:57] So all the wrapper classes they are available inside the same package.
[02:01] So if I try to create the object of these wrapper classes, I'm not going to get any compilation error,
[02:07] even though I'm not mentioning any import statement.
[02:10] This is because they are also present inside the java.lang package.
[02:16] So this is the only flexibility that the Java team has given.
[02:20] Apart from java.lang package, if you try to access any other class present inside any other package
[02:27] of the JDK library, you need to make sure you are mentioning the import statement.
[02:32] For example, I have a class which is Arrays.
[02:35] So this Arrays class is present inside the java.util package.
[02:40] Using these class I can perform lot many operations on the arrays.
[02:45] I know where to discuss about the arrays, but I'm just trying to give an example here.
[02:49] By taking a class which is present outside of the java.lang package.
[02:54] So if I try to access it, you'll be able to see there is an import statement automatically added by
[03:00] my IntelliJ.
[03:01] So if you try to remove these, you're going to get a compilation error saying that that Java compiler
[03:07] is not able to identify the where the Arrays class is present, since right now I have the import statement
[03:13] from these Arrays class, I can invoke any of the methods that are available.
[03:18] I hope you are clear about the power of java.lang package.
[03:22] All the details that we have discussed about the java.lang package I have mentioned inside this slide
[03:28] for your reference.
[03:29] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
