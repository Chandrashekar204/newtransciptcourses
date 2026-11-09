# 4.28 — Differences between static & instance variables

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's quickly discuss about the differences between the static variable and the
[00:07] instance variables.
[00:08] As of now, inside Java class, we can create two types of variables and fields.
[00:13] One is static variable like we discussed in the previous lectures.
[00:16] And the other type of variables are instance variables or non static variables.
[00:22] Let's try to talk first about the static variables.
[00:25] Because we just discussed about them.
[00:26] It should be very quick.
[00:28] Static fields are also known as class variables because they are associated with the class, rather
[00:34] than with an instance of the class or an object.
[00:37] Whenever I say instance, I'm referring to the object.
[00:40] What is the other name for the object,
[00:42] it is instance and the next point that we need to aware is how to declare the static variables.
[00:48] By using the static keyword and the variables that we declare with the help of static keyword, they
[00:55] are going to be initialized only once when the class is loaded into the memory, and all the instances
[01:02] are the objects of the class, they're going to share the same static field and its value.
[01:07] And what is the syntax that we need to follow to invoke a static field?
[01:11] We need to follow the syntax which is class name dot
[01:15] what is your static field name?
[01:17] For example, here I have mentioned a class which is Example.
[01:21] And inside this Example class we have two variables.
[01:25] One is static and the other one is an instance field.
[01:27] The syntax that I need to follow here is to invoke the static field,
[01:31] Example.staticField.
[01:34] Now moving on to the next type of variables which are instance variables or non static variables.
[01:41] Why do we call these variables as instance variables.
[01:44] Because these variables they are going to hold the unique data for different, different objects.
[01:50] Since these are associated with the instance of the classes or the object of the class.
[01:55] In other words, we can call these variables as instance variable inside the industry, when someone
[02:01] is saying variable or a field, by default, they are referring to the instance variable.
[02:07] If they are trying to refer to a static variable, they will specifically mention static variable.
[02:12] So that's a standard that developer usually followed during the conversations are during the discussions.
[02:18] So whenever we try to create variables or fields as instance variables, each and every instance or
[02:24] object is going to have its own copy of that instance field.
[02:28] That's why whenever we want to access an instance field, the syntax that we need to follow is first,
[02:34] we need to make sure we are creating the object of the class and post that using the object we need
[02:40] to access the instance field.
[02:42] So here I also gave an example by using the same Example class.
[02:47] I hope you are clear with the differences of the static and instance variables.
[02:51] Always refer to this slide for more details around the differences between them.
[02:56] This is going to be a favorite interview topic.
[02:59] That's why always make sure you are learning in detail about what is an instance variable and static
[03:05] variable whenever you are trying to attend an interview.
[03:08] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
