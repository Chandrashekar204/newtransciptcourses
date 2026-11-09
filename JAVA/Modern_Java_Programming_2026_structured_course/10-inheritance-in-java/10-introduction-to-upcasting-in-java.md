# 10.10 — Introduction to upcasting in Java

> Section 10: Inheritance in Java

[00:00] When I'm explaining about the primitive data types.
[00:03] I also explain you about the type casting in Java.
[00:07] So there are two types of castings that can happen inside Java whenever we are dealing with the primitive
[00:12] data types.
[00:13] So what are these castings.
[00:15] The very first one is Widening casting or automatic or implicit casting inside these type of casting
[00:21] whenever we are trying to convert a small data type to a larger primitive data type, then the casting
[00:27] is going to happen automatically.
[00:30] And since there is no loss of data, we're not going to get any compilation error.
[00:35] Whereas if you look at the second type of casting, which is Narrowing casting or manual or explicit
[00:41] casting, in this kind of casting, when we try to convert a large primitive data type to a small primitive
[00:48] data type, then we are going to get a compilation error.
[00:51] To resolve that compilation error, we need to manually perform that type casting.
[00:56] So why
[00:57] I'm trying to explain about the type casting again inside a section where we are talking about inheritance.
[01:04] So there is a reason why I'm trying to explain about type casting.
[01:07] So for now I am assuming you got a very quick revision about the type casting.
[01:12] So just like how we can perform the type casting whenever we are dealing with the primitive data types.
[01:18] Very similarly, whenever we are trying to implement inheritance between a subclass and a superclass
[01:24] in these kind of scenarios, also we can try to perform a casting.
[01:28] And these casting is called as Upcasting and Downcasting.
[01:33] So let's try to understand more details about these Upcasting and Downcasting.
[01:37] Inside Java we know each class represents a data type.
[01:41] For example, I can create a class of Person and using the same Person class, I can create an object
[01:49] that represents a data type called Person.
[01:52] So once we define our classes with the help of inheritance, we are able to establish a parent and child
[01:59] relationship.
[02:00] That's what we discussed in the previous lectures.
[02:02] So whenever you try to establish inheritance between your Java classes, so always your superclass is
[02:10] going to represent a broader or more general data type, whereas a subclass is going to represent a
[02:18] specific subtype.
[02:19] For example, in the example of Animal and Dog inheritance relationship, Animal is a superclass, and
[02:25] Animal represents a broader or a general data type, which means Animal is a broader topic.
[02:32] And using Animal we can represent lot many types of animals.
[02:37] Whereas coming to the subclass which is a dog, so it is a specific subtype of an Animal.
[02:43] So with this it should be very clear for you, as we are trying to travel from subclass to the superclass
[02:49] inside the inheritance hierarchy, the transition is going to happen from a more detailed type to a
[02:56] broader or general data type.
[02:58] I can always say that a Dog is an Animal, but I cannot say Animal is a Dog because not each Animal
[03:07] is a Dog, but each Dog can be an Animal.
[03:10] So let's try to remember this discussion using these concepts only.
[03:14] We are going to try to perform the Upcasting and Downcasting in Java.
[03:19] Before I try to explain you about what is an Upcasting and Downcasting, first let me try to explain
[03:25] you what are the advantages that we are going to get whenever we perform Upcasting and Downcasting
[03:31] in Java, inside Java project, we are going to write a lot of Java code, and there is a good chance
[03:36] that you may create hundreds of Java classes inside your real projects.
[03:41] And obviously you're going to implement inheritance between your classes wherever is applicable, so
[03:48] that you're going to improve the reusability of your common code.
[03:52] So when we implement inheritance inside Java, it is going to impact the client code.
[03:57] So what is a client code?
[03:59] Client code means whatever Java code that you're going to write to trigger the logic present inside
[04:05] your superclass or subclass.
[04:07] So such kind of code we can call it as client code.
[04:10] So when you try to build the client code inside your real project, you're going to write the client
[04:16] code by considering the superclass and the same logic, or the client code is going to seamlessly work
[04:23] even for subclasses as well.
[04:25] So how that is possible with the help of Upcasting and Downcasting.
[04:29] I know you may have so many questions here.
[04:32] First, let's try to jump into some examples here.
[04:35] In the same process, I will try to explain more details about the advantages that we are going to get
[04:40] with the help of Upcasting and Downcasting.
[04:43] First like you can see here, I have a superclass with the name Animal.
[04:47] And inside this superclass I have a variable name of type String.
[04:51] And apart from this variable I also have methods inside Animal superclass like setName() and getName() and
[04:58] the eat() methods.
[04:59] And this superclass is going to be extended by a subclass called Dog.
[05:04] So that's what you can see here.
[05:05] There is an extends keyword after the Dog class name.
[05:09] So now using these superclass and subclass relationship.
[05:13] First let me give you a demo of Upcasting.
[05:16] Here I'm going to show you two examples.
[05:18] In the very first line, I'm trying to create an object reference with the name anm.
[05:23] So this object reference belongs to that data type Animal and to this object reference
[05:28] I'm trying to assign the object of Animal which I have created with the help of this new operator.
[05:35] So there is nothing new here.
[05:37] So we're just trying to create an object of Animal.
[05:39] So using the object reference I'm trying to invoke the method setName().
[05:44] And to this setName() method we are passing a name Scooby.
[05:47] The same is going to be set into the variable name.
[05:50] Later on I can try to get the same name with the help of the method, which is getName().
[05:56] So this is very normal code
[05:57] there is nothing fancy happening here, but if you closely look at the second example first, I'm trying
[06:03] to create an object reference of Animal data type later on to this object reference, I'm trying to
[06:10] assign the object of subclass, which is Dog.
[06:14] Do you think this is going to be allowed,
[06:16] off course it is going to be allowed.
[06:18] The reason is every subclass is a type of superclass.
[06:23] So I can safely say a Dog is a Animal.
[06:26] So since I can say Dog is a animal, the object of subclass can be easily assigned to the object reference
[06:34] of superclass.
[06:36] So that's what it is happening here.
[06:38] So once the object of Dog is assigned to the anm, I'm trying to invoke the same code which is setName()
[06:44] and getName() methods.
[06:45] So if you see here at the second line there is a conversion is happening from subclass to the superclass.
[06:52] So this type of conversion or casting we call it as Upcasting.
[06:57] So Upcasting inside Java in other words we can call it as Widening conversion because we are assigning
[07:06] a more specific type data type, which is Dog, to a reference variable of more general data type,
[07:13] which is Animal.
[07:14] Inside Java, Upcasting is always allowed, so you won't be getting any compilation error.
[07:20] So this is very similar to the implicit casting that we have discussed as part of the primitive data
[07:26] types.
[07:26] So just like how implicit casting or widening casting is automatically allowed inside Java, very similarly
[07:34] Upcasting or Widening
[07:35] conversion is also going to be automatically allowed by your Java compiler.
[07:40] Whenever you are trying to assign the object of a subclass to a object reference of superclass.
[07:46] I hope you are clear what is Upcasting, but here you may have a question
[07:51] why should someone will try to assign an object of subclass to a superclass?
[07:56] What are the advantages that they are going to get?
[07:58] So let's try to answer the same question in the next lecture.
[08:01] Thank you,
[08:02] bye.

----------------------------------------
