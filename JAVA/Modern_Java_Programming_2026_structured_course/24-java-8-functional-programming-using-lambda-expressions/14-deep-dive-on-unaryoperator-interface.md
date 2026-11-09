# 24.14 — Deep dive on UnaryOperator interface

> Section 24: [JAVA 8] Functional Programming using lambda expressions

[00:00] Inside this lecture, let's explore the unary operator Functional interface.
[00:05] You can use this Function interface to implement a lambda expression in the scenarios where the data
[00:11] type of input parameter and the output is going to be the same.
[00:16] With that, you may have a question which is we should be able to achieve the same behavior with the
[00:21] Function functional interface as well, just inside the angle brackets, I just have to mention String,
[00:27] String.
[00:28] And with that I'm going to get the same behavior like unary operator.
[00:32] Then why should I use the unary operator?
[00:35] It's a great question.
[00:36] You can use this unary operator just to avoid mentioning multiple data types inside the angle brackets.
[00:44] It's just a convenience provided to you by the Java team to make your code more shorter and concise.
[00:50] In fact, this unary operator is a child of Function interface.
[00:56] Let's explore these interface inside the IntelliJ.
[00:59] Inside my interface, I'm going to search for unary operator.
[01:04] If you see here
[01:05] this is extending the Function interface, which is accepting input and output of same data type.
[01:13] With that, all the methods that we have discussed as part of Function, they are going to be inherited
[01:18] by these unary operator.
[01:20] On top of that, we have one more extra static method available inside the unary operator which is identity().
[01:26] So this static method, it is going to give the same input as an output without making any modifications.
[01:34] You can use these identity() method in the scenarios where you want to return the same input data as an
[01:40] output.
[01:41] In such scenarios, you can happily use these identity() static method.
[01:45] So here you can see they are simply accepting an input parameter of type T and they are returning the
[01:50] same as an output.
[01:52] Let's see the demo of this unary operator.
[01:54] For the same
[01:55] I'm going to copy the FunctionDemo class inside the same package, but I'll rename this class to
[02:03] UnaryOperatorDemo.
[02:05] With that, we have our code ready, but we need to make some changes here.
[02:09] Here instead of Function String, String I'm going to mention unary operator, and for unary operator
[02:16] we need to pass a single type which is String.
[02:19] So the same string data type is going to be considered as an input and the output data type.
[02:25] So that's why I'm not getting any compilation error.
[02:28] In fact the abstract method also same which is apply because like we saw previously, unary operator
[02:34] is a child of Function interface.
[02:37] But in this scenario we can't use the unary operator because the input and the output data types, they
[02:43] are different.
[02:44] That's why let me delete these piece of code followed by
[02:48] I'm going to invoke the identity() static method with the help of unary operator.
[02:54] And on the left hand side I'm going to mention unary operator with a single data type inside the angle
[03:00] brackets, and with these variable, which is same value, we can invoke the apply() method.
[03:04] And with that we are going to get the same output whatever we are trying to provide.
[03:08] Now let me scroll down here and replace this Function with UnaryOperator.
[03:13] And instead of mentioning integer two times one time should be enough.
[03:18] The same I need to do inside the next lambda expression as well.
[03:23] After making these changes, we don't have to change any code here.
[03:27] Here, if you try to replace this Function with the UnaryOperator related code, you're going to get
[03:33] a compilation error because this addThen() method is getting inherited from the Function interface,
[03:39] and it has a return type as Function.
[03:42] That's why if you try to catch with the UnaryOperator, which is a subclass, you're going to get a
[03:47] compilation error until unless you are doing the casting.
[03:51] But it should be fine
[03:52] we can catch with the Function interface itself.
[03:55] So if I execute this program this time, the output is going to be very similar to what we have discussed
[04:01] previously.
[04:02] So let me execute this program.
[04:03] You can see my input is converted into uppercase letters followed by I'm getting the same output.
[04:09] Whatever I have provided followed by we have 13 and 16.
[04:13] With this, I'm assuming you are clear about the purpose of UnaryOperator, so always use this Function
[04:19] interface to define the lambda expressions in the scenarios where you are input and output data types
[04:24] are same.
[04:25] Apart from that, there is no other difference between the Function interface and the UnaryOperator
[04:31] interface.
[04:31] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
