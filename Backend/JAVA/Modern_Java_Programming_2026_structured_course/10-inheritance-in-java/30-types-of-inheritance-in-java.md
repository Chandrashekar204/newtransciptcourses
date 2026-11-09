# 10.30 — Types of Inheritance in Java

> Section 10: Inheritance in Java

[00:00] We have been talking a lot about inheritance throughout this section, and we know using the extends
[00:07] keyword, any subclass, it can inherit the properties from its superclass
[00:12] but sometimes you may want to inherit from multiple classes like here.
[00:17] I want to inherit both from Vehicle and Person superclass.
[00:21] But inside Java this is not allowed.
[00:25] So this is one of the limitation that we have with inheritance while we are trying to inherit the multiple
[00:31] super classes.
[00:32] That's why inside this lecture, let's try to put some efforts in understanding what are the different
[00:38] types of inheritance usually available inside any object oriented programming language, and which one
[00:44] of them is going to be supported by Java.
[00:46] And in the same process, I'm also going to explain you why these multiple inheritance is not allowed
[00:53] in Java.
[00:54] Inside object oriented programming we have five different types of inheritance available.
[00:59] The very first type of inheritance is single inheritance.
[01:04] In this Single inheritance, a single subclass is going to extend the properties from a single superclass.
[01:10] You can see here I have a superclass with the name class A, and there is a subclass which is class
[01:16] B, and class B is going to extend the properties from the class A, so this is perfectly allowed inside
[01:23] Java.
[01:23] We also saw this kind of inheritance many times in the previous examples that we have discussed.
[01:29] The next type of inheritance is Multilevel inheritance.
[01:33] First, I'm going to have a class A later on
[01:36] this class here is going to be inherited by the class B, and the class B is going to be inherited by
[01:42] the class C.
[01:42] This way we can maintain any levels of inheritance.
[01:46] The class A here
[01:47] it is going to act as a super superclass for the class C and the class B.
[01:52] Here it is going to act as a immediate subclass for the class A, whereas the class C is not a immediate
[01:59] subclass of class A, it is a normal subclass which is inheriting from the class A also, since in this
[02:06] kind of examples, the inheritance is flowing into multiple levels, we can call this as multi-level
[02:13] inheritance.
[02:14] This is also perfectly allowed inside Java.
[02:18] The next type of inheritance available is Hierarchical inheritance.
[02:22] That means a single superclass is being extended by the multiple subclasses, and this kind of inheritance
[02:30] also is completely acceptable inside Java.
[02:33] We also saw this kind of inheritance in the previous lectures, where we created a single superclass
[02:39] Person, and this single superclass is inherited by multiple subclasses like SpiderMan, IronMan,
[02:45] CaptainAmerica.
[02:46] So this also confirms Hierarchical inheritance is completely supported by the Java.
[02:53] Now let's try to understand what is the fourth kind of inheritance available.
[02:57] The fourth kind of inheritance is Multiple inheritance.
[03:01] In this kind of inheritance, two different kinds of super classes, they are going to be inherited
[03:07] by a single subclass.
[03:09] And this is not allowed inside Java.
[03:12] There is a problem.
[03:13] I'll explain you why this is not allowed inside Java in few seconds.
[03:17] We also saw here we are getting a compilation error when we are trying to inherit multiple super classes.
[03:24] So here the compilation error also
[03:26] clearly telling class cannot extend multiple classes.
[03:31] I hope it is clear that multiple inheritance is not supported by Java, but there is a workaround to
[03:37] achieve these Multiple inheritance in Java.
[03:40] That is, with the help of Interfaces, we are ready to discuss about another important topic inside
[03:46] Java, which is Interfaces.
[03:48] When we are talking about Interfaces, I will explain you how to achieve these Multiple inheritance.
[03:54] And the last type of inheritance is Hybrid inheritance.
[03:57] If you try to club any of the previously discussed for inheritance, then that is going to become Hybrid
[04:04] inheritance.
[04:05] Here you can see on the top a single superclass is being inherited by the two subclasses.
[04:11] So what is this type of inheritance?
[04:13] It is called as Hierarchical inheritance.
[04:16] Whereas if you look at the bottom this is a Multiple inheritance.
[04:20] So since there are two types of inheritance involved, we can call these kind of inheritance as Hybrid
[04:26] inheritance.
[04:27] If you are Hybrid inheritance involves multiple inheritance, then that is also not allowed inside Java.
[04:35] I hope you are clear with all the types of inheritance.
[04:38] Now let me show you why Multiple inheritance is not allowed inside Java.
[04:42] Think like for a second
[04:44] java is allowing Multiple inheritance.
[04:46] Here you can see
[04:48] first I have a superclass which is class A, and inside this I have a method which is Sample.
[04:54] The same is being extended by two different subclasses like B and C and in.
[05:00] Both of these subclasses, the sample() is being overridden by the developer.
[05:05] Now, if both of these subclasses, like B and C are being extended by another subclasses with the help
[05:11] of Multiple inheritance, then my class D will not have any clue which sample() method it has to inherit,
[05:20] like here
[05:21] the class B is also giving a sample() method, and the class C is also going to give a same sample() method
[05:27] with that my subclass, which is d, it is going to have a confusion or " Ambiguity " around which sample()
[05:34] method it has to inherit.
[05:36] So this kind of problem we call it as a " Diamond " problem.
[05:39] Because you can see we are getting that diamond shape here due to this diamond problem
[05:44] only inside Java Multiple inheritance is not allowed.
[05:49] When we are trying to extend multiple Java classes.
[05:53] I hope you are clear when we are discussing about the interfaces in the coming lectures, I'm going
[05:58] to explain you how to achieve these Multiple inheritance with the help of Interfaces.
[06:04] So please have these details around the types of Interfaces handy whenever you are going for an interview.
[06:10] Because most of the times people may ask you what are the types of inheritance available inside Java
[06:16] and why
[06:17] particularly Multiple inheritance is not supported by Java.
[06:21] In such scenarios, you can try to explain about all the inheritance that we discussed, but please
[06:26] make sure you are also highlighting about that diamond problem.
[06:29] Along with that, please also highlight that we should not say that Java is not going to support Multiple
[06:36] inheritance.
[06:37] There is a workaround in Java to implement Multiple inheritance with the help of Interfaces.
[06:43] So this is how you need to answer the questions around the Multiple inheritance and the types of inheritance.
[06:49] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
