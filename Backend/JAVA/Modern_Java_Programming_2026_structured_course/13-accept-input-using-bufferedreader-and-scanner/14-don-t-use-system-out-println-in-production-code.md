# 13.14 — Don’t use System.out.println in Production code

> Section 13: Accept input using BufferedReader and Scanner

[00:00] As of now, we discussed a lot of concepts and topics inside Java.
[00:05] With all the knowledge that we have gained so far by this time, you might have became a fan to the
[00:10] System.out.println(), and you may have intentions to use this a lot inside your real projects as well.
[00:18] But I want you to stop there and I want to give you a cautious note here, which is it is not recommended
[00:24] to use the System.out.println() or any other print methods inside production code.
[00:31] What is the meaning of production code?
[00:33] Whenever you are building the Java logic or any code for a real application which will be deployed eventually
[00:40] into your production environment in the form of website or in the form of mobile application, or in
[00:45] the form of a API service.
[00:47] Regardless of how your code is deployed, it is always considered as a production code because your
[00:54] code is going to be served to the actual end users.
[00:58] So in all these kind of production related scenarios, we are not allowed to use a System.out,.println().
[01:05] We should only use this during learning Java, or whenever you are trying to debug your code, or whenever
[01:11] you are trying to test your code.
[01:13] In those scenarios only we are supposed to use this, but not in the production code.
[01:17] With that definitely you might have surprised and you may have questions.
[01:23] Why should I not use a System.out.println() ?
[01:26] Let me try to explain what are the drawbacks that we have.
[01:29] If we use the System.out dot.println(), your compiler is not going to stop you.
[01:34] You can always mention System.out.println().
[01:37] In fact, even today there are many developers who use these System.out.println() unknowingly inside their
[01:44] production code.
[01:45] But inside the projects where a strong review process is established.
[01:50] In this kind of projects, the lead or the senior developer who is trying to perform a code review of
[01:56] a junior developer if he sees this System.out.println().
[01:59] Which is trying to get pushed into the production code in such scenarios, they will definitely blame
[02:04] you and they will give a code review comment saying that remove these System.out.println().
[02:10] So I don't want you to be into that embarrassing situations.
[02:14] That's why let's try to understand why we should not use them and what are the alternatives that we
[02:19] have.
[02:19] The very first drawback using System.out.println() is, performance degradation.
[02:25] If you write a small program with the System.out.println() are two different places, nothing is going
[02:31] to happen.
[02:32] It is not going to impact your application in any way, but in real projects there will be thousands
[02:38] of classes and inside these thousands of classes, there will be millions of lines of code in all these
[02:44] millions of lines of code.
[02:45] If each developer end up using System.out.println(), wherever he wants will be, end up having thousands
[02:52] of System.out.println() statements.
[02:54] And with that, it is going to have a performance degradation problem inside your application, especially
[03:00] while we are trying to print the a large message.
[03:04] Why there will be a performance degradation.
[03:06] Because whenever you want to print a big message onto your console like we discussed previously, first
[03:12] it has to get an object of PrintStream.
[03:16] So when this object of PrintStream is getting created, a connection to your console will be opened
[03:22] behind the scenes.
[03:22] And with that connection, only the message will be printed onto the console.
[03:26] And at last, the connection with the console, which is established by the PrintStream object, has
[03:31] to be closed behind the scenes, since these kind of operations are happening behind the scenes, so
[03:37] there is a good chance that a performance degradation can happen.
[03:41] The second disadvantage is lack of flexibility.
[03:44] Whenever you are trying to print a message to the console, you will have very limited control on how
[03:50] you can format your message.
[03:53] Especially you can't add the details like under which method, under which class the printing of the
[03:58] statement happened, at which point of time, and using which thread.
[04:02] So all these kind of information you will not be able to print with the help of System.out.println()
[04:09] statements.
[04:10] Believe me, in real projects the logging requirements are even more complex.
[04:15] When I say logging.
[04:16] What is the meaning of logging?
[04:18] Logging is the process of printing a value onto the console or onto a file, which we can use at later
[04:26] point of time to debug what happened inside our program.
[04:30] So in real projects, the logging requirements are going to be super complex.
[04:34] All such complex requirements can't be achieved with the help of System.out.println().
[04:40] And the third disadvantage is inability to disable logging.
[04:44] When I try to print a message with the help of System.out.println(), there is no way for me to disable
[04:51] that printing other than deleting the entire line of System.out.println().
[04:57] Whereas with the alternatives that we are going.
[05:00] To discuss in the coming lectures.
[05:02] They're going to provide you an ability to disable your logging if it is on.
[05:07] The logging is going to happen if it is off.
[05:10] In such scenarios, the logging is not going to happen.
[05:13] So it is a kind of having a control to disable the logging whenever you want.
[05:18] Whereas with System.out.println() we will not have any such control
[05:22] always
[05:22] the only option to disable the logging with the help of System.out.println() is to delete the code itself
[05:29] and at last using the System.out.println() will have some security risks, especially if you try
[05:35] to log the sensitive information such as passwords, personal data, health data.
[05:41] So all these details
[05:42] if you try to print into the console, it can pose a security risk as anyone who has access to your
[05:49] console can see the information.
[05:51] So using System.out.println(), we can only log the output into the console.
[05:57] So anyone who has access to the server where it is deployed, they will be able to easily see the sensitive
[06:03] information that is logged.
[06:04] So with all these we should always not use the System.out.println() inside production code.
[06:11] Instead we should look for the advanced options.
[06:14] So what are these advanced options?
[06:16] We should use the logging frameworks.
[06:19] So what is a framework?
[06:20] A framework is a project or a library which is focused to solve a given problem with less effort.
[06:28] So to overcome all the drawbacks of System.out.println(), there are good amount of logging frameworks
[06:33] available inside the Java ecosystem.
[06:35] The Java library itself.
[06:37] It has a package with the name java.util.logging.
[06:41] Inside this package we have logging related classes which we can use to perform the logging, and apart
[06:47] from these basic support of logging from the Java, we also have dedicated logging frameworks like
[06:54] Log4j, SLF4J.
[06:56] So these are the most advanced logging frameworks.
[06:59] And they allow you to configure logging levels, log rotation, log aggregation and more.
[07:06] So what is logging levels?
[07:07] I'm going to discuss about logging levels in the coming lectures.
[07:11] Log rotation and log aggregation is a process where these frameworks, they will allow you to log your
[07:17] output data into a log file.
[07:20] So if you keep appending the log data to a single log file at some point of time, it can become
[07:26] 2GB, 5GB or 1TB text file and you will not be able to open such files.
[07:31] So that's why these frameworks to avoid these kind of challenges, they provide you log rotation and
[07:38] log aggregation.
[07:40] So whenever we are using these logging frameworks we can configure these frameworks such a way that
[07:45] every one hour or every five minutes you can create a new file.
[07:49] And the logging is going to happen in the new log file that got created.
[07:53] I'm not going to focus a lot about the logging frameworks inside this course, because these are super
[07:59] advanced topics
[08:00] and since right now we are focusing on the Java programming language, I'm just giving some hints around
[08:06] what are the best practices that you need to follow so that you can become a good developer inside your
[08:12] projects.
[08:13] Once you master Java, obviously, as a next step, you're going to learn frameworks like spring spring
[08:18] boot microservices.
[08:20] During your advanced journey inside the spring ecosystem, you should also learn one of the logging
[08:27] framework.
[08:27] For example, inside my Spring Spring Boot related course, I have discussed in detail about the logging
[08:34] framework, so when the time is apt, you can also learn this logging frameworks.
[08:39] For now, let's try to understand how to achieve the logging with the help of java.util logging library
[08:47] available inside JDK, so that we can avoid using the System.out.println() from now onwards, wherever
[08:54] is possible, we can use the logging.
[08:57] I hope you are clear
[08:58] thank you and I'll catch you in the next lecture bye.

----------------------------------------
