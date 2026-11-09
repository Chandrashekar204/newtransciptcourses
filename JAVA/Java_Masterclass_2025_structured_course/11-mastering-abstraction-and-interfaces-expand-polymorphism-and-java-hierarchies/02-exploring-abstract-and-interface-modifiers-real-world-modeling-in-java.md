# 11.2 — Exploring Abstract & Interface Modifiers: Real-World Modeling in Java

> Section 11: Mastering Abstraction & Interfaces: Expand Polymorphism & Java Hierarchies

Kind: captions Language: en We use the terms Abstraction and Generalization, when we start trying to model real world things in software. Before I launch into interface types and abstract classes, I want to talk about what these concepts mean. When you start modeling objects for your application, you start by identifying what features and behavior your objects have in common. We generalize when we create a class hierarchy. A base class is the most general class, the most basic building block, which everything can be said to have in common.

Part of generalizing is using abstraction. You can generalize a set of characteristics and behavior into an abstract type. If you consider an octopus, a dog, and a penguin, you will probably say they're all animals. An animal is really an abstract concept. An animal doesn't really exist, except as a way to describe a set of more specific things. If you can't draw it on a piece of paper, it's probably abstract. An animal would be hard to draw for example, if you weren't given more information about the actual type of animal to draw.

Abstraction simplifies the view of a set of items' traits and behavior, so we can talk about them as a group, as well as generalize their functionality. Java supports abstraction in several different ways. Java allows us to create a class hierarchy, where the top of the hierarchy, the base class, is usually an abstract concept, whether it's an abstract class or not. Java lets us create abstract classes. ; Java gives us a way to create interfaces.

In the videos that follow, I'll be talking a lot about abstract and concrete methods. An abstract method has a method signature, and a return type, but doesn't have a method body. Because of this, we say an abstract method is unimplemented. Its purpose is to describe behavior, which any object of that type will always have. Conceptually, we can understand behaviors like move or eat on an Animal, so we might include those as abstract methods, on an abstract type.

You can think of an abstract method as a contract. This contract promises that all subtypes will provide the promised functionality, with the agreed upon name and arguments. Don't worry if that's confusing right now. I'll be getting into it in a lot more depth throughout this section. A concrete method has a method body, usually with at least one statement. This means it has operational code, that gets executed, under the right conditions. A concrete method is said to implement an abstract method, if it overrides one.

Abstract classes and interfaces can have a mix of abstract and concrete methods. I've already covered access modifiers and what they mean for types, as well as members of types. And you know there are public, protected, package, and private access modifiers, as options for the members. In addition to access modifiers, methods have other modifiers, which I'll list here, as a high level introduction. When you declare a method abstract, a method body is always omitted.

An abstract method can only be declared on an abstract class or an interface. I've talked about the static modifier, it's sometimes called a class method, as opposed to an instance method. It's called directly on the Class instance and doesn't access any single instance of the class. A method that is final can't be overridden by subclasses. This default modifier is only applicable to an interface, and I'll talk about it in the videos dedicated to interfaces, coming up in this section of the course.

A native method is another method declared with no body, but it's very different from the abstract modifier. The method body will be implemented in platform dependent code, typically written in another programming language such as C. This is an advanced topic, and not commonly used. The synchronized modifier manages how multiple threads will access the code in this method. I'll cover this in a later section on multi threaded code. Ok, so now that you have a high level concept of these topics, you'll hopefully be able to better understand both the abstract class and the interface.

Let's start with the abstract class in the next video, since we're already familiar with inheritance and class hierarchy. Ok, I'll see you in that next video.

----------------------------------------
