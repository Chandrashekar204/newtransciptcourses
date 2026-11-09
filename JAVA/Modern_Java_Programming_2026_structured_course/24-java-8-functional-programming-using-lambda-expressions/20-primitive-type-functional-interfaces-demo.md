# 24.20 — Primitive Type functional interfaces - Demo

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] In the previous lecture, we discussed a good amount of primitive functional interfaces.
[00:06] If I start showing the demo of each and every primitive functional interfaces that we have discussed,
[00:12] it is going to take a lot of time.
[00:15] That's why, to save some time here behind the scenes, I have created a class with the name
[00:20] PrimitiveFunctionsDemo.
[00:21] Inside this class you can see I have written a lot of code which you can refer to
[00:26] see the demo of on how to use the primitive functions that we have discussed so far.
[00:32] I'll try to quickly explain about these core, since the same code is going to be available inside the
[00:37] GitHub repo, I'm assuming you are going to be fine, because we already discussed the concepts around
[00:43] the lambda expressions and the role played by the functional interface, and how to define them and how
[00:48] to invoke them.
[00:49] Since you are already familiar with all these basic concepts, it should be pretty easy for you to understand
[00:54] this class.
[00:55] If you have any questions, I'm always there for you.
[00:57] You can always post your question inside the Q&A so inside the main method, you can see I'm trying
[01:02] to invoke multiple other static methods that I have defined inside this class.
[01:07] So the very first method that I'm trying to invoke here is problemWithNormalFunctionalInterfaces().
[01:13] So inside this method I tried to show you the problem that we are going to face if we use normal functional
[01:21] interfaces whenever we are dealing with the primitive data type values.
[01:24] So here you can see using the normal functional interface which is Function
[01:29] I'm trying to create a lambda expression which is going to accept the input
[01:33] and this input
[01:34] it is going to multiply with the two.
[01:36] So it's just a doubling the value.
[01:38] That's why I have given this number.
[01:40] If you observe here closely I have mentioned the data types as Integer, Integer.
[01:46] So these are the wrapper classes corresponding to the int primitive data type.
[01:51] I hope you are clear with this line.
[01:52] First we have created a lambda expression with the help of these Function interface.
[01:56] Later on you can see how created an array which is storing ten different integer values.
[02:02] And I also created an output array with the same length as input array. Inside these for block
[02:08] I'm trying to iterate all these elements for each element
[02:12] I'm trying to invoke the lambda expression that we have written with the help of these apply() method
[02:16] available inside these Function interface.
[02:19] So what is output we are going to get for each number.
[02:21] It is going to multiply with the two and return the output.
[02:25] But if you see here to make this work for each element these steps has to follow.
[02:30] So first the input value provided will be converted into integer using autoboxing followed by
[02:36] second, the input value provided to the method body will be converted to int, because at the end of
[02:43] the day, we can perform these Arithmetic operations only by using the primitive data type values.
[02:49] At last, in the final step, after the business logic is executed, the return value has to be converted
[02:55] back to integer.
[02:56] Because the return type of your function is integer, and eventually this integer has to be converted
[03:02] back to int.
[03:03] Because we have created the output array with the data type as int.
[03:08] So here I have ten different elements.
[03:10] I hope you are seeing how many times the compiler has to perform the auto unboxing auto boxing.
[03:16] If I have lakhs or millions of elements inside my array, or inside my collection object or inside my
[03:22] stream, then you can think of the performance issues we are going to see.
[03:27] That's why always please leverage the primitive functions that we have discussed in the previous lecture.
[03:33] So in this method you can see I'm trying to give a demo of primitive functions around the Predicate.
[03:38] So here using the IntPredicate I'm trying to pass an int value as an input which is ten.
[03:45] And with that we are trying to avoid the auto boxing.
[03:48] Similarly, I built a logic which is going to accept the double as an input with the help of this
[03:55] DoublePredicate, followed by I built a logic with the help of LongPredicate, which is going to accept the
[04:00] long as an input. In the similar lines, I have provided the sample code on how to create a lambda expression
[04:07] by using all these primitive functions like IntFunction, DoubleFunction, LongFunction, ToIntFunction,
[04:13] ToDoubleFunction, ToLongFunction.
[04:16] So there are good amount of samples here.
[04:19] I don't want to discuss all of them, because it is going to take a lot of time.
[04:24] Since you have enough knowledge on how to understand these sample code, I leave these as a homework
[04:29] to you, so please refer this code present inside the GitHub repo and try to understand on how I am
[04:35] trying to use these primitive functions to create the lambda expressions.
[04:39] The only point that I want you to be aware is always use the primitive functions
[04:45] if you are dealing with the primitive data types as an input or output, I hope this makes sense to
[04:50] you.
[04:51] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
