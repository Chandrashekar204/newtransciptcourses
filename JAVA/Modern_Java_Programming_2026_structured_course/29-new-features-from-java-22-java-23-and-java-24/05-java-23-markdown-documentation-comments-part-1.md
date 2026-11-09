# 29.5 — [JAVA 23] Markdown Documentation Comments - Part 1

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] Java 23 version released on 17th September 2024.
[00:05] These are all the new features that got introduced as part of this new release. So let's try to understand
[00:11] what are these features.
[00:12] Majority of the features that got introduced as part of JDK 23 are Preview features.
[00:18] So you can see the very first one is a Preview feature,
[00:21] similarly the second one also Second Preview followed by fourth one,
[00:25] it is second preview and module import declaration,
[00:28] it is also a preview feature followed by the next one is in the third preview stage and structured concurrency
[00:34] it is in the Third Preview followed by scoped values.
[00:36] It is Third Preview and flexible constructor bodies,
[00:40] it is in the Second Preview.
[00:41] First, let's try to understand what is a preview feature.
[00:44] What I'll do is, inside my IDE, I'll go to the Codium chart.
[00:47] Codium is a plugin that we have installed inside our IDE long back.
[00:51] Please go and check the last lecture inside the section_03 where we have installed the Codium plugin,
[00:57] which is a artificial intelligence coding companion tool. To this Codium,
[01:01] I'm going to ask what is a preview feature in JDK.
[01:07] If you try to read this, response, preview features are intended to give
[01:11] developers an early look at the upcoming changes and allow them to
[01:15] provide feedback to the Java development team.
[01:18] They are not yet part of the standard Java API and may change or be removed in the future releases.
[01:26] So there is a good chance these preview features may change, or they may be entirely removed from the
[01:32] future releases based upon the developer community feedback.
[01:36] I hope you got some clarity about what is a preview feature.
[01:39] Since these preview features are not yet finalized, I'm not going to discuss any of the preview feature
[01:44] from the JDK 23.
[01:45] .
[01:46] If one of the preview feature got finalized and released in the upcoming releases, definitely I'm going
[01:51] to discuss about them,
[01:52] when a feature got released fully. With that discussion, it should be pretty clear for you that most
[01:57] of the features are preview features, but there are few production ready features.
[02:02] The very first one is markdown documentation comments, which I am going to discuss in a few minutes,
[02:08] followed by this vector API, which is change happened inside the Java library.
[02:13] We don't have to worry much as a Java developer.
[02:15] Similarly, there is another change happened inside the Java library and this is the one that I'm talking,
[02:21] deprecate the memory access methods in unsafe class for removal.
[02:26] And there is also a feature around the garbage collection which we don't have to worry.
[02:30] And with that, from developer perspective, there is a single important feature that got introduced
[02:35] inside JDK 23 which is marked down documentation
[02:39] comments.
[02:40] So let me click on this link and this will take you to the 467 JEP.
[02:46] What is JEP ?
[02:48] JDK Enhancement Proposal.
[02:51] So whenever someone planning to release a new feature, they will write down all the requirements,
[02:55] how this feature is supposed to work, all such details they are going to capture inside this JEP page
[03:01] and each JEP is going to have a number.
[03:03] So for this feature the number is 467.
[03:05] So let's try to understand what is this Markdown Documentation
[03:09] Comments.
[03:10] First let's try to understand what is a Markdown.
[03:12] So let me ask the same question to Codeium.
[03:14] What is markdown?
[03:17] As soon as I ask my question, you can see I'm getting a response saying that markdown is a lightweight
[03:23] markup language that allows you to create formatted text using plain text syntax.
[03:29] So these are all the same syntaxes.
[03:32] For example, inside the markdown, if you want to create headers, you need to start the heading with
[03:37] the hash symbol followed by space.
[03:39] Similarly, for bold text, you need to use two asterisk symbols, so there are a good amount of syntaxes
[03:45] as part of markdown, I would recommend you to read this response, or you can also go to the website
[03:50] which is markdownguide.org.
[03:53] And here you can click on this cheat sheet.
[03:56] And inside this page you'll be able to see all the syntaxes around the markdown.
[04:02] I'm going to walk through a few of these syntaxes in a few seconds, but if you are new to the markdown,
[04:08] you can read more details about the markdown here.
[04:10] The same markdown syntax is also used to write Readme files inside the GitHub repositories.
[04:17] If any time you have written a Readme document inside the GitHub repo.
[04:21] There's a very good chance that you might be already comfortable with all these syntaxes.
[04:25] Now to explain you about these new feature, first let me create a new class.
[04:31] So inside my section_29 project I'm going to create a new package with the name com.eazybytes.java23.
[04:40] .
[04:41] Inside this new package, I'm going to create a new Java class.
[04:45] Here I'll mention the class name as MarkDownComments. Inside Java,
[04:50] as of now, whenever you want to write comments, we have three different options.
[04:55] The very first one is, by mentioning forward symbol two times.
[04:59] You can write the single line comments, and the second option that we have is, by mentioning these forward
[05:06] /* symbol.
[05:08] We should be able to write multi-line comments.
[05:11] For example, first I need to start the comment with the /* symbol, followed by
[05:16] I need to terminate the comments also with the * symbol followed by / symbol.
[05:21] Between these two lines, I can write any number of lines of comments.
[05:25] So this is one style of comments inside Java.
[05:29] And the third style that we have inside Java is, Javadoc
[05:34] comments.
[05:34] So whenever you want to write Javadoc comments, you need to type forward slash followed by two asterisk
[05:40] symbols and press enter.
[05:42] And with that you will be able to write the Java documentation.
[05:47] To know more details about these Javadoc comments, you can open one of the Java library class, which
[05:54] is Object itself.
[05:56] So this is present inside the java.lang package.
[05:59] If you go to the method which is hashCode(), you'll be able to see there are Javadoc comments on top
[06:05] of this method explaining about how this hashCode() method is going to work.
[06:09] If you click on this pencil icon, you'll be able to see the actual Javadoc comments.
[06:15] This is the third syntax that we can follow to write the comments.
[06:18] Now as part of these markdown comments feature, a new option has been introduced for the developers.
[06:25] All these days,
[06:26] whenever a developer wants to write a good Java documentation, they need to rely on the HTML syntax.
[06:33] For example, if you go to the hashCode() documentation here, you can see there is a p which indicates
[06:39] paragraph inside the HTML.
[06:41] Similarly, if you want to start a new bullet element, you need to use this li under ul element.
[06:49] This way developer
[06:50] they have to rely on the complex HTML syntax to write good Java documentation.
[06:55] But these days everyone is relying on the simple syntax, which is markdown syntax, to write to documentation.
[07:02] Because it is very easy to write, it is very easy to learn and remember compared to the HTML, HTML
[07:08] used to be a hot option when Java introduced in 1990s, but right now we have better options compared
[07:15] to HTML, which is markdown.
[07:17] That's why Java Team decided to allow the Java developers to leverage markdown as well, to write the
[07:24] Java documentation.
[07:25] I hope you got some good introduction about this new feature.
[07:29] In the next lecture,
[07:29] let's try to understand more details about this feature.
[07:32] Thank you,
[07:33] bye.

----------------------------------------
