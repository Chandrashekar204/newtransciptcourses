# 15.2 — Introduction to the methods in Object class

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] We have made a very good progress inside this course.
[00:04] As of now, you should be comfortable with the basics of Java.
[00:08] As a next step, I want to teach you about few of the advanced concepts like collections.
[00:14] Collections is an advanced concept inside Java, which is going to be challenging and interesting.
[00:19] But before we try to discuss about the advanced concepts of Java first, inside this section I want
[00:25] to teach you one of the basic concept inside Java, which is about the Object class.
[00:32] We know inside Java there is a class with the name Object inside the package java.lang.
[00:39] This is the superclass for all the classes that we have inside the JDK library, and all the custom
[00:46] classes that we create inside a Java project.
[00:49] So inside this class we have certain methods like clone(), equals(), finalize() hashCode() twoString().
[00:56] Inside this section I want to teach you more details about these methods.
[01:00] What is the purpose of these methods?
[01:02] There is a very good reason in Java on making these Object classes superclass and providing all these
[01:08] methods inside the Object superclass.
[01:11] We all know Object is a superclass for all the classes, either directly or indirectly.
[01:16] This is present inside the package java.lang.
[01:19] And this package is going to be present as part of the java.base module.
[01:24] So every class that you are going to use or create in Java is connected to this Object class in some
[01:31] or other way.
[01:32] If you think Java as a big family tree, all classes are going to be children or grandchildren or even
[01:40] great grandchildren of the Object class.
[01:43] In simple words, we can say Object class is the ultimate ancestor for all the classes in Java.
[01:49] It is at the top of the inheritance class hierarchy.
[01:53] Every class inside Java, they are going to have at least one parent, because by default, every class
[02:00] they are going to have object as a parent.
[02:02] But if you talk about the Object class itself, it is not going to have any parent class.
[02:07] So these are only class inside Java which does not have a parent.
[02:11] Since Object is a superclass for all the classes in Java, a reference variable of the Object class
[02:18] can be used to hold a reference of an Object of any class.
[02:22] For example, you can see
[02:24] first I'm trying to create an object reference obj of type Object itself.
[02:29] To this I can assign null and if needed, I can create an Object of this class itself with the help
[02:36] of this new object code.
[02:37] So this is perfectly fine inside Java.
[02:39] But the interesting part that I want to highlight here is, you can see first I'm trying to create a object
[02:45] of some class in Java, which is Person, the same Person object I can assign to the obj, which is
[02:53] the object reference of Object class.
[02:55] So this is perfectly fine because my Person class is a subclass of Object class.
[03:02] So what is this?
[03:03] This is Upcasting.
[03:04] So whenever you have the subclass on the right hand side and the object reference of superclass on the
[03:09] left hand side, we can call such assignment as Upcasting.
[03:13] Not only person, we can try to assign any class object to the obj object reference.
[03:20] Here you can see I have given some example.
[03:22] You can try to create an object of any class in Java, and the same you can assign to the obj Object
[03:28] reference.
[03:29] And this is going to work without any issues because every class inside Java is a subclass of Object
[03:35] class.
[03:36] But if you try to do the opposite assignment, you're going to get a compilation error like you can
[03:42] see here to the person Object reference
[03:45] if I try to assign the object of Object class, I'm going to get a compilation error because you're
[03:51] trying to assign an object of superclass to the object reference of the subclass.
[03:56] So this is not going to be allowed by default inside Java because this is Downcasting.
[04:01] But in the scenarios where you have some special kind of logic inside your program, you should be able
[04:08] to achieve the same by manually casting it like you can see here.
[04:12] Here you can see in the very first line
[04:14] I'm trying to assign the object of Person to the object reference of Object with the name obj2.
[04:21] Since I'm pretty confident that these obj2 contains the object of Person, I can do that Downcasting
[04:29] like you can see here. You should be familiar with these syntax.
[04:33] There's nothing new that I'm trying to discuss.
[04:35] I'm just trying to share with you that since the object is a superclass for all the classes, you can
[04:42] write these kind of logic inside your programs.
[04:45] Whenever you have some requirements inside your project, where you need to write a method which needs
[04:50] to accept any object, and the same needs to be processed inside the method.
[04:55] In such scenarios, you can use the Object class reference
[05:00] variables as the method input parameters.
[05:02] And with that, you don't have to build multiple methods accepting various kinds of objects.
[05:09] But with this downcasting that we are trying to do here, there is a drawback.
[05:13] Do you know what is the drawback?
[05:14] We are going to get a runtime exception if this casting fails at runtime.
[05:19] What is that exception?
[05:20] Come on, we discussed about it.
[05:22] It is class cast exception.
[05:25] So to avoid this ClassCastException, we can verify if the object reference variable contains an object
[05:31] of a class with the help of instanceOf operator like you can see on the screen.
[05:36] I hope you are clear on how the upcasting and downcasting is going to work with the help of Object
[05:42] Superclass.
[05:43] Now let's try to understand what are the methods available inside Object class. In total, the Object
[05:49] class in Java has nine methods that all classes can use.
[05:54] These methods are divided into two categories.
[05:58] The very first category is final methods.
[06:01] So whatever methods that I have highlighted under final methods, they are going to be final and you
[06:06] will not be able to change the logic present inside them, which means you have to use them as it is
[06:13] without making any changes inside your subclasses.
[06:17] So what are these methods?
[06:18] getClass(), notify(), notifyAll() and wait(), so there are some overloaded methods around
[06:25] wait().
[06:26] We are going to discuss in detail about all these methods.
[06:28] For now, let's try to understand the two categories of methods available inside the Object superclass.
[06:35] So under the first category we have all final methods.
[06:38] Whereas under the second category we have non final methods.
[06:43] Whatever methods that I have highlighted under the non final methods category, we can customize these
[06:49] methods based upon our business requirements by overriding them in the subclasses.
[06:54] So what methods we have under these non final methods toString(), equals(), hashCode() clone() and finalize().
[07:02] I also have a detailed table explaining the each of the method with a brief description.
[07:08] You can see inside the table.
[07:09] The very first column has the method name.
[07:12] The second column that we have here which is implemented, indicates that a given method has implementation
[07:19] logic provided by the Java library, and it can be used without writing our own custom implementation
[07:26] logic.
[07:26] For example, the hashCode() method that we have here, it is going to have a default implementation
[07:32] logic provided by the Java library, and we can use this method as it is without making any changes.
[07:39] Whereas the methods like finalize() and clone().
[07:41] If you want to use them, we should make some changes inside them in order to use them.
[07:47] It is going to make sense to you when we are discussing more details about these methods.
[07:52] For now, please note that what is this implemented conveys here.
[07:56] On the similar lines, we also have a third column which is overridden.
[08:00] So this column conveys whether a developer can override this method inside the subclass.
[08:06] So all the methods like hashCode() equals(), toString(), finalize() and clone().
[08:10] The developer can override these methods inside the subclass, whereas the methods like getClass(), notify(),
[08:18] notifyAll(), and wait() related overloaded methods.
[08:21] We cannot override them, and we are supposed to use these methods without making any changes.
[08:28] And at last we have a column with the name description.
[08:31] So this column is going to give a brief description about this method.
[08:35] For now I am not going to discuss all these methods in detail.
[08:39] This is just a summary table that I'm trying to provide here.
[08:42] From the next lecture, we can try to talk about these methods in detail along with the examples.
[08:48] I hope you are clear with the agenda of this section.
[08:51] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
