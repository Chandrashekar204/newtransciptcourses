# 11.14 — Marker Interface

> Section 11: Interfaces in Java

[00:00] Inside this lecture, let's try to understand what are Marker interfaces in Java.
[00:05] You won't be creating are going to use marker interfaces a lot inside your real projects.
[00:12] But I still want to cover about this topic because inside interviews people may ask about these Marker
[00:19] interface, what is the purpose of them and how to create them.
[00:22] That's why let's try to spend few minutes around these Marker interface.
[00:27] So what is a Marker interface?
[00:29] Just like you can see, this tin is an empty tin or empty box.
[00:34] Similarly, inside Java, a Marker interface is an interface that does not contain any methods and it
[00:41] is completely empty.
[00:42] Marker interface are also sometimes referred as tagging interfaces.
[00:47] Immediately you're going to get a question here, which is if Marker interfaces are empty interfaces,
[00:53] then what is the purpose of creating them and using them?
[00:57] Let me try to answer the same.
[00:58] Using these Marker interfaces, we are going to provide some metadata about a class indicating that
[01:07] some special behavior of the class to the compiler.
[01:10] In other words, whenever a class is going to implement a Marker interface, we are communicating to
[01:17] the compiler that my class.
[01:19] Since it is implementing so and so Marker interface, it is going to have a special behavior or a special
[01:26] characteristic that my compiler should aware.
[01:29] For example, inside the Java library we have two important Marker interfaces clonable and serializable.
[01:36] Let's quickly validate these interfaces inside IntelliJ.
[01:40] Inside IntelliJ, you can press the shortcut command O for the Mac operating system.
[01:45] Otherwise, for windows, you can use control O. Here inside the search box
[01:50] if you can type clonable, you will be able to see an interface inside the package
[01:56] java.lang.
[01:57] That's what I can see here,
[01:59] it is of type interface.
[02:00] So let me open this.
[02:01] If you can closely look at these interface.
[02:04] It is just an interface without any content inside its body.
[02:09] So this is a perfect example of Marker interface.
[02:12] If you try to read the documentation about this interface, there are clear instructions given that
[02:20] whenever an class is implementing these Marker interface, which is clonable, that class object can
[02:28] be clonable.
[02:29] For example, if I have a class which is Employee, to this Employee, if I'm trying to implement Clonable
[02:37] interface, then I'm telling to my Java compiler,
[02:40] since I have implemented Clonable interface inside these Employee class, the object of Employees can
[02:48] be Clonable.
[02:49] So it is an indication to the compiler and to other developers as well.
[02:53] What is a cloning?
[02:54] Inside Java,
[02:55] cloning means we want to create an exact copy of an object.
[03:00] After the cloning is completed, we are going to have two different objects which are copy of each other.
[03:06] So if I'm not using these implements Cloneable, then I will not be able to do the cloning.
[03:12] My Java compiler is going to throw an exception.
[03:15] Apart from implementing this Clonable, my Employee class should also override a method available inside
[03:23] the object superclass.
[03:25] Like you can see here
[03:26] I have a clone() method from the Object class, which is going to be inherited by my Employee class.
[03:32] The same needs to be overridden by my Employee class, so that whenever someone is trying to clone my
[03:39] object, whatever I have written inside this clone() method, the same is going to be executed. For some
[03:45] reason
[03:45] if I'm not implementing this Clonable interface, then I'm always going to get these CloneNotSupported
[03:51] exception even though this method is overridden inside the Employee class.
[03:56] So you can see there is a special purpose to this Clonable interface.
[04:01] So for all these kind of interfaces where they don't have any logic inside them, such interfaces,
[04:07] we are going to call them as Marker interface.
[04:10] Let me show you other interface that we have which is Serializable.
[04:13] So this Serializable interface is available inside the package java.io.
[04:20] If I can open this interface you can see this interface is also empty.
[04:24] The purpose of this interface is whenever I am implementing these interface inside any class, it is
[04:31] an indication to the compiler that the object of these Employee class can be Serialized.
[04:37] So what is a serialization in Java
[04:40] serialization is a process of converting an object into the stream of bytes data, so that these streams
[04:48] of byte data I can save into a disk space, or I can send to some other application over the network.
[04:55] So whenever we have these kind of requirements where if I want to send the my entire
[04:59] data object data into some other application, I can follow the serialization.
[05:05] And similarly, deserialization is a process of converting stream of byte data into an object representation.
[05:13] So whenever an object of a class needs to be serialized or deserialized, the very first basic requirement
[05:19] that it has to follow is it has to implement the Marker interface, which is serializable.
[05:25] Otherwise compiler at runtime it is going to throw an RuntimeException.
[05:30] I hope you are clear about the purpose of Marker interface and the examples that we have discussed around
[05:35] this.
[05:36] Like I said before, in real projects you may never create the Marker interfaces, you may never have
[05:42] such requirements.
[05:43] But if you want to understand how to create a Marker interface, it is going to be very simple.
[05:48] First you need to mention public followed by interface keyword and what is your interface name and post
[05:53] that you should have empty curly braces and with that you will be able to successfully create your own
[06:00] custom marker interface.
[06:01] If you want to use the same inside any other class, just like any other normal interface you can using
[06:08] the implements keyword, you should be able to inherit or implement your My Marker interface.
[06:14] But like I said these days Marker interface are not being used frequently inside Java because alternative
[06:22] mechanisms like annotations came into picture and they become more popular.
[06:27] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
