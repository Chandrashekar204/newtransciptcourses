# 4.13 — Syntax of method invocation in Java

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now, we only define the methods inside the Java classes that we have, but we don't know how
[00:07] to invoke these methods.
[00:08] So let's try to understand what is the syntax that we need to follow whenever we are trying to invoke
[00:13] a method.
[00:14] Here you may have a question what is the meaning of method invocation?
[00:18] When I say method invocation or calling a method that means some other method inside your Java program
[00:25] is trying to invoke another method which can be present inside the same class, or it can be present
[00:31] inside another class.
[00:32] So the syntax to invoke a method is going to change based upon multiple parameters, like where your
[00:39] method is present and what is the type of your method.
[00:42] So based upon these parameters, the syntax is going to change.
[00:45] For example, think like you're trying to invoke the sum() method which we have declared inside the arithmetic
[00:52] operations Java class.
[00:53] If these sum() method is trying to be invoked by some other method present inside the same Java class,
[01:00] in such scenarios, the syntax is going to be very simple.
[01:04] We just have to mention what is the method name like sum() and you need to pass the input parameter values.
[01:10] And these values we call them as method arguments.
[01:14] So here I'm trying to pass two into values like 6, 24.
[01:18] But the same sum() method is present inside some other Java class.
[01:22] Then you have two options based upon the type of the Java method.
[01:26] If the Java method is a non-static Java method where there is no static keyword inside the method declaration,
[01:33] then in such scenarios, you need to create an object of the class where the sum() method is present,
[01:39] where to discuss on how to create an object from a Java class.
[01:43] For now, let's assume the object variable name is object name.
[01:48] So with the help of the variable name and dot operator, you need to invoke the method sum().
[01:53] And to this sum() method you need to pass the input parameter values like 6, 24.
[01:59] Whereas if the same sum() method is declared as an static method in some other Java class, in such scenarios,
[02:07] it is not required to create the object of the class.
[02:11] You can directly invoke the static method sum() with the help of the class name itself.
[02:16] So the syntax is going to be ClassName.sum(6,24).
[02:21] And at last we need to mention the semicolon.
[02:23] So this is how you're going to invoke the methods.
[02:26] And this syntax is going to change based upon where the method is present and what is the method type,
[02:32] whether it is a static method or a non-static method.
[02:35] More details about static and non static methods we are going to discuss in the coming lectures.
[02:40] So here we are just invoking the methods.
[02:43] We are not catching the output that we are going to get from the sum() method.
[02:48] Catching the output or
[02:50] accepting the output from the given method is completely optional and the caller method side.
[02:55] That's why you can see I have not mentioned any syntax to catch the output of the sum() method, but most
[03:02] of the times we want to catch the output and we want to process that in the caller method.
[03:07] In such scenarios, the syntax is going to be very simple, like you can see here under the third point,
[03:13] first on the left hand side we need to define what is the data type of the output.
[03:18] Since the sum() method is going to return the int data type value, we have to mention int and what is
[03:24] the variable name using which you want to catch that output value.
[03:28] So here I'm trying to give the variable name as result.
[03:31] So this is how you need to invoke the methods and catch the results inside the caller method.
[03:37] And going to show you lots of demos
[03:39] once we learn the concepts of objects creation in the coming lectures.
[03:43] And the important point that I want to highlight here is like you can see in the second point, whenever
[03:48] we are trying to send some input values like 6 and 24 to the as part of the method invocation, then
[03:54] these 6 and 24 are going to be binded to the method parameters.
[03:59] By the time they are trying to invoke the sum() method for the execution of the business logic.
[04:05] So these are the syntax that we need to follow.
[04:07] I just wanted to share a very quick information about this.
[04:10] As of now, we can't see the demo because we are yet to learn on how to create the objects from the
[04:16] given class.
[04:17] Once we learn about that, then I'm going to show you the demo of this method invocation.
[04:22] Till that time, please hold your thoughts around this.
[04:25] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
