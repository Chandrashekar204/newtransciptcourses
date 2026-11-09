# 8.14 — Deep dive on while statement - Demo

> Section 8: Control flow statements in Java

[00:00] Inside section8 Java project, I'm going to create a new Java class, and the class name is going
[00:06] to be WhileStatementDemo.
[00:09] Inside this class
[00:10] first we need to create main() method.
[00:13] Now think like I have a requirement to print the numbers from 1 to 10.
[00:19] If I don't use any of the looping logic, I will end up writing System.out.println() like this
[00:26] multiple times.
[00:28] After writing these statements multiple times, I need to update with the different numbers like one,
[00:34] two, three, four, five, six, seven, eight, nine, ten.
[00:37] So if you see here my code is going to be duplicated a lot.
[00:41] The only logic which is going to change inside my Java code is this int value.
[00:48] So printing up to ten numbers may look fine to some extent, but if someone asks you to print up to
[00:53] 100 number or 1000 number, then mentioning that System.out.println() 100 times or 1000 times is going
[01:01] to look very clumsy and cumbersome.
[01:03] So to overcome these kind of challenges, only we have loops inside Java programming.
[01:09] The very first approach that we can use to build the loops is while statement.
[01:13] So how to build the while statement.
[01:15] So first we need to declare an int variable.
[01:19] The variable name I'm going to give as i.
[01:21] And to this I'm going to assign a value one post that I'm going to mention while keyword followed by
[01:28] parentheses and after the parentheses I can mention the curly braces. You can see without the boolean
[01:36] expression
[01:36] I'm going to get an compilation error saying that expression is expected always inside the while statement.
[01:43] So let me write the expression here.
[01:46] I want to check always before trying to execute my while statement, which is i <= 10.
[01:53] .
[01:53] With this, as soon as my I becomes 11, the while statement execution is going to be stopped.
[02:00] So inside my while loop I'm going to write a System.out.println() using which I'm going to print
[02:07] the i value.
[02:08] So my while loop execution is going to be started when the i value is one, that means first I'm going
[02:14] to have a value one printed on my console.
[02:17] Post that inside the while loop itself, I need to update the I value based upon my business requirements.
[02:24] For example, here I can mention i++.
[02:27] That means after the execution of my while statement, every time I want to increment my i value.
[02:34] Otherwise if I don't have this i++ inside my while statement, my loop is going to be run continuously
[02:42] because we are never changing the value of i.
[02:45] I can also show you this very quickly.
[02:47] Let me try to execute this program and you'll be able to see that the value of one is being printed
[02:54] continuously on my console.
[02:56] So that's why whenever you are trying to build a while statement, please make sure you are altering
[03:02] your initial condition expression inside your while loop based upon your business requirements.
[03:09] Otherwise, your while loop is going to run continuously like an infinite loop.
[03:14] So let me bring back i++ here.
[03:17] So now I'll try to execute my program.
[03:19] But before that let me keep a breakpoint inside my while statement.
[03:23] So if I try to execute my program, you can see the program stopped very first time with the value i
[03:30] is equal to one.
[03:31] So at this point of time the value is one.
[03:34] That's why my condition became true.
[03:36] Since it is true the while statement is executed.
[03:39] Now if I try to release a breakpoint next time you can see the while statement execution right now is
[03:44] happening with the i value two.
[03:46] So if I keep trying to skip this breakpoint the next time, it is going to stop with the i value three,
[03:51] four, five, six, seven, eight, nine and ten after the value become ten.
[03:59] If I try to debug my program line by line, by using this f8, you can see
[04:04] now after executing this Java statement, the i value is going to become 11.
[04:08] With that, the expression that I have written inside my while statement is going to become false,
[04:13] and eventually the execution of the while statement is going to be stopped.
[04:17] That's why you can see now the program stopped at line number 12, because this entire execution of
[04:23] the while statement is completed.
[04:25] Now, if you go and check inside the console, you will be able to see the numbers like one, two,
[04:30] three, four, five, six, seven, eight, nine, ten.
[04:32] I hope you are clear with the syntax of while statement.
[04:35] As a next step, let me show you how to build an infinite loop.
[04:39] We already saw how to build an infinite loop inside the previous example.
[04:44] If you try to remove this i++, which means if you're not updating your initial I value, then
[04:49] your while statement is going to execute continuously.
[04:53] Otherwise, we can also follow one more simplest approach, which is we can simply mention while
[05:00] true and inside the while statement, we can write any logic like printing out a statement, which is
[05:06] I can print infinitely.
[05:09] So this is the statement which is going to be printed infinitely, because I'm never changing the boolean
[05:15] value, it is always going to be true.
[05:17] And with that, my while statement is going to be executed continuously.
[05:21] So let me remove this breakpoint and run the program in a debug mode.
[05:25] And you can see we are having a statement continuously being printed on the console.
[05:31] And this is because the while statement is running infinitely inside your real projects
[05:36] always make sure you are not building the infinite loops.
[05:40] If you try to build the infinite loops, then the program is going to run continuously and with that
[05:46] you may do a damage to your application.
[05:49] I hope you are clear about the while statement.
[05:52] Let me close this lecture on a fun note.
[05:54] You can see inside this image we are having an infinite loop, so the cats are going to keep on looking
[06:00] for each of them continuously.
[06:03] So this is a funny representation of infinite loop.
[06:06] I hope you like this.
[06:07] And similarly I also have another image if you try to read this message, which was written by a husband
[06:15] or boyfriend to his girlfriend or a wife.
[06:17] So the statement is babe just went to the bar with the guys for a couple of hours.
[06:23] If I am not back in a couple of hours, read this note again love.
[06:28] So you can see this is a representation of a while statement in a funny way.
[06:32] Don't do this at your home.
[06:34] Your partner may not like it.
[06:36] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
