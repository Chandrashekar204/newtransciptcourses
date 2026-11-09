# 10.6 — Inheritance Demo - Part 2

> Section 10: Inheritance in Java

[00:00] In the previous lecture, we implemented Inheritance inside our Java project and we also validated all
[00:07] our subclasses.
[00:09] They are able to inherit the methods and fields from the parent class, which is Person.
[00:14] So what is the advantage that we're getting with Inheritance here?
[00:18] The advantage is we are maintaining all the common logic or the common Java fields in a single place.
[00:25] So this is going to give a great advantage to the developers.
[00:29] Think like in future, if someone wants to change the logic that we have written inside the each method,
[00:35] they need to change at a single place which is inside the Person parent class, and the same is going
[00:41] to be reflected in all the subclasses.
[00:44] So this brings reusability as an advantage.
[00:49] You can write your code at one place, and you can reuse that in many other places like subclasses.
[00:56] And here you may have a question which is I do understand that my subclasses are child classes
[01:01] they are able to inherit the properties and the behaviors from the parent class.
[01:06] But does that mean that my child classes they have to live with this behavior
[01:11] off course not.
[01:12] In case if your child class, if they want to override the logic present inside the parent method,
[01:18] they can do that happily by defining the same method inside the subclass.
[01:24] And similarly they can also override the Java fields as well.
[01:28] So all the overriding logic we are going to talk in the coming lectures.
[01:32] For now, let's try to focus on the basics of Java inheritance.
[01:36] So in the previous lecture, I showed a demo from the Marvels main() method that my IronMan class is
[01:43] able to access the all the methods that are present in the parent class.
[01:49] There is also a another shortcut that you can use to validate what are all the methods and fields that
[01:55] are derived or inherited by a subclass from its superclass.
[02:00] The shortcut is you can go to any of your subclass like I'll go this time to the SpiderMan.
[02:05] Here I'm going to look for the list of methods and fields available inside my given class.
[02:12] So inside my given class, like SpiderMan, I'm trying to press a shortcut which is command F12,
[02:19] and inside windows the shortcut is going to be control F12.
[02:23] So here there are three checkboxes like inherited members
[02:27] anonymous classes or lambdas.
[02:29] So if I try to uncheck these inherited members you will be able to see only the methods and fields available
[02:37] inside these given class.
[02:39] But if I select these checkbox which is inherited members, I'll be able to see all the methods and
[02:46] fields that are inherited by my subclass from its superclass.
[02:50] So you'll be able to see other methods like eat(), sleep(), walk().
[02:55] So these are all the methods that are inherited from the person superclass.
[03:00] There are other methods also which are inherited from the object.
[03:03] We'll discuss about the object superclass in the next lecture.
[03:07] For now, let's focus on only the person superclass, because we are explicitly inheriting the properties
[03:14] and behaviors from the Person superclass.
[03:17] So if you select any of the method like eat() method, you'll be able to see that this method is inherited
[03:24] from the Person.
[03:25] That's why you are able to see these arrow marks as well.
[03:28] Whereas for the usePower() method, you're not able to see any of the arrow marks or any of the superclass
[03:34] name, because this method is directly defined inside the given subclass.
[03:39] And similarly, if you go to the fields like age and name, you'll be able to see that these are also
[03:45] inherited from the Person superclass, and for them, the icon you'll be able to see there is a lock
[03:51] icon, which means these are defined as protected variables.
[03:56] Whereas for the methods like eat() and sleep() and walk(), you are able to see an icon which is open lock.
[04:04] Since we define the methods as public,
[04:07] so that's why we have this symbol.
[04:08] So this is one of the shortcut that you can use to always understand what are the methods and fields
[04:15] that are derived by my subclass from its superclass.
[04:20] Can we validate the same for CaptainAmerica as well.
[04:23] So I'm trying to press command F12 here.
[04:25] So here also we have all the methods from the Person superclass.
[04:29] And we also have the fields.
[04:31] So the same you can also validate inside the IronMan as well.
[04:34] So let me press F12.
[04:36] So here also we have the fields and methods.
[04:39] If you try to select any of the method which is inherited from the Person, it will take you to the
[04:44] Person superclass where this method is defined.
[04:48] So this is the beauty of intelliJ.
[04:50] That's why in real projects it is always advisable or mandatory to use IDE's like IntelliJ, Eclipse,
[04:57] NetBeans.
[04:58] They are going to make our life
[05:00] super easy.
[05:01] So as of now we are only inheriting from one of the class which is Person.
[05:06] But here you may have a question which is can I inherit from more than one class?
[05:12] The answer for this question is no.
[05:14] In Java, a single subclass cannot inherit the methods or fields from multiple Java classes.
[05:21] So if I try to put one more class name like MarvelsMain, you can see here I'm getting an compilation
[05:28] error saying that class cannot extend the multiple classes.
[05:32] So always please note that in a single subclass you cannot inherit or extends from multiple classes.
[05:40] We are going to talk more about these in the coming lectures.
[05:43] But now I just wanted to share this important note.
[05:46] So as of now my Person is being inherited by my IronMan, so can any other subclass can inherit my
[05:54] IronMan,
[05:55] off course it can inherit.
[05:56] For example, if I go to the MarvelsMain here, I can try to add the extends and mention any of the
[06:03] subclass like IronMan.
[06:05] So this way the inheritance can go to up to any level, like a parent will have a child, and a child
[06:12] can have its own child.
[06:14] So that kind of chaining of inheritance is always possible in Java.
[06:19] I hope it is clear.
[06:20] Let me remove this extends keyword inside this MarvelsMain because it is not necessary here.
[06:27] As a next step, let me go to any of the subclass and press command F12 to see my class structure.
[06:34] You can see there are good amount of methods are being inherited from the class called object.
[06:40] So the methods like clone(), equals(), finalize(),
[06:43] getClass(), hashCode(), notify(),
[06:46] notifyAll(),
[06:47] sleep(),
[06:47] wait().
[06:48] This confirms that our class is also inheriting the behavior from the object superclass.
[06:55] But we know where given the object to superclass inside our extends keyword.
[07:00] If you go to any of the class like MarvelsMain here
[07:03] also there is no extends keyword and we are not inheriting any of the class including object.
[07:09] But if you still press the command F12, you will be able to see the all the methods that are inherited
[07:15] from the object superclass.
[07:17] So why is this happening?
[07:19] Let's try to understand the same in the next lecture.
[07:22] Thank you
[07:23] bye.

----------------------------------------
