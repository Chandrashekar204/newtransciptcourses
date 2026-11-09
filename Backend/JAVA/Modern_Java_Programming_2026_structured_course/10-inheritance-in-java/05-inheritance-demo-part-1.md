# 10.5 — Inheritance Demo - Part 1

> Section 10: Inheritance in Java

[00:00] Since we are into the new section, I have created a new Java project with the name section_10.
[00:06] .
[00:07] Inside this project only, I'm going to make all the changes that we are going to discuss related to
[00:13] Inheritance.
[00:14] For any questions, you can always refer to the GitHub repo that I have shared previously.
[00:20] Here under the section_10 project.
[00:22] I will open the source folder.
[00:23] As of now it is empty.
[00:25] First I'm going to create a new package and the package name I'm going to give as com.eazybytes.marvel.base
[00:33] .
[00:36] So these are random package name that I want to do based upon my scenario.
[00:41] Now inside this package I'm going to create a new class with the name Person inside this Person class.
[00:49] first I'm going to create few fields.
[00:51] The fields are going to be protected String followed by variable name which is name.
[00:58] Similarly, I'm going to create another variable which is protected int age.
[01:03] So these are the two variables that I want to create inside my Person class.
[01:07] And these two variables are fields
[01:09] they're going to be common for all the Marvel superheroes that we have.
[01:14] And do you know the reason why I'm using protected here?
[01:17] Because I want only my subclasses to be able to access my Java fields.
[01:23] That is the reason I'm trying to mention the protected here.
[01:26] Otherwise, if you mention public all kind of classes, they can access your fields.
[01:32] Private means only your own class should be able to access, and with the default all the classes within
[01:38] the same package they should be able to access.
[01:41] Whereas with protected all the classes and subclasses present inside the same package and the subclasses
[01:47] present inside the different package, they should be able to access my Java fields.
[01:52] As a next step, let me create the method which is public void eat().
[01:57] So eat() is the method to this method
[02:00] I want to pass an input which is String food and inside this method body I'm going to simply write a
[02:07] logic which is System.out.println() which and to this println() method.
[02:12] I'm going to pass a string message which is person is eating the food followed by semicolon space
[02:22] and at last I'm going to append the food input that we have received.
[02:26] As a next step, let me create few more methods here, which is public void walk() and to this walk() method
[02:33] I'm not going to pass any method input parameters.
[02:37] And inside this method also I'm going to write System.out.println().
[02:41] And to this println() method I'm going to pass an input which is person is walking after the walk() method
[02:49] similarly, I'm going to create one more method with the name sleep.
[02:53] So to this sleep() method
[02:55] also I'm not going to send any method input parameters.
[02:58] And inside this method I'm going to have a System.out.println() statement which is person is
[03:04] sleeping.
[03:05] So these are all the common behavior or the common attributes that I want to maintain for all my superheroes.
[03:12] So now my super class is ready.
[03:14] So did you see there is nothing new that we have to do to define a super class.
[03:19] And the person class itself does not know that it is going to act as a super class for other child classes.
[03:26] So that's a beauty we have here.
[03:28] As a next step, I can create the subclasses either in the same package or in the different package.
[03:33] So let me try to create a different package and the package name I'm going to keep it as com.eazybytes.marvel.heros
[03:40] .
[03:44] So inside this package I'm going to maintain all my heros related classes.
[03:49] So the very first class that I want to create here is related to the IronMan.
[03:54] So let me give the class name as IronMan.
[03:58] And since we want this IronMan to inherit the properties from the Person super class immediately after
[04:04] the IronMan, we need to mention the extends keyword followed by space, and after that you can type
[04:10] the super class name Person.
[04:13] As soon as I press enter, you can see there is a import statement automatically imported by the intelliJ.
[04:20] If it is not importing automatically, then you need to add these import statements manually.
[04:25] As a next step inside this IronMan class, I'm going to create a method which is public void usePower(),
[04:33] and inside this method I'm going to write as System.out.println() with the statement which is IronMan
[04:40] is using his power.
[04:43] So this is the business logic or the statement that we want to write, which is specific to the IronMan
[04:49] only.
[04:50] Very similarly, let me create other classes as well.
[04:53] For the same,
[04:53] I'm going to copy the IronMan and paste it inside the heros package.
[04:57] And with that it is going to ask
[04:59] me,
[05:00] what is the new name that we want to give for the new class that we are trying to create?
[05:04] So this time I'll give the name as SpideMan.
[05:08] As soon as I press enter, you can see I have the subclass which is SpiderMan, which is extending
[05:14] thePerson superclass.
[05:16] But inside this usePower(),
[05:18] this time instead of IronMan
[05:20] I want to mention the statement as SpiderMan is using his power.
[05:25] Let me create one more subclass here under the heros package.
[05:30] This time the class name is going to be CaptainAmerica.
[05:34] So as soon as I press enter, you can see the new class is created and inside this usePower(),
[05:39] I can mention CaptainAmerica is using his power.
[05:46] So let me correct the spelling mistake.
[05:48] So with this I have total three different subclasses that are extending the same parent which is Person.
[05:54] So now here you may ask me a question which is can you prove me that my all subclasses or child classes
[06:02] or derived classes.
[06:03] They are inheriting the properties or the methods of parent class.
[06:07] So that's a very valid question.
[06:09] Let me try to prove you that all child classes, they are going to inherit superclass properties and
[06:15] methods for the same
[06:16] I'm going to create a new package here under the Marvel the package name
[06:21] this time it is going to be marvel.app.
[06:24] So inside this app package only, I'm going to create a marvel's Main class with the name MarvelsMain.
[06:32] And inside this Main class I'm going to create the main() method.
[06:36] So psvm
[06:38] so with that shortcut you can see I have a main() method right now inside my MarvelsMain.
[06:43] So here you can create the object of any of the subclass.
[06:48] For example, if you like the IronMan, you can try to create an object of IronMan by using the class
[06:55] name of IronMan, which is IronMan itself.
[06:58] Followed by variable is equal to new operator IronMan.
[07:03] So this is the syntax that we need to use to create an object of a class.
[07:07] So now using these object reference of IronMan, if I press dot you will be able to see all the methods
[07:14] that you can invoke with the help of the IronMan object.
[07:18] You can see I'm able to see the methods like walk(), usePower(), eat() and sleep().
[07:24] So from where these walk(), eat() and sleep() methods are derived, those are derived or inherited from the
[07:31] parent class which is Person.
[07:33] As a next step, let's try to validate if my IronMan object is able to access the fields of Person
[07:40] superclass.
[07:41] So as of now here, if I type, I'm not able to see any field dot name.
[07:46] The reason is for the Java fields that we have created inside the Person class.
[07:50] We have mentioned them as protected, whereas for the methods we have mentioned the access modifier
[07:55] as public.
[07:56] That's why even when I'm trying to create the IronMan object in a different package, in a different
[08:02] class, that is not extending my parent superclass, I'm still able to access the methods like walk(),
[08:10] eat() and sleep() which are coming from the Person superclass, but I'm not able to access the Java fields
[08:17] from the Person using my IronMan object, because I have created the object of IronMan inside the
[08:23] MarvelsMain class, which is present in a different package.
[08:27] And since this MarvelsMain class is not extending the person, I will not be able to access these
[08:33] fields.
[08:34] For example, if I try to create the same main() method inside the IronMan class, this time I will be
[08:42] able to access the fields like name and age.
[08:46] You can see I'm able to access the fields.
[08:48] The reason is this time I'm creating the IronMan object inside a class which is extending the Person
[08:55] superclass.
[08:56] I hope you are clear.
[08:57] Let me remove this main() method from the IronMan class.
[09:01] So once this main() method is removed, we can go back to the MarvelsMain.
[09:06] And here first let's try to invoke the walk() method.
[09:10] And similarly, let me try to invoke the eat() method to the eat() method
[09:15] I'm going to pass the input as pasta, followed by I'm going to invoke the sleep() method.
[09:22] At last I'm going to invoke the usePower() method.
[09:25] So if I try to execute this main method, you will be able to see all the statements on the console
[09:31] confirming that that my subclass or child class
[09:35] they are deriving the methods from the superclass and the properties
[09:39] also they are getting derived.
[09:41] But for the properties, since we have mentioned the access modifier as protected, we are not able
[09:46] to access them from these
[09:48] Marvels main() method.
[09:49] I hope you are clear till this point.
[09:51] Let's try to continue this discussion in the next lecture as well.
[09:55] Thank you
[09:55] bye.

----------------------------------------
