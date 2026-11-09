# 14.2 — Agenda of the section

> Section 14: Exception handling using try, catch and finally

[00:00] Life is full of surprises
[00:03] regardless of how carefully we are planning our life, sometimes it is going to do unexpected things.
[00:09] In similar lines, regardless of how carefully you are developing our programming, your Java programs,
[00:15] sometimes your programs may throw unexpected results due to an invalid input from an end user, are
[00:23] due to some network issue, or due to some system error, or due to some invalid input path are due
[00:30] to some invalid input values.
[00:32] So the reason can be anything but there is a good chance that your program may not work like you are
[00:38] expecting.
[00:39] So all these kind of situations, we call them as error scenarios or exception scenarios. Whenever we
[00:46] are writing a risky Java method.
[00:48] When I say risky Java method, this Java method may have lot many operations.
[00:52] Like for example, you're trying to read the data from a file.
[00:56] You should always think about both happy ending and not happy ending scenarios.
[01:01] Happy ending scenario is the file is properly present.
[01:05] Your Java program is able to open it, read it and close it.
[01:08] This is a happy path scenario.
[01:09] In this scenario, everyone is going to happy because your program executed like everyone expecting,
[01:16] whereas coming to the unhappy scenario, think like the file is not present in the mentioned path or
[01:23] mentioned folder.
[01:24] In such scenarios, obviously your code will throw an error or exception.
[01:29] So to handle these kind of unhappy scenarios, we should always build some safety mechanisms inside
[01:36] our Java program so that we are handling these kind of exception scenarios or error scenarios gracefully
[01:43] and accordingly we are acting on them.
[01:45] Safety measures is very common even in the real life scenario
[01:49] also.
[01:50] For example, whenever we are trying to perform some adventurous activities like bike racing or bungee
[01:56] jumping.
[01:57] So in all these kind of scenarios, we'll make sure there is some safety mechanism as safety measures
[02:02] have been taken, so that even in the unexpected scenario also, we are not going to get harmed a lot.
[02:09] I can also show you some videos around this.
[02:11] For example, you can see this person is doing the bungee jumping right now, and there are enough safety
[02:17] measures for him so that he won't get harmed even in the unexpected scenario.
[02:23] Very similarly, this person is doing bike racing or bike riding, so he has a proper helmet and there'll
[02:30] be a first aid kit as well along with him.
[02:33] So he's ready to face any kind of scenario.
[02:36] On the similar lines, you can see these persons, they are doing the cycling and they have a proper
[02:41] helmet, and they have taken enough safety measures so that even if they fall down, there won't be
[02:46] any injury, especially for their head.
[02:49] On the similar lines, while we are trying to drive our car, the very first safety measure that we
[02:54] are going to take care is, to have the seatbelt locked around us, so that even in an unexpected scenario,
[03:01] this seatbelt is going to protect us.
[03:03] Even the car manufacturers as well
[03:06] they will have some inbuilt safety mechanisms inside the car, like there'll be air balloons, which
[03:12] is going to help the passengers in an unexpected results.
[03:17] Just like how we are taking safety measures whenever we do some activity inside real life.
[03:22] In very similar lines, whenever you are writing a Java program, you need to make sure your code is
[03:28] always ready to handle any kind of situations.
[03:31] Especially the error situations are the exception situations.
[03:35] Here you may have a question which is I agree with you boss, but how do we know if a method is a risky
[03:40] and where do we develop the code to handle the exceptions or any risky situations?
[03:46] So you may have all these questions floating inside your brain.
[03:49] So don't worry.
[03:50] We're going to put a lot of efforts throughout this section to understand how to properly implement
[03:57] exception handling inside any Java program.
[04:00] I hope you are clear with the agenda of this section.
[04:03] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
