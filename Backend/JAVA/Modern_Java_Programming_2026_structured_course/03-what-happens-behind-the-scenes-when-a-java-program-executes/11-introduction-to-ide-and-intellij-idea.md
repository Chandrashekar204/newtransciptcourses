# 3.11 — Introduction to IDE & IntelliJ IDEA

> Section 3: What happens behind the scenes when a Java program executes

[00:00] As of now, we have built our first Hello World Java class with the help of a text editor.
[00:06] So inside my text editor, I have typed all this Java code post that I have compiled with the help of
[00:12] Java C command, and after the compilation is successful, I executed my Java program with the help
[00:18] of Java command.
[00:19] But this approach, whatever we have followed to develop our Java program with the help of text editor
[00:26] is not going to be super helpful because inside real projects we are going to develop hundreds of Java
[00:32] classes, thousands of Java methods.
[00:35] So for such real scenarios, the text editor is not a recommended approach.
[00:40] And obviously Jshell also is not a recommended approach because using Jshell, we can only execute few
[00:47] lines of code to validate if the syntax is correct.
[00:50] If the code is correct.
[00:52] That's why we cannot use both Jshell approach and text editor approach to develop Java classes.
[00:58] Then the immediate question that you may have is then what is the approach that I need to follow inside
[01:03] any real project by the same.
[01:05] The alternative to JCL and text editor is IDE.
[01:09] So what is an IDE?
[01:11] Integrated Development Environment?
[01:13] IDE are a software application that provides developers with a comprehensive set of tools to write,
[01:20] test, and debug your code in one place.
[01:24] Just like how we have various software applications are tools like Ms. Word, Excel, PowerPoint, which
[01:31] can be leveraged by the people who want to build documents.
[01:35] Very similarly for the developer who want to develop the code based upon Java programming language,
[01:41] we have software applications with the name IDE.
[01:45] So these IDE means integrated development environment.
[01:48] So from now onwards we are going to use IDE.
[01:51] And we are going to say bye bye to JCL and text editor.
[01:55] The reason why we should look for IDE, compared to the basic approaches like JCL and text editor,
[02:01] is with the help of these Ides, we have so many advantages.
[02:04] The very first advantage is it is going to increase your productivity.
[02:08] Because inside ID we have so many tools like code completion, refactoring, debugging, testing.
[02:15] So with all these tools, the developer productivity is going to increase.
[02:20] For example, if I don't remember a particular class or a method name, I can simply start typing whatever
[02:26] I remember and my ID is going to recommend some code completions.
[02:32] And from the code completion recommendations, I can select what is a Java class or the Java method
[02:37] that I'm trying to invoke.
[02:38] So these kind of tools are available inside IDE.
[02:42] I know as of now it is not going to make any sense to you, but when I show you that demo, it is going
[02:47] to make more clear for you.
[02:48] And throughout this course we are going to use IDE.
[02:51] And in the same process I'll also teach you everything about IDE, how we should use IDE, and how to
[02:57] debug our code whenever there is a bug inside our program.
[03:01] So all such techniques I'm going to teach you so that you are going to be ready for your real time projects.
[03:08] Apart from increased productivity, we have other advantages with the IDE, like integration with other
[03:14] tools and frameworks.
[03:16] From the IDE itself, you can integrate with other products like git, GitHub, or frameworks like spring,
[03:21] spring, boot, maven build system.
[03:24] So these are all the advanced options that you may look for once you start learning about the advanced
[03:31] frameworks that are available inside the Java ecosystem.
[03:34] But right now, since you are learning only the basics of Java language, that's why these Maven spring,
[03:41] they will not make any sense for you.
[03:43] But like I said, once you start looking for what is beyond Java programming language, how I can become
[03:49] a web developer or a back end developer, or a full stack developer or a mobile developer.
[03:54] In all such scenarios, you have various options to learn beyond Java programming language.
[03:59] So whenever you choose your advanced path and select a particular framework in that scenario.
[04:05] Also, the IDE is going to help you a lot because it is going to provide lot many integrations with
[04:12] lot, many tools and frameworks.
[04:14] The next advantage that we have here is whenever we try to develop our Java program, with the help
[04:18] of IDE, your code quality is going to increase because whenever you are not following any particular
[04:25] syntax or any code standards, your IDE is going to help you by highlighting what error or what mistake
[04:32] you have done.
[04:33] This way, your code is going to have a great quality and you will not have any surprises during the
[04:39] compilation stage.
[04:40] With the text editor, you are not going to get an inline feedback.
[04:44] You will only know what is a syntax error or the compilation error that you have done only after the
[04:50] compilation, but with IDE you're going to get immediate feedback, and with that feedback, you can
[04:56] immediately correct your code and improve your code quality.
[05:00] Apart from all these advantages, one more great advantage that we have with IDE is collaboration.
[05:05] With the help of Ides, you can collaborate with other multiple developers to work on the same code
[05:11] base simultaneously.
[05:13] For example, your friend might be staying in different city or different country, but with the help
[05:19] of IDs, both of you can collaborate with each other and work on the same code base.
[05:24] So these are the advantages.
[05:26] I hope you are convinced that why we should use ID compared to the basic approaches like jshell and
[05:31] text editors.
[05:33] As a next step, we need to set up ID inside our local system.
[05:37] Whenever you are trying to set up an ID inside your system, we have various options in the market,
[05:43] but let me show you the most commonly used IDs like you can see here.
[05:47] We have IntelliJ Idea, eclipse, Visual Studio Code, NetBeans.
[05:52] So these are the most commonly used Ides in the Java ecosystem.
[05:57] From this we can choose any one of them.
[06:00] But my recommendation is IntelliJ Idea because this is the ID which is used to heavily by the Java developers
[06:08] due to its ease of use.
[06:10] Various features provided by IntelliJ Idea.
[06:13] Compared to other Ides, IntelliJ Idea has an advantage because it is more of developer friendly and
[06:19] it provides a lot many features compared to other Ides, which is going to make our life super, super
[06:25] easy.
[06:25] If you are still not convinced about why we should use IntelliJ Idea, I have mentioned more details
[06:31] about why we should use IntelliJ Idea in the next slide.
[06:34] So let me show you that.
[06:35] So here I have highlighted many points why we should use IntelliJ Idea.
[06:39] The main points that I want to highlight here is the third point.
[06:42] Whenever you are trying to set up IntelliJ Idea, there are two types of versions available a paid version
[06:48] and a free community edition.
[06:50] When you start working in an organization, your organization, or your project, they are going to
[06:56] provide you the paid version.
[06:59] Using this paid version, you can start developing the Java programs.
[07:02] So this paid version is widely regarded as one of the top Java IDE.
[07:08] But for the developers who are learning Java programming language or who want to use the IntelliJ Idea
[07:15] at free of use.
[07:16] We have a community edition, so this is also highly capable.
[07:20] And this is almost similar to the paid version.
[07:23] So if you ask me what is the difference between a paid version and community edition?
[07:27] It is like a Netflix plan inside Netflix.
[07:30] We have plans with HD and 4K.
[07:32] If you really want a high resolution, you will go with 4K plan by paying more amount of money.
[07:39] But for most of the users, HD plan is more than sufficient.
[07:43] If you try to bring the same Netflix analogy for the IntelliJ Idea scenario, we should be fine with
[07:49] the community edition.
[07:50] We can use this edition without paying any money.
[07:53] But like I said, when you start working in real projects, there is a very good chance that your project
[07:59] or an organization, they're going to support you by giving a paid version to use, so that it is going
[08:05] to help you to improve your productivity.
[08:08] So to install IntelliJ Idea, we need to go to the IntelliJ Idea website which is jetbrains.com/idea.
[08:15] So let me navigate to this URL.
[08:17] So this is a URL that I was talking before.
[08:20] JetBrains is an organization who developed and maintaining these IntelliJ Idea.
[08:25] They're claiming IntelliJ Idea as a leading Java and Kotlin IDE.
[08:29] So if you can click on this download option by default, you'll be asked to download the ultimate version.
[08:36] The ultimate version is the paid version.
[08:38] You can use this ultimate version only for 30 days with a free trial period, but we decided to use
[08:44] the Community Edition.
[08:46] That's why you can scroll down on this page and there is an option to download the IntelliJ Idea Community
[08:53] Edition, so please select your operating system here.
[08:57] Since right now I'm using Mac OS by default, this Mac OS is selected for me.
[09:01] So based upon your operating system, you can select the option and you can click on this download button
[09:07] which will download the IntelliJ Idea into your local system.
[09:11] You can install by clicking next, next, next and post that.
[09:15] You should be able to easily open the IntelliJ idea.
[09:18] So inside the next lecture, I'll show you how the IntelliJ Idea is going to look like.
[09:23] Apart from IntelliJ, I also said there are other options like eclipse.
[09:27] This is a completely open source IDE, but my recommendation is to go with interlaced as this is the
[09:34] mostly used IDE inside Java ecosystem.
[09:37] Very similarly, we have Visual Studio Code from the Microsoft.
[09:41] This IDE also open source and we can use at free of cost.
[09:45] But Visual Studio Code is not a great idea for the Java development.
[09:50] It is a top IDE for the JavaScript or Python developers, according to me for Java.
[09:56] Still, IntelliJ Idea is the number one IDE.
[09:58] Apart from Visual Studio Code, we also have Apache NetBeans.
[10:02] This IDE also comes under the open source.
[10:05] We can use this IDE at free of cost.
[10:07] Among all these options we have selected interlace.
[10:10] Please download these and set up interlace inside your local system.
[10:14] I'm going to show you how to use IntelliJ in the next lecture.
[10:18] Thank you and I'll catch you in the next lecture by.

----------------------------------------
