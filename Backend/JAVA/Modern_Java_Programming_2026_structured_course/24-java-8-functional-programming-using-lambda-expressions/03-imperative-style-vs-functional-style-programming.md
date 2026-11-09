# 24.3 — Imperative style vs functional style programming

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Based upon our previous lecture discussion, it should be pretty clear for you right now that from Java 8
[00:06] we have two styles of programming supported by Java.
[00:10] The old style or traditional style
[00:12] we call it as imperative style, whereas the new style that is introduced from Java 8 is functional
[00:19] style.
[00:19] Inside this lecture I'm going to explain about these two styles.
[00:23] What are the differences between them?
[00:24] To make it more clear about these two styles of programming, first, let me take a real life scenario.
[00:30] Imagine you are baking a cake.
[00:33] In this cake scenario, I'm going to explain you the process we are going to follow in the imperative
[00:38] style and the functional style.
[00:40] The very first style that we have is imperative style.
[00:43] We can also call this style as procedural programming.
[00:47] In this kind of scenario, you're going to act as a head chef and you're going to use step by step clear
[00:54] instructions to your assistance.
[00:57] These instructions are going to be pretty low level, which means you're going to provide each and every
[01:04] minute detail to your assistant, such as beat the eggs, pour batter, adjust to own temperature.
[01:12] So by following all these clear instructions, your assistance, they are going to bake a cake.
[01:17] So this style may look very simple and it may also look very intuitive.
[01:23] But if you closely observe, this style has some disadvantages, which is the errors may happen very
[01:29] easily in this kind of style.
[01:31] For example, think like either you might have forgot to give a clear instructions to your assistant
[01:36] or one of your assistant.
[01:38] He might have misinterpreted your instructions.
[01:41] So in all these kind of scenarios, the taste of the cake is going to be affected very easily.
[01:47] Now let's try to imagine the same scenario using the functional style.
[01:52] In other words, we can also call this as functional programming.
[01:56] In this style, you're going to act as a recipe author describing the desired outcome and leaving the
[02:03] execution to the expert bakers.
[02:06] This time there won't be any assistance.
[02:08] Instead, you're going to have some experts who are good at baking the cakes. To these experts
[02:15] as a recipe author, you're going to give high level instructions saying that I want so and so cake
[02:21] with so and so taste with so and so
[02:23] weight.
[02:23] Apart from giving high level instructions inside this approach, you're also going to provide some already
[02:30] available ingredients like cream butter.
[02:33] So these expert bakers, they just have to use these already available ingredients.
[02:38] And by following the high level instructions they should be able to prepare the cake very easily.
[02:44] The advantage with this approach is since the ingredients are already available to the expert bakers,
[02:50] if they simply follow the high level instructions, the taste of the cake at the outcome of the cake
[02:56] is always going to be the same.
[02:58] I hope it makes sense to you.
[02:59] Now let's try to take these two styles of programming and try to understand how to build a Java logic
[03:06] with these two styles. Whenever we want to follow the imperative or traditional style inside Java,
[03:12] we need to provide the low level instructions to the compilers with the help of loops, variables,
[03:18] Java statements.
[03:20] Whereas if we follow the functional style of programming, we are going to leverage lambdas streams.
[03:25] So using these predefined ingredients like lambdas and streams, we are going to write any complex of
[03:32] code with no chance of errors.
[03:35] Let's take an Java example to understand more details about these imperative style and functional style.
[03:42] Imagine that I have a requirement to find the sum of squares of even numbers in a list.
[03:49] First, I'm going to show you how I'm going to implement a solution to my problem.
[03:55] So here you can see I have an list of numbers right from 1 to 10.
[04:00] So in these numbers first I need to identify the even numbers.
[04:04] Once I identify the even numbers, I need to calculate the square of the even number.
[04:10] And at last I need to sum all the squares of even numbers to get the desired output. For the same
[04:16] you can see
[04:17] first, I'm trying to create a variable post that I'm trying to manually iterate all the elements inside
[04:24] my list, using these for each block, inside this for each block, I have a logic to identify whether
[04:31] a number is a even number or not, with the help of these if block later on inside this if block, I'm
[04:37] trying to calculate the square of a given even number by multiplying itself two times and the same
[04:43] I'm trying to add to the variable which is sum of squares of events, and at last I'm trying to print
[04:50] it with the help of System.out.println().
[04:52] If you see inside this approach, we are giving each and every instruction to the compiler, since we
[04:59] are
[04:59] trying to provide low level instructions to the compiler
[05:03] the number of lines of code that we are going to write here is very high.
[05:07] On top of that, whenever you are following the imperative approach, there is a very good chance that
[05:11] you may end up introducing a defect inside your code.
[05:15] Think like you have not looped your elements properly, or think like you have not created the variables
[05:21] properly.
[05:22] So there can be thousands of things that can go wrong whenever you are dealing with the imperative style.
[05:27] Now let's try to understand how to implement a solution for the same problem using the functional style.
[05:34] In the functional style, you can see
[05:36] first I'm going to have the same numbers list which is formed with the help of Arrays.asList().
[05:42] So inside this we have ten different numbers right from 1 to 10.
[05:46] So here you can see I have a piece of code that I have written with the help of Lambda Expressions,
[05:53] which is going to help me to implement a solution using functional style of programming.
[05:58] So this code may not make sense for you right now because you are new to the functional style of programming
[06:04] or to the lambda expressions. But I'll try to explain it to you so that it is going to make at least
[06:10] some sense to you.
[06:11] But if something is not clear, don't worry
[06:13] when we discussed everything about the functional programming using Lambda expressions, it is going
[06:18] to be super, super clear for you.
[06:20] So here first from the list, we are trying to get a stream by invoking the stream() method.
[06:25] So inside java 8 there is a concept of stream introduced.
[06:29] Stream is nothing but a flow of data.
[06:31] So inside these stream I'm going to have all these numbers.
[06:35] So first requirement I have is to filter only the even numbers.
[06:39] That's why I'm trying to invoke one of the existing method which is filter().
[06:44] And to this I'm trying to pass a lambda expression.
[06:47] So for now don't try to understand what is this lambda expression and how it is going to work.
[06:51] But I'm assuming at least you are clear about this condition, where we are trying to evaluate if the
[06:57] given number is even number or not.
[06:59] So once this filtering is completed, we are trying to map each of the elements that we received from
[07:06] the filtering logic by multiplying itself two times, because as per our business requirement, we need
[07:12] to calculate the square of each even number.
[07:15] So once the square of the even numbers is calculated with the help of this lambda expression, and with
[07:20] the help of this mapToInt() method, at last we are invoking a sum() method.
[07:25] So this sum() method
[07:26] it is going to sum all the square of the even numbers and the output we are going to assign on the left
[07:32] hand side to this variable.
[07:34] So here, if you closely observe this functional style of programming I'm just giving high level instructions.
[07:39] Nowhere I'm trying to create the temporary variables.
[07:42] Nowhere I'm trying to perform the addition.
[07:45] So all these low level responsibilities I'm trying to assign to the expert API methods like filter(),
[07:51] mapToInt().
[07:52] So think like these methods are like expert bakers.
[07:55] And these lambda expressions are the ingredients that I'm trying to provide.
[08:00] So as long as the ingredients are same, the output always I'm going to get also is same.
[08:06] I hope you got some basic understanding about what is a functional style and imperative style.
[08:12] So with the imperative style though, the job is getting done, but it can feel a bit messy with all
[08:18] the low level details that we are trying to implement inside our code.
[08:22] It's not our fault since this approach is available from day one.
[08:26] We got used to write everything with the imperative style, but as a new advancements came into picture,
[08:33] java team realized that functional style of programming is very required for the Java programming language.
[08:38] That's why they have introduced inside Java 8 this functional style programming with the help of
[08:44] Lambda Expressions, Streams.
[08:46] So whenever we write the functional style of programming, there is a very less chance of error like
[08:51] you can see here.
[08:52] Rather than explicitly going through the numbers list, we use special methods like filter() and mapToInt()
[08:58] these methods take an anonymous function, a lambda expression as a parameter.
[09:04] Then at last we are trying to call the sum() method a special form of the reduce operation to compute
[09:09] that total based upon the result of the mapToInt() method.
[09:13] I hope this makes sense to you.
[09:14] I know you may have many thousands of questions like what is a lambda expression, how to write it,
[09:19] what are the special methods?
[09:21] Don't worry too much about them because we are ready to discuss about all of them, and we are going
[09:25] to discuss in detail step by step for now through this lecture, I'm just trying to provide you a clarity
[09:31] about the difference between imperative approach and the functional style approach.
[09:35] I also highlighted the advantages are the enhancements that we are going to get when we follow the functional
[09:43] style of programming, compared to the imperative style of programming.
[09:47] So please refer these slides for more details.
[09:49] So those are all very easy to understand.
[09:51] I'm just leaving them here inside this slide for your reference.
[09:55] Thank you
[09:56] and I'll catch you in the next lecture, bye.

----------------------------------------
