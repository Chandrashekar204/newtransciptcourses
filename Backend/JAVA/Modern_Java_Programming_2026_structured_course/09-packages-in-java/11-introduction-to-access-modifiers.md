# 9.11 — Introduction to access modifiers

> Section 9: packages in Java

[00:00] As of now, whenever we are trying to create a Java class or a Java method or a Java field, in all
[00:06] these scenarios we are using the public access modifier.
[00:11] But apart from public access modifiers, there are other access modifiers also available inside Java.
[00:17] Since these access modifiers are tightly coupled with the concept of packages, I have not discussed
[00:23] about them as of now.
[00:25] But now since we know everything about the packages, it is the right time to discuss about the access
[00:31] modifiers in Java.
[00:32] So what is our purpose of access modifiers in Java?
[00:35] With the help of these access modifiers, we can specify what is the visibility of our Classes,
[00:42] Methods and variables or fields, which means I can control who can access my class or who can access
[00:50] my methods and variables.
[00:52] In Java there are four access modifier.
[00:54] The very first access modifier that we have is public.
[00:58] We are using these public access modifier a lot.
[01:01] as of now.
[01:02] Whenever we are using these modifier as part of the class definition or method definition or variable
[01:08] declaration.
[01:09] In those scenarios we are letting to access our class, our method, our variable from anywhere.
[01:16] When I say anywhere within the class or outside the class, or from any other class which is present
[01:22] inside another package. There are no restrictions
[01:25] anyone can access our class, method
[01:28] or variable. The next access modifier that we have is private.
[01:31] So this is completely opposite of public.
[01:34] Whenever we are defining a private access modifier for a class, method or a variable, it can only
[01:40] be accessed within the same class where it is declared.
[01:44] Here you may have a question which is how can I access a class within a class for that
[01:49] the answer is very simple.
[01:50] Java allows you to declare inner classes as part of a outer class.
[01:55] That means your Java class can contain other Java classes.
[01:58] When you make your inner class as an private class, that class can be only be accessed within the same
[02:06] class, whereas for methods and variables, it should be pretty clear for you.
[02:10] If you define a private method or a private variable, the method or variable can only be accessed within
[02:17] the same class.
[02:17] So understanding public and private should be pretty simple.
[02:21] The third access modifier that we have is protected, when we define a class, our method or variable
[02:27] as protected.
[02:28] In such scenario, the class
[02:30] or method
[02:31] or variable can only be accessed by the classes in the same package, and subclasses which are present
[02:39] inside or outside of the same package.
[02:41] So what is a subclass?
[02:43] Subclass is a concept that we are going to discuss as part of the inheritance concept.
[02:48] Using the inheritance concept, a Java class can inherit another Java class.
[02:53] That means a Java class can act as a parent to the child Java class.
[02:58] In this kind of scenarios, the child class we can call it as subclass.
[03:02] So more details about subclasses inheritance we are going to discuss in the coming sections.
[03:07] For now
[03:07] please note that when we define a access modifier protected, all the classes in the same package can
[03:14] access our class, method or variable.
[03:17] But if one of the class which is outside of the package is trying to access them, they will be able
[03:23] to access only if the class is a subclass of the given class where we have defined the protected access
[03:29] modifier.
[03:29] I know it may be confusing to you to understand about protected.
[03:34] Don't worry, when we discuss about inheritance it is going to be super clear for you.
[03:38] For now, please focus on that definition.
[03:40] Next, moving on to the last access modifier which is default.
[03:44] If you are not mentioning any access modifier for your class, method or variable, then behind the
[03:51] scenes Java is going to consider that default access modifier.
[03:55] Whenever we are using the default access modifier, it is going to provide package private access that
[04:02] means any class, method or variable which are using default access modifier
[04:08] they can only be accessed within the same package, but not from the outside of the package.
[04:14] I hope you are clear with these definitions.
[04:16] Always make sure you are using the access modifiers to control the access to your classes, methods
[04:23] and variables.
[04:24] You should not build a business logic by using completely public access modifier or private or protected
[04:31] or default.
[04:32] You should use a mix of these modifiers based upon your business requirements.
[04:37] If there is a method which is going to be accessed to only within the same class, then in such scenarios
[04:43] it is always makes sense to make that method as private instead of public.
[04:48] Why do you want to unnecessarily expose your method to the other classes or other packages?
[04:53] So these kind of restrictions you can achieve with the help of access modifiers in Java.
[05:00] Let me show you a very quick example here.
[05:02] Like you can see here, I have a class which is MyClass.
[05:05] For the class I have given the access modifier as public and inside my class there are multiple variables
[05:11] that I have defined like publicVar, privateVar, protectedVar.
[05:15] So for these variables I have mentioned the access modifiers like public, private, protected.
[05:20] Whereas for the last modifier I have not mentioned any access modifier.
[05:24] That means the last variable which is defaultVar, it is going to have the access modifier default
[05:30] behind the scenes.
[05:31] In the similar lines, we can also define any number of static or non static methods by using these
[05:37] access modifiers.
[05:38] The very first method is using the public access modifier followed by private access modifier in the
[05:45] second method, and the third method is using protected access modifier.
[05:48] Under class, we have a method where we have not mentioned any access modifier.
[05:53] Since we have not mentioned any access modifier for the last method, it is going to follow the default
[06:00] access modifier behind the scenes.
[06:02] So this is the syntax on how to use this access modifiers as part of the class definition
[06:08] or method definition
[06:09] or variable declaration.
[06:11] Inside these examples, like you can see, since publicVar and publicMethod has a access modifier
[06:17] public, they can be accessed from anywhere inside your project, even from other packages, whereas
[06:24] privateVar and privateMethod they can only be accessed to within the same class.
[06:29] Now coming to the protectedVar and protectedMethod, they can be accessed within the same package
[06:35] by any class or any subclass of the MyClass, which is present even if it is present outside of the
[06:41] package.
[06:42] So what is the class name here?
[06:43] MyClass.
[06:44] So any class which is extending or inheriting my class, it is going to become a subclass.
[06:50] So the subclass can be present in the same package or in other package.
[06:54] So such subclasses, they can access my protected method and protected variable even though they are
[07:00] present in other packages.
[07:02] And at last coming to that default variable and default method, they can only be accessed within the
[07:08] same package.
[07:10] Here I want to highlight one important point though.
[07:13] I made my class as public the content of the class I'm not trying to allow to access by others with
[07:20] the help of the private access modifier.
[07:22] Similarly, think like I might have declared the class as default in such scenarios, even if I have
[07:28] public methods and public variables inside my default class, the classes present inside another packages
[07:35] they cannot access my public method and the public variables.
[07:38] The reason is, whenever they want to access any of the methods or fields of a class, first, they
[07:44] should be able to access the class without accessing the class
[07:48] they cannot access the method and variable even though they marked as a public.
[07:53] So always class is the very first entry.
[07:56] Once you are able to access the class post that only you should be able to access the Java fields and
[08:02] Java methods based upon the access modifiers defined.
[08:05] I hope you are clear.
[08:06] I know you may have some questions around these access modifiers.
[08:09] In the next lecture, let's try to create some examples to clear our understanding around the access
[08:15] modifiers.
[08:16] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
