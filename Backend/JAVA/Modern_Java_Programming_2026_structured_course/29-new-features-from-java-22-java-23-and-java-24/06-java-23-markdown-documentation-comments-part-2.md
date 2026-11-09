# 29.6 — [JAVA 23] Markdown Documentation Comments - Part 2

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] Before we try to explore about these new features, first, we need to perform certain housekeeping
[00:06] activities.
[00:07] The very first activity that you need to take care is, updating your IntelliJ Idea.
[00:12] If you are planning to use Java 23 and its features, definitely the IDE has to be updated.
[00:19] The minimum IntelliJ Idea version that you need to install is 2024.2.1.
[00:26] Regardless whether you are using Ultimate Version or Community version, please make sure you are updating
[00:32] your intelliJ to this version.
[00:35] Otherwise, you can't use Java 23 version.
[00:38] Once you update your intelliJ, you need to go to your module and open the settings.Here
[00:45] under the project Settings, you can click on this project option and under the SDK.
[00:51] As of now you can see I have 22 selected, but we need to make sure we have set up the Java 23.
[00:57] I have an option of Java 23 because I already installed inside my system.
[01:02] If you don't have this option, you just have to click on this download JDK here
[01:07] inside this pop up window, first you need to select the version as 23, followed by you need to select
[01:12] the vendor.
[01:12] You can go with this Oracle Open JDK option.
[01:16] Later on you can confirm whether you are fine with the location, otherwise you can change the location.
[01:21] As soon as you click on this download button.
[01:23] A new SDK option is going to appear inside your system.
[01:27] The same you need to select, and with that, you're going to have these pop up, which is going to
[01:33] ask you to accept the few license and agreements.
[01:36] So let me click on this accept.
[01:38] Next, coming to the language level, you need to make sure you are selecting the 23 Markdown documentation
[01:46] comments.
[01:46] In case if you are looking to explore the preview features as well, which are available as part of
[01:52] 23, then you need to select these 23 preview option.
[01:56] In my case, I'm fine with these 23 Markdown documentation
[01:59] comments.
[02:00] So let me select the same.
[02:01] If your intelliJ is not up to date, then you will not have these 23 option.
[02:06] That's why I requested you to update the intellij previously. The same kind of selections you need
[02:12] to make for your module as well.
[02:14] For section29 module you can go to the dependencies and here please make sure you have selected project
[02:21] SDK which is open JDK 23.
[02:24] After making all these changes you can click on this apply,
[02:27] okay.
[02:27] Now my project or module is set up with Java 23.
[02:31] To write the comments using this markdown option, a new syntax is introduced inside Java.
[02:38] This new syntax is three forward slash symbols.
[02:42] So after mentioning these three forward symbols you can define your documentation command or Java comments.
[02:50] But before I try to write some comments inside this class, let me create few methods inside this class.
[02:56] To create these methods
[02:57] very quickly I'm going to take help from the codeium.
[03:00] Let me click on this shortcut, which is command I to give instructions to the codeium.
[03:05] So here I'm going to type generate methods that perform arithmetic operations on two numbers. Followed
[03:16] by I'm also going to give instructions Don't provide comments.
[03:22] So let me press enter and it is going to generate the code I need to accept this code,
[03:26] So let me click on this accept option.
[03:29] You can see we have four different methods generated inside the class.
[03:32] Let me try to write comments on top of the class.
[03:35] After mentioning these three forward symbols, I'm going to mention a comment which is,
[03:39] this class contains methods for performing basic math operations.
[03:44] If you can click on these option, you'll be able to see the preview of your comments.
[03:49] So if you see this is a normal comment in case if you are looking to use markup syntax, you are free
[03:55] to use the same.
[03:56] For example, here I'm going to mention two asterisks symbols at the start and ending of this comment.
[04:02] And with that, the comment is going to be converted into bold style. Inside markup syntax,
[04:07] whenever we are surrounding a text with these two asterisks, it is going to convert into a bold text.
[04:13] Now, if I press enter, I'm going to get an option to create one more line of Markdown
[04:18] comments.
[04:19] The beauty of this feature is, inside this feature you can still use the Javadoc comments as well.
[04:25] For example, I can use @author tag available as part of Java documents.
[04:31] To do this I'm going to mention Eazybytes followed by,
[04:35] I'm going to use @version tag as well.
[04:38] And to this version I'm going to mention 1.0 as a value.
[04:41] So if you click on this, you'll be able to see how these comments are going to look like.
[04:45] Did you see the beauty?
[04:46] I'm able to write the comments using Javadoc style and markdown style as well.
[04:52] If needed, you can also use HTML style as well.
[04:55] Now, very quickly I'm going to paste comments on top of the add method so that we can discuss more
[05:01] details about these MarkDown Comments.
[05:04] So let me paste the code that I have.
[05:07] So here you can see I'm trying to build comments with the help of Markdown comments, because I'm trying
[05:12] to use these three forward symbols.
[05:15] First, let's try to visualize how these comments are going to look like.
[05:18] So I have a tabular format where I'm trying to mention if you try to give an input 2,3,
[05:24] the output from this method, it is going to be 5.
[05:26] Similarly, I have given other examples as well.
[05:29] With this,
[05:30] what I'm trying to convey is, we should be able to build comments that supports tabular format as well.
[05:36] Previously it is not possible, but right now, since markdown allows us to create tables, we just
[05:42] have to follow the markdown syntax to create a table.
[05:45] And with that, your comments are going to have a tabular structure.
[05:48] So how to create a table,
[05:50] you just have to use this pipe symbol followed by your column name, followed by pipe symbol, followed
[05:55] by second column name,
[05:57] and you need to end with the pipe symbol.
[05:59] So whenever you want to mention a value under a column, you just have to make sure you are mentioning
[06:04] the value between the pipe symbols.
[06:06] So you can see here,
[06:07] if I go to the preview of this command, you will be able to see these are the columns and these are
[06:12] the values corresponding each of the column.
[06:15] So please try to understand these comments.
[06:17] Since you are going to have this file inside the GitHub repo, you can copy the same and try to understand
[06:22] how this is working.
[06:23] And later on I'm trying to mention a bold text value by using these double asterisk symbol, followed
[06:29] by I'm trying to use @param, @return, which are from the Javadoc library.
[06:34] So this is how the comment is going to look like.
[06:36] Now let me show you more flavors of markdown comments.
[06:40] This time I'm going to paste some comments on top of the subtract method.
[06:45] Here you can see I'm trying to paste some comments.
[06:48] # symbol we are going to use inside the markdown whenever we are looking to mention a header value.
[06:54] So please mention hash followed by space.
[06:56] The space is very important, otherwise the header is not going to appear like you are expecting. Followed
[07:03] by whenever you are looking to mention list of elements, you need to use the syntax which is hyphen
[07:09] followed by space.
[07:10] So here I have mentioned two list elements explaining if you give so-and-so input, you're going to
[07:16] get so-and-so output. Later on,
[07:18] I have used @param and @return, but this time for the @return,
[07:22] I have mentioned three asterisk symbols.
[07:24] Whenever you are using three asterisk symbols, it is going to look like bold italic,
[07:31] that's what you can see here.
[07:32] So if you try to compare to the add and subtract commands here the return statement it is only bold,
[07:38] whereas here it is both bold and italic.
[07:41] And you can see here this method subtract two numbers.
[07:44] It is displayed as a header.
[07:46] And these are the list of elements which are being displayed as a list.
[07:50] In case if you are looking to reduce the font of the header, you can mention two hash symbols and it
[07:56] is going to reduce the size of your header.
[07:59] I hope you are clear.
[08:00] Now let me go to the multiply() method and try to mention few comments. This time
[08:06] also, the comment mostly looks like subtract only, but I just mentioned these three hyphens as the
[08:12] very first comment.
[08:14] So with the help of these three hyphens, we should be able to introduce a horizontal line like you
[08:20] can see here
[08:21] there is a line came and this is the heading,
[08:23] and these are the params,
[08:25] and this is the returns where I am trying to use three asterisk symbols.
[08:29] That's why the multiplication of the two numbers is being displayed as bold italic.
[08:34] I hope you are clear.
[08:35] Let's go to the divide and try to mention some comments here as well.
[08:39] This time you'll be able to see that I have used three backtick symbols.
[08:44] So whenever you are surrounding some content with these backtick symbols, then such content is going
[08:52] to be displayed as a code.
[08:54] Sometimes you may have a requirement to write some code inside the comments itself, so this can be
[09:00] easily achieved with the help of these backtick symbols.
[09:03] So this content I have surrounded with these backticks if you try to visualize,
[09:08] so this is how it is going to look like.
[09:10] Please note inside this backtick I am trying to use an @override symbol which is originally from Java
[09:17] docs. But in this scenario it is not going to be considered as a Java doc tag.
[09:22] Instead, it is going to be considered as a simple code, because we have surrounded this entire text,
[09:28] with these three backtick symbols.
[09:30] That's why you are seeing these code segment here on top of the divide() method.
[09:34] This way you can always try to use all the supported markdown syntax to write to more beautiful comments
[09:43] on top of your methods and classes.
[09:46] I hope you got some clarity.
[09:47] The most important information that I want you to carry from this lecture is, Java
[09:52] introduce fourth approach to write the comments, which is markdown comments.
[09:57] And this feature is available only from the Java 23.
[10:01] Whenever you are looking to write comments with the help of markdown comments, you need to use the
[10:06] symbol which is three forward slash symbol.
[10:09] You can read more details about this feature by opening this page.
[10:13] Here I have an example which I want to highlight so that you'll get more clarity.
[10:17] Inside this page, they have given a screenshot highlighting the differences between the two versions.
[10:22] So on the left hand side they try to write the documentation with the help of Java docs, whereas on
[10:30] the right hand side they have written the same comments with the help of Markdown
[10:35] comments.
[10:35] So these are the comments
[10:37] belongs to the hashCode() method available inside the Object class.
[10:41] They clearly highlighted about the differences.
[10:44] So here you don't have to use these asterisk symbols.
[10:46] You should always use these three forward slash symbols.
[10:50] Here,
[10:50] you can see instead of using these paragraph symbol from the HTML, you just have to create an empty
[10:56] line.
[10:56] So inside the markdown, whenever you created an empty line, the immediate next line will be considered
[11:02] as a new paragraph. And the list of elements you can see,
[11:05] instead of using this ul and li tags, you can simply use this hyphen symbol.
[11:10] And whenever you're looking to display a specific word in a code style, you need to surround that word
[11:17] with the help of these backtick symbols.
[11:19] Whereas with the Javadocs, you need to surround it with the curly braces and use these tag which is
[11:25] @code.
[11:25] So it's very complex.
[11:26] Now it became very simple.
[11:28] You just have to use these backtick symbols surrounding that word.
[11:32] The same is highlighted here as well.
[11:34] So try to analyze this screenshot to understand the differences between these two approaches.
[11:39] With that,
[11:39] now you may have a question which is,is it mandatory to convert all my Java doc based comments to the
[11:46] markdown comments.
[11:47] Definitely it is not mandatory.
[11:49] It's up to you if your documentation is so bad that others are not able to read and understand, then
[11:55] definitely it is worth to spend some time updating your comments with the help of markdown approach,
[12:02] so that the readability of your comments is going to be increased.
[12:06] Otherwise there is no need.
[12:08] But in future, whenever you are trying to write new commands, please always consider these markdown
[12:14] approach because your comments readability is going to increase a lot with the minimum syntax and minimum
[12:22] effort.
[12:22] I'm going to check in this file for your reference into the GitHub repo.
[12:26] Please try to understand all these commands,
[12:28] Please try to write these comments with your own hands,
[12:31] and with that, you're going to get some more clarity around this new feature.
[12:35] Thank you and I'll catch you in the next lecture, bye .

----------------------------------------
