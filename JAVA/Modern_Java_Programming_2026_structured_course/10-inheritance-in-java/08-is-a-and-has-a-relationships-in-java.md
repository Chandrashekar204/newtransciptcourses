# 10.8 — is-a & has-a relationships in Java

> Section 10: Inheritance in Java

[00:00] Inside Java are in any object oriented programming language we can use is-a relationship or has-a relationship
[00:09] to represent our established relationship between different classes. Inside your Java interviews or
[00:16] inside your Java related exams.
[00:18] Definitely
[00:19] sometimes you may hear questions about what is a , is-a relationship or has-a relationship in Java.
[00:26] So let's try to understand what are those. Using is-a relationship we can express Inheritance relationship
[00:34] between two classes.
[00:35] So whenever we use extends keyword that means we are establishing Inheritance relationship between a
[00:42] superclass and a subclass.
[00:44] For example, here I have a superclass with the name Animal, and I also have a subclass that is extending
[00:51] the Animal superclass, and the subclass name is Dog.
[00:54] So both of these Dog and Animal, they have a relationship which is established with the help of inheritance
[01:01] concept.
[01:02] So this kind of relationship that is established with the help of inheritance, in other words we can
[01:08] call it as is-a relationship.
[01:10] So how this is an is-a relationship.
[01:12] So let's try to understand the same.
[01:14] So if someone asks you what is a Dog, you will say Dog is a animal.
[01:20] Very similarly, we can also say SpiderMan is a Person, Car is a Vehicle, Orange is a Fruit.
[01:27] So this way using is-a relationship, we can always express our establish Inheritance relationship between
[01:36] two classes.
[01:37] If you can't build a sentence like Dog is-a Animal, you should not be establishing the Inheritance.
[01:43] It is not going to make sense.
[01:45] For example, if I say SpiderMan is-a Vehicle, do you think it is going to make any sense?
[01:51] off course not.
[01:52] That's why in this kind of scenarios, I should not try to establish the Inheritance between Vehicle
[01:58] and SpiderMan.
[01:59] Though your compiler is not going to stop anything around this, but it is a best practice to make sure
[02:05] that you are establishing the Inheritance only when a is-a relationship is established between different
[02:12] classes.
[02:12] I hope you are clear.
[02:13] What is an is-a relationship?
[02:15] Now let's try to understand what is a has-a relationship.
[02:19] Has a relationship is used to indicate that a given class has a certain property or object of another
[02:27] class.
[02:27] For example, here I have a class with the name Car, and inside this Car I can create any number of
[02:34] instance variable, and these instance variables can belong to another classes as well.
[02:40] For example, you can see I have an instance variable created inside my Car class,
[02:45] what is the instance variable?
[02:47] It is engine of data type Engine class.
[02:50] So here I have an Engine class, using the same Engine class
[02:54] I'm trying to create an instance variable inside my Car class.
[02:59] That means my Car class is holding an a property of another class.
[03:05] So this kind of relationship we can call it as has-a relationship.
[03:10] So here there is no inheritance involved.
[03:13] But my given class has an embedded property or a variable representing another class.
[03:20] So since a Car is going to have an engine in real world also, it is going to make a perfect sense to
[03:27] create an engine related embedded variable inside my car
[03:32] and with that we are going to establish an has-a relationship between Car and Engine.
[03:38] In other words we can also call this has-a relationship as aggregation or composition.
[03:45] So please make a note of this very important point.
[03:48] So people may ask you in interviews in a different style.
[03:52] So they may ask you what is an aggregation or a composition in Java.
[03:57] In such scenarios, you should explain about the has-a relationship that we are discussing right now.
[04:03] So with the help of is-a relationship, we can always implement inheritance
[04:08] and with inheritance we are encouraging lot of code reusability, whereas with the help of has-a relationship,
[04:16] we are going to represent an object which is a composition or aggregation of many other objects.
[04:23] So a Car can has-a Engine, a Car can has-a Tire.
[04:26] So this way I can create any number of instance variables inside my Car class that represents other
[04:33] classes.
[04:34] Let me show you a few more examples around is-a relationship and has-a relationship.
[04:40] We can say a Car is a Vehicle, a Truck is a Vehicle, Motorcycle is a Vehicle.
[04:46] So since is-a relationship is going to make sense here, we can make Vehicle class as a super class
[04:52] and all the Car, Truck and Motorcycles as subclass.
[04:56] And the similar lines we can say Dog is a Animal,
[05:00] Cat is a Animal,
[05:01] Bird is a Animal.
[05:02] If you try to understand the next example, it is also going to make sense to you.
[05:06] Circle is a Shape,
[05:08] Square is a Shape,
[05:09] Triangle is a Shape,
[05:10] Similarly, we can say Apple is a Fruit, Orange is a Fruit, Banana is a Fruit.
[05:16] And at last we can also say Manager is a Employee, Developer is a Employee, Tester is a Employee.
[05:23] So if you see it is pretty clear whenever we are able to establish an is-a relationship in that scenarios,
[05:30] we can confidently go for an inheritance.
[05:33] Whereas if you try to understand has-a relationship
[05:36] examples.
[05:37] We can say a Car has-a Engine, a Car has-a Tires, a Car has-a SteeringWheel.
[05:43] Similarly, we can say a Computer has a Processor, Computer has a Memory, Computer has a Storage, Building
[05:50] has a Walls, Building has a Doors, Building has a Windows ,Library, has a Book, Library has a Shelves,
[05:57] Library has a Librarian,
[05:59] Hospital has a Doctor,
[06:01] Hospital has a Nurse,
[06:02] Hospital has a Patient.
[06:04] So in all these kind of scenarios, we should go for the composition or aggregation or for the has a
[06:11] relationship.
[06:11] So inside my Car class I should be having instance variables that belongs to the Engine class, Tire
[06:19] class, SteeringWheel class.
[06:21] I hope you are clear.
[06:22] Let me show you the demo of this relationship very quickly
[06:26] inside our IntelliJ inside the base package, I'm going to create a new Java class and the class name
[06:33] is going to be Animal.
[06:34] For now, I'm going to keep this Animal class as empty because we don't need to implement any logic
[06:40] inside Animal to establish an is-a relationship.
[06:43] Next, I'm going to create a package with the name com.eazybyes.marvel.animals.
[06:51] Because even inside the Marvel universe we have animals.
[06:55] So let me create this package.
[06:57] So inside the animals package I'm going to create a class which is Dog.
[07:02] So since I can establish a is-a relationship between Dog and Animal by saying Dog is a Animal, I can
[07:10] use extends keyword here and mention Animal.
[07:14] So with this we established is-a relationship between Dog and Animal.
[07:19] I hope it is making sense.
[07:21] In the place of Animal I can keep Person
[07:25] so compiler is not going to complain anything because technically it is possible.
[07:29] But if you bring our human intelligence or common sense, do you think Dog is a Person?
[07:35] Off course not.
[07:36] That's why we should not try to establish the inheritance relationship between these two classes.
[07:42] With that reason, let me revert back to the Animal and now we have a proper is-a relationship.
[07:49] As a next step, I'm going to create a new Java class inside my base package, and the class name is
[07:56] going to be Vehicle.
[07:58] And very similarly, I'm also going to create one more Java class which is Engine.
[08:03] So both these Vehicle and Engine, they are two different classes right now.
[08:09] But I can build a has-a relationship between them because Vehicle is going to have Engine.
[08:15] So to establish a has-a relationship between Vehicle and Engine, I can simply try to create an instance
[08:22] variable of Engine inside my Vehicle class.
[08:26] So with this, whenever we are trying to create an object of Vehicle class, it is also capable of holding
[08:32] the object of Engine class as well.
[08:35] So here we are trying to bring the aggregation or composition with the help of has-a relationship with
[08:41] this,
[08:42] I'm assuming you have a good understanding about what is a is-a relationship and a has-a relationship.
[08:49] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
