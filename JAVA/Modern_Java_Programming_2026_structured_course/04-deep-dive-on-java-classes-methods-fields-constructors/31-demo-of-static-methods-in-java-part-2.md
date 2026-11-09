# 4.31 — Demo of static methods in Java - Part 2

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Long back, we discussed about the syntax that we need to follow to invoke a method.
[00:05] So there are three types of syntax that we need to follow based upon the type of method, and based
[00:10] upon the method where it is present.
[00:12] If your method that you're trying to invoke is present inside the same class file, then you don't have
[00:18] to do a lot of work.
[00:19] You can simply invoke it with the help of its name along with the method arguments.
[00:23] But like we discussed in the previous lecture, we have some limitations where we cannot invoke a instance
[00:29] method from a static method.
[00:31] By simply using the method name, we have to create the object of the class.
[00:35] Then only we can invoke it.
[00:37] Moving on to the other scenarios where
[00:39] think like your method which you are trying to invoke, is present inside another class.
[00:44] In such scenarios, first, you need to understand whether the method is a static method or a non static
[00:50] method.
[00:50] If the method is a static method, then you can simply invoke it with the help of class name, whereas
[00:57] if the method is a non static method, you have to make sure you are creating the object of the class
[01:02] and using the object of the class only you can invoke the instance method.
[01:06] So let's try to see these in the demo for the same,
[01:09] what I'm going to do is as of now, we explored in the previous lecture by trying to invoke the methods
[01:14] which are present inside the same class.
[01:16] As a next step, I want to create a new Java class.
[01:20] So let me create this new Java class.
[01:22] And the class name that I want to give here is ArithmeticMain.
[01:25] So this is the class that I want to create.
[01:27] Post that inside this class I'm going to first define the main() method from the main() method
[01:33] first I want to invoke the static method which is available inside the ArithmeticOperations.
[01:39] So what is a static method that we have here?
[01:41] We have a static method with the name addition().
[01:44] So let me try to invoke that.
[01:46] So to invoke the static method what is the syntax that we need to follow.
[01:49] We need to first mention what is our class name post that,
[01:53] what is the method name?
[01:54] You can see as soon as I type dot, it is showing me all the static methods.
[01:59] One of the static method that I have here is addition() to this addition() method
[02:04] I need to pass two method arguments like 20, 4, and I'm going to catch the output using the
[02:12] result variable the same
[02:14] I can print it on the console.
[02:16] If I try to execute this program, you'll be able to see the output which is 24.
[02:22] Now, as a next step, I want to show you how to access the static variables available inside another
[02:28] class.
[02:28] So let me take this System.out.println() and paste it inside the next line.
[02:33] And here first I'm going to mention the class name which is ArithmeticOperation.
[02:38] As soon as I press dot, you can see there is an option for me to use the PI_VALUE.
[02:44] Since this is a static variable, I can invoke it with the help of class name.
[02:48] So that's what I'm trying to do here.
[02:50] If I try to execute this, you can see I'm going to get 3.14 as an output.
[02:55] Now let's try to understand how to invoke the instance methods which are present inside another class.
[03:01] So this is going to be very simple
[03:03] first we need to create the object of ArithmeticOperations.
[03:07] So let me create the same using the new operator and the default constructor.
[03:13] After that, using the object reference I'm going to invoke the sum() method.
[03:19] And to this sum() method I'm going to pass the value and post that
[03:22] I'm going to catch the value inside the variable called result instance method.
[03:29] So this is the variable name that I want to go.
[03:31] Maybe I can rename it to result from instance method.
[03:35] So this is going to make more sense.
[03:37] So the same I'll try to print it on the console
[03:40] and this time you can see we are going to get 25 as an output.
[03:45] So this is how we need to invoke the instance methods which are available in the another class.
[03:51] Very similarly if you want you can access the instance variables as well with the help of the same object
[03:57] reference.
[03:58] So let me take this object reference
[04:00] and as soon as I type dot, you'll be able to see my value variable which we can access
[04:05] and if I try to print it you'll be able to see 3.14 in the output.
[04:09] With this, I'm assuming your super clear about what are the kinds of methods and fields that we can
[04:15] create inside a Java class, and how to invoke them.
[04:18] There are various approaches to invoke the methods based upon various parameters, like where the method
[04:23] is present, what is the type of the method.
[04:26] So always refer to the slide that we have discussed
[04:28] if you have any questions around the syntax that we need to follow to invoke a method or to invoke a
[04:34] variable. I hope this is all clear to you.
[04:36] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
