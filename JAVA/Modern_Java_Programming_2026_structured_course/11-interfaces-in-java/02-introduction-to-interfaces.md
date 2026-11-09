# 11.2 — Introduction to Interfaces

> Section 11: Interfaces in Java

[00:00] We use USB drives or pen drives a lot on our day to day basis.
[00:06] The same pen drive or USB drive, we should be able to connect to various brands of laptops, and even
[00:13] we should be able to connect the USB drive to the smart TV.
[00:17] So how is this is possible?
[00:19] This is because there is an international standard body which takes care of publishing
[00:25] the standards or specifications or a guidelines to build an USB drive or a pen drive.
[00:31] So any company who are manufacturing the laptops, smart TVs, they should stick to the same specification
[00:38] or the guideline which is published by the international standard body around the USB drives.
[00:44] That's why the same USB drive were able to connect across devices without any issues.
[00:50] The same kind of specifications or
[00:53] the guidelines is usually published by many organizations to bring some consistency in the implementing.
[01:01] For example, in the covid time, the World Health Organization, it published the guidelines at the
[01:07] protocol or the specifications that every hospital in the world that has to follow to treat a Covid
[01:15] positive patient.
[01:16] Along with the treatment, they also published the specifications or the guidelines on how to clean
[01:23] the surrounding of the hospitals or the surroundings of the Covid affected person.
[01:27] Why I'm telling about all these right now.
[01:30] This is because whatever I have discussed just now, they are very closely related to the interfaces
[01:37] concept in Java.
[01:38] So what is an Interface, in Java
[01:41] Interface provides a way to define a contract that a class must follow in order to implement a certain
[01:50] set of behaviors.
[01:51] For example, think like you have a scenario where you are going to build a group of classes around
[01:57] that business scenario.
[01:59] So in this kind of scenarios to bring some consistency in all these group of classes, we can define
[02:05] a contract or a guideline or the specifications with the help of an Interface.
[02:11] So inside an Interface we can define all abstract methods without worrying about the actual implementation
[02:18] logic.
[02:18] And all the classes who are trying to implement these Interface, they need to adhere to the contract
[02:25] or the specifications that we have defined with the help of abstract methods.
[02:30] In simple words, an Interface always going to provide method, signature, return types and parameters
[02:36] that the implementation classes must follow.
[02:38] Here you might be clear about the definition of interface and you may say okay, I understand what is
[02:45] an Interface and what's the definition of it.
[02:47] But the question you may have here is what are the advantages that I am going to get with Interfaces?
[02:53] And why should we define Interfaces first of all inside a Java project.
[02:57] So it's a very great question and a valid question.
[03:00] So let's try to discuss more details about Interface by taking a scenario.
[03:04] Think like you have a business requirement where you want to build a multiple Java classes that portray
[03:11] different heroes that we have inside the Marvel Universe.
[03:16] Like inside Marvel Universe, we have IronMan, SpideMan, CaptainAmerica.
[03:21] This way we have many other superheroes inside the Marvel Universe.
[03:26] So the task that you have right now is you need to build the Java classes representing each of these
[03:32] superheroes. In real projects
[03:35] obviously, a single developer is not going to develop all the Java classes, so the task is going to
[03:41] be divided among the multiple developers.
[03:43] Think like you, as one of the developer received this task and your team manager or team lead, he
[03:49] has given a day time to implement these business logic since three developers, they are going to work
[03:55] on these three different classes.
[03:57] This is how the final result from three different developers.
[04:01] You can see every developer
[04:03] he created a class representing his superhero like IronMan, SpiderMan and Captain America.
[04:10] All these superheroes, they have a common behavior, which is they have a special power using which
[04:17] they can kill or stop a villain.
[04:19] So these two behaviors is implemented by using different method names, different method signature by
[04:28] different developers.
[04:29] For example, inside the IronMan, the method name is usePower(), which is not going to return anything,
[04:35] whereas inside the SpiderMan the method name is applyPower() with the return type of int, and in the
[04:42] Captain America we have the method name as throwPower() with the return type of String.
[04:47] Similarly, regarding the behavior around the stopping the villain or killing the villain, we have
[04:52] different method names with the different method signatures.
[04:55] So from this, it should be pretty clear for you that there is no consistency
[04:59] though
[05:00] all the superheroes have the common behavior.
[05:03] So to handle these kind of scenarios, only we can have an interface in Java.
[05:08] Before we try to understand how to resolve this problem with the help of Interfaces in the coming lectures.
[05:14] First, let me more details about the disadvantages that we have
[05:18] if we don't follow Interfaces in Java, like we discussed in the previous slide, three different developers,
[05:25] they develop three different classes representing three different superheroes from the Marvel Universe.
[05:30] The very first disadvantage with this approach is each developer has written the classes methods inside
[05:37] them based upon their own understanding.
[05:39] Though all these heroes have the common functionality.
[05:42] The method names the return type, and the accepting parameters are different, so there is no consistency
[05:49] like we discussed.
[05:50] So what is the problem if we don't have any consistency?
[05:53] Think like you want to go with the war with Thanos, and you may want to call all your superheroes and
[06:00] invoke their powers, issue commands to kill the villain.
[06:03] So in this kind of scenarios, since we have no consistency inside the superhero Java implementation
[06:10] classes, the code that you are going to write to invoke all the methods present inside these superheroes
[06:17] is going to be super clumsy, and you need to write a lot of code handling different, different superheroes
[06:23] in a different manner.
[06:25] For example, if you want to invoke the method related to the power inside the IronMan, you need to
[06:30] invoke these usePower() method.
[06:32] And we can't use the same logic to invoke the power related method present inside the SpiderMan, because
[06:38] the method name is different.
[06:40] So these kind of problems you will face due to inconsistency code.
[06:45] And here you may also have a question why can't we solve this problem by defining a super class?
[06:51] And inside the super class we can have all these common functionality.
[06:56] I agree with you.
[06:57] To some extent we can follow that approach, but the problem with the super class is whenever you are
[07:03] trying to define a super class, the developer has to provide some implementation logic and the subclasses.
[07:11] Either they can follow that implementation logic, or they can override the super class methods with
[07:17] their own implementation logic.
[07:18] For example, think like you have 100 different methods representing 100 different common functionality
[07:25] between multiple classes.
[07:27] In such scenarios, why should we force a developer to define a super class
[07:32] and inside the super class, he need to write 100 different methods, and inside the 100 different methods,
[07:38] he need to provide some default common implementation.
[07:41] So to avoid such kind of pain points, we can follow the Interface approach.
[07:47] When we use the Interface approach, we don't have to provide any implementation logic.
[07:52] The Interface can simply define the specifications or the contract, or the guidelines that all the
[07:58] superhero related classes has to follow.
[08:01] So the advantage that we get when we use Interfaces is, we are going to build a more maintainable, reusable
[08:08] and modular code.
[08:10] So just like how a subclass can inherit from a super class, very similarly, with the help of Inheritance,
[08:16] a class can inherit the specifications from the Interface.
[08:21] Once the Inheritance is established between an Interface and a Java class, the Java class has to take
[08:27] care of implementing the business logic in all the abstract methods which it inherited from the Interface.
[08:33] I hope you got a clarity around what is an Interface, what are the problems that we may face without
[08:39] interface.
[08:40] From the next lecture, let's try to understand how to create an Interface, how to define a contract
[08:46] or specification with the help of Interface, and how to use an Interface to provide an consistency
[08:52] behavior across multiple classes.
[08:55] Thank you, and I'll catch you in the next lecture bye.

----------------------------------------
