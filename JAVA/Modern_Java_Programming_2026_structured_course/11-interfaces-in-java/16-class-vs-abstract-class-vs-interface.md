# 11.16 — Class Vs Abstract Class Vs Interface

> Section 11: Interfaces in Java

[00:00] As of now, we discuss everything about what is a class, what is a abstract class, and what is an
[00:06] interface.
[00:07] Inside this lecture, I want to spend a few minutes explaining about the differences between these three
[00:13] different components.
[00:14] Understanding them is very important, otherwise you may get confused very easily.
[00:20] First, if you start with the inheritance, both the class and abstract class, they support a single
[00:27] inheritance, whereas with the help of interface we can achieve multiple inheritance.
[00:33] The next point that we have is, around the implementation or the creation of the object.
[00:39] Can we create an object of a class?
[00:40] Off course we can create.
[00:42] That's why I have mentioned can be instantiated.
[00:45] Whereas both abstract class and interface, we cannot instantiate them or we cannot create an object
[00:52] of them.
[00:53] Coming to the constructor, both the class and abstract class, they can have constructors, whereas
[00:58] inside interface constructor eaters are not allowed.
[01:01] And here you may have a question.
[01:03] We said abstract class cannot be instantiated.
[01:07] Then why
[01:08] abstract class can have constructors?
[01:10] Because constructors can only be used during the object creation.
[01:15] If we will not be able to create an object of abstract class, then why constructors are allowed inside
[01:20] an abstract class.
[01:21] So that's a question you may have here.
[01:23] Let me try to answer the same.
[01:25] Like we discussed in the previous sections, whenever a abstract class is inherited by a class inside
[01:32] the subclass constructor, the compiler automatically is going to add the super keyword to invoke the
[01:39] abstract class constructor.
[01:40] Why Java compiler is going to do that automatically?
[01:43] Because abstract classes, they can have some instance fields the same are going to be inherited by
[01:50] the normal subclass.
[01:51] So when we are trying to create an object of a normal class, all the instance fields present inside
[01:58] the class and the abstract class, they're all going to be initialized or created as part of the object
[02:05] creation of the subclass.
[02:06] So to support these initialization, abstract class also should have an its own constructor, which
[02:13] is going to be invoked from the subclass constructor with the help of super keyword. Coming to the methods
[02:19] and fields inside class, we can write all kinds of methods except abstract methods.
[02:25] Like
[02:25] we can write a concrete method, static method, and we can have non static and we can have static fields,
[02:31] instance fields.
[02:33] The only limitation inside a class is we cannot define an abstract method.
[02:38] Coming to the abstract class
[02:40] it can have an abstract method, concrete method, static method and all type of fields are allowed
[02:46] inside abstract class, whereas inside interface we can only have constant static fields, default method,
[02:53] abstract method, static methods and private methods. Even abstract class and normal class
[02:59] also they can have private methods coming to the purpose.
[03:03] The purpose of classes is to create the objects and define behavior as part of the class definition.
[03:09] Whereas abstract class purpose is to provide a base for all the derived classes or for all the subclasses
[03:17] and define some common behavior.
[03:19] Whereas interface main purpose is to define a contract or a behavior in a more abstract manner.
[03:27] If you want to simply define a contract and don't worry about providing any implementation logic, then
[03:34] always interface is a good choice, whereas abstract class can be a good choice if you want to provide
[03:39] some base functionality as some common functionality with the help of concrete methods followed by.
[03:45] You can also define some abstract methods inside abstract class.
[03:49] Coming to the access modifiers, we can use public, protected and private access modifiers for the
[03:55] methods in class, and the same applies for the abstract class.
[04:00] Whereas inside interface by default all methods are going to be public if needed
[04:04] we can define default methods and private methods as well.
[04:09] And the last point that I have here is relationship to the subclasses.
[04:12] If a class is being inherited by another subclass, then the superclass is going to act as a blueprint
[04:19] for that derived class.
[04:20] Whereas coming to the abstract class, like I said, it is only going to act as a base by providing
[04:26] some implementation details.
[04:29] And with an interface, we can define a contract for all the implementation classes.
[04:34] I hope you understand all these differences, all the points that we also discuss.
[04:39] I mentioned inside the slide for your reference.
[04:42] I also have a couple of memes around interfaces, abstract classes and inheritance.
[04:47] Like you can see, this is a funny definition of abstract class
[04:51] in a nutshell, the combination of interface and inheritance
[04:55] we are going to get the abstract class.
[04:57] I hope you like this funny meme.
[04:59] Moving on to the second meme, someone is trying to identify the differences between interface and abstract
[05:06] class.
[05:06] But from Java 8, since the default method static methods, private methods, everything is allowed.
[05:12] The difference between these interface and abstract class is reduced drastically.
[05:18] That's why, on a funny note, we can say slowly interface is trying to become an abstract class.
[05:24] That's why this lady here, she's also telling they are the same picture.
[05:29] I'm not able to identify any differences between them.
[05:31] It is true to some extent, but like we discussed just now, there are some minute differences between
[05:38] an abstract class and interface.
[05:41] On a funny note, we can always say they both are same.
[05:44] Before I try to close this lecture, I want to highlight about the Sealed interfaces.
[05:48] Like we discussed in the previous section, there is a concept of Sealed classes using which a superclass
[05:54] can select its own subclasses.
[05:57] Very similarly, using Sealed interfaces
[05:59] also, we can permit list of implementation classes that can inherit your Sealed interface.
[06:06] Here you can see
[06:07] first we need to mention sealed keyword followed by interface, followed by your interface name and
[06:12] after the interface name with the help of permits keyword
[06:15] you can mention the list of classes. Like here
[06:19] I'm trying to mention Dog and Cat, and with that, only these two classes will be able to inherit or
[06:26] implement this sealed interface.
[06:29] I hope you are clear.
[06:30] Thank you,
[06:31] bye.


########################################
