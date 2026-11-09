# 10.21 — super keyword to invoke super class methods from sub class

> Section 10: Inheritance in Java

[00:00] Sometimes when we are overriding the methods of superclass inside the subclass, we may have a requirement
[00:07] to invoke the superclass method from the subclass.
[00:12] I know it may not be clear, so let me try to explain this scenario with an example. For the same inside
[00:19] my Person class
[00:20] as of now you can see I have a eat() method.
[00:23] So the eat() method is having a logic which is Person eating the food.
[00:28] And to this statement, the food that we are sending as an input is going to be append.
[00:33] Now inside my IronMan I'm going to overwrite this eat() method.
[00:38] So how to do that?
[00:39] First we need to make sure we are mentioning the Override annotation followed by,
[00:43] we need to make sure we are mentioning the same method name, same input parameters, same return type.
[00:50] That's why I'm trying to copy the method from the superclass and paste it here just below the Override
[00:56] annotation.
[00:57] Now inside this method I'm going to pass a different input to the println() method.
[01:03] So let me remove this person and mention IronMan is eating the food.
[01:10] So this is what I want to change inside this eat() method.
[01:13] Till this point I hope you are clear.
[01:15] We have not done anything we have done only the method overriding.
[01:19] Now think like I have a scenario to invoke the eat() method present inside the superclass from my subclass.
[01:28] So from my subclass which is IronMan, I want to invoke the eat() method present inside the Person superclass.
[01:35] So how to do that?
[01:36] So in this kind of scenarios you need to use the super keyword.
[01:41] So first you need to type super followed by dot operator.
[01:46] And with that you're going to have an option to invoke all the parent class methods and parameters.
[01:54] So here I have a eat() method.
[01:57] You can see to this eat() method I can pass an input which is Pasta.
[02:02] Very similarly maybe from one of my private methods present inside my subclass,
[02:08] I want to invoke the eat() method available inside the Person superclass.
[02:12] So let's try to understand how to do that.
[02:14] For the same, I'm going to write a private method, and the method name that I'm going to give here
[02:20] is call overridden eat() method.
[02:24] So this is the method name.
[02:26] So it seems there is a spelling mistake.
[02:27] Let me add one more d here.
[02:29] So now from this method I want to invoke the eat() method present inside the Person superclass.
[02:35] So if I try to simply type eat() inside this private method, I'm going to invoke the overridden method
[02:44] present inside the subclass.
[02:46] So I'm going to invoke this.
[02:48] But since I want to invoke the method present inside the superclass, that's why I need to use the super
[02:55] keyword.
[02:55] So if I just mention super.eat() in this scenario, the method present inside the superclass is going
[03:03] to be invoked.
[03:04] So whenever you have a situation where you want to call a method of superclass or a field of superclass,
[03:12] you should always use the super keyword.
[03:15] I hope this is clear.
[03:16] Now let me show you the demo of this by going to the Dynamic Polymorphism class here
[03:23] what I can do is, using the same Person object reference
[03:28] I'm going to invoke the eat() method.
[03:30] So to this eat() method I'm going to pass the input which is Icecream.
[03:36] So let's try to understand how this is going to work.
[03:38] So if I try to keep a breakpoint inside my eat() method of my IronMan class, the execution is going to
[03:46] stop.
[03:46] So let me execute this program and you can see the execution is stopped here.
[03:51] So first the eat() method present inside the superclass is going to be invoked.
[03:56] That's why as soon as I execute this statement I'm going to get an statement inside a console, which
[04:02] is Person is eating the food pasta.
[04:04] Now, if I try to continue with the execution by releasing the breakpoint, you will be able to see
[04:10] the other statement as well, which is IronMan is eating the food Icecream.
[04:15] So this confirms our eat() method present inside the Person superclass is also being invoked because we
[04:22] are using the super keyword.
[04:24] Similarly, if you try to invoke this private method as well, from this private method, we are invoking
[04:31] the eat method* present inside the superclass.
[04:34] I can also show you a demo for the same
[04:36] I can change this to public, and I'll go to the DynamicPoly class.
[04:41] Here in order to invoke the method of this callOverriddenEatMethod() , I have to create an object of IronMan.
[04:48] I can't use the object reference of Person because using Person object reference, I cannot invoke the
[04:55] method available which is specific to the subclass alone.
[04:59] .
[05:00] So that's why first let me create the object of IronMan.
[05:03] So once this object is created using the IronMan variable, I'm going to invoke the method which is
[05:10] callOverriddenEatMethod().
[05:12] This time, if I try to execute this program, you will be able to see a statement inside my console
[05:18] which is Person is eating the food pasta.
[05:21] This is because from the method callOverriddenEat Method() we are trying to call the eat() method present
[05:28] inside the superclass.
[05:29] If you remove these super, then the method which is present inside the same subclass is going to be
[05:35] invoked.
[05:36] You can also confirm the same by running the program again one more time.
[05:40] This time you can see we are getting the output as IronMan is eating the food pasta.
[05:45] I hope you are clear.
[05:46] Let me bring back my super keyword here.
[05:49] So always use the super keyword to access the super class related variables or methods.
[05:56] All the points that we have discussed are on the super keyword
[05:59] I have updated inside this slide for your reference, along with the example that we have discussed
[06:05] before
[06:05] I try to close this lecture
[06:07] I want to share an very important note around the super keyword.
[06:11] So if you see here this last point, it is highlighting
[06:15] we cannot invoke the instance method that is available inside the super class,
[06:21] super class.
[06:22] That means, for example, in a scenario where we have three classes like A, B, and C, if B is inheriting
[06:29] from A and C is inheriting from B, then there is no direct mechanism for my C class to call the methods
[06:37] of class A, because for my class A is a super class of super class.
[06:42] So to achieve this we must create a method first in the middle super class, which is class B that calls
[06:49] a method inside the class A with the help of super keyword.
[06:53] Then class C can call the method inside the class B, which in turn is going to invoke the method in
[07:01] class A.
[07:01] So this indirect approach is necessary for invoking the methods of the distant to super classes in the
[07:09] inheritance hierarchy.
[07:11] I hope you are clear.
[07:12] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
