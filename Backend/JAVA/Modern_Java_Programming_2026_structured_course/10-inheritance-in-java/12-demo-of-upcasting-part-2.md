# 10.12 — Demo of upcasting - Part 2

> Section 10: Inheritance in Java

[00:00] Inside this lecture, I am going to show you a complex scenario that you may face whenever you are dealing
[00:06] with the Upcasting scenario.
[00:08] So to show you this demo, first let me go to the Animal superclass.
[00:12] So inside this superclass, as of now you can see we have a method which is public void eat().
[00:19] So the same method is going to be inherited by the subclasses.
[00:23] But let's try to take a scenario where the subclasses, they are trying to override this eat() method
[00:29] that is received from the parent superclass.
[00:32] So first we are going to override this method inside the subclasses and post that
[00:37] I'm going to show you a small demo.
[00:38] What is going to happen in this kind of scenarios?
[00:41] Whenever we are dealing with Upcasting, I'll copy this method and I'll go to the Cat.
[00:46] And inside this Cat class I'm going to paste the same method, but instead of Animal is eating, I'm
[00:52] going to mention the logic as Cat is eating.
[00:56] So if you see here the eat method which is present inside the Animal superclass is being overrided by
[01:03] the Cat subclass.
[01:04] So if I look for the list of methods inside the Cat subclass, I'm going to have only one method of
[01:11] eat().
[01:12] And whenever someone is trying to invoke the eat() method with the help of Cat object, whatever method
[01:18] that we have inside the subclass is going to be invoked, but not the method present inside the superclass.
[01:25] I hope you are clear.
[01:26] Let me try to copy the same method into the Dog subclass as well.
[01:32] So inside this class as well, I'm going to paste the same method.
[01:35] And here the logic is going to be Dog is eating.
[01:38] Now we have our subclasses overriding a method present inside superclass.
[01:43] As a next step, I'll go to the UpcastingDemo.
[01:45] Inside this class I'm going to make few code changes.
[01:48] So just after this line number 12, I'm going to invoke the eat() method with the help of a anm object
[01:55] reference.
[01:56] Let me do the same after the line number 17.
[01:59] So here also I'm trying to do.
[02:00] After defining these two lines of code, let's try to understand what is the output that we are going
[02:06] to get from the eat() method that we have defined at the two different places.
[02:11] So at the line number 13 I'm going to get the output which is Animal is eating because the eat() method
[02:19] present inside the Animal class is going to be invoked.
[02:22] But if you try to evaluate the next eat() method present at the line number 18, so which method is going
[02:29] to be invoked?
[02:29] Do you think that eat() method inside the superclass or eat() method present inside the subclass?
[02:35] So which eat() method is going to be invoked?
[02:37] Do we have any guesses here?
[02:39] If you guess that the eat() method present inside the Dog class is going to be invoked, then you are
[02:45] correct.
[02:45] So let's try to understand how this is going to happen.
[02:48] So here at the line number 15, the upcasting is going to happen after the upcasting is happening
[02:55] if you try to invoke one of the method which is present in both the superclass and the subclass in such
[03:01] scenarios, your Java, it is always going to invoke the method present inside the subclass, because
[03:07] to this reference we are passing the object of Dog, which is a subclass.
[03:12] So using these object of subclass, only the method is going to be invoked.
[03:17] That's why always the thumb rule is whatever physical object that you are trying to assign to the object
[03:23] reference.
[03:24] The same class data type method is going to be invoked in the very first scenario
[03:29] here we are trying to assign the object of Animal class itself.
[03:32] That's why with this piece of code we are going to get the output which is Animal eating.
[03:37] Whereas with this line of code we are going to get the output as Dog is eating, because we are trying
[03:43] to assign the Dog object to the anm object reference.
[03:48] So let's confirm the same by executing this program.
[03:51] You can see we are getting first Animal is eating.
[03:53] Later on we are getting Dog is eating.
[03:56] I hope you are clear.
[03:57] What I can do is I can take this anm.eat() and mention the same inside the printName() method.
[04:04] So let me update the variable name which is animal.eat() post that
[04:09] I can try to remove this code as well.
[04:11] So now what is going to happen is whenever we call the printName() method, we are going to pass the
[04:17] object reference to this object reference
[04:20] we are going to assign a physical object based upon the physical object that you have assigned.
[04:24] The same is going to be considered to invoke the eat() method.
[04:29] So let's try to execute this UpcastingDemo.
[04:31] And this time you're going to get the output
[04:33] Animal is eating, Dog is eating and Cat is eating.
[04:37] I hope you are clear with the upcasting and the scenario that we have discussed.
[04:41] Whenever you are trying to build a common logic, that is going to be same for your superclass and subclasses,
[04:48] then always try to leverage the Upcasting.
[04:50] You don't have to do anything.
[04:52] You can simply write a common logic and try to accept the object of the superclass.
[04:58] And to this method
[04:59] regardless of your object input data type, the code is always going to work without any issues because
[05:06] behind the scenes upcasting is going to happen by your Java compiler.
[05:10] So since the same code is executing and behaving differently based upon different inputs.
[05:17] So this kind of behavior we call polymorphism inside Java.
[05:22] More details about polymorphism we are going to discuss in the coming lectures.
[05:26] For now I just wanted to give you a clue around the polymorphism in the next lecture.
[05:30] Let's try to understand what is downcasting.
[05:33] Thank you,
[05:34] bye.

----------------------------------------
