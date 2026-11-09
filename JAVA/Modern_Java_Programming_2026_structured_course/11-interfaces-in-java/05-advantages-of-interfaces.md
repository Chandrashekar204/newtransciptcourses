# 11.5 — Advantages of interfaces

> Section 11: Interfaces in Java

[00:00] In the previous lecture,
[00:01] we have created multiple superhero Java classes and in all these classes we implemented a common interface,
[00:08] which is superhero.
[00:10] Now let's try to understand what is the advantage that we are getting whenever we are trying to implement
[00:15] a superhero. We already know about one advantage, which is we are getting a code consistency in all
[00:23] the classes where a particular interface is being inherited.
[00:26] From this consistency advantage, we will have many other advantages.
[00:30] So let me show you what are those?
[00:32] To demo you the same I'm going to create a new package and the package name is going to be
[00:40] com.eazybytes.marvel.hero.app.
[00:43] Inside this package I'm going to create a Java class which is MarvelHeroDemo inside this class
[00:52] first let me create a main() method.
[00:54] And inside this method first I'm going to write a logic to invoke the methods available in one of the
[01:01] superhero class.
[01:02] Think like we are going a war with the Thanos or any other villain.
[01:06] In this kind of scenarios, we need to alert our superheroes by invoking their methods.
[01:12] So let's try to understand how to do the same.
[01:14] First, I'm going to create the object of IronMan using IronMan new Ironman() and post that I'm going
[01:22] to invoke the method IronMan.usePower() and whatever we are trying to return from this method, the
[01:30] same is going to be printed onto the console.
[01:32] So let me try to do the same for the other method where I'm going to invoke the method which is top
[01:38] villain
[01:39] and to this I will send the value n as an input.
[01:44] So if I try to execute this logic, you'll be able to see an output saying that IronMan using his power
[01:51] and IronMan stop the villain.
[01:52] Let me try to do the same for other two superheroes I have.
[01:57] So I'm going to create the object of SpiderMan and by using the SpiderMan class, the object reference
[02:04] also, I'm going to change to SpiderMan.
[02:06] Now using the SpiderMan Object reference, I'm going to invoke the methods which are usePower() and
[02:12] stopVillain().
[02:13] And at last let me try to create the object of Captain America by using the class of Captain America.
[02:21] Now, using the same object reference of Captain America, I'm trying to invoke the methods, usePower()
[02:27] and stopVillain().
[02:28] So if I try to execute this method, you can see I'm getting all the output like we expect.
[02:34] So here you can see there is a lot of code is being repeated.
[02:38] Like whenever we want to invoke a SuperHero related methods, we are trying to repeat the same statement
[02:45] multiple times.
[02:46] The only thing is changing here is object reference name.
[02:49] We can try to solve this problem by using the interface type as an object reference name.
[02:55] For example, here instead of IronMan IronMan, I can try to use the interface name, which is SuperHero.
[03:02] So the casting is always acceptable because every IronMan is a superhero.
[03:08] So here, right now, the IronMan object variable, it is trying to refer to the type SuperHero.
[03:14] Whereas on the right hand side we are trying to create an object of IronMan.
[03:19] So inside these variable IronMan, the IronMan object is going to be stored.
[03:24] So let me try to do the same for remaining objects like SpiderMan and CaptainAmerica.
[03:29] As a next step, I can create a private method inside the same class, and this private method is going
[03:35] to be private static void, and the method name I'm going to mention as invokeSuperHero().
[03:42] And to this method I'm going to pass the object of type SuperHero interface.
[03:48] After this I'm going to mention the curly braces.
[03:51] And inside this new method I'm going to mention the business logic with the help of superhero variable
[03:57] name.
[03:58] So now you can see I have an static method which is going to hold the common logic that is required
[04:04] for my all superheroes.
[04:06] So instead of writing this logic at multiple places, I can simply try to invoke the method invokeSuperHero(),
[04:14] and to the same I can try to pass the object reference of my superheroes.
[04:19] So let me do the same for SpiderMan as well.
[04:22] So instead of IronMan, I need to mention the SpiderMan, and at last let me do the same for
[04:28] CaptainAmerica as well.
[04:29] So this way you can see now the code is looking very short and concise, and in future, whenever we
[04:36] want to make any changes, the change is always going to be inside a single method.
[04:42] So here you can see the other advantage that we are getting from the interface is, we are encouraging
[04:47] the reusability.
[04:48] And we are also building the common logic in a separate method.
[04:53] So this is also kind of Polymorphism.
[04:55] The same method is trying to act differently based upon the input that you are
[04:59] trying to send.
[05:00] So this kind of discussion we also did when we are discussing about the superclass and subclass in the
[05:07] previous section.
[05:08] So the advantages are always going to be similar to the subclass and superclass scenario.
[05:13] But here you may have a question which is, if you are able to achieve the same with the subclass and
[05:18] superclass, why should I go with an interface?
[05:21] It's a great question.
[05:22] The answer is very simple.
[05:24] With interface we are not taking the headache of providing the implementation logic, we are just defining
[05:31] the standard or the specification or the contract which all my implementation classes has to follow.
[05:38] I hope you are clear with the demo.
[05:39] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
