# 10.32 — abstract methods and classes - Part 2

> Section 10: Inheritance in Java

[00:00] In the previous lecture, we have created an abstract class with the name Subject and inside this abstract
[00:06] class we have created an concrete method with the name totalMarks().
[00:10] And we also created an abstract method with the name teach().
[00:13] Now let's try to understand how the abstract classes is going to behave when they are inherited by a
[00:21] subclass.
[00:22] For the same, I'm going to create a new package inside my com.eazybytes.marvel
[00:28] the package name is going to be com.eazybytes.marvel.subjects.
[00:34] Inside this package
[00:35] first I'm going to create a new class with the name Mathematics.
[00:41] So these are class name.
[00:42] Now here I'm going to type extends keyword followed by I'm going to extend the abstract class which
[00:49] is Subject.
[00:50] As soon as I extend you can see it is showing an compilation error saying that inside the abstract class
[00:57] that we are trying to extend, there is an abstract method with the name teach().
[01:01] Since I have not implemented any business logic and I have declared my class as concrete class, it
[01:08] is throwing an error to me.
[01:10] Hey buddy, you have an abstract method inherited from the superclass, but you have not implemented
[01:16] any business logic inside it.
[01:18] So to resolve this error, we can try to run this and go to more actions.
[01:23] Here we have two options.
[01:25] One is either we canent the implem abstract method inside the subclass and make it as a concrete method,
[01:32] or we can make the Mathematics class also as an abstract class.
[01:37] On the left hand side you can see it is showing me code recommendation.
[01:41] If I hover on the implement methods, it is asking me to override a method with the name teach().
[01:47] So let me select the first option and post that I'm going to click on this okay button.
[01:52] Here you can see right now the IntelliJ IDEA
[01:56] It has given me an concrete method with an empty body.
[02:00] So inside this I can write my business logic, which is I am trying to teach mathematics.
[02:08] With this, you should have got some good clarity about the purpose of abstract classes and abstract
[02:14] methods.
[02:15] With the help of abstract classes and abstract methods, we are going to build some guidelines to the
[02:21] subclasses to follow.
[02:23] So inside my abstract class I have only implemented the business logic which is mandatory or which is
[02:30] going to be common for all my future subclasses.
[02:34] And the remaining unnecessary or the business logic, which is going to vary greatly from one subclass
[02:40] to other subclass.
[02:41] So such methods I have defined them as abstract methods like you can see here.
[02:47] So inside an abstract class we can define concrete methods,
[02:50] we can define abstract methods.
[02:52] And very similarly if needed we can also define instance variables, static variables, static methods.
[02:58] So the abstract class is going to be very normal to the concrete class.
[03:03] There is only one difference between concrete class and abstract class, which is we will not be able
[03:10] to create the object of your abstract class, because since we have not defined complete business logic
[03:17] inside an abstract method, Java is not going to allow you to create the object of abstract class.
[03:24] So that's the only difference between a normal concrete class and an abstract class.
[03:29] Here, let me try to create a instance variable which is public int marks.
[03:35] Very similarly, I can try to create a static variable which is public static int minMarks.
[03:43] I can also mark this minMarks as final because this value I don't want to change anywhere inside my subclass,
[03:50] so I'll keep the value as zero.
[03:52] That means the minimum number of marks that is going to be secured by someone in a subject is going
[03:58] to be zero.
[03:58] This way you can always try to create instance variables, static variables, static methods, instance
[04:05] methods very similar to concrete class inside a abstract class as well.
[04:09] But the advantage that we have with the abstract class is we can also define the abstract methods.
[04:14] Now let's try to understand a few rules and guidelines around the Abstraction concept or abstract class
[04:21] or abstract method concept.
[04:23] The very first rule is when you are defining a class as abstract.
[04:27] That doesn't mean you should always have at least one abstract method inside it.
[04:32] It is not a mandatory to have at least one abstract method.
[04:35] For example, even if I try to remove these, I'm not going to get any compilation error.
[04:40] You can define a class as an abstract
[04:43] if you think in future there might be a business requirement for you to add abstract methods.
[04:48] In such scenarios, you can happily mark a class, an abstract class, and you can define concrete methods
[04:55] without any abstract methods. And in future, whenever you want to
[04:59] introduce abstract methods, you can happily introduce them like you can see here.
[05:05] The next rule that you need to be aware is, whenever a subclass is extending your abstract class, it
[05:12] is not mandatory for the subclass to override your abstract methods.
[05:17] For example, I can remove these overridden method and I can make my Mathematics class as abstract class.
[05:25] Even IntelliJ is also recommending one of that as a solution.
[05:29] If you click on this more actions, you can see I have a solution, which is I can make Mathematics
[05:35] as abstract.
[05:36] And with that there won't be any compilation error.
[05:39] So now inside my Mathematics I can define other concrete methods and other abstract methods.
[05:46] That means any other concrete subclass which is going to extend my Mathematics superclass.
[05:52] It is going to get all the methods inherited both from subject and Mathematics super classes.
[05:58] I hope you are clear.
[05:59] Let me roll back and make this class as a normal class and bring back these teach() method.
[06:04] The next important rule that you need to be aware is we cannot create an object of an abstract class.
[06:12] For example, I can go to any of the class like ConstructorDemo here
[06:16] if I try to create an object of subject, I'm going to get a compilation error.
[06:22] Let me show you the same.
[06:24] You can see I'm getting a compilation error
[06:26] saying that subject class is abstract cannot be instantiated.
[06:31] So this is one of the major difference between a concrete class and abstract class.
[06:37] So that's why never ever try to create an object of abstract classes.
[06:42] So let me remove this piece of code.
[06:43] The next rule that you need to be aware whenever we are trying to define an abstract method is you can't
[06:49] define an abstract method as private like you can see here
[06:53] I'm going to get an compilation error.
[06:56] The reason is if you make a method as private, the same is not going to be inherited by the subclass.
[07:02] And with that, they will never be a scenario where someone is going to define the business logic for
[07:08] this abstract method.
[07:09] That's why please don't try to create private abstract methods.
[07:13] You're going to get a good compilation error. On the similar lines
[07:17] you can't define an abstract method as an static method.
[07:22] If I try to type static here, I'm going to get a compilation error.
[07:25] Because static methods are applicable to a Java class, they're not belongs to any subclass, or they
[07:33] are not belongs to any object of a class.
[07:36] So that's why even defining the static abstract methods is also not allowed.
[07:42] So let me remove this static keyword.
[07:44] With that, the compilation error is going to be resolved.
[07:48] The next rule that you need to be aware is, you cannot mark your abstract class as final.
[07:54] The reason is, whenever you are making a class as final, you are making your class to be not inherited
[08:02] by any other subclass.
[08:04] If you are not allowing your class to be inherited by another subclasses, then there is no meaning
[08:10] of defining the abstract methods and abstract classes in Java, because without inheritance, the abstract
[08:18] methods and abstract classes that you are going to write, they are going to be useless because no one
[08:23] is going to define a logic inside them.
[08:26] We are going to talk about final keyword in the coming lectures in detail.
[08:31] For now, please note that we can't define a final keyword inside the abstract class definition.
[08:38] Let me remove this final keyword.
[08:39] The next guideline that you need to take care while you're trying to create the abstract classes is,
[08:45] you should not create private constructors inside your abstract class.
[08:50] For example, here I can try to create a public constructor with the name Subject, and inside this
[08:58] I'm going to keep it as empty.
[08:59] You can see this is perfectly allowed, whereas if I try to change this access modifier of the constructor
[09:06] to private, I'm going to get a compilation error inside my subclasses, because we know by default
[09:13] every subclass constructor, they are going to have an super keyword to invoke the constructor of the
[09:20] superclass.
[09:20] That's why when you make your abstract class constructor as private, your subclass can never be able
[09:27] to execute the abstract class constructor.
[09:31] With that reason, we should always try to define the public constructors only.
[09:36] I hope you are clear.
[09:37] These are all the rules and regulations that you need to take care while you are trying to build the
[09:42] abstract classes and abstract methods.
[09:44] So with the help of abstract classes we can define 100% of the abstract methods are 100% of the concrete
[09:53] methods are a combination of concrete and abstract methods,
[09:57] so it's up to us.
[09:58] That's why in Java
[09:59] there is a saying we can achieve the 0 to 100% abstraction with the help of abstract classes, whereas
[10:07] with the help of Interfaces, only 100% Abstraction is allowed.
[10:12] We are going to talk about what is an Interface in the coming sections, but now please focus on only
[10:18] on the abstract classes.
[10:20] My humble request is try to create some abstract class and try to define some concrete and abstract
[10:26] methods inside these abstract classes.
[10:28] The same you can try to inherit in another subclass.
[10:31] If you try to do all these exercises, you're going to get used to the syntax on how to create an abstract
[10:38] method and the abstract class, all the concepts and the important details that we discussed around
[10:43] the Abstraction in Java.
[10:45] I have highlighted in all these slides, so please refer to them whenever you have some questions.
[10:51] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
