# 10.9 — What a subclass inherits from its superclass

> Section 10: Inheritance in Java

[00:00] Based upon our discussions in the previous lecture.
[00:03] Now, you should be pretty clear about the basics of the inheritance.
[00:08] So what is the purpose of inheritance?
[00:10] Whenever we implement inheritance, a subclass can inherit Java fields and Java method from its superclass.
[00:18] But usually inside a superclass we can write lot of other types of members as well. Like static fields,
[00:25] static methods, instance methods, instance variables, constructors.
[00:30] So there'll be different kinds of members, usually inside a Java class.
[00:34] And we should not be under the assumption everything inside the superclass is going to be inherited
[00:40] by the subclass.
[00:41] So that's not going to be the case.
[00:43] There are certain limitations, our rules and regulations that you need to be aware.
[00:48] So let's try to understand what are those inside this lecture.
[00:51] Like I said before, it is important to note that a class does not automatically acquire or inherit
[00:58] everything from its superclass class.
[01:00] It is going to selectively inherit Non-private members from the superclass.
[01:06] That means the members of the class that are declared with the public, default, and protected, they are
[01:13] going to be passed down or inherited to the subclass, whereas private members they are going to be
[01:20] remain confined within the superclass, and they are not going to be accessible to the subclass.
[01:26] I'm going to talk in detail how access modifiers are going to influence the inheritance process in few
[01:32] minutes.
[01:33] But before that, let's try to understand few general rules and regulations and thumb rules that we
[01:39] need to be aware around inheritance.
[01:42] The very first rule is the constructors and the initializers that we are going to write inside a superclass.
[01:48] They are not going to be inherited by the subclass.
[01:52] A superclass can have any number of constructors, and it may also have a static initializer or a instance
[01:59] initializer.
[02:00] So since these are not fall under the category of the members within a class, they are not going to
[02:07] participate in the inheritance process.
[02:10] Moving on to the next rule, all the static members that you are going to define inside your superclass,
[02:17] they are going to be inherited by the subclass.
[02:19] When I say static members, what are those?
[02:21] It can be a static field or a static method.
[02:24] So these static methods and static fields, they will be inherited by the subclass without any issues.
[02:32] We're also going to see the demo in few minutes.
[02:34] Apart from static members like static fields and static methods, we can also define instance method
[02:41] and instance variables.
[02:42] We know that these instance methods and instance variables
[02:46] they are also going to be participate in the inheritance process regardless whether a method is static
[02:51] or non static, whether a field is static or non static.
[02:55] So all of them, they are going to participate in the inheritance process.
[02:59] But they are going to be greatly influenced by the access modifiers.
[03:05] For example, if you define a class member with a private access modifier, its accessibility is going
[03:12] to be restricted solely to the class in which it is declared.
[03:16] That means private class members are not going to be passed down to the subclasses, and they are going
[03:22] to be remain exclusive, but the superclass alone. After the private
[03:27] we can also define class members by using the public access modifier.
[03:32] So when we use the public access modifier, all of your class members, they are going to be inherited
[03:39] to the subclass.
[03:40] That means a subclass inherits all public members of its superclass, whether it is a method or a field.
[03:47] If it is a public, the same is going to be inherited by the subclass.
[03:51] On the similar lines, when we define a class member with a package level or a default access modifier,
[03:58] then in this kind of scenarios, if the subclass is present inside the same package, then these default
[04:04] are package level class members
[04:06] they are going to be inherited by the subclass, whereas if your subclass is belongs to a different
[04:12] package compared to the superclass, then in such scenario, the subclass does not going to inherit
[04:18] package level members or default members from its superclass.
[04:23] So to resolve this challenge, we can use protected Access modifier.
[04:28] When we use the protected access modifier, your subclass always going to inherit that class members
[04:35] regardless your subclass present inside the same package of superclass or a different package compared
[04:40] to the superclass.
[04:41] So these are the guidelines or the rules that you need to be aware to understand.
[04:46] What is subclass inherits from its superclass.
[04:49] As a next step, let's see that demo of these rules very quickly
[04:53] inside the intelliJ, inside my IntelliJ
[04:56] as of now, you can see we have a superclass with the name person,
[05:00] inside this super class, I'm going to define a private method by mentioning private void and the method
[05:08] name
[05:08] I'm going to keep it as calculateEdge().
[05:11] To this method, we are going to accept the input parameter which is int year.
[05:17] So based upon the year, we want to calculate the age.
[05:20] But in order to calculate the age based upon the year, first you need to be aware about the dates concept
[05:26] inside Java.
[05:27] As of now, we have not discussed on how to represent a date inside Java, since we are going to discuss
[05:33] about all these concepts in the coming sections,
[05:36] for now, I'll keep the logic of this method very simple by writing a System.out.println() and to this
[05:41] println() method, I'm going to pass an input which is age() method.
[05:46] So with this we successfully created a private method inside my Person super class.
[05:51] Now if I go to any of my subclass of the Person like IronMan here, if I try to look for the list of
[05:59] methods and fields that are available inside this class by pressing the command + F12 shortcut, you will
[06:05] not be able to see any method with the name calculateAge() because calculateAge(), we marked it as private
[06:12] and all the private members of a super class
[06:15] they are not going to be inherited by the subclass.
[06:18] I hope it is clear now I'm going to change this private to default.
[06:23] So how to do that?
[06:24] By just removing the private access modifier
[06:27] and if you don't mention any other access modifier, it is going to become default access modifier or
[06:33] a package level access modifier.
[06:35] So even in this scenario also my calculateAge() method is not going to be inherited by the subclass.
[06:41] The reason is both this Person and IronMan
[06:45] they are present inside two different packages.
[06:48] I can also confirm you by pressing command F12.
[06:51] So here you can see
[06:53] still my calculateAge() method is not visible or is not inherited by my IronMan class.
[07:00] As a next step, I can change this access modifier to protected by mentioning protected access modifier.
[07:07] This time this method should have been inherited by the IronMan subclass.
[07:12] So let me go to IronMan and this time and press command F12.
[07:17] And you can see there is a method called calculateAge() which is inherited from the person superclass.
[07:24] The same you can confirm by looking other subclasses like SpiderMan.
[07:29] So here also I'm going to check.
[07:31] You can see there is a calculateAge() method.
[07:33] I hope this is clear.
[07:35] As a next step, let me create a static variable inside my Person superclass.
[07:41] For the same I'm going to type public static followed by int and the variable name.
[07:47] I'll keep it as numberOfHands.
[07:50] So this is a variable name.
[07:51] And to this variable I'm going to assign a value to
[07:54] so every person is going to have two hands.
[07:57] So the same I'm trying to represent with the help of this static variable.
[08:01] Now let's try to validate if this static variable is going to be inherited by the subclass.
[08:08] So let me go to the IronMan.
[08:09] And here if I press F12 you'll be able to see a static variable which is numberOfHands of type int
[08:18] with a value two at the end.
[08:20] So this variable inherited from the Person superclass.
[08:23] So this confirms the static members of a superclass
[08:27] they are also participating in the inheritance process.
[08:30] And these static members, they are also going to be influenced greatly by the access modifier.
[08:36] For example, if I mention private, then I will not be able to see the static variable inside my IronMan
[08:43] subclass.
[08:44] So this confirms the access modifiers are playing a very important role in the inheritance process.
[08:51] I have reverted the access modifier back to public so that these number of hands static variable is
[08:57] always going to be inherited by all the subclasses of the Person
[09:01] superclass class.
[09:02] I hope you are clear now since you have some knowledge around the inheritance this time, this image
[09:08] is going to make sense for you if you look
[09:11] this is the funny representation of the inheritance.
[09:13] He is the parent and he's the child.
[09:15] So what is the child inherited from his father?
[09:18] It is very funny.
[09:19] If you closely look at the years of both father and child, it is going to confirm their parent child
[09:26] relationship.
[09:27] I hope you like this funny representation of the inheritance.
[09:30] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
