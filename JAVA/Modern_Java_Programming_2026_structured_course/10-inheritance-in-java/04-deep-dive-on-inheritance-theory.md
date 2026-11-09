# 10.4 — Deep dive on Inheritance - Theory

> Section 10: Inheritance in Java

[00:00] In the previous lecture we talked about Inheritance on a high level.
[00:04] So what is an Inheritance?
[00:06] Inheritance is a mechanism that allows one class to inherit the properties and behavior of another class.
[00:14] This is very similar to real world scenario on how a child inherits certain physical attributes and
[00:21] characteristics from their parent.
[00:24] As a next step, let's try to take a scenario and try to solve it with the help of Java Inheritance.
[00:30] The scenario is going to be super interesting.
[00:33] This scenario revolves around the superheroes that we have in the Marvel universe.
[00:40] You might have seen lot many movies from the Marvel universe.
[00:43] So inside the Marvel Universe we have so many heroes like Iron Man, Spider-Man, Doctor Strange, Hulk,
[00:52] Wonder Woman.
[00:53] So there are many great heroes that we have inside this Marvel universe.
[00:58] So now let's try to take a scenario around this, and let's try to build the Java classes for each of
[01:05] our superheroes.
[01:07] Like think like, I want to build a Java class representing three different heroes from the Marvel Universe.
[01:14] So these three different heroes can be IronMan, SpiderMan, and CaptainAmerica.
[01:20] So if you look at the three classes, they have a logic which is very similar.
[01:25] Like every hero, they should have a name and age attributes.
[01:29] So that's why these two attributes are repeated in all these three classes.
[01:34] And similarly all these heroes, they have the behaviors like eating, walking, sleeping and using
[01:41] the power.
[01:42] So to reprint these behaviors I have methods like public void eat() that is going to accept the food as
[01:48] an input.
[01:49] Similarly, I also have a walk() method which will make my superhero to walk, and after the walk we have
[01:56] sleep() method and after the sleep() method
[01:58] we also have usePower() method.
[02:01] So if you look closely at all these methods, the same methods are behaviors are repeated in all the
[02:07] three classes.
[02:08] Do you think the behavior is going to change from one hero to other hero,
[02:12] off course not.
[02:13] They will all eat with their own mouth.
[02:15] They will walk in a similar manner,
[02:17] they will sleep in a similar manner.
[02:19] Maybe using the power can be different from one hero to other hero.
[02:24] Like for Iron Man, he will use the power from his suit, whereas for the Spider-Man he will use the
[02:31] power
[02:31] with the help of Spider Web, for Captain America, he will have his weapon to use it as a power.
[02:37] So the only difference between all these three classes is on how they are going to use their power.
[02:43] Remaining all the attributes and the behavior is going to be same.
[02:47] So with the current Java classes that we have, there is a lot of duplicate code across all the classes.
[02:53] So how to handle these kind of scenarios?
[02:56] I'm pretty confident you know the answer here.
[02:58] The answer is Java Inheritance.
[03:02] Let's try to understand how we can solve this problem with the help of Java Inheritance.
[03:07] Like you can see here
[03:09] first I'm going to create a super class with the name Person.
[03:13] When we are creating a super class, we don't have to take care of any special syntax.
[03:18] It can be a normal Java class like you can see here.
[03:21] I have created a super class with the name Person by using the public class Person and inside this Person
[03:27] class body I have all the common code like the name age fields and the methods like eat(), walk() and sleep().
[03:35] I have not put the use power() method inside the Person, because the uses of the power can be vary from
[03:41] one hero to other hero.
[03:43] So once you define your super class like this as a next step, you need to create all your different
[03:50] subclasses or child classes.
[03:52] Like first you can see I have created the IronMan, followed by SpiderMan, followed by CaptainAmerica.
[03:58] If you closely look at these classes after the class name I am using, the keyword extends, with the
[04:05] help of extends keyword
[04:07] we are trying to inherit the attributes and the methods from the super class.
[04:12] So what is the super class that I have here, Person.
[04:14] So extends Person,
[04:16] I need to mention immediately after my child class name or subclass name our derived class name.
[04:23] So the same I have done after the SpiderMan and CaptainAmerica.
[04:27] Now if you closely look at the child classes inside the child classes, I don't have all these common
[04:33] code because anyway, they are going to inherit from the parent.
[04:36] The only logic that I have inside my subclasses are child classes is the method usePower().
[04:42] So inside this usePower() I can write different logic based upon to which hero that subclass belongs
[04:50] to.
[04:50] I hope you are clear with this explanation.
[04:52] Inside Java, we are always going to return that child and parent relationship by using these upwards
[05:00] arrow mark.
[05:00] Like you can see when we use this upwards arrow mark, this indicates that this child is inheriting
[05:07] the properties or the methods from the parent class, which is Person.
[05:12] So usually inside a Java class we'll be having the Java fields, methods and constructors.
[05:19] Since the constructors are not the members, they are not going to be inherited by the subclasses or
[05:26] by the child classes.
[05:27] But if needed, a constructor of the superclass can be invoked from the subclass.
[05:32] We're going to discuss how the constructor invocation is going to change based upon this parent and
[05:38] the child relationship in the coming lectures.
[05:41] But now, please note that constructors are not going to be inherited by the subclasses from the superclass.
[05:47] I know you might be learning these Java Inheritance very first time, and it might be still be confusing
[05:52] for you.
[05:52] That's why
[05:53] let me show you another example like you can see here we have an Interface diagram related to Animals.
[06:00] So for all the animals that we have on the earth, they are going to have the common attributes and
[06:07] behaviors such as name, age and the ability to move from one place to other place.
[06:13] So all these common attributes and behaviors we can keep inside a superclass with the name Animals.
[06:20] And this superclass can be extend by the subclasses or the child classes like mammals, reptiles and
[06:28] birds.
[06:28] So again each of these child classes, they can have their own behavior like birds.
[06:33] They'll have their unique behavior which is they can fly.
[06:37] So this kind of unique features are unique variables or behaviors
[06:42] the subclasses they can still have or they can still build.
[06:45] But all the common logic or the common attributes and the common behavior, we can always keep and maintain
[06:52] them inside the superclass like Animals.
[06:55] So what are the advantages that we get with these Inheritance?
[06:58] We are getting a flexibility to maintain all the common code in a single class.
[07:03] And in future, whenever we want to make a change inside this common code, the change has to be done
[07:10] at a single place, which is the superclass.
[07:12] So as soon as you make a change inside the superclass, the updated business logic is going to be immediately
[07:18] reflected inside all the child classes and the subclasses.
[07:22] On top of that, if needed
[07:24] my child classes, they can overwrite the behavior or they can override the properties provided by the
[07:31] superclass.
[07:32] I'm going to explain the concept of overriding in the coming lectures, but for now, I'm assuming you
[07:37] are clear about the Java Inheritance.
[07:40] So one more time, if you try to understand the syntax that we need to follow whenever we want to implement
[07:45] the Java Inheritance is, first you need to mention what is your access modifier.
[07:50] It can be a public or default
[07:52] and after that you can keep the class keyword followed by what is your subclass name or child name or
[07:58] derived class name, and after your subclass name you need to mention the extends keyword.
[08:04] So extends is very important here.
[08:06] This is going to enable the Java Inheritance.
[08:09] After the extends keyword, you need to mention what is the superclass name.
[08:14] For example, think of a scenario where we have a superstar in dance.
[08:19] So if the superstar is trying to teach some dance moves to another fellow or to another subclass, in
[08:26] such scenarios we can have these kind of class definition where my subclass name is going to be funky
[08:33] subclass, and this is going to extends the parent class, which is superstar class.
[08:39] So all the dance moves that my superstar knows, it is going to be inherited by my funky subclass.
[08:46] And whenever you are trying to mention the parent class just after the extends keyword, you need to
[08:51] be very careful about mentioning the import statement as well.
[08:56] If your superclass is present inside the same package, then obviously you don't have to mention any
[09:02] import statement.
[09:03] Otherwise, if your superstar class is present inside another package, then in such scenarios, definitely
[09:10] first you need to mention an import statement.
[09:12] Once the import statement is mentioned, then only you can mention your parent class.
[09:17] Otherwise, if you don't want to mention the import statement, you can mention the complete qualified
[09:23] name of your parent class after the extends keyword.
[09:27] I hope you remember all the import and packages concept that we have discussed in the previous lecture.
[09:33] With this, we discussed about Java Inheritance theoretically.
[09:37] Now in the next lecture, let's try to create some super classes and subclasses and try to implement
[09:43] the Java Inheritance with the help of extends keyword.
[09:47] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
