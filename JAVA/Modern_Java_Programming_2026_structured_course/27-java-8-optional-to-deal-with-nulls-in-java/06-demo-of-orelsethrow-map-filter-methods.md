# 27.6 — Demo of orElseThrow, map, filter methods

> Section 27: [JAVA 8] Optional to deal with nulls in Java

[00:00] The next to commonly used method available inside the Optional class is orElseThrow().
[00:06] This method, you can use in the scenarios where you want to throw the exception, which is
[00:12] no such element exception if your optional instance does not have a value.
[00:18] You can also read the documentation of this method, which says if a value is present, returns a value
[00:23] that's a happy scenario, otherwise it is going to throw NoSuchElementException.
[00:28] So let's see that demo of this.
[00:30] Here I'm going to copy these two lines of code.
[00:32] And instead of msg2 I'm going to mention the variable name as msg3.
[00:37] And this time I'll try to invoke orElseThrow().
[00:41] And it is not going to accept any input.
[00:43] That's why I need to remove this post that I need to use this msg3 here.
[00:48] And I'll also mention this method name which is orElseThrow().
[00:51] So with this line of code, whenever the optional MSG has a null value, we are going to get an exception.
[00:59] Let's see the same.
[01:00] So this time we are not getting any exception because we got a proper element inside the Optional instance.
[01:07] So if I try to execute one more time this time you can see we are getting an exception which is
[01:13] NoSuchElementException.
[01:14] So whoever is trying to use these orElseThrow() method, they need to be ready to handle the NoSuchElementException.
[01:21] Because it is going to create runtime exceptions unnecessarily.
[01:25] So that's why I'm trying to comment these line of code.
[01:28] Just like how we have orElseThrow().
[01:31] We also have another orElseThrow() overloaded method which is going to accept and Supplier as an input.
[01:38] If you can open this, there is one more orElseThrow() method.
[01:42] So this Supplier lambda expression it needs guidance to the Java which runtime exception it has to throw.
[01:48] So with the help of orElseThrow() we are always going to throw the runtime exception which is
[01:54] NoSuchElementException.
[01:55] Instead of this we can try to throw our own exception.
[01:58] So let me show you how to do that.
[02:00] So here I need to write a lambda expression adhering to the Supplier functional interface.
[02:05] From this lambda expression I'm going to throw an runtime exception which is IllegalStateException
[02:11] to this IllegalStateException constructor
[02:14] I'm trying to pass a message which is value is absent.
[02:18] So you can see here with these orElseThrow()
[02:20] we are trying to throw our own custom exception here.
[02:23] Instead of IllegalStateException
[02:25] you can create your own business exception and use the same here.
[02:29] So let me execute this program.
[02:31] And you can see we are getting IllegalStateException.
[02:34] But like I said, don't try to use this unless you are ready to handle these kind of exceptions inside
[02:40] your business logic.
[02:41] That's why I'm trying to comment all this code for your reference.
[02:44] Next, we have a method with the name map(), just like how we saw a method inside the stream API with
[02:51] a similar name.
[02:52] This is also going to work very similarly.
[02:54] So what this method is going to do is if a value is present, it is going to return a new Optional
[03:00] after applying the given mapping function to the value.
[03:04] Otherwise it returns an empty Optional.
[03:07] So here you can see to this map() method.
[03:09] We are trying to pass a lambda expression adhering to the Function functional interface.
[03:13] So if you are optional instance has a value inside it.
[03:18] It is going to fetch that element and apply the business logic that you have written with the help of
[03:23] lambda expression.
[03:24] Once the business logic calculated the new value, the same value is going to be wrapped and sent inside
[03:30] the optional instance like you can see here.
[03:33] So let me show you a demo so that it is going to be clear for you.
[03:35] So what I'm going to do is using the same optionalMsgand going to invoke the map() method.
[03:42] Using this map() method, I can try to process the data that I'm going to fetch inside these optionalMsg.
[03:48] .
[03:49] So what we are trying to store inside this optionalMsg, we are trying to store the String object.
[03:54] If my requirement is to convert my String object into the uppercase value, I can try to write a lambda
[04:00] expression which which is going to accept an input parameter with the name input followed by lambda
[04:05] symbol, followed by using the same input.
[04:08] I can try to invoke that toUppercase(). If you see here
[04:11] now where I fetch the element present inside this optional message.
[04:15] So behind the scenes, this map() method is going to do that for me.
[04:18] And once the value is fetched, it is going to feed as an input to my lambda expression.
[04:23] And once the output is returned by my lambda expression, the same is going to be wrapped inside a new
[04:29] Optional instance, and the return type from this method is going to be optional of String.
[04:35] So let me mention the variable name as mapOptionalStr.
[04:41] So this is how it is going to work here.
[04:43] Instead of this lambda expression we can straight away use the method reference.
[04:47] Like for example using String two colons I can invoke the toUppercase() method.
[04:53] This is also going to work very similarly in the scenarios where my optional message is going to have
[04:59] the null values.
[05:00] Then this map() method, it is not going to be invoked.
[05:02] Instead, I'm going to get directly an empty Optional instance.
[05:07] We can also confirm this behavior by printing out these map optional str onto the console.
[05:14] So if I try to execute this here, you can see I got an empty because my optionalMsg has a null value
[05:21] let me execute this one more time.
[05:23] This time also, I'm getting empty.
[05:25] This time you can see I got an Optional instance which has an element hi world in completely capital
[05:33] letters because we executed a map logic which is toUppercase() with the help of this lambda expression.
[05:40] Just like how we have a map() method, we also have filter() method.
[05:43] If you can scroll down, there is a filter() method.
[05:46] So let me search for filter here.
[05:49] The purpose of this filter() method is it is going to accept and Predicate lambda expression.
[05:55] This Predicate logic is going to be applied on the element that we have inside an Optional instance.
[06:01] So if the element is passing my Predicate condition, I'm going to get the same as an output inside
[06:08] an Optional instance.
[06:09] In the scenarios where my initial element did not satisfy the Predicate condition are in the scenarios
[06:15] where I filled an empty Optional instance to the filter() method.
[06:19] In all such scenarios, we are going to get an empty Optional instance as an output.
[06:25] Let's see the demo of this method also.
[06:27] So here I'll try to copy these two lines of code and paste it here.
[06:32] And this time instead of map(), I'm going to invoke the filter() method.
[06:36] The Predicate condition that I want to write here is,
[06:39] first, I want to accept the value inside these optional messages with a parameter name as value.
[06:45] Post that I'm going to write a check, which is to check the length of the String object.
[06:52] If the length of the object is greater than five, then only wrapper these filtered value into the.
[06:59] Another Optional instance that I'm trying to catch on the left hand side.
[07:03] So here let me rename this to filterOptionalStr.
[07:08] The same I can try to print out.
[07:09] So if I execute this I'm going to get empty because this optional message right now it holds the null
[07:16] value.
[07:16] So let me execute one more time.
[07:18] This time you can see I got the output which is hi world because this optionalMsg as an element
[07:24] which satisfied these predicate condition.
[07:27] If I mention the length as greater than 50, then I know it is never going to satisfy and every time
[07:33] I'm going to get empty Optional.
[07:34] So I can also validate the same.
[07:36] This time we got empty because odd number is generated.
[07:40] Let me execute one more time.
[07:42] So this time you can see though there is an element inside the Optional.
[07:46] We are still getting the empty because its length is not greater than 50.
[07:50] That's why we are getting the empty Optional.
[07:53] I hope you are clear.
[07:54] Let me revert back to the length five.
[07:57] So I tried to explain all the important methods available inside the Optional class.
[08:02] So use all of them and try to master all of them so that you can build your business program using functional
[08:09] style.
[08:09] So optional is giving a lot many options to you that you can use on your day to day basis.
[08:15] My favorite method is using these
[08:18] ifPresent() with these, you don't even have to build any
[08:22] if conditions or null checks within a single line, you're going to process your element inside the
[08:28] optional if it is present
[08:30] otherwise you're going to simply ignore it.
[08:32] Off course, in the scenarios where you can't simply ignore, you can't use this method.
[08:37] You need to rely on other type of methods like ifPresentOrElse().
[08:41] Please always refer to this slide whenever you want to quickly brush up around the methods supported
[08:46] by the Optional class.
[08:48] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
