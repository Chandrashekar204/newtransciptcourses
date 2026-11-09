# 29.3 — [JAVA 22] Unnamed Variables & Patterns - Theory

> Section 29: New features from Java 22, Java 23 and Java 24

[00:00] Java 22 released a new feature with the name Unnamed Variables and Patterns.
[00:07] Inside this video, let's try to explore what is this new feature, why it has been introduced, and
[00:13] under which scenarios we need to use this new enhancement.
[00:17] Many times inside our Java code, we end up writing lot many unused local variables, and deleting these
[00:25] unused local variables may not be an option, because we will have some tricky scenarios where we can't
[00:33] delete these unused variables from our code just because Java syntax forcing us defining them.
[00:39] Or there might be some dependency on these unused variables inside our business logic as a side effect.
[00:45] So in these kind of scenarios where deleting an unused variable is not an option, we can simply use
[00:52] the unnamed variable so your unused variable name can be anything.
[00:56] The name can be replaced with underscore symbol.
[01:00] So that's a simple purpose or explanation about these unnamed variables.
[01:04] So what do we get by using these unnamed variables and patterns?
[01:08] Developers know more
[01:09] they have to worry about giving some names to the unused variables
[01:13] many times we scratch our head what name we should give to these unused variable name.
[01:18] Can I give temp or I can give some x or y.
[01:21] So these kind of thought process we don't have to go because all these unused variable names which we
[01:27] can't delete can be replaced with an unnamed variable which is underscore.
[01:32] On top of that we also have one more advantage, which is many times IDE's like IntelliJ or eclipse and
[01:39] static code analysis
[01:40] like sonar cube, they will always complain about there is an unused variable inside our code, but
[01:46] we know we can't delete them because there are some tricky scenarios which we are going to discuss in
[01:51] few minutes.
[01:52] So all these false positive alarms by the IDE's and sonar cube can be resolved with the help of unnamed
[01:59] variable.
[02:00] So whenever we are using unnamed variable, we are indirectly telling to IDE's and static code analyzer
[02:05] saying that I know it is an unused variable, but I have some dependency on it, or I have to declare
[02:11] it just because Java syntax expects that.
[02:14] So this kind of communication we we can give to the tools so that they no more going to throw any warnings.
[02:20] So on a high level, if someone asks you what is an unnamed value and pattern, just tell them it is
[02:25] introduced as part of Java 22.
[02:27] All the unused local variable names and pattern variable names can be replaced with a symbol called
[02:33] underscore.
[02:34] So these are simplest definition that you can give.
[02:36] But it is important to note that that these unnamed variables and patterns cannot be applied to the
[02:42] instance fields or class level fields, like static fields or instance fields that you are going to
[02:48] create inside your class body.
[02:50] On top of that, these unnamed variables cannot be passed to the methods.
[02:55] So these are the limitations
[02:56] I know you may have million dollar question, which is what are the scenarios where we can use these
[03:01] unnamed variables?
[03:02] What are those tricky scenarios where I can't delete an unused variable.
[03:06] So so these kind of questions might be running behind the scenes.
[03:09] So let's try to answer those.
[03:11] You can see here I have a static method.
[03:14] The purpose of this method is it is going to count the number of words available inside the input that
[03:20] it has received in the form of iterable.
[03:23] You can see here
[03:23] inside this method we have a for loop.
[03:26] Here we're just iterating the words and this word which is a temporary variable.
[03:32] It is unused variable.
[03:33] We are nowhere using inside our business logic.
[03:36] Does that mean we can delete this word?
[03:38] Off course we can't delete because Java expert to define a variable name as a syntax.
[03:44] So in these kind of scenarios we can simply leverage the unnamed variable.
[03:48] Like you can see here,
[03:50] I rewrite the same method with the unnamed variable just in the place of word.
[03:54] I'm trying to use a underscore.
[03:56] With this, I will be able to clearly communicate to the other developers that there is a unused variable
[04:02] inside my code
[04:03] don't delete that because I have some dependency inside my code, and it is also an indication to my
[04:09] IDE and sonar cube to not throw any warning on the unused variable.
[04:14] I hope this is clear to you in the next lecture.
[04:17] Let me try to explain more about these new enhancement.
[04:20] By taking some examples.
[04:22] We can write some code and we can see this enhancement in action.
[04:25] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
