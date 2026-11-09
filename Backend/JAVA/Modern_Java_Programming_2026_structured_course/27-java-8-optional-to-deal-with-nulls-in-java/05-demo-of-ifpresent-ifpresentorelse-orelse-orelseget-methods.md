# 27.5 — Demo of ifPresent, ifPresentOrElse, orElse, orElseGet methods

> Section 27: [JAVA 8] Optional to deal with nulls in Java

[00:00] As of now
[00:01] we explored about the Optional by using the very basic methods available inside the Optional class.
[00:09] But apart from these basic classes that we have discussed, there are many other advanced methods available
[00:14] inside optional, which we can use based upon our requirements.
[00:18] You can see this is the list of important methods available inside the Optional class.
[00:23] As of now, we saw the demo of the first to five methods like of(), ofNullable(), empty(), isPresent()
[00:30] and get(). Inside this lecture,
[00:32] let's try to see the demo of the remaining important methods available inside the Optional class for
[00:38] your reference.
[00:39] Inside this slide, I provided the brief description about each of these method.
[00:43] So let's go to the intellij and try to explore all these methods.
[00:47] The next method that I want to explain inside the optional class is ifPresent().
[00:52] So there is a method ifPresent(), which you can use to execute some consumer business logic.
[00:59] If an proper non null element is present, you can see this
[01:03] ifPresent(), it is going to accept a lambda expression that is built based upon the Consumer functional
[01:09] interface.
[01:09] So whenever you use these, ifPresent() method you don't even have to invoke the isPresent() method.
[01:16] Because whatever business logic that you are trying to provide to this method as an input, it is going
[01:21] to be invoked directly.
[01:22] If you are optional, instance has a valid element.
[01:26] If it has a null element, then obviously your business logic is not going to be executed.
[01:31] So let me show you the demo of this very quickly.
[01:34] So here, instead of writing these if condition, what I can do is I can straight away invoke
[01:41] optionalmsg.ifPresent().
[01:43] So to this
[01:44] if present I want to pass a lambda expression.
[01:47] So what is a business logic that I have here?
[01:49] I want this logic to be executed.
[01:52] That's why I'll take the element inside my Optional instance as an input with the variable name as m,
[01:59] s, g followed by lambda symbol.
[02:01] And inside the lambda body.
[02:03] I'm going to write this piece of logic.
[02:05] So where I'm going to take this msg and using the msg I can try to invoke that toUppercase() method.
[02:12] So do you see here I'm nowhere checking the null.
[02:14] And still my code is not going to throw NullPointerException
[02:18] even in the scenarios where my optional message may have null element.
[02:22] So this is the beauty of optional inside Java.
[02:26] So if I try to execute this I'll be able to see the output couple of times.
[02:30] So this last message I'm getting from the ifPresent() method, maybe what I can do is just to differentiate
[02:37] that I'm getting the output from
[02:39] ifPresent(), I can try to append a String just before displaying the msg, so I'll just mention ifPresent()
[02:47] colon.
[02:48] So if I execute this you'll be able to see the output.
[02:50] But this time we got a odd number.
[02:53] That's why we are seeing this output.
[02:54] Let me execute this one more time and you can see we are getting our output which is ifPresent
[03:00] Hi world.
[03:00] So just like ifPresent() we also have another method which is ifPresentOrElse() this method is going
[03:09] to accept two input parameters.
[03:11] One is the lambda expression that you want to execute if the element is present, or if the element
[03:17] is not present, which is in the scenario of null object present inside your Optional instance.
[03:21] Then this second Runnable emptyAction is going to be executed.
[03:26] So let me show you how to invoke these method.
[03:28] So after invoking the ifPresentOrElse() first I'm going to pass the consumer lambda expression, followed
[03:36] by
[03:36] after the comma I'll just mention an action, which is I'm not going to accept any input to my lambda
[03:44] expression, followed by I'll try to invoke the System.out.println() and using the System.out.println(),
[03:50] maybe I can try to display a message saying that value is absent.
[03:56] So this way whenever you want to have a else condition
[04:00] also, you can use this ifPresentOrElse().
[04:02] So let me try to append these method name here so that we can differentiate the output that we are getting
[04:09] from these lambda expression.
[04:10] So if I execute this you'll be able to see that I'm getting value as option because a odd number is
[04:17] generated inside our method which is storing a null object inside my Optional instance.
[04:22] So always use this ifPresent() or ifPresentOrElse() method.
[04:26] If you want to build your business logic without any if conditions or null checks, I'm able to achieve
[04:33] my business logic with only a single line of code.
[04:36] If we don't have this optional, we may need to write a if condition
[04:39] curly braces and other business logic which will take at least 4 to 5 lines of code.
[04:44] Now let's try to understand the next method which is orElse().
[04:50] So there is a method with the name orElse().
[04:53] So what this method is going to do is if a value is present, it is going to simply return the value
[04:58] present inside your
[04:59] optional instance.
[05:00] Otherwise it is going to return another value which you have provided as an input to this method.
[05:07] Let me show you a demo of this, so that it is going to be clear for you here using these optionalMsg
[05:12] I'm invoking the orElse() method. To these orElse() method
[05:16] I'm trying to pass an input which is value is absent.
[05:21] So whenever someone invoke these orElse(), they can catch the output on the left hand side with the data
[05:28] type as String and the variable name as msg one.
[05:32] Since my optionalMsg is storing the String data type, I'm trying to catch the output with the help
[05:38] of String.
[05:38] So if you see the beauty of this orElse() is if your optionalMsg has a value, it is going to return the
[05:46] same.
[05:46] Otherwise it is going to return this default value which is value is absent.
[05:51] So let me try to print out the same unto the console with the help of System.out.println() and
[05:57] to this msg one I can try to append the method name.
[06:01] So here the method name orElse().
[06:04] So I'm trying to mention the same.
[06:06] So if I execute this program, you can see whenever a null object is present inside our Optional instance
[06:12] we are getting the output as OrElse() value is absent.
[06:16] Otherwise, if a value is present we are going to get a output which is orElse().
[06:22] Hi world, I hope you are clear with the purpose of orElse().
[06:25] In the similar lines we also have another method which is orElseGet().
[06:30] Instead of providing the element directly like we are doing here to the r ls, we can provide a lambda
[06:36] expression which is going to return a value.
[06:39] That's why you can see the input to this method is Supplier functional interface.
[06:43] Using this Supplier lambda expression we are going to calculate that default value.
[06:48] And the same is going to be considered whenever a null element is present in inside my Optional instance.
[06:54] So this method also can be used with a very simple logic of code.
[06:58] So let me copy these two lines of code and paste it here and rename this variable name to msg2
[07:04] followed by I'm going to invoke the method orElseGet(), to this orElseGet()
[07:10] we need to pass a lambda expression.
[07:12] Since we need to pass the lambda expression based upon the Supplier function interface, there won't
[07:17] be any input parameters.
[07:18] So from my lambda expression, I'm going to simply return a String object here, which is
[07:25] same, Value is absent. In real projects,
[07:29] we may have complex requirements to calculate these default value.
[07:33] In such scenarios, you can have a lengthy lambda body, which is going to help you to calculate that
[07:38] default value.
[07:39] So for now we're just trying to see the demo of these orElseGet()
[07:42] that's why I'm trying to use these simple Supplier lambda expression.
[07:46] So let me use this msg2 and use these or else get to print the output.
[07:52] So if I try to execute this you'll be able to see the output which is orElseGet Value is absent.
[07:58] So in the scenarios where a value is present, we're going to get the output as orElseGet Hi World.
[08:03] I hope you are clear with the discussions that we have done so far.
[08:07] Let's continue this discussion in the next lecture as well.
[08:11] Thank you,
[08:11] bye.

----------------------------------------
