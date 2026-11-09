# 13.15 — Logging in Java - Part 1

> Section 13: Accept input using BufferedReader and Scanner

[00:00] Inside this lecture, I'm going to show you a demo of logging for the same
[00:04] first I'm going to create a new package and the package name is going to be com.eazybytes.log
[00:11] inside this package
[00:15] first I'm going to create a new Java class.
[00:18] The class name can be LoggingDemo. Inside this class
[00:22] first I'm going to create a main() method.
[00:25] Inside this main() method I have intentions to perform some logging, so to perform the logging first
[00:30] we need to make sure we are creating the object of Logger by using the classes available inside that
[00:37] Java library to create the object of Logger, we're not going to use a new operator or the constructor
[00:43] of the Logger class.
[00:44] Instead, we need to create the Logger object as an static variable.
[00:50] That's why here I'm going to type private static followed by Logger.
[00:55] Logger is a class which is available inside the java.util.logging.
[01:01] So please make sure you are selecting the class but not the interface which is available inside the
[01:06] java.lang.System.
[01:08] So once you selected these first option, you can give a name to your static variable of type Logger.
[01:15] So the name I'm trying to give here is logger itself.
[01:18] And post that on the right hand side
[01:20] I need to mention the class name which is logger followed by I need to invoke the method getLogger()
[01:28] to this method, I need to pass the class name where this Logger object is being created.
[01:33] So right now this Logger object is getting created inside these LoggingDemo class.
[01:38] That's why I need to take the same class name followed by I need to mention .class.getName().
[01:46] So with this statement we are telling to the Logger class.
[01:49] Please create me a Logger object by considering the name of the class which is LoggingDemo.
[01:55] So why we need to provide this class name?
[01:57] I'm going to share more details about this in few minutes.
[02:00] For now, please note that any time you want to use the logging inside Java library, you need to follow
[02:07] this syntax to create the object of Logger so it's not super complex.
[02:11] First, we need to invoke the getLogger() method, and to this get logger method we need to pass what
[02:16] is the class name.
[02:18] And on the left hand side we need to create the static variable of type Logger. Using these Logger object
[02:25] now I can try to perform the logging or printing an output into the console.
[02:31] Let me use this object which is Logger.
[02:34] As soon as I press dot, you can see I have so many methods available inside this object.
[02:40] One such method is info().
[02:42] So whenever I'm using the info() method and to this info() method, if I pass a statement, the same is
[02:48] going to be printed onto the console.
[02:50] So here I can mention a statement which is
[02:52] this is info() level
[02:55] logging info is one such severity
[02:58] similarly we will have many other severities like warning is one such severity.
[03:03] So this is one way of logging a statement.
[03:06] The other approach is using the same Logger object
[03:09] we can invoke the log() method to the log() method
[03:13] we can pass two parameters.
[03:15] One is what is the log level.
[03:17] So the log level that right now I want to use is info().
[03:21] And after mentioning the log level I'm trying to mention the same message which is This is info level
[03:28] logging.
[03:29] I'm getting a compilation error at level.
[03:32] My IntelliJ Idea is not able to resolve this, so let me try to type one more time
[03:37] Level belongs to java.util.logging.
[03:40] If you can click on this INFO you will be able to see lot many other levels as well like INFO, WARNING,
[03:47] SEVERE and similarly we also have CONFIG, FINE, FINER, FINEST.
[03:53] Based upon the type of message you are trying to display, you need to use the corresponding level.
[03:59] Suppose if you are just trying to give a information or an info by just printing a value.
[04:06] In such scenarios we can use the info level.
[04:09] Whereas if you're trying to give a warning like this should be handled properly.
[04:14] In such scenarios you can use a warning level, but if you're trying to convey a very serious issue
[04:19] or a serious problem in such scenarios, you can use a severe level so you can see each level has a
[04:26] value for severe
[04:27] It is thousand.
[04:28] For WARNING it is 900 for INFO it is 800 CONFIG 700.
[04:33] So this way you have various levels available inside the logger library, which you need to use based
[04:41] upon the severity or based upon the seriousness of your message.
[04:45] So most of the times developers they will use INFO for debugging purpose and WARNING to warn about an
[04:52] situation and SEVERE to complain about a serious situation or a critical situation as of.
[04:59] Now you can see I'm trying to use the INFO level.
[05:02] In the second approach you can see
[05:03] first we need to mention what is the level followed by what is a message.
[05:07] Whereas with the very first approach, since you are already invoking the info() method, it is pretty
[05:12] clear to the logging framework that you are trying to follow the INFO level.
[05:16] So now let me try to execute this program and see what is going to happen.
[05:20] You can see I am getting a lot of details, so this is a very first message.
[05:25] If you try to see the very first logging message, I have a date, time details and from which class
[05:31] this logging statement is happening and from which method and what is the level and what is the message.
[05:37] The same applies for the next message as well.
[05:40] So these kind of statements will help you inside your real production applications as well.
[05:45] Since you have that time and date as well, you can easily identify when this particular issue happened
[05:51] or when this particular statement is printed.
[05:54] Whereas if I try to print the same kind of statement with the help of System.out.println(),
[06:00] you will not be able to see all the details that we are getting with the help of logging framework.
[06:05] You can see I'm simply getting a message, but it is not giving me any other details like what is the
[06:11] class name?
[06:12] What is the method name?
[06:13] Where this logging happened?
[06:14] What is the time?
[06:15] What is the date?
[06:16] So all such details are going to be missed whenever you are using System.out.println().
[06:21] I hope you are clear why we should use the logging.
[06:24] So this is just a introduction to the logging inside Java.
[06:28] Let's try to discuss more details about logging in the next lecture as well,
[06:32] thank you
[06:33] bye.

----------------------------------------
