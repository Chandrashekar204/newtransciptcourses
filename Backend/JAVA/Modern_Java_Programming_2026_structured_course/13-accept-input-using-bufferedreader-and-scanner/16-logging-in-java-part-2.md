# 13.16 — Logging in Java - Part 2

> Section 13: Accept input using BufferedReader and Scanner

[00:00] I will try to update this program further by adding more logging statements.
[00:05] So as of now we are only logging the INFO related statements.
[00:09] Maybe what I can do is, I can try to update these level two WARNING, and at the same time, I'm going
[00:15] to update this statement saying that This is warning level logging.
[00:20] And after that inside the System.out.println(), I can have some other message.
[00:25] Maybe I can say hello using System.out.println().
[00:33] So this is a statement that I want to print with the help of this System.out.println().
[00:37] In the similar lines, I'm also going to add one more level logger statement with the help of Logger
[00:44] object.
[00:45] This time I want to use SEVERE.
[00:47] If I use the severe() method that gives a confirmation to the logging framework that I'm trying to log the
[00:54] statement with the SEVERE level, so I can directly mention what is my logging statement here, I can say
[01:01] this is SEVERE level logging.
[01:05] So now I'll try to execute this program.
[01:08] And this time you can see first I have info level logging followed by warning level logging and severe
[01:14] level logging.
[01:14] And at last I have statement saying that hello using System.out.println().
[01:19] So like I said before, most of the times developers they will end up using these levels like info, warning
[01:27] and severe usually inside production applications developers, they will write lot of information related
[01:34] statements like with the help of info, they will write log of logging statements saying that now the
[01:41] execution has reached to this point.
[01:43] At this point of time, I have this kind of data.
[01:46] So this kind of information messages, they'll try to log a lot, which is going to help them to debug
[01:52] that defect or any bug that they may face in future.
[01:56] And similarly, whenever they are trying to deal with a warning related scenario where it may not be
[02:01] super critical and at the same time it should not be neglected in such kind of scenarios, they're going
[02:06] to log a message with a warning level, but if the severity is too high, they will go with the severe
[02:12] level inside testing environment or inside local environment.
[02:16] They will enable the entire logging so that they can see what is happening.
[02:20] With the help of info statements, they can see what is happening with the help of warning statements
[02:25] and the severe statements.
[02:27] But this kind of info statements may not be needed inside the production environment
[02:32] if you try to log too much of details inside the production environment, it may bring some performance
[02:38] issue.
[02:39] So if needed developers they can disable these info logging without deleting this code.
[02:44] So how to do that?
[02:46] It's very simple.
[02:47] Using the Logger object we need to invoke the method which is setLevel(), and to this setLevel() method,
[02:54] we need to tell what is the level that logging has to consider to perform the logging.
[03:01] So for now I'm going to mention level as warning.
[03:05] So if I mention the level as warning to the setLevel() method, the logging framework is going to log
[03:11] only the warning related log statements and the severe related logging statements.
[03:17] So any level which is above the warning will also be enabled.
[03:21] So if you go and check inside the level class warning has a value 900 whereas severe has a value 1000.
[03:28] If you are setting the level as warning, that means the logs with the level warning and severe both
[03:34] of them will be printed.
[03:35] So let me go to this class and let me execute this program.
[03:38] You can see right now I have only warning and severe related logging.
[03:43] I don't have any statements related to the info logging because I disabled it by setting the minimum
[03:50] level as warning, whereas you can see the statement which you are trying to print with the help of
[03:54] System.out.println()
[03:56] we are not able to control it.
[03:57] If you don't want this to be printed, the only option is you need to remove this entire code.
[04:03] But with the logging framework, I'm able to not print the statement by disabling the info logging.
[04:10] This time I'll try to mention the level as info, and with this, all the logging along with the info
[04:18] and above the info level will be considered for the logging.
[04:22] So now if I try to execute this program, all the logging statements is going to be printed like info
[04:28] level, warning level and the severe level.
[04:30] This time let's try to mention the level as severe.
[04:33] So severe is a top level above severe
[04:36] we don't have any other level.
[04:37] That means whenever you are setting the level as severe, only the severe level statements are going
[04:44] to be logged.
[04:44] So let me execute this program.
[04:46] And this time you can see we only have severe level logging but not warning level and info level.
[04:52] This way logging is always going to provide you some flexibility to enable or disable the logging
[05:00] based upon the requirements of developers.
[05:02] I hope you are clear about the logging.
[05:04] So the important takeaway from this lecture is please never use the System.out.println() inside real project
[05:12] applications.
[05:12] You can use them very happily while you are trying to learn java, or while you are trying to test a
[05:17] java application, or while you are trying to debug the java application.
[05:21] But never ever try to push the code that has System.out.println() into the production environment.
[05:29] Everything that we discussed around the logging I have mentioned in this slide for your reference.
[05:34] So there are seven logging levels inside java.logging package.
[05:40] So always use SEVERE to represent a message with highest severity followed by warning, info, config
[05:47] fine, finer or finest.
[05:49] So the finest is going to have lowest severity by default
[05:52] if you are not mentioning any level, the logging framework is going to consider the info as a default
[05:58] level.
[05:58] I also attached a sample code snippet for your reference.
[06:02] Thank you and I'll catch you in the next lecture bye.


########################################
