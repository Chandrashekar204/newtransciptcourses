# 19.4 — Generic class in Java - Demo

> Section 19: Generics in Java

[00:00] Inside this lecture, let's try to build a similar Pair class, but with the help of Java generics.
[00:08] For the same, I'm going to create a new Java class with the name GenericPair.
[00:14] Since we are trying to build a class that is capable of storing and handling any kind of objects here
[00:21] inside this class, we need to mention two generic type elements.
[00:25] So how to mention generic type elements?
[00:28] Just after your class name, we need to mention the angle brackets.
[00:31] And inside this I can mention a char like T, U with this
[00:37] now whenever someone is trying to create an object of this class, it is going to expect the developer
[00:43] to pass
[00:44] what are the type of objects that they are trying to store inside the Object of this class?
[00:49] We're going to see the demo of that in few seconds.
[00:52] But before that, let me try to create the same two instance variables, which is private T first.
[01:00] So the first type of instance variable is going to be represented with the same data type, which is
[01:06] mentioned at the placeholder T.
[01:08] Similarly, let me try to create one more instance variable with the name second.
[01:13] But this time the data type of this instance variable is of type U.
[01:18] As a next step, I'm going to generate the constructor by accepting these instance variables as an input
[01:24] parameter, followed by
[01:26] I'm also going to generate the getter and setter methods.
[01:30] So let me select both of these instance variables and click on these okay button.
[01:34] Now you can see I have the GenericPair class ready.
[01:38] And inside all the methods that we have generated, the return type of the method and the input parameters
[01:44] of the method
[01:44] they are being represented with the T for the first object and U for the second object.
[01:50] It's not mandatory that you need to use only T and U.
[01:53] You can use anything like you can use A as well, or B it's up to you.
[01:58] I'm trying to use T here because T represents type.
[02:01] Since I can't use the same T for the second object, I'm trying to use U here.
[02:08] As a next step, let's try to create the object of this GenericPair and try to see how it is going
[02:13] to work.
[02:14] I'm going to copy this class which is NonGenericCodeDemo into the same package, but I'll rename
[02:20] this class to GenericCodeDemo.
[02:22] Inside this class we need to make some changes.
[02:25] Here instead of Pair I'm going to use the GenericPair.
[02:29] And since I'm trying to create the object of GenericPair, I need to mention the angle brackets.
[02:34] The first data type I'm going to mention as String, Integer, and on the right hand side I
[02:40] need to mention the same class, which is GenericPair with angle brackets.
[02:44] Since Java supports diamond operator on the right hand side, we are not getting any compilation error.
[02:49] But if you are trying to use any Java version which is less than seven, then you need to mention the
[02:55] same data types on the right hand side as well.
[02:57] As of now you can see I'm getting a warning because it is redundant.
[03:01] So let me remove the same with this object declaration.
[03:04] We are telling to the compiler to please treat the first element as String and the second element as
[03:11] Integer object.
[03:12] That's why we're not getting any compilation error, because the first object is of type String and
[03:17] the second object is of type Integer.
[03:19] If I try to pass a second object as String, I'm going to get a compilation error, because now my compiler
[03:27] is smart enough to detect this kind of issues with the information that we have provided inside this
[03:33] angle brackets.
[03:35] To resolve this compilation error, we need to revert back to the integer element, which is 42.
[03:40] Moving on to the next line of code, this one I can try to delete.
[03:44] Since we are using generics now, we don't have to use this casting.
[03:48] We can simply remove this casting expression and with that we are free from the casting drawback.
[03:55] Whenever we are using generics, we will not have any casting dependency.
[04:00] On top of that, if someone is trying to set an invalid object into the generic class object, they
[04:06] are going to get a compilation error.
[04:08] For example, here, if I try to set Integer object into the first object, I'm going to get a compilation
[04:14] error because the compiler is smart enough to detect this error based upon the data types that we have
[04:20] mentioned inside these angle brackets.
[04:22] So did you see we're able to overcome the two drawbacks that we discussed in the previous lecture.
[04:27] So with the help of generics we are getting the benefits from two different worlds.
[04:33] The very first advantage is we are able to write the generic code inside this main() method
[04:37] I'm trying to use this GenericPair object to store String and Integer objects. If needed,
[04:42] inside another methods I can try to create the object of GenericPair to store Double and Character
[04:49] objects.
[04:50] It's up to me what I want to store.
[04:51] So based upon how I am trying to declare the object of this GenericPair, the same generic code is
[04:57] going to behave differently.
[04:59] So that's a very first
[05:00] advantage.
[05:00] The second advantage is we are empowering the compiler to do the compile time checks so that we don't
[05:07] end up into the ClassCastException scenarios.
[05:11] On top of that, we also don't have to do any casting.
[05:14] Let me execute this program and you'll be able to see the output.
[05:18] Hello and 42 if needed.
[05:20] I can also try to overwrite the information that I have inside this object with the help of setter method.
[05:27] So let me show you how to do that.
[05:29] I'm going to invoke the first object setter method.
[05:32] And to this I'm going to send the another String object which is with the value another String.
[05:37] Similarly, I'm also going to overwrite the second object details with the value 123.
[05:44] So now if I execute this program, you will be able to see the output as another String and 123.
[05:49] .
[05:50] This confirms if needed, we can change the content of the first object and second object, because
[05:55] we have not created this Generic class as immutable, but the assurance that we are going to get from
[06:01] the compiler is it is only going to accept the String object inside the first object and the Integer
[06:07] object inside the second object.
[06:09] I hope this makes sense to you.
[06:10] As of now, like I said, we are using T and U indicates type.
[06:15] Similarly, you can use any character, but the standard is always to use the T to represent a data
[06:21] type.
[06:21] And if you are trying to represent an element, you can use E, whereas if you are trying to represent
[06:26] a number, you can use N for key, you can use K for value, you can use V.
[06:32] So these are the best practices.
[06:34] But it's up to you which character you want to use.
[06:37] I'm trying to use T and U here.
[06:39] Whatever we discuss inside this lecture, along with the example I have mentioned in these two slides.
[06:46] So please refer these two slides to understand more details about how to define a class with the help
[06:52] of generics in Java. It is very easy
[06:55] like we discuss.
[06:56] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
