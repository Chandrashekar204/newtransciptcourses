# 5.10 — Generating javadoc using IntelliJ

> Section 5: Comments in Java

[00:00] As of now, we have written the javadoc comments inside this class and with the help of this render
[00:06] view, we are able to see the HTML view of our javadoc comments.
[00:11] So javadoc comments is a great improvement compared to the multi-line comments, especially when we
[00:16] want to provide our documentation to the other developers or to other organizations, or whenever we
[00:23] want to publish our project as an open source library.
[00:27] So in all such scenarios, javadoc is a best option.
[00:31] Sometimes you may have to provide the documentation about your classes in an HTML format for others
[00:39] to read.
[00:39] To handle such scenarios, you should learn how to generate the HTML documentation from your javadoc
[00:46] comments with the help of javadoc tool.
[00:49] It is going to be a simple task.
[00:50] To get started around this, let's go to the official documentation of IntelliJ inside this URL like
[00:57] we were discussing previously, there is good amount of information that is going to help us to get
[01:03] started with javadocs inside IntelliJ. Like how to add javadocs
[01:07] we already know we have to use these /**
[01:11] post that if you press enter the IDE autocompletes the doc comment for you.
[01:17] And apart from adding javadocs, we can also add the javadocs for our methods based upon context.
[01:24] Based upon what my method accept, what my method returns, we can simply use the shortcut and click
[01:30] on this Add javadoc.
[01:32] We already explored this in the previous lecture, and similarly, if you have some errors inside your
[01:37] javadocs, you can fix them by referring to this section.
[01:40] And after this fix javadocs
[01:42] you also have a section explaining how to render Javadocs.
[01:45] We already explored this in the previous lectures, like there is a regular view which is going to show
[01:50] you the Javadoc comments in a raw format, and if you want to see in a render view, you can click
[01:56] on this toggle render.
[01:58] It is going to show you in an HTML format.
[02:01] If you can scroll down on this page, there is a lot of information that you can read, but the section
[02:06] that we are more interested here is how to generate a Javadoc based upon our Javadoc comments.
[02:13] For the same, we need to go to the Tools, Generate JavaDoc option inside IntelliJ.
[02:18] Inside my IntelliJ, I'm going to click on this tools and there is an option Generate JavaDoc.
[02:23] So let me click on this.
[02:25] Here you have an option to generate the JavaDoc for whole project or for a given particular file,
[02:31] since as of now we have written JavaDoc comments only inside the JavaDocCommentsDemo class, I'm
[02:37] going to select this file option by default
[02:40] this file option will show you the current file that you have open, so please make sure you have opened
[02:45] this class post that you can select this file option.
[02:48] After selecting this value, you need to select the output directory where you want to generate your
[02:54] HTML documentation.
[02:55] For the same
[02:56] let me click on this output directory.
[02:58] Post that I'll go to desktop and there is a folder that I have created with the name JavaDoc.
[03:03] So let me select the same.
[03:05] Inside this folder, I want to generate the HTML JavaDoc by my intelliJ.
[03:10] And after that if you can scroll down by default, the Javadoc is not going to generate the documentation
[03:17] for @use, @author, @version.
[03:20] So please select them if you want the documentation to generate for these stacks as well.
[03:25] The default behavior of Javadoc is to not generate the documentation for these tags, since right now
[03:32] we are using @author inside our class, I have selected these and similarly I also selected
[03:38] other options as well.
[03:40] After selecting all these options, you can click on this generate button.
[03:44] And with that the Javadoc is going to be generated
[03:47] and the HTML file is going to open inside your browser.
[03:51] You can click on your class name which is JavaDocCommentsDemo.
[03:55] You can see this is the description that we have.
[03:57] These are sample class to show demo about Javadoc.
[04:00] Let me click on this link.
[04:01] So we have all the details like paragraph highlighted in a bold text.
[04:05] And since he is available as 1.0 and author details available.
[04:10] see also
[04:11] available with the class name as MultiLineCommentsDemo and there is a information about the default
[04:16] constructor.
[04:17] The methods that we have.
[04:19] What are the static methods?
[04:20] What are the instance methods?
[04:22] What are the concrete methods that we have?
[04:24] Under the concrete methods you'll be able to see a method sum().
[04:27] So let me click on this sum() method and which will take me to the documentation of this sum() method.
[04:33] So here we have the documentation that we have written with the help of Javadoc comments.
[04:39] We can also see this HTML file inside my Javadoc folder
[04:44] you can see all these files are automatically generated by my Javadoc tool.
[04:49] And the HTML file that we are seeing right now in the browser is JavaDocCommentsDemo.html the
[04:56] same we can see here.
[04:57] I hope you are clear with the
[04:59] process that we need to follow.
[05:01] There are three important steps that you need to be aware.
[05:04] First, you need to know how to write the Javadoc comments.
[05:07] What is the syntax that you need to write post that you should understand
[05:12] what are the Javadoc tags available,
[05:14] what are the HTML tags that we can use?
[05:17] You can always find these information by referring to the existing Javadoc comments inside the Java
[05:23] library
[05:24] classes.
[05:25] Once you have defined your Javadoc comments as a last step, you should also know how to generate the
[05:31] HTML documentation for your Java classes with the help of Javadoc tool.
[05:35] So please note about all these three steps.
[05:38] You should be good with those basics.
[05:40] For your quick reference, I also put a sample screenshot of Javadoc comments that you have built inside
[05:46] the slide.
[05:47] I also mentioned important tags available inside the Javadoc, so these are all the most important tags
[05:53] that you may see in most of the Javadoc comments.
[05:57] Anytime if you have any questions, please refer to the resources that I have mentioned previously.
[06:02] With this, I'm assuming your super clear about the three approaches that we have discussed related
[06:07] to the comments inside Java.
[06:10] Before I try to close this lecture, I want to share a couple of funny meme images related to the Java
[06:16] comments.
[06:17] This is the very first meme image like you can see here
[06:20] developers.
[06:21] usually they don't like using the comments to describe about their program, whereas they are going
[06:27] to like it a lot to temporarily remove part of code or to temporarily comment a particular code.
[06:33] This meme clearly conveys most of the times in real projects developers
[06:38] they use comments to temporarily comment their code, but to not document about their programs.
[06:44] It is very unfortunate, but I would always encourage you to take some time to document about your complex
[06:51] piece of code
[06:52] with the help of Java
[06:53] comments.
[06:53] Few organizations, they expect the Java developers to describe their program with the help of Java
[07:00] comments.
[07:00] Otherwise, they are not going to approve your code into the GitHub master repository.
[07:05] Inside the review process, they are going to reject your code saying that please add comments describing
[07:11] about your program.
[07:12] If there is no such process, then this is going to happen always where developers they're not going
[07:17] to use comments to describe the program.
[07:19] Instead, they are going to use the comments to temporarily remove the part of code.
[07:23] And the next funny image I have here is, sometimes developers
[07:27] they write the comments describing about their program for name sake.
[07:31] Here you can see the pizza box
[07:33] they have a instructions saying that open box before eating pizza.
[07:38] This very obvious, right?
[07:40] People obviously will open the box to eat the pizza.
[07:43] There is no need of mentioning these instructions on the box.
[07:47] Very similarly, many times you will see inside the real projects developers mentioning the comments
[07:53] saying that this is a method which accepts two parameters and return an output.
[07:57] So such comments
[07:58] we should never write other developers
[08:01] they are going to laugh at those comments.
[08:03] That's why my humble request is if you decided to describe your code with the help of Java comments,
[08:09] then put some good efforts in writing good Java comments.
[08:13] Don't do this for the namesake.
[08:15] So these are the images and advice that I want to share.
[08:18] I hope you like them and you're going to follow my advice.
[08:22] Thank you and I'll catch you in the next lecture bye.


########################################
