# 5.7 — Introduction to javadoc comments

> Section 5: Comments in Java

[00:00] As of now, we discuss two types of comments inside Java.
[00:04] Now is the time to discuss the last type of comments in Java, which is javadoc comments.
[00:10] Javadoc comments are a special type of comments that we can use inside Java programming language to
[00:18] document about our code or about or methods and classes.
[00:23] Here you may have a question which is we are already documenting our methods, classes, fields, and
[00:29] any other kind of business logic with the help of multi-line comments and single line comments.
[00:35] When we already have these two approaches.
[00:37] What is so special about Javadoc comments?
[00:40] Why should we use this third approach?
[00:42] What is the scenarios where we should use this approach?
[00:45] So you may have these kind of questions.
[00:47] So let me try to answer them one by one.
[00:49] Whenever we try to define the comments or try to define the documentation of a class or a method or
[00:56] any other component inside a Java code, with the help of Javadoc comment, it is going to give a flexibility
[01:03] to you to extract your documentation in an HTML format so that these HTML files can be shared to others,
[01:12] or they can be deployed into some server so that anyone who don't have access to your code, they can
[01:18] still read the documentation about your Java program.
[01:22] I know you may have many, many questions here.
[01:24] Don't worry, I'm going to resolve them one by one.
[01:27] But before that, let me tell you what is a syntax that we need to follow whenever we want to define
[01:34] Javadoc comments.
[01:35] This syntax is very similar to multi-line comments.
[01:39] The only difference is when we start the Javadoc comment.
[01:42] First, we are going to provide the forward slash followed by two asterisks (/**).
[01:47] In the scenario of multi-line comments, we are going to use single asterisk.
[01:51] Whereas with the Javadoc comments we need to use that two asterisks.
[01:56] And how to end the Javadoc comment.
[01:58] It is same as multi-line comments.
[02:01] You need to use asterisk followed by forward slash (*/). Your JDK installation folder
[02:06] also have a command-line tool with the name Javadoc, which you can use to generate the HTML documentation
[02:14] based upon the Javadoc comments that you have defined inside your Java code.
[02:19] We are going to explore more about these in few minutes.
[02:22] But before that, let me highlight so we can define this Javadoc comments anywhere inside the Java
[02:28] source code, the javadoc tool provided by your JDK.
[02:32] It is only considered those comments to generate the HTML pages that appear just before the declaration
[02:39] of your classes, nested classes, Interfaces, Enums, Annotations, Constructors, methods, and fields.
[02:47] You might be hearing few jargons very first time like Interface, Enum, Annotation, nested class.
[02:54] Don't worry much about them because we are going to discuss about them in the coming sections.
[02:59] But for now these are the list of places where the javadocs can be placed, and the same can be considered
[03:07] by the javadoc tool.
[03:09] You can mention javadoc comments in other places as well.
[03:12] For example, you can try to explain a block of code with the help of javadoc, but that javadoc comments
[03:19] is not going to be considered by the javadoc tool to generate the HTML documentation pages.
[03:25] As a next step, let me show you how these HTML documentation is going to be look like whenever we try
[03:32] to mention the comments with the help of javadoc for the same, I came to the browser and inside my
[03:38] Google search I tried to search for the keyword, which is Java documentation.
[03:43] When you search for these keywords, you're going to get a website which is docs.oracle.com Java.
[03:50] Please click on the same inside this website.
[03:53] You need to click on this Java SE Technical Documentation.
[03:57] SE means standard edition.
[03:59] Let me click on the same link and this will take you to the other website.
[04:04] So as of now when I'm recording this lecture, Java 21 is the most latest and stable version.
[04:11] That's why I'm redirected to the JDK 21 documentation.
[04:16] In this website
[04:17] you can click on this API documentation.
[04:20] As soon as I click on this link you will be redirected to this website.
[04:25] I'm also going to mention this website details inside the GitHub repo.
[04:29] Inside this website you can find the javadoc documentation for all the classes, interfaces, methods that
[04:38] you can find inside that JDK libraries.
[04:41] As of now, we are using certain pre-built JDK classes and methods
[04:47] one such class is System.
[04:49] With the help of System only, we are invoking the out static variable and after that we are invoking
[04:55] the method println().
[04:57] Using the println() method, we are trying to print the
[05:00] given input.
[05:00] If you want to read more about the System class, you can always come to this website and go to the
[05:07] search box and type System.
[05:09] So System is present inside a package called java.lang, lang indicates language.
[05:16] We are ready to talk about packages for now
[05:19] please note that package is a place where you can try to combine multiple classes and interfaces that
[05:27] are providing a common functionality.
[05:29] Here
[05:30] inside the search results, I have a very first option which is "java.lang.System ".
[05:36] If I click on this, I will be taken to the documentation about this class.
[05:41] So this is the class definition
[05:43] and these are the details about the class.
[05:45] Like what is the purpose of this class and from which version this class is available.
[05:51] This is available since 1.0.
[05:53] Apart from that you can also see what are the fields available, what are the methods available inside
[05:59] the System as of now, using this System class, we are trying to invoke a static variable which is
[06:05] out.
[06:06] So you can see this is our variable or field.
[06:08] It is of type static.
[06:10] If I click on this, I will be taken to the section where I can read more details about these variable
[06:16] which is out.
[06:17] So these are all the documentation that I'm able to read here.
[06:21] So all these documentation is built with the help of javadoc comments.
[06:27] Do you want to see how this is built.
[06:29] Let's go to our IntelliJ.
[06:31] Inside our IntelliJ we need to first open the System class that is available inside the JDK library.
[06:38] Whenever you want to open a class, you need to use a shortcut.
[06:43] Inside this shortcut PDF you can look for go to class.
[06:47] So inside mac the shortcut is command O, whereas inside the windows operating system it is going to
[06:55] be Ctrl + N.
[06:56] So please use the shortcut based upon your own operating system.
[07:00] Since I'm into the mac, I'm pressing command O, and this is going to open the search box in the top.
[07:06] So as of now I'm trying to look for class.
[07:09] If I'm trying to look for a file I need to select file.
[07:12] But class should be fine for now.
[07:14] Here I'm going to type System and you can see system from the package java.lang we want to open.
[07:21] So let me click on this
[07:23] inside this class you will be able to see lot of Java documentation.
[07:28] And at certain places you will also see some multi-line comments as well.
[07:33] For example on top of this method they have mentioned multi-line comments.
[07:39] So this is a multi-line comment because I'm seeing only the single asterisk mark after the forward slash.
[07:46] Let's try to analyze how the Java team, they have mentioned that Javadoc comments for the same
[07:52] we want to go to the how to static variable, which is present inside the System class.
[07:57] Again, there are multiple ways to look for your out variable.
[08:01] I can simply type a shortcut which is command F to search inside this class and type out.
[08:08] And this will show me all the places where the out text is matching.
[08:12] But you can see there are too many matches.
[08:14] This is not a recommended approach inside your IntelliJ
[08:17] whenever you want to search for a given text, you can always use command F shortcut if you are using
[08:24] mac operating system.
[08:26] Otherwise for windows it should be control F.
[08:29] I can also confirm the same by looking into the PDF.
[08:33] So inside this PDF shortcuts if you can scroll down here you can see under find there is a shortcut
[08:39] which is Ctrl + F for mac this should be command F, but we are not looking to find a specific
[08:46] text.
[08:47] We are simply looking for the a variable inside my Java class.
[08:52] So whenever you are looking for a variable or a Java method inside your Java class, you can use this
[08:57] shortcut which is file structure popup.
[09:00] So inside mac it is command F12.
[09:03] Whereas inside windows operating system it is going to be Ctrl + F12.
[09:09] So inside my mac I'm pressing command F12.
[09:13] Based upon your keyboard settings you may want to press Command plus function plus F12.
[09:19] So as of now I'm trying to press command plus function plus F12.
[09:24] And this is going to give you the pop up at the file structure.
[09:27] So you can see these are all the methods and variables available as of now
[09:33] inside my System class I'm more interested about the field which is out.
[09:38] So how to search for it?
[09:39] I can simply keep typing out and this is going to show me all the matching variables or methods
[09:48] with the name out.
[09:49] So as of now you can see there is a field with exact matching which is out.
[09:53] I can click on this and it will take me to the place where this variable is present inside my class.
[09:59] Now
[10:00] on top of this variable you can see there is a documentation available.
[10:05] Your intelliJ is trying to show you all this documentation.
[10:09] So this is a Javadoc.
[10:10] How I can say that because the starting of this command we are able to see forward slash followed by
[10:16] double asterisk.
[10:17] And at the end we are closing with a asterisk forward slash.
[10:21] Here they are using lot many keywords lot many standards.
[10:25] We can try to understand that in few minutes, but sometimes we may want to read the comments in an
[10:31] HTML format inside your intelIij itself.
[10:34] In such scenarios, you can toggle the view you can see on the left hand side there is a icon.
[10:39] If you can click on this, you will be able to see all your comments in an HTML format.
[10:45] But if you are looking for the raw javadoc comments, you can click on this button which is toggle
[10:51] render View and that is going to show you all your Javadoc comments in the raw format.
[10:57] So whatever you see here, the same is going to match with what you are seeing inside the Oracle website.
[11:04] So here I am able to see The "standard" output stream.
[11:08] Here you'll be able to see the same here The " standard " output stream.
[11:11] So all the documentation that you are seeing for these output variable is built with the help of these
[11:18] javadoc comments defined here.
[11:20] So if I try to click on this toggle button inside this javadoc
[11:24] comments
[11:24] apart from plain English they have used so many keywords or words.
[11:29] There is an @code.
[11:30] There is p which indicates paragraph inside HTML.
[11:34] This means whenever we try to define comments with the help of javadoc, we can use HTML tags like
[11:41] p,
[11:41] for bold, we can use b, for breaking line, we can use br, so all such HTML tags
[11:47] also we can use,
[11:48] apart from HTML tags we can also use certain kinds of javadoc tags.
[11:54] What is a tag.
[11:55] So whatever you can see here @code this indicates it is a tag, t a g.
[12:01] So when we define these @code we are telling to the javadoc tool,
[12:06] please consider this console as a Java code.
[12:09] Let's try to see how this is going to look like inside the javadoc documentation.
[12:13] If I try to toggle this view, you can see whatever we have mentioned
[12:17] with the help of @code tag, it is going to display in a different style.
[12:23] Maybe here you are not able to see it clearly because we are using some dark theme.
[12:27] If you go to the browser, you will be able to clearly identify that this console word is being displayed
[12:34] in a different font.
[12:36] So whenever we are using @code tag, that entire word is going to be displayed in a special
[12:42] font.
[12:42] Similarly, whenever we want to display a comment with a hyperlink, you can see here I have a code
[12:48] which is Console.charset().
[12:50] If I try to hover on that, it is showing me a hyperlink which will take me to the place where these
[12:56] charset() method is declared like it is available inside a class called Console.
[13:02] So this kind of linking also we can establish by using a tag at the rate link.
[13:08] Let me show you the same here by toggling into javadoc comments.
[13:11] Here you can see just before this Console I am trying to use @link with these curly braces.
[13:18] So inside the curly braces I have to use this @link followed by what is a class name and
[13:24] what is the method name, which is charset().
[13:26] So if I try to follow this format, the comment is going to be displayed as a Java code along with the
[13:32] hyperlink, which will take us to the corresponding class and method.
[13:36] So this way there are multiple tags available inside the javadoc, which we can use based upon different
[13:43] different scenarios.
[13:44] Let me go to the top of this class.
[13:46] On top of this class we have some documentation about this class.
[13:50] If I try to toggle the view, I should be able to see the javadoc comments.
[13:55] Here we are using a tag which is @since.
[13:59] After this, @since we are mentioning 1.0, let's see how the same is going to be visible
[14:04] inside the HTML that is generated by the javadoc.
[14:08] And going to the top of this class, you will be able to see
[14:11] here you can see under a section called,
[14:13] since we are going to display a number which which is 1.0.
[14:17] This tells you the users that this class is available from the initial version of Java, which is 1.0.
[14:25] This way we can use various tags of javadoc and write beautiful javadoc comments.
[14:32] We can generate the HTML file for our Java class or for our methods based upon the javadoc
[14:38] comments.
[14:39] So this is a very quick introduction that I want to give you.
[14:42] I know javadoc comments are complex compared to other comments.
[14:45] That's why let's try to put more efforts in the coming lectures as well.
[14:49] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
