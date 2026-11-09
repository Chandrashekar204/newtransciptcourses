# 10.7 — Object class is the default Superclass

> Section 10: Inheritance in Java

[00:00] In the previous lecture,
[00:01] while we are seeing that demo of the Inheritance, we saw the methods from the Object class are also
[00:07] being inherited by default.
[00:09] This is because inside Java, every class is going to have a default superclass which is Object.
[00:18] So this object class is present inside the package, which is java.lang package.
[00:25] Since this class is present inside the java.lang, we don't need to use any import statement as
[00:30] well.
[00:31] So behind the scenes, the Java is always going to add these object as a superclass for each and every
[00:38] class that you are going to create.
[00:40] So this is going to happen implicitly.
[00:43] As a result, any class that you create will inherit the instance methods of the Object class.
[00:50] So this Object class has many important methods related to the Java objects.
[00:55] So these methods are like clone(),
[00:57] using clone we can create another copy of an given object.
[01:02] And after the clone we have equals() method
[01:04] using equals() method, we can validate whether the current Java object is equal to another Java object,
[01:12] and after the equals() we have
[01:14] finalize() method.
[01:14] Using these finalize() method, we can write a logic that can be executed whenever our object is going
[01:22] to be garbage collected.
[01:24] So just before removing our object from the heap memory by the garbage collector, we can try to execute
[01:31] some logic with the help of this finalize() method.
[01:34] And we also have getClass() method, which is going to give the what is the class name or the class data
[01:40] type of an given object.
[01:42] And with the help of hashCode(), we can calculate the hashCode() value of an object.
[01:47] And at last we have toString() method here
[01:49] So using the toString() method we can return an string representation of the object.
[01:56] So apart from these method, there are many other methods also available inside Object class.
[02:01] So we're going to talk in detail about the all the object class related methods in the coming sections.
[02:07] For now, let's try to understand why this Object class is made as the default or implicit superclass
[02:15] for all the Java classes.
[02:17] The reason is very obvious, since we are going to create objects for all our Java classes.
[02:24] So while dealing with all these Java objects that we create, we may have some requirements like creating
[02:30] the copy of a Java object, or checking the equality of the Java object, or knowing the class name
[02:36] of the Java object, or calculating the hashCode value, or printing our object content in an string
[02:43] representation.
[02:43] So since every Java object may have all these common requirements, so all these kind of object related
[02:50] functionality has been developed inside a Object class.
[02:54] And the same are being inherited by default by all the Java classes.
[02:59] I hope it is clear.
[03:00] Now, if you try to understand more details about the Object class. Like you can see here
[03:05] on the left hand side, I'm trying to create a Java class which is Person and on the right hand side
[03:11] I'm also trying to create the same class which is Person, but this time I have mentioned the extends
[03:16] Object.
[03:17] So both of these class definitions, they are same.
[03:21] Regardless I'm mentioning the extends Object or not.
[03:24] The behavior is always going to be same, which is we will be able to inherit the methods from the Object
[03:31] class.
[03:32] For example, in all the earlier sections that we have discussed, nowhere we have not used the extends
[03:39] keyword to inherit the Object class, but still behind the scenes we are quietly inheriting the Object
[03:47] class.
[03:48] That's why any class that you have created so far without using the extends keyword.
[03:52] When you try to create the object of those classes, you will be able to invoke the methods from the
[03:57] object class like hashCode() and toString().
[04:00] So this means we are using our writing the Inheritance train since the very first Java program that
[04:09] we have created, but we never realized it
[04:11] the reason is behind the scenes, the Object superclass is going to be inherited implicitly by each
[04:19] and every Java class.
[04:21] Let me try to show you the demo of hashCode() and toString() methods for the same
[04:25] inside my Marvels main() method, I can try to create an object of any of the classes.
[04:31] For example, here I can try to create an object of Person class.
[04:35] For the same I need to mention Person,
[04:38] what is the object reference name followed by equal to followed by new operator followed by Person()
[04:44] default constructor.
[04:45] If I open this Person Java class.
[04:48] As of now, you can see this is not extending any of the superclass.
[04:52] But if I go to the MarvelsMain and try to mention that dot operator after the object reference, you
[04:59] will be able
[04:59] to see all the methods from the Object class.
[05:03] Like for example, I can try to invoke the hashCode() method, and this hashCode() method is going to give
[05:10] an output in an into format.
[05:13] So that's why I'm going to assign the output to a variable which is int hc,
[05:18] hc indicates hashCode().
[05:19] Very similarly, I'll try to create one more variable of type String.
[05:24] And the variable name I'm going to give here is str.
[05:27] And to this I'm going to assign the output from the toString() method.
[05:32] So you can see I'm trying to invoke the toString()method by using the object reference of the Person
[05:38] class.
[05:38] So I can keep a breakpoint here and try to debug this program.
[05:42] You'll be able to see the what is the value inside the hc at runtime.
[05:47] So this is the hashCode value for this object.
[05:49] And very similarly this is the string representation of the Person object that we have created.
[05:55] So this confirms that all our Java classes implicitly inheriting the Object class.
[06:01] And inside this Object class what do we have,
[06:03] we have all the important methods related to the object related operations.
[06:09] So these are Object class, Object.java and it is present inside the package java.lang.
[06:16] That's what you can confirm here.
[06:18] And it has so many methods related to the Java objects.
[06:22] So all these methods we can try to invoke based upon our business requirements.
[06:27] We are going to talk in detail about the purpose of these methods in the coming sections.
[06:32] I hope you are convinced with our discussion that Object class is the default superclass.
[06:36] So with this information, if you try to check the class hierarchy relationship, this is how it is
[06:43] going to look like.
[06:44] So if you take the same animal scenario, Object will be the first superclass inside the class hierarchy.
[06:51] And this Object is going to be inherited by the Animals,
[06:54] and the Animals is going to be inherited by other subclasses like Mammals, Reptiles, Birds.
[07:00] So this inheritance can go to any level like bird subclass can be inherited by any number of other subclasses.
[07:08] So just like how we have ancestors who are wise elders.
[07:12] So all the super classes are like ancestors, so they are wise elders of the coding tribe and all the
[07:18] classes below a class,
[07:21] they are like descendants who are the next generation coders learning the ropes from their superiors.
[07:27] So it is like a family tree, but for the Java classes.
[07:31] So the interface relationship between the classes can always be represented by using the UML diagram.
[07:38] So what is UML Unified Modeling Language.
[07:41] So inside UML diagrams always a connection between a superclass and a subclass is going to be represented
[07:48] by an arrow pointing from the subclass to the superclass.
[07:52] Let me share more details about Inheritance.
[07:55] So whenever we are dealing with the Inheritance a class can be granted the power of only a single Inheritance,
[08:03] meaning it can have only just one superclass or parent.
[08:08] But this does not mean a class can't be a super hero or a super class to multiple other classes.
[08:16] In fact, a single class can play the role of superclass for many other classes.
[08:21] In the examples that we have taken, the same Animal superclass are the same Person superclass,
[08:27] they are acting the role of superclass for many other subclasses.
[08:31] So every Java class except the Object class is going to have a superclass
[08:38] and guess who is sitting at the V.I.P
[08:40] spot of all the Inheritance hierarchy,
[08:43] you are right, the Object class.
[08:45] So Object class is like the Grand Master overseeing the coding universe from the top in Java.
[08:53] At times you may hear the jargon which is immediate superclass.
[08:57] So this jargon we can use to denote the ancestor class that is one level above in the Inheritance hierarchy.
[09:06] Just like immediate superclass, we also have another jargon which is immediate subclass, which can
[09:12] be used to represent a descendant class that is one level below in the Inheritance hierarchy.
[09:19] Whereas normal jargons like superclass or subclass, they represent a superclass or descendant class
[09:27] at any level.
[09:28] For example, if you look at this Interface class hierarchy for the Animals, what is the immediate
[09:35] superclass?
[09:36] The Object.
[09:37] Similarly for Reptiles, what is the immediate superclass?
[09:40] It is going to be the Animals.
[09:42] Very similarly for Animals, what are the immediate subclasses?
[09:47] It will be Mammals, Reptiles and Birds.
[09:50] Whereas for the Object, the immediate subclass is Animals.
[09:53] I hope you are clear with these jargons and all the subclasses of a given class
[09:58] in other words, we can
[09:59] call them as descendants.
[10:01] For example, for Animals, the descendants are Mammals, Reptiles and Birds.
[10:07] So since these subclasses are the descendants for Animals, they can also be called as descendants for
[10:13] the Object class.
[10:14] So for the Object class, who are the descendants Animals including Mammals, Reptiles and Birds.
[10:21] With this, I'm assuming you're clear about the Object superclass and how to imagine a Interface hierarchy
[10:28] whenever you are trying to build the Inheritance logic for your Java classes.
[10:33] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
