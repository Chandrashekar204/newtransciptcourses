# 5.8 — Introduction to javadoc comments Demo - Part 1

> Section 5: Comments in Java

[00:00] In the previous lecture, I gave a very quick introduction about the Javadoc comments.
[00:05] Now, inside this lecture let me create a Java class and on top of that, let me try to define some
[00:10] Javadoc comments for the same
[00:12] I'm going to create a new class inside my Java project.
[00:18] The class name is going to be
[00:21] JavaDocCommentsDemo.
[00:22] .
[00:23] Once I have defined this class name, I can press enter which will create a new class on top of this
[00:28] class.
[00:29] First I want to define some Java doc comments.
[00:32] So what is the format that we need to follow?
[00:34] Forward slash two asterisks (/**) and after that you can press enter inside your intelliJ and it is going
[00:41] to take care of generating the end symbol which is asterisk followed by forward slash (*/).
[00:47] Whenever you are trying to define Javadoc comments, please make sure each and every line has this
[00:53] asterisk symbol that is a standard that we need to follow.
[00:56] You can see inside one of the JDK library class that we have, which is System.java.
[01:01] The same standard is followed.
[01:03] So first.
[01:03] So here I can simply write normal plain text.
[01:07] For example this is a Sample class to show demo about Javadoc.
[01:16] So this simple language I can write.
[01:18] And till this point this is no different from multi-line comments.
[01:23] The advantage of Javadoc comments will come into picture only when we start using some Java doc tags
[01:30] and HTML elements.
[01:32] Let me show you how to define that.
[01:34] First I want to use a tag of javadoc, which is @since.
[01:39] After mentioning the since, I'll just mention some version number which is 1.0.
[01:44] This tells to my readers who are reading the documentation of my class, that this class is available
[01:50] from the version 1.0, and very similarly, I can also use one more tag available, which is
[01:57] @author.
[01:58] So the author I will give my name, which is Madan Reddy.
[02:02] This way we can use any number of tags I know here you may have question which is how do I know the
[02:08] list of tags supported by the Javadoc?
[02:11] So there are multiple ways to identify the list of tags.
[02:14] You can open any of the Java provided class like System.java.
[02:19] If you can try to observe these enter javadoc comments return.
[02:24] You'll be able to see multiple tags.
[02:26] So here I have a tag which is @code, @since.
[02:30] So whatever
[02:31] starting with @ symbol that represented tag inside javadoc comments.
[02:36] So if you can scroll down you can scroll down.
[02:39] You should be able to see lot many tags like @link, @see.
[02:43] So each and every tag has a purpose.
[02:46] I have mentioned all the important tags inside this slide for your reference.
[02:51] Most of the times you may end up using these tags, so please try to understand the purpose of these
[02:56] tags and the description around them.
[02:58] It is super easy when we use @author we are trying to tell who created that class.
[03:03] Similarly, by using @see,
[03:05] we we are trying to tell.
[03:07] Please look at the related class name
[03:09] and similarly @link, we are trying to establish an URL.
[03:12] And very similarly, when we are trying to use @code tag, we are trying to represent a comment
[03:18] using source code font and with the help of @param, we can indicate method input parameters
[03:25] and @return indicates what is the return type of the method @exception indicates
[03:30] what is the exception that can be thrown by a given method @deprecated
[03:35] represents a particular method are a class is about to be deprecated or removed from the Java library,
[03:41] so it is a warning to the developers
[03:43] please do not use a particular method or a class which is marked as deprecated, because there is a
[03:49] good chance that a given method or class may be removed in the future
[03:54] releases.
[03:54] You can also find more details about how to write Java doc comments from this link.
[04:00] I'm going to mention this link inside the GitHub repo as well, so there is a good amount of information
[04:06] inside this page.
[04:07] Like what is the purpose of @param , @return, @see,
[04:11] how to use them?
[04:12] Apart from these tags, we can also use HTML elements like p, p indicates paragraph.
[04:18] Whenever we want to start a new paragraph
[04:21] we can mention these HTML tag.
[04:23] You can try to read this entire page to understand more details, but as a developer, you don't have
[04:29] to know everything about javadoc, as long as you know the basic syntax of javadoc and you know how
[04:35] to write a simple javadoc, that should be more than enough for your interviews.
[04:40] Because in real projects, whenever you end up writing a javadoc comments, you can always refer the
[04:47] existing javadoc comments like you can open the System.ava and you try to understand how the Java
[04:53] team built the javadoc.
[04:54] The same standards
[04:55] you can use them inside your javadoc as well.
[04:59] For example
[04:59] you can see
[05:00] they have use @see tag.
[05:02] First, I can try to understand how this is going to look like inside my HTML documentation.
[05:08] This is how it is going to look like with a prefix as
[05:11] see also.
[05:11] And it is going to give a hyperlink of that particular Java class and Java method.
[05:17] I can use very similar inside my javadoc as well.
[05:21] For example, on top of my Javadoc comments, I can use the @see tag.
[05:27] After mentioning these @see , I can type any class name.
[05:31] For example, from this javadoc
[05:33] comments.
[05:33] If I try to establish a link to this MultiLineCommentsDemo, I can simply type MultiLinesCommentsDemo
[05:40] .
[05:41] You can see my intelliJ is trying to help me here with the recommendations.
[05:45] With this, if I try to toggle this view, you will be able to see the same kind of structure inside
[05:51] our class which is javadoc comments demo as well.
[05:55] This time I'll try to use a HTML tag element for the same
[05:59] just after my initial javadoc comments, I'm going to press enter and use a HTML tag which is , and
[06:08] between these opening and the closing , I can type anything I want and whatever I type here it is
[06:15] going to display as a paragraph.
[06:17] For example, I can type
[06:19] this is a sample demo of paragraph.
[06:24] After mentioning this text, I can also use another HTML tag which is .
[06:29] B indicates bold, so paragraph I'll just try to mention within the bold tags.
[06:35] This way I can use HTML tag elements as well
[06:39] inside javadoc.
[06:40] If I try to view the Java documentation for this javadoc comments, you can see this is how it is going
[06:46] to look like.
[06:47] Paragraph is highlighted in a bold font.
[06:50] This way, with the help of javadoc comments, we can improve the documentation because this option
[06:57] allows us to generate the HTML format documentation.
[07:02] So whenever you have these kind of requirements, you can always go with this third approach.
[07:07] As a next step, let's try to create a method.
[07:09] And on top of that method, let's try to define the javadoc
[07:13] comments.
[07:14] Once we have defined the javadoc comments on top of the method, we can try to generate our own HTML
[07:20] documentation from the javadoc by using the javadoc tool.
[07:24] I hope you are with me till this point.
[07:26] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
