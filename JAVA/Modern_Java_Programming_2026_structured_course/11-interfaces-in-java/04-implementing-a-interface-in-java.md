# 11.4 — Implementing a interface in Java

> Section 11: Interfaces in Java

[00:00] As of now, we have created an interface with the name SuperHero.
[00:04] As an next step, let's try to understand how to implement an interface with the help of Java inheritance.
[00:11] Below is a syntax for a class that implements an interface.
[00:16] So while we are trying to create the class definition like modify our class class name, we should use
[00:22] the implements keyword in the case of interfaces, whereas in the case of classes we need to use the
[00:30] extends keyword.
[00:31] Since we are talking right now about the interface concept, we need to use the implements keyword followed
[00:37] by comma separated list of interfaces.
[00:41] With the help of extends keyword, we can only extend a superclass, whereas when we are using the implements
[00:48] keyword, we can implement any number of interfaces that are separated by comma.
[00:54] And whenever a class is trying to implement an interface, all the abstract methods that it is inheriting
[01:00] from an interface must be overridden inside the class
[01:05] otherwise, the class must declare itself as an abstract class.
[01:09] When a class implements an interface, it can also include additional methods that are not inherited
[01:16] from the implemented interface.
[01:18] These additional methods
[01:20] they can have their own name based upon the specific business requirement related to that class, or
[01:26] they can also share the same name that is derived from the interface.
[01:30] But when they are sharing the same name, they should have different number of method
[01:34] parameters or the types of parameter to those declared in the implemented interface.
[01:39] When we have the same method name of interface inside the class with a different number or different
[01:45] types of parameters, then it will result into the method overloading.
[01:49] And at last I also want to highlight you that just like how a class can implement an interface, an
[01:57] interface can also extend or inherit from other interface.
[02:02] So while we are trying to establish an inheritance between two interfaces, we need to make sure we
[02:08] are using the extends keyword.
[02:10] The reason why we should use extends keyword in the case of interface is, when we are trying to create
[02:15] an interface, it is not mandatory to override the methods that is inherited from the super interface.
[02:22] So that's why we should always use the extends keyword whenever we are trying to inherit a super interface
[02:28] into an subinterface.
[02:30] Whereas when you are trying to establish an inheritance logic between a class and interface, then we
[02:37] need to use the implements keyword.
[02:39] I hope you are clear.
[02:40] So this is how our super hero classes are going to be changed when we implement an interface.
[02:47] You can see all my super hero classes
[02:49] they are implementing a single interface with the name SuperHero.
[02:53] So since they are implementing the SuperHero interface, they need to make sure they are following
[02:58] the same method signature that we have defined inside the interface.
[03:02] Apart from maintaining the same method signature, they should also take care of implementing their
[03:07] own business logic inside these methods.
[03:10] Like right now you can see all my super hero classes
[03:13] they have the same method name like usePower(), usePower(), usePower() with the different implementation
[03:19] code.
[03:20] Similarly, the same applies for stopVillain() method.
[03:23] I hope you are clear.
[03:24] Now as a next step, let's go to the intelliJ and try to implement an interface across multiple superhero
[03:31] classes. For the same,
[03:33] first I am going to create a new package
[03:35] here.
[03:35] The package name is going to be com.eazybytes.marvel.hero.impl so what is impl
[03:43] impl means implementation.
[03:46] So inside this package I am going to have implementation classes which are going to implement my interfaces
[03:54] that I have defined inside the package which is com.eazybytes.marvel.hero.
[04:00] So let me first try to create a new Java class which is IronMan.
[04:05] Once the class is created I need to type implements followed by what is the interface name.
[04:12] So the interface name is going to be SuperHero.
[04:15] As soon as I try to implement, you can see I'm getting a compilation error saying that class IronMan
[04:20] must either be declared abstract or implement abstract methods
[04:25] usePower() in SuperHero.
[04:27] As of now we are getting an error for the usePower() method.
[04:31] Once we fix this error, we are going to get another compilation error for the different abstract method
[04:37] that we have.
[04:38] So there are two options that we have here.
[04:40] The very first easiest option is we can try to create the class as an abstract class.
[04:45] So now my class is going to inherit two methods from the interface which is stopVillain() and the
[04:53] usePower().
[04:53] And both of them are of type abstract.
[04:56] But in the scenarios where you want to provide your own business logic
[04:59] then you can remove these abstract keyword.
[05:02] And with that we are going to get a compilation error.
[05:04] Select these Implement methods option and select both of these two methods.
[05:09] Post that
[05:10] you can click on these okay button.
[05:12] And you can see I am getting two methods with the annotation @Override.
[05:18] So this annotation @Override is completely optional, but it is always a good practice to
[05:24] mention these @Override annotation.
[05:27] Whenever you are trying to override a abstract method which inherited from a super interface, we also
[05:34] have another method which is stopVillan().
[05:36] So in both of these methods, as of now, we have a business logic to return a null.
[05:41] Let's try to change the same.
[05:42] So what I'm going to do is, I'm going to return a String value which is IronMan using his power.
[05:51] So this is the business logic which is specific to the IronMan.
[05:55] Now as a next step I can try to write my customization logic for the stopVillain() as well.
[06:01] Inside my stopVillain().
[06:02] Let me try to write an if block saying that if c equals to Y, I'm going to return a statement which
[06:11] is IronMan, kill the villain.
[06:14] Otherwise I'm going to write an else statement, which means I might have got a value n or different
[06:20] value other than y.
[06:21] In all such scenarios, I'm going to return a statement which is IronMan stopped the villain.
[06:27] So these are the logic that I have written.
[06:29] Now let me try to create one more superhero.
[06:33] The superhero name is going to be SpiderMan.
[06:37] And inside this SpiderMan also I'm going to implement SuperHero interface.
[06:42] So as soon as I implement this interface, you can see I'm getting a compilation error.
[06:45] So what I can do is, I can go to Iron Man, and I can try to copy the body of IronMan and paste it inside
[06:52] the SpiderMan.
[06:54] So now as a next step, I'm going to make few changes, which is related to SpiderMan.
[06:58] Here I'm going to mention SpiderMan using his power very similarly
[07:04] I can also update the statements SpiderMan kill the villain, SpiderMan stop the villain as an external.
[07:10] Let me try to do the same for the last superhero that we have, which is CaptainAmerica.
[07:17] And inside this class
[07:19] also, I'm going to implement the SuperHero interface post that I'm going to copy the body of the SpiderMan
[07:26] class and paste it inside the CaptainAmerica.
[07:29] As a next step, I'm going to update the logic saying that CaptainAmerica using his power, Captain
[07:36] America kill the villain, Captain America stop the villain.
[07:39] So this way we can create any number of classes that are inheriting from the same interface.
[07:46] So the advantage that we are getting with the interface is now all the classes which are related to
[07:52] the marvel superhero, they are going to follow the same standard or the specification or the contract
[07:58] that I have defined inside my SuperHero interface.
[08:01] Since I'm defining an interface, I don't have to worry about the implementation logic for these abstract
[08:07] methods.
[08:07] The classes who are trying to inherit my interface, they are going to provide the actual implementation
[08:14] logic.
[08:15] So just like how we established an inheritance between a class and an interface, very similarly, we
[08:20] can also establish the inheritance between two interfaces.
[08:24] So to demo you the same, I'm going to create a new interface inside the hero package.
[08:30] This time the interface name is going to be Person.
[08:34] So for now I'll just keep this Person interface as empty.
[08:37] Later on in the coming lectures, I will try to update this interface, but the point that I want to
[08:42] highlight here is, we can extend these Person interface into another interface as well.
[08:48] For example, I can go to the SuperHero interface here
[08:51] I should use the extends keyword followed by what is the interface name?
[08:55] I hope you are clear on how to implement our extend and interface inside Java
[09:00] with the help of inheritance.
[09:03] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
