# 15.3 — Deep dive on getClass() in Object class

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Like we discussed in the previous lecture, the object superclass has so many methods.
[00:05] As a very first step, let's try to talk about one of the simplest method available inside object superclass,
[00:12] which is getClass().
[00:14] So let me open this getClass() method.
[00:16] So there are lot many new things you're going to see here.
[00:20] The very first observation that you may have here is what is the purpose of this native.
[00:24] And the second observation is what is the purpose of this question mark.
[00:28] And obviously the third observation is this method does not have any business logic.
[00:34] It seems this method is an abstract method, but there is no abstract keyword on top of that, this
[00:40] method is marked as final and in fact the Object class itself is not marked as abstract class.
[00:46] So what is going on here?
[00:48] You may be concerned about all these observations because they're not matching with what we have discussed
[00:54] in the previous sections.
[00:56] But don't worry, I'm going to share the details in a step by step manner so that you're going to be
[01:01] super clear around it.
[01:03] First, let's talk about the purpose of this native keyword.
[01:07] We as a Java developers, 100% of the time we are not going to use this keyword.
[01:12] This is only going to be used by the developers who build the Java library classes.
[01:18] Since we are going to build our own custom Java classes, we don't have to use this keyword.
[01:23] But if you ask me, what is the purpose of this native keyword?
[01:26] It's very simple.
[01:27] Whenever a method signature has this keyword, it is an indication to the JVM that the implementation
[01:33] logic of this method has written in the format of platform dependent native code.
[01:40] Behind the scenes
[01:41] this method logic might have implemented inside the JVM libraries with the help of platform dependent
[01:48] native code, by using the languages like C or C++.
[01:52] And with that, you may have another question, which is why can't we write the logic by using the Java
[01:58] language itself?
[01:59] Some library methods like this getClass().
[02:02] They may want to access low level details inside JVM.
[02:06] For example this method, it is going to go to the class details of an object at runtime.
[02:12] So since the evaluation is going to happen at runtime, this method has to check inside the JVM memory
[02:19] to understand what is the actual class to which a particular object belongs.
[02:24] So to handle these kind of methods where they need access at very low level of JVM Java team, they
[02:31] are going to build the methods with the help of native keyword.
[02:34] That's why the Java compiler is not throwing any error, even though there is no method body for this
[02:40] method.
[02:41] And with that, this method is going to be treated as a normal method.
[02:45] That's why there is no need of defining abstract keyword either in the method signature or in the class
[02:52] definition.
[02:52] I hope you are clear with the very first observation.
[02:55] And the second observation you might have is what is the purpose of this question mark?
[02:59] So the question mark here it is indicating a wild card.
[03:03] So what is a wild card?
[03:04] With the help of this wild card, we are able to build the method signature that can return any class
[03:10] detail at runtime based upon the object that we are trying to return.
[03:14] If I don't have this wild card, then for each and every Java class that I have inside my Java project,
[03:20] I need to build different, different methods with the different, different method
[03:24] signature. Wild cards and generics are advanced concepts inside Java, which we are going to discuss
[03:29] in the coming sections.
[03:31] For now, please note that this question mark indicates a wild card, which means at runtime, this
[03:37] getClass() method, it is going to return the details of any class based upon the object using which we
[03:44] are trying to invoke these getClass() method.
[03:46] So when we see the demo, it is going to make more sense to you.
[03:49] And at last you can see we have a final keyword inside the method signature.
[03:53] This also should give a confirmation to you that no subclass can override the logic present inside this
[04:00] method.
[04:01] They should be able to use this method without making any changes.
[04:05] I hope you are clear with this initial discussion around this getClass() method.
[04:09] Now let me show you a demo on how to invoke these method and what type of details that these method
[04:16] is going to return based upon the object that you are using to invoke this method to demo you the same
[04:22] like you can see, since we are into the new section, I have created a Java project with the name
[04:28] section_15.
[04:29] Inside this first I'm going to create a Java package.
[04:32] The Java package name is going to be com.eazybytes.ObjectDemo.
[04:40] Inside this package I'm going to create a Java class.
[04:44] The Java class name is going to be Person.
[04:47] But now this class is going to be empty.
[04:50] Let's not worry about defining the fields and methods.
[04:54] This empty class should be enough for our demo.
[04:57] The next class that I'm going to create under
[04:59] the same package is GetClassDemo.
[05:03] So inside this class I'm going to write the main() method and post that
[05:09] I'm going to create the object of Person.
[05:12] So to create the object of Person I'm going to write
[05:15] Person person = new Person().
[05:18] So the object reference is person.
[05:20] Since this Person is also a subclass of Object superclass, we should be able to invoke all the methods
[05:27] available inside the Object superclass.
[05:30] For example, by using these Person object variable reference, you can see I'm able to invoke the getClass()
[05:37] method.
[05:38] The return type of this getClass() method is Class.
[05:41] So on the left hand side I'm going to mention Class.
[05:45] So Class itself is a class available inside that java.lang package post that I'm going to give the
[05:52] name to the variable of the object of this class.
[05:56] So the object variable name is going to be prsnClass
[06:01] So whenever you invoke these getClass() method on top of any object at runtime, it is going to give
[06:08] that details of that Object class in the form of these class Object.
[06:14] So now using these class Object I should be able to invoke many other methods inside these class Class.
[06:22] For example, using these Person class I can invoke the methods like getName().
[06:29] Similarly, I will be able to invoke the other methods available like getSimpleName() and if needed
[06:37] I can also invoke getPackageName().
[06:41] If I try to execute this program, you should be able to see the details of this Person object like
[06:48] to which class this object belongs.
[06:50] What is the complete name,
[06:51] what is the package name to which this Person object belongs?
[06:55] So all those details we should be able to identify at runtime by invoking these methods.
[07:01] So let me execute this program.
[07:03] You can see get name will give you the complete qualified name.
[07:06] Whereas getSimpleName() will only give you the class name followed by getPackageName().
[07:12] It is going to give you the package name with the given Object class is present.
[07:17] I hope you are clear with the purpose of this getClass() method inside the Object superclass.
[07:22] This method is going to be super helpful to the developers whenever they are into a situation where
[07:28] they have a object in their hand at runtime, but they don't know to which class that object belongs.
[07:35] So in all such scenarios they can use these getClass() method to get the Object of this class.
[07:42] By using the Object of this class, they should be able to invoke these methods like getName(),
[07:47] getSimpleName(), getPackageName() to understand the complete details of a given object.
[07:53] So what is the object that we are trying to use here?
[07:55] Person object using the same, we are trying to invoke the getClass() method.
[08:00] Similarly, you can take object of any class inside your project.
[08:05] The code is going to be the same.
[08:06] You should be able to invoke the getClass() method using your object.
[08:11] Post that using the Object of class, you should be able to invoke the methods like getName(), getSimpleName(),
[08:17] name and getPackageName().
[08:19] I hope this is clear.
[08:20] Thank you,
[08:21] bye.

----------------------------------------
