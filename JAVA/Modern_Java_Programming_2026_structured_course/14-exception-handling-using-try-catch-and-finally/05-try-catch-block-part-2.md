# 14.5 — try-catch block - Part 2

> Section 14: Exception handling using try, catch and finally

[00:00] Let's try to implement try and a catch block inside the ArrayIndexOutOfBoundsExceptionDemo class
[00:07] as well.
[00:08] I want you to pass this video and try by yourself.
[00:11] It is going to be super easy.
[00:13] Otherwise you can simply follow my discussion.
[00:16] The very first step that we need to do is we need to define a try block.
[00:20] And into this try block, we need to move all our code which we feel it is a risky code post that we
[00:27] need to define a catch block.
[00:29] And inside the catch block I'm going to handle the exception which is ArrayIndexOutOfBoundsException
[00:37] .
[00:38] So please type ArrayIndexOutOfBoundException.
[00:42] All the exceptions
[00:44] they are present inside the java.lang package.
[00:47] So that's why we don't have to add the import statement
[00:50] specifically I'm selecting the first class here.
[00:52] And I'm giving a object reference name which is ex post that inside the catch block I can write a
[00:59] System.out.println() with a message Invalid Array Index followed by,
[01:06] Please try again with a valid index number.
[01:13] So this is the message that I want to show to the end user.
[01:16] Whenever an exception happens due to an ArrayIndexOutOfBoundsException inside my class.
[01:22] So let's see the demo of this code.
[01:24] I'm executing the program in a debug mode, and you can see we are getting the message which is invalid
[01:31] array index,
[01:32] Please try again with a valid index number. instead of having this
[01:36] System.out.println().
[01:38] Maybe we can have logger statement as well.
[01:40] Let me show you that very quickly how to have a logger statement inside the catch block.
[01:45] First we need to mention private static logger.
[01:49] Logger is a class which is available inside the java.util.logging.
[01:53] So let me select the same post that I'm going to give a name to this Logger.
[01:58] Static variable followed by I'm going to invoke Logger.getLogger() followed by what is our class
[02:06] name.
[02:06] So this is the class name.
[02:08] So let me copy the same using the same class name I need to invoke class followed by getName().
[02:14] Now my logger object is ready.
[02:16] Using the same Logger object, I can simply invoke the method, which is severe() because getting an runtime
[02:24] exception is a very critical scenario.
[02:27] I want to have a logger statement with a highest severity, so that's why I'm trying to use a SEVERE
[02:33] level to log my statement.
[02:35] And to this method I can simply pass this value which is, Invalid Array Index,
[02:42] Please try again with a valid index number.
[02:46] So this time if you try to execute this program, the logger statement is going to look like more professional
[02:52] along with the date time, the class name, the method name, and the log level.
[02:57] We are going to get complete details inside your logger statement.
[03:01] I hope this makes sense to you.
[03:03] Regardless of whether you are using System.out.println() or logger statement, the logic that you are
[03:08] going to write with the help of try and catch block is going to be same.
[03:12] The next point that I want to highlight here is as of now, you can see we are trying to handle a specific
[03:18] type of exception like ArrayIndexOutofBoundsException are InputMismatchException.
[03:24] So with this what is going to happen is this catch block is going to be executed only if these exception
[03:31] occurs inside your Java code.
[03:33] If you want to write a generic catch block which is going to handle all type of runtime exceptions inside
[03:40] your Java code, you can simply replace these ArrayIndexOutofBoundException with Exception.
[03:46] So Exception is a class available inside the java.lang package.
[03:50] All the exceptions that we have inside the Java, they are going to have these exception as a super
[03:56] class.
[03:56] That's why instead of a specific exception, we can also mention these generic exception.
[04:01] And with that the behavior is not going to change.
[04:04] And your Java program can handle any kind of exception regardless of whatever exception your program
[04:11] is going to throw.
[04:12] The same catch block is going to handle all type of exceptions.
[04:16] Let me execute this program one more time and show you a demo that the behavior is not going to change.
[04:22] You can see the behavior is not changing.
[04:24] We are getting the same kind of behavior.
[04:26] So after seeing these exception, my end user, he will understand that he's trying to access an invalid
[04:33] index.
[04:34] With that, if we try to correct this index number to four, the program is going to work in a proper
[04:40] way.
[04:40] I hope you are clear.
[04:42] Let me revert back to five so that it is going to have as a reference for you, the two examples that
[04:47] we have discussed, I have mentioned inside this slide for your reference, along with the other details,
[04:53] please refer these slides at the code present inside the GitHub repo for any questions.
[04:58] Thank you and I'll catch you in the next lecture,
[05:00] bye.

----------------------------------------
