# 14.23 — Funny memes around exception handling

> Section 14: Exception handling using try, catch and finally

[00:00] We discussed everything about the exception handling by spending a good amount of time. As a tradition
[00:06] before we try to conclude this section, let me share you some funny memes around the exception handling
[00:13] so that it is going to be a relaxing for you.
[00:15] This is the very first meme that I have, so whenever you feel some dangerous or unsafe code that may
[00:23] break everything inside your Java program, you are simply going to fix it with the help of try and
[00:30] catch the same this meme is trying to convey.
[00:32] Moving on to the next meme.
[00:34] Here you can see some method are some try block.
[00:37] It is trying to throw lot many exceptions at you like IndexOutofBoundsException, NullPointerException,
[00:43] FileNotFoundException.
[00:45] It is throwing different types of exception at you.
[00:47] So you as a developer what you have done you have simply have a single catch block that is accepting
[00:56] exception which is a generic exception data type.
[00:59] So with this single exception catch block you are able to handle all of them with a breeze.
[01:04] So that is what happening here.
[01:06] So most of the developers they try to do this in their real programs as well.
[01:10] So regardless of whatever kinds of exceptions that your program may throw, your catch block is always
[01:16] going to be handle that.
[01:18] Let's go to the next meme.
[01:20] Here you can see someone is saying you don't have to worry about exceptions.
[01:24] All you have to do is, wrap all your code in a giant try catch block and leave the catch empty.
[01:31] Don't take this meme seriously.
[01:33] This meme is telling you just implement, try and catch, but don't write any handling logic inside
[01:39] catch block.
[01:39] You just leave the catch block empty.
[01:41] So it is recommending to implement try and catch just for namesake.
[01:45] But that is not the approach that we need to take inside production applications.
[01:50] So this is just a funny representation.
[01:52] The next meme we have is, you can see we have a try block inside the try block
[01:57] an exception may happen, but to handle these exception we have a catch block.
[02:02] So using catch block you might be catching a specific exception like NullPointerException or SQLException
[02:09] or ArrayIndexOutofBoundException.
[02:12] But if you see here there is an unhandled exception that may kill you or that may happen inside your
[02:19] program.
[02:19] So this is another funny representation I liked.
[02:22] The next meme that we have here is you can see try and catch blocks inside your code
[02:27] literally
[02:28] they are going to stop thousands of exceptions or errors that may happen at runtime so that you are
[02:34] beautiful
[02:35] code is going to execute without any issues at runtime.
[02:40] I hope you like this representation.
[02:41] Let's go to the next meme.
[02:43] On the packing of McDonnell, we have a message which is an error occurred attempting to read properties
[02:50] for the burger site text resource type so invalid class String and this is the error ID in ideal happy
[02:57] scenario
[02:57] what should happen is, the code should read a property or a String value
[03:01] and the same is going to be printed here.
[03:04] But unfortunately that didn't happen
[03:06] and someone write this logic inside the catch block like they have mentioned
[03:10] these exception details like an error occurred and at last
[03:12] they also mentioned what is the reason and the error id. Since this is the handling logic inside your
[03:18] catch block.
[03:19] The same is printed on this box, but I think leaving the catch block empty might have done more better
[03:25] job.
[03:26] Instead of printing these error messages, we should have print an empty message itself.
[03:31] But sometimes these things happen because runtime exceptions, they won't be in our control.
[03:36] That's why always do the proper testing before you try to deliver your code into production.
[03:42] Let's move to the next meme.
[03:43] So this is a very funny meme.
[03:45] So guys, she's trying to post her profile in a dating app.
[03:49] You can see she has written her requirements with the help of try and Catch.
[03:54] If Altura is less than 1.89, then only she's going to accept your dating request.
[04:02] Otherwise she's going to keep you in a friend zone.
[04:05] So what is Altura?
[04:06] Altura is a representation of your height.
[04:09] If your height is less than 1.89m, then this girl is not going to accept your dating request.
[04:17] I think this girl is a Java developer.
[04:19] She's trying to convey that with the help of this try and catch, let's move to the next meme.
[04:24] So this memes conveys languages like C++, C#
[04:28] they have very good support to the exception handling how they are going to perform the exception handling
[04:34] with the help of try catch throw.
[04:36] Whereas the C language which is the oldest language it is telling, the best I can do is null check.
[04:42] It is not going to handle any kind of runtime exceptions.
[04:45] There is no concept of try, catch and throw inside C.
[04:48] .
[04:49] Let's move to the next meme.
[04:51] The next meme says this is the kind of pressure that you will go through whenever you are trying to
[04:57] handle an exception inside your catch block.
[04:59] Sometimes you will have a confusion whether you want to throw this exception simply to the parent method,
[05:05] or you want to return null.
[05:07] So return null means you just want to execute the method without any handling logic.
[05:12] So this kind of procedure developers will always go through.
[05:16] But my advice is always go with your business requirements.
[05:20] Please ask your client or your senior developer what handling logic you want to write inside the catch
[05:25] block.
[05:26] The next meme we have is around the catch block.
[05:29] Think like your method is capable of throwing so many exceptions like FileNotFound, SQLException,
[05:35] NullPointerException.
[05:37] In an ideal world, the best recommendation is to have catch blocks handling all these exceptions,
[05:42] but few smart developers.
[05:44] They will have a single catch block with the generic exception data type.
[05:49] And with that they are going to kill three birds with a single stone.
[05:54] Let's move to the next meme.
[05:56] So this is the meme from Harry Potter.
[05:59] So we have three kinds of exceptions in the down like IndexOutofBounds, NullPointer and
[06:04] FileNotFound.
[06:05] The developer is asking these three different exceptions, saying that why is it when something happens
[06:11] it is always you three.
[06:13] So if anything happens inside my program, why you always three are going to be present.
[06:18] So this should also give a clue to you that these are the most commonly faced exceptions by that developers
[06:25] inside their programs.
[06:26] If you are a fan of Harry Potter, I'm assuming you like this meme.
[06:30] The next meme that we have is around the object reference name that we are going to give for the exception
[06:37] data type inside the catch block.
[06:38] Most of the times developers they'll go with the ex or simply e, so it is not mandatory
[06:44] but somehow all the developers in the world they used to the object reference names like ex and e.
[06:51] The funny part here is this person face is looking like e only.
[06:56] That's what they are trying to convey from this meme.
[06:58] Let me close this meme with that
[07:00] we can see the next meme that we have here.
[07:03] Few developers
[07:04] they don't like unhandled exceptions.
[07:06] That means they always like to handle the exceptions.
[07:09] But do you know what they are going to do inside the catch block?
[07:12] They're not going to do anything.
[07:14] They'll just write a catch block and inside the catch block, maybe they will invoke the print stack
[07:19] trace or maybe they will log the message.
[07:21] And sometimes people will simply have the catch block as empty.
[07:25] That's very dangerous.
[07:26] So don't be such kind of lazy developer.
[07:29] Moving on to the next meme, here we have a program you can see in the very first program, developer
[07:35] is trying to throw the IOException.
[07:38] He's not handling the exception.
[07:39] Few developers, they'll say, I don't like this approach, but if you see what they have done, they
[07:44] have removed the throws block and they have returned, try and catch from the catch block
[07:48] they are again throwing a runtime exception.
[07:50] Again, this is a very bad way of handling the exception.
[07:53] We should properly handle the exception instead of simply throwing the exception
[07:57] again, back to the caller method, we should try to perform some actions, like doing the logging or
[08:04] triggering an email to the support team.
[08:06] So such kind of things we need to handle as part of the catch block.
[08:11] According to me, there is no difference between these two methods.
[08:14] They are going to have the same behavior because inside the catch block, there is nothing that this
[08:19] developer is doing in terms of handling the exception.
[08:22] The next meme that we have is on the similar lines.
[08:25] Few developers,
[08:26] they don't like handling the exceptions.
[08:28] They'll always be lazy.
[08:29] They don't want to write, try and catch.
[08:31] They simply always want to add the throws keyword into the method signature, because that is the most
[08:37] easiest job of handling a checkered exception.
[08:40] We know whenever there is a checkered exception, the compiler is going to throw a compilation error.
[08:45] The ideal way is to write a try and catch block to handle the checkered exception, but we know some
[08:51] developers they'll be lazy and they don't like this approach, whereas the approach that they are going
[08:56] to like is by simply adding the throws keyword along with the exception.
[09:01] But like I said, this is not the recommended approach.
[09:04] Always try to handle your exceptions properly.
[09:07] Moving on to the last meme developers, they don't like having separate, separate catch blocks.
[09:14] This is the exception handling logic from other languages.
[09:18] This is not from Java because we don't see any catch block.
[09:22] We are seeing different syntax.
[09:23] But the funny message that this meme is conveying is developers they don't like always the ideal way,
[09:30] which is like handling the exceptions individually with their own handling logic.
[09:35] Instead, they always want to go with a generic exception.
[09:38] This is allowed to some extent whenever you have the same handling logic for all kinds of exception,
[09:44] but if you have a business requirement to handle different exceptions with a different business logic
[09:50] in such scenarios, the first approach is the ideal or the recommended approach.
[09:55] I hope you liked all the funny memes that we have discussed.
[09:58] I am concluding this section around the exception handling.
[10:02] Please take a break
[10:03] come back and I'm going to catch you in the next section bye.


########################################
