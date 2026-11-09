# 16.8 — Autoboxing and unboxing - Demo

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] Let's see the demo of Autoboxing and unboxing for the same.
[00:04] I'm going to create a new Java class.
[00:07] The Java class name is
[00:11] AutoboxingUnboxingDemo. Inside this class
[00:14] first let me create the main() method.
[00:17] First, I'll show you Autoboxing.
[00:19] That's why I'm trying to mention the comments, which is Autoboxing.
[00:24] Here, I'll try to create an Integer object with the name as Integer, and to this I can assign directly
[00:33] the 16 value.
[00:34] You can see this 16 value represents the entire primitive data type, but I'm able to directly assign
[00:41] into the wrapper object of Integer class.
[00:45] So what is happening here?
[00:46] Behind the scenes, the Java compiler is trying to invoke the Integer.valueOf() method to convert
[00:54] these primitive data type value into the wrapper class object.
[00:58] As a developer, I don't have to worry what is happening behind the scenes.
[01:01] I can simply assign my primitive data type value directly into the wrapper class object.
[01:07] So this is Autoboxing.
[01:09] Very similarly, we can try to create object of Character wrapper class.
[01:14] So I'll just mention the object name as Character.
[01:17] And to this I can directly assign a char which is M.
[01:21] So this is also autoboxing.
[01:23] Let me try to assign a boolean primitive data type value to the object of Boolean object.
[01:29] So the object name I'll just mention as boolObj.
[01:33] To this, I can directly assign the primitive data type value false.
[01:38] So you can see these are all the examples of Autoboxing.
[01:41] Now let's see the demo of unboxing or auto unboxing this time
[01:46] also it is going to be very simple.
[01:48] You can directly assign the wrapper objects to the primitive data type values.
[01:53] What I can do is I can type int num here to the same
[01:57] I can assign the Integer object.
[02:00] Let me do the same for char as well.
[02:03] So after char I'll just give the name as M.
[02:07] To this I can directly assign the object Character.
[02:10] So this is also unboxing.
[02:12] As a last step, I can try to perform the unboxing for boolean data type.
[02:16] Let me mention the boolean variable name as F.
[02:19] To this I can try to assign the object of boolean, which is boolObj.
[02:24] If I try to print out all these values, I will be able to see the original values that I wrapped inside
[02:31] my wrapper objects.
[02:33] So let me invoke the System.out.println() and to this I can try to pass some variable, and at last I
[02:41] can try to pass a variable f.
[02:43] So if I execute this program, you'll be able to see the output like 16, M and false.
[02:48] I hope you are clear on how these autoboxing and unboxing making our life easy.
[02:53] Once we started learning about collections, you will realize how convenient these autoboxing and unboxing
[03:00] in day to day work.
[03:01] Before I try to close this lecture, let me show you the null pointer scenario that we have discussed.
[03:07] For the same
[03:07] first, I'm going to create an Integer wrapper object with the name as nullObj.
[03:14] To this, I can assign the null value when we are assigning null value.
[03:19] What does that mean?
[03:20] This object reference is not pointing to the any object inside the heap memory.
[03:25] It's just a name that we have reserved for this object.
[03:29] And behind the scenes, this name is not pointing to any of the object.
[03:33] So as a next step, I can try to assign these null object to the int variable with the name num1.
[03:41] So if I try to assign the null object, I'm not going to get any compilation error.
[03:46] I will be able to run the program, but when I try to run this program, I'm going to get a
[03:52] NullPointerException.
[03:52] You can see behind the scenes, my compiler is trying to invoke the intValue() method with the help of
[03:59] these null object.
[04:01] Since null obj has null, we are getting the NullPointerException.
[04:06] That's why
[04:06] please be very cautious about Autoboxing and unboxing whenever you are using null wrapper objects here
[04:14] IntelliJ Idea
[04:15] it is also throwing a warning saying that unboxing of null obj may produce NullPointerException.
[04:22] Did you see how IntelliJ IDE is trying to warn us with the help of this warning.
[04:27] So always
[04:27] that's why anytime if you're intelliJ is conveying some warning or error, please pay some attention
[04:33] to it.
[04:34] After you reading the warning or error and understanding it, it's up to you whether you want to ignore
[04:39] it or whether you want to handle.
[04:41] But reading these warnings and errors is most important.
[04:45] I hope you are clear with the autoboxing and unboxing.
[04:48] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
