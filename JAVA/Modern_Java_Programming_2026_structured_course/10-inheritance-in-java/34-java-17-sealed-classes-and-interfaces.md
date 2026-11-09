# 10.34 — [JAVA 17] sealed classes & interfaces

> Section 10: Inheritance in Java

[00:00] In the previous lecture, we saw the demo of how to disable the inheritance using the final keyword.
[00:07] So whenever we are using the final keyword, we are stopping no other class to inherit.
[00:13] And in case if we are not using the final keyword every other class, they can inherit my superclass.
[00:20] So it is like either going completely with Inheritance or not going with the Inheritance.
[00:26] We don't have any middle solution where I'm going to allow the Inheritance only to the set of subclasses
[00:34] to achieve the same.
[00:35] Inside Java 17, the Sealed classes and interfaces are introduced. With the help of a Sealed class
[00:44] we can permit which subclass can inherit a superclass.
[00:49] For example, here you can see I have created a Sealed class with the name Person.
[00:54] So the keyword that you need to use is just before your class keyword
[00:58] you need to use the Sealed keyword.
[01:00] After defining public sealed class Person, you need to use the permits keyword and after that permits
[01:07] keyword
[01:08] you can mention the list of subclasses to which you want them to inherit the Person superclass.
[01:14] This way, with the help of the sealed classes, the developers, they are going to have more control
[01:21] on inheritance by controlling which subclasses can inherit from a given superclass.
[01:27] But like I said, this feature is only available from Java 17.
[01:33] It is introduced in Java 15 as a preview feature, but from Java 17 it is fully enabled.
[01:40] Let's try to create a sealed class and see how it is going to work. For the same,
[01:44] first, let me try to close all my classes post that I'm going to create a new package, and the package
[01:51] name that I'm going to give here is, com.eazybytes.marvel.sealed inside this package
[01:58] first I'm going to create a new superclass with the name Person.
[02:03] I know we already have a superclass with the name Person, but since that is present inside a different
[02:08] package which is base, my Java compiler also is not going to complain anything because we are creating
[02:15] two different classes in two different packages, and that is perfectly allowed inside Java.
[02:20] So let me create this Person class.
[02:22] So like we discussed, first we need to mention sealed keyword just before the class keyword.
[02:29] Once we define the sealed keyword, immediately we are going to get a compilation error saying that
[02:34] we have defined the sealed class, but we have not defined any subclasses that are allowed to inherit
[02:41] from this Person
[02:42] superclass.
[02:43] Before I try to define some subclasses with the help of permits keyword, first let me try to create
[02:48] few other classes in the same package inside the same package
[02:52] first, I'm going to create a new class with the name student, and I'm going to keep this class empty
[02:58] for now.
[02:59] Very similarly, I'm also going to create one more class which is Employee.
[03:04] Now I have two different classes, which is Student and Employee to these new two classes that I have
[03:10] created.
[03:10] I want them to allow to inherit the Person superclass.
[03:15] So how to do that,
[03:16] we need to go to the sealed Person class.
[03:18] And here we need to type permits followed by what are the subclasses name.
[03:24] First I'm going to mention Student followed by comma Employee.
[03:28] This way we can define any number of subclasses by using the comma separator.
[03:35] So as soon as we add these new classes to the permits keyword, we are getting a compilation error saying
[03:41] that as a sealed class, you have permitted the subclasses to inherit from the Person superclass, but
[03:47] they are not inheriting the superclass.
[03:49] That's a compilation error
[03:50] right now we are facing.
[03:52] So to resolve this, first we can go to the Student subclass and here I can simply mention extents followed
[03:59] by Person.
[04:00] Let me do the same for Employee as well.
[04:03] Here also I'm mentioning the extents followed by Person.
[04:06] As soon as we try to extend the Person sealed class, we are getting compilation error inside the Employee
[04:14] and Student as well.
[04:16] So let's try to understand why we are getting these compilation error.
[04:20] So whenever a subclass is trying to extend from one of the sealed class, then in such scenarios the
[04:26] subclass it needs to mark itself either as a sealed class or a non sealed class or a final class.
[04:34] So if I update these Student class as final, you can see the compilation error is resolved.
[04:41] So with this we are telling that Student class is not going to be inherited by any other subclasses.
[04:47] So this kind of confirmation we need to give to the compiler by either mentioning final sealed or non
[04:54] sealed.
[04:54] Let me go to the Employee here
[04:56] also, you can see I have three options to resolve this
[04:59] compilation error.
[05:01] So let me go to the more actions.
[05:03] The very first option is marking the class as final like we did for the Student class.
[05:08] The second option is I can mark the Employee subclass as sealed.
[05:13] If I mark my Employee class as sealed, then immediately it is going to ask me to provide the what are
[05:20] the permitted subclasses.
[05:22] If I don't have any intentions to allow these Employee class to act as a superclass for other subclasses,
[05:29] then there is no need of defining the sealed here.
[05:32] We can roll back and with that we are going to left with the final option which is non sealed.
[05:39] If I mention this non sealed keyword inside my class definition.
[05:43] In that scenario, I am making this Employee class to be inherited by any other class inside my Java
[05:51] project.
[05:52] That means when we use this non sealed, we are not going to restrict any restrictions.
[05:58] Whoever want to inherit my Employee as an superclass.
[06:02] So these are the rules that you need to follow.
[06:04] The rule number one is inside your superclass
[06:07] you need to make sure you are mentioning the sealed keyword, followed by permits and the list of subclasses.
[06:12] The subclasses they need to make sure the class is marked either as final sealed or non sealed.
[06:20] If they mark themselves as sealed classes
[06:22] then again, my subclass also need to define permits keyword followed by list of other subclasses.
[06:29] So these are the basic rules that you need to be aware when you are trying to build sealed classes.
[06:35] Apart from these rules, there is also one more rule that you need to be aware, which is if you didn't
[06:40] build your Java project with the help of Java modules, then you need to make sure all your sealed classes
[06:48] and its subclasses are present inside the same package.
[06:51] As of now, we are only using the packages to build the Java classes inside our Java project.
[06:57] We are not using the Java modules which are introduced in Java 9, but if a given Java project is
[07:03] implemented with the help of Java modules and packages, in such scenarios, the condition is your sealed
[07:09] class and subclasses can be in different packages, but all these different packages they should be
[07:14] present inside a single module.
[07:17] I hope you are clear with all the explanation around the sealed classes.
[07:21] Whatever rules are constraints that we discussed around the sealed classes, I have highlighted all
[07:26] of them inside this slide for your reference.
[07:29] Just like how we have sealed the classes, we also have sealed interfaces. Even for interfaces
[07:35] also the sealed mechanism or
[07:37] the sealed concept is going to work in a very similar fashion.
[07:41] Since we are to discuss about the interfaces, it may not be clear for you on how to create an Interface.
[07:47] What is the purpose of interface?
[07:49] So don't worry, we are going to talk about the interfaces in the coming sections.
[07:53] But for now, please note that even for the interface also we can use the same keyword sealed, permits.
[07:59] Using these permits and sealed, we can also build a selective inheritance for interfaces as well.
[08:06] And overall, if you ask me, what is the advantage that we are getting with the sealed class and sealed
[08:10] interfaces is, they are going to provide an useful tool for designing more secure and flexible class
[08:19] hierarchies inside Java, particularly if you are going to work in an enterprise Java project where
[08:25] they are going to have thousands of Java classes and interfaces,
[08:28] in such scenarios, it is always advisable to go with the inheritance selectively
[08:34] with the help of these sealed classes and the interfaces.
[08:38] I hope you are clear about these sealed concepts.
[08:41] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
