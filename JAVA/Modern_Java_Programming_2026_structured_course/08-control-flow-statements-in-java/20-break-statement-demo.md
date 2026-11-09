# 8.20 — break statement - Demo

> Section 8: Control flow statements in Java

[00:00] To show you the demo of Break statement
[00:02] first I'm going to create a Java class.
[00:05] The class name is going to be BreakStatementDemo.
[00:11] Inside this class
[00:12] first we need to create the main() method and after the main() method I'm going to write a for loop.
[00:18] This
[00:19] for loop it is going to print the first ten numbers right from 0 to 9.
[00:24] So let me try to define the initialization logic as int i = 0.
[00:30] Post that the condition as I < 10, followed by i++.
[00:36] And inside the curly braces I'm going to print the i value.
[00:40] So if I try to execute this program, obviously you can see I'm going to get the output right from 0
[00:46] to 9.
[00:46] Now I'm going to define a condition inside my for loop with the help of if statement,
[00:53] whenever my i value becomes five, I want to exit from this for loop.
[00:58] So how to achieve this with the help of break statement.
[01:02] So let me try to mention the condition
[01:04] first i = = 5.
[01:07] And inside the if statement I'm going to mention the break.
[01:10] And with this, if I try to execute this program this time, you will be able to see only up to four
[01:16] as an output.
[01:18] The reason is the remaining iterations we didn't execute because we have a break statement based upon
[01:26] the condition that we have defined.
[01:27] I know this may look very simple.
[01:29] As a next step, let me define one more for loop, where I'm going to show you the real power of break
[01:36] statement. For the same,
[01:37] first, I'm going to create an int [].
[01:40] I know where to discuss about arrays, but I'll take some luxury here to define an int [], and
[01:47] I'll make sure I'm explaining you everything.
[01:49] If something is not clear, don't worry
[01:51] try to grasp whatever you can understand.
[01:54] When we discuss more details about array, then it is going to make more sense to you.
[01:59] So first, to define an array, first we need to mention two square brackets after the int followed
[02:05] by we need to give a name to the array of ints.
[02:09] So I'll just mention arrayOfInt.
[02:12] So this is a name and how we can store multiple numbers inside an arrayOfInt.
[02:17] First we need to mention the curly braces followed by semicolon.
[02:21] Inside these curly braces I am going to mention some random numbers
[02:25] like you can see I'm trying to type whatever I want.
[02:29] As of now you can see I have five different numbers. In real projects,
[02:33] sometimes you may have more than 1000 numbers or 1000 elements inside your array.
[02:38] If you are trying to look for a specific number array for a specific element inside your array, you
[02:43] can achieve the same with the help of for loop.
[02:46] So how to do that.
[02:47] So first we need to write for loop with the curly braces.
[02:50] So once you have defined the for loop I'm going to mention int i = 0 because the first
[02:57] element inside array is always going to start from the index zero.
[03:02] Post that I'll mention i<.arrayOfInt.length.
[03:08] Whenever I invoke this length parameter available against an array, it is going to give me the total
[03:15] length of the array.
[03:16] So what is the length of the array
[03:17] in this case, it is going to be five since we have five elements.
[03:21] So since we are starting the index from zero, we are going to have total for index like 01234.
[03:29] That's why I'm trying to mention the condition as I < 5 post that I'll try to mention increment
[03:36] operator.
[03:37] Now as a next step,
[03:38] first I need to decide which number I want to search.
[03:41] Think like I'm looking to search for the number for 455.
[03:46] So that's why here I'm going to mention int lookingFor is a name is equal to four five, five and post
[03:54] that,
[03:55] I'm also going to create a boolean variable which is isFound.
[03:59] And by default I'll make it as false.
[04:01] Now using these two variables I'm going to build a logic inside my for loop.
[04:05] The logic that I'm going to write is with the help of if statement, I am going to search for,
[04:11] If the element inside an array based upon the current index is same as the number which I'm looking
[04:16] for.
[04:17] So how to get an element or number from the array based upon the index?
[04:21] First we need to mention the array name followed by square brackets and inside the square brackets
[04:27] you can mention the index number since we are holding the index number with the help of i variable,
[04:33] I'm going to mention the same, followed by
[04:35] I'm going to compare it with the looking for variable.
[04:40] If this is true, then I'm going to update the isFound as true and post that
[04:46] I'm going to break the statement as well.
[04:49] With this, whenever a match is found, I'm going to immediately breaking out of the for loop so that
[04:55] I don't have to look for other numbers inside my array of numbers.
[05:00] So based upon this boolean, I can write an logic outside of my for loop
[05:04] like if isFound is true,
[05:07] I'm going to print out a statement which is, Hurray number is found, whereas if I don't have the given number
[05:16] inside my array of elements, I'm going to print out the statement which is Oops number is not found.
[05:25] I hope this is clear.
[05:26] Now if I try to execute this program, you'll be able to see that I'm getting an output which is Hurray
[05:32] number is found.
[05:33] So with the help of break statement we're trying to achieve some performance.
[05:38] If I don't have this break statement, even though my logic found the element at the first index itself,
[05:44] it is still going to look for the other indexes as well, which is unnecessary, and introduce performance
[05:51] issues.
[05:51] You may face these kind of scenarios inside your real projects as well.
[05:55] Maybe you may have a collection of person objects.
[05:59] So from the collection of person objects, you might be looking for a specific person.
[06:03] In all such scenarios, you can write your business logic to identify the person inside your for loop.
[06:08] As soon as you identify the person, you can use the break statement to come out of the for loop.
[06:13] I hope this is clear.
[06:14] As of now we are using the unlabeled break statement and this kind of break statement you can use in
[06:21] the scenarios only when you have a single for loop, but sometimes you may build a nested for loops
[06:27] and from the inner for loop, you may want to break the outer for loop as well.
[06:32] So for these kind of scenarios we have labeled the break statements.
[06:36] So let me show you very quickly how to do that.
[06:39] So first I'm going to mention the label as outer for loop followed by I'm going to mention colon
[06:46] and behind this label I'm going to write my for loop.
[06:50] So here I'm going to mention a condition which is int i is equal to one and post that i <5,
[06:58] followed by i++.
[07:01] And after this outer for loop I'm also going to write one more inner for loop.
[07:05] So first let me create the inner for loop.
[07:09] And on top of this I can put a label which is inner for loop followed by colon.
[07:16] For this inner for loop I'm going to define the conditions which are like int j is equal to one, followed
[07:23] by j < 3, followed by j++.
[07:28] After defining the conditions for my inner for loop, I'm going to write a small logic inside my inner
[07:33] for loop, the logic is to print out a statement which is,
[07:38] first, I'll try to print out what is the i value by appending the i variable from the outer statement,
[07:45] followed by,
[07:46] I'm also going to print the j value also.
[07:50] But before that let me mention and j = and what is the j value.
[07:56] So if I try to simply execute this for loop I'm going to get output like this.
[08:01] You can see enter my outer for loop and inner for loop is executed.
[08:05] But this time I'm going to write an condition inside my inner for loop with the help of if statement.
[08:12] The condition is if i is equal to is equal to three,
[08:17] I want to break the outer for loop.
[08:20] So how to break the outer for loop?
[08:21] You just have to mention the label which is outer for loop.
[08:25] So this time if I try to execute, the output is going to change based upon our logic.
[08:30] For example, I can also try to break the inner for loop by just mentioning the inner for loop.
[08:36] I don't even have to mention these inner for loop, because if I simply mention the break statement
[08:41] anyway, it is going to do the breaking of the inner for loop only.
[08:45] That's why using the labeled break statements to break the inner for loop is not needed.
[08:50] But still, let's try to execute this program and this time you can see the output is changed again.
[08:55] I hope this is clear.
[08:57] Let me revert back to the outer for loop.
[08:59] So please refer to this class if you have any questions.
[09:03] My sincere request is to execute all these examples inside your IntelliJ as well, so that you will
[09:09] get used to the syntax of the break statement.
[09:12] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
