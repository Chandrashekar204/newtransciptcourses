# 2.25 — Demo of implicit and explicit casting - Part 1

> Section 2: Primitive data types in Java

[00:00] Inside my shell,
[00:01] first, I'm going to show you the demo of automatic casting or implicit casting or widening casting.
[00:07] For the same,
[00:08] first I'm going to create an integer.
[00:10] The integer variable name is going to be myIntNum
[00:14] to this variable, I'm going to assign a value which is 16.
[00:18] So there is nothing wrong in this.
[00:20] We already know about the syntax.
[00:21] So now my my int number variable is going to hold the 16 value.
[00:26] Now what I'm going to do is, I'm going to create a variable of type double.
[00:31] And the name is going to be myDoubleNum.
[00:34] To this I'm going to assign the variable that I have created previously.
[00:40] So what is the variable that I have created previously myIntNum.
[00:44] So here whatever value that I have inside myIntNum going to be assigned to the myDoubleNum.
[00:50] So what is happening here?
[00:52] I'm trying to upgrade my int value to that double since it is an upgrade and I'm not going to lose any
[00:59] data,
[01:00] we call this kind of casting as automatic casting or implicit casting or widening casting.
[01:06] And in these kind of scenarios, my compiler is not going to throw any error.
[01:11] So this is very similar to airport scenario.
[01:13] Suppose think like you are traveling from one city to other city through a plane.
[01:17] All of a sudden if the airport staff, if they're trying to upgrade you from economy class to business
[01:23] class, are you going to oppose?
[01:24] Off course not
[01:25] right?
[01:26] You're going to more than happy to accept that offer.
[01:29] The same thing is happening here.
[01:30] Very similarly
[01:31] let me show you few more examples here.
[01:34] First, I'm going to create a float and the variable name is going to be myFloatNum.
[01:39] To this I'm going to assign a value which is 3.14f.
[01:44] And if I execute this there is no wrong here.
[01:47] Now if I try to upgrade this float value to the double, there will be no compilation error because
[01:52] this is an implicit casting.
[01:54] So let me try to do that.
[01:55] Like to my myDoubleNum which we have created previously.
[01:59] I'm going to assign the variable which is myFloatNum.
[02:03] So if I execute this you can see now my myDoubleNum is upgraded and there is no loss of data.
[02:11] In fact more new data is added which we can use based upon our needs.
[02:16] Now if you try to do the other way, then we call it as narrowing casting or manual casting or explicit
[02:24] casting.
[02:24] Suppose think like
[02:25] I want to assign these myDoubleNum value to the float, which means I'm trying to downgrade my double
[02:33] number to the float.
[02:34] Float is capable of storing only up to the seven decimals, so let's see what is going to happen.
[02:39] So here first I'll try to create a variable of type float.
[02:44] So I'll just mention myFloatNumber.
[02:47] So this is going to be the variable to this variable I'm going to assign the variable of double which
[02:53] is myDoubleNum,
[02:54] we know inside the myDoubleNum we have this value.
[02:57] So if you try to assign this value to the float it is a downgrade scenario which is like someone is
[03:03] asking you to move to the academy class even though you have booked a business class ticket.
[03:08] So are you going to accept it?
[03:10] You are not going to accept it.
[03:11] Very similarly, compiler is going to throw an error.
[03:14] So to resolve this issue, the developer has to do manual casting.
[03:18] So let's try to understand how the developer has to do the manual casting.
[03:23] The syntax is going to be very simple.
[03:25] First you need to write float.
[03:26] MyFloatNum is equal to myDoubleNum.
[03:29] Now just before the myDoubleNum you need to mention brackets.
[03:33] And inside the brackets you need to mention what is the data type that you are trying to convert.
[03:39] So float is a data type that I'm trying to convert.
[03:42] And with this I'm telling to my compiler, I know that I'm trying to do double to float, and I'm completely
[03:48] fine to lose the data.
[03:50] Please allow this.
[03:51] So we're trying to request to the compiler and after seeing the syntax my compiler is going to accept
[03:58] my manual casting are narrowing casting.
[04:01] And this is the value we are going to have inside the float.
[04:04] So here we lost the data.
[04:06] So all these decimals we lost.
[04:08] That's why this kind of castings we call it as narrowing casting or explicit casting or manual casting.
[04:15] Next let me show you the casting from a double to int.
[04:19] So we're trying to downgrade a double number from int or long.
[04:24] In such scenarios we are going to lose the decimal values.
[04:27] So let's try to understand how to do that.
[04:29] For the same,
[04:30] let me clean my console.
[04:32] Post that first I'm going to create a double number and the variable name is going to be myDoubleNumber.
[04:39] To this I'm going to assign a decimal value which is 3.14.
[04:44] Now, I'll take this myDoubleNumber and try to assign to an integer.
[04:48] So here first I'll mention int and what is the variable name.
[04:52] The variable name is going to be myIntNumber.
[04:55] To this myIntNumber I'm going to assign the my double number.
[05:00] Variable.
[05:01] So let's see what is going to happen.
[05:02] Like you can expect we are going to get an compilation error saying that there is a possibility of losing
[05:09] the data when we try to downgrade from double to int.
[05:12] So how to resolve this issue?
[05:14] We just have to do the manual casting by just mentioning what is the target data type just before the
[05:20] myDoubleNumber variable.
[05:22] So what is the target type int.
[05:24] So let me try to execute this command.
[05:26] You can see this time I'm getting a perfect output.
[05:29] But it is pretty clear now we are losing the data of decimals.
[05:33] We simply having a whole number which is three.
[05:35] So the developer has to do this manual casting only if he's fine
[05:39] losing the data.
[05:40] I hope you are clear with these demos.
[05:42] Let's try to continue this discussion in the next lecture as well, where I'm going to show you more
[05:47] examples about implicit and explicit casting.
[05:50] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
