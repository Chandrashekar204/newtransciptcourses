# 10.14 — instanceof Operator

> Section 10: Inheritance in Java

[00:00] In the previous lectur,
[00:01] while we are discussing about the Downcasting, I told you that there is a very good chance of getting
[00:07] a Runtime ClassCastException whenever we are doing a downcasting.
[00:12] Do you know under which scenarios we are going to get this exception?
[00:15] We are going to get this exception if a developer perform an invalid downcasting.
[00:20] For example, here inside this line of code we know a enum object reference.
[00:26] It is going to hold the object of Dog class, but if you try to downcast it to Cat, we are going to
[00:33] get a RuntimeException.
[00:35] So let me show you this demo one more time.
[00:37] You can see I'm getting a ClassCastException.
[00:41] That's why while you are trying to perform that downcasting, you need to be very careful regardless
[00:46] of how careful you are
[00:48] sometimes this RuntimeException may happen because someone might have invoked your method with an object
[00:55] reference, and that object reference may not hold the Cat object that you are expecting.
[01:01] So to handle these kind of scenarios in a more, better and safe manner, we have an operator which
[01:07] is instance of operator with the help of instance of operator.
[01:12] Before we try to perform the downcasting, we can validate if the given object reference is holding
[01:19] a desired object.
[01:20] So let me show you the demo of this here.
[01:22] First I'm trying to create an if block.
[01:25] And inside this if block I'm going to move these Downcasting code.
[01:29] So this Downcasting code is going to be executed only when my if expression is going to become true.
[01:36] So inside my if expression first I'm going to check if my A an object reference is holding the object
[01:44] of Cat.
[01:45] So how to do that?
[01:47] After mentioning the object reference name which is anm, I can use instance of operator.
[01:53] So you can see this is an operator inside Java.
[01:56] You need to type instance of without any space and capital letters.
[02:01] Post this instance of keyword, you need to mention the class name like Cat
[02:06] you need to mention here because I want to check whether this a an object reference is pointing to a
[02:12] object of type Cat.
[02:14] So only when this condition is true, then only I am going to perform that downcasting.
[02:19] Otherwise I'm not going to perform the Downcasting.
[02:22] And with that we'll be saved from the RuntimeExceptions.
[02:25] So if I try to execute this program this time, you can see we are not getting any exception because
[02:31] my if block never executed.
[02:33] I hope you are clear with the purpose of instance of operator.
[02:37] Now let me try to answer your question, which is what is the advantage that we get with the downcasting
[02:43] under which scenarios the developers may have to do the Downcasting.
[02:47] So to demo you the same, I'll go back to the AnimalUtility.
[02:51] Inside this utility I am going to write a new static method.
[02:55] The static method that I am going to create here is public static void, and the name of the method
[03:02] is going to be performAction().
[03:05] So to this method also I'm going to accept the object of type Animal.
[03:10] And inside the static method I'm going to write some business logic before I try to define some business
[03:15] logic inside this method.
[03:16] First I want to go to the Cat class, and here I want to create a method which is specific to Cat alone.
[03:23] So the method name is going to be public void meow.
[03:28] Because cat is the only animal which can perform the meow action or meow sound.
[03:34] So inside this method I'm going to write a println statement which is Cat is meowing.
[03:41] So this is the data that I want to pass to the println() method.
[03:45] Now very similarly, let me try to create a method inside that Dog subclass as well.
[03:50] So inside the Dog subclass I'm going to first copy the meow() method post that I'm going to rename this
[03:56] to bark(), because dog is only the animal that is capable of barking.
[04:01] So inside this bark() method I'm going to update this println() statement which is Dog is barking.
[04:09] So now you can see my Dog and Cat class
[04:12] they are going to have their own method which which is bark() and meow().
[04:17] So these methods exist inside my subclasses only.
[04:20] They are nowhere related to the superclass.
[04:23] So now I'll go to the AnimalUtility.
[04:25] So here I want to write a piece of logic based upon the object type that I am receiving.
[04:31] First, using the Animal object, I'm going to invoke the eat() method.
[04:36] Since all kind of subclasses and the superclass, they have this eat() method.
[04:41] This line of code is going to execute for all kind of subclasses object and superclass object.
[04:47] As a next step, I want to invoke the bark() method, for example using the Animal.
[04:53] If I try to invoke the bark() method, I'm going to get a compilation error because right now Animal object
[04:59] reference is pointing to the Animal superclass and inside the Animal superclass we don't have any method
[05:06] with the name bark().
[05:07] So what I can do here is first I can remove this code post that I will write the if block and inside
[05:13] the if condition I'm going to perform if Animal instanceof Dog.
[05:18] So when this expression becomes true inside my if block, I'm going to perform that Downcasting.
[05:24] So how to do the Downcasting?
[05:26] I'll just mention Dog = animal.
[05:29] So with this the downcasting is not going to happen automatically.
[05:33] We need to specifically do the casting with the help of parentheses and inside the parentheses.
[05:38] We need to mention the Dog class name.
[05:40] Post that using the Dog object reference name, I can try to invoke the bar() method very similarly
[05:46] I can also write one more else if statement and inside this else if statement, I'm going to check whether
[05:52] my given animal instance belongs to Cat.
[05:55] So let me try to copy the same condition here and post that I will change this to Cat.
[06:01] So once I have mentioned this condition, I can write very similar logic inside my else if block also.
[06:07] So instead of casting to the Dog, I will try to do the down casting to the Cat class.
[06:12] So let me copy this Cat class name everywhere and the reference name
[06:16] also, I'll try to update to Cat, and now using the Cat I'm going to invoke the method which is meow().
[06:23] So if you see the beauty here, the same method is able to handle all kinds of objects that it may receive.
[06:31] I may receive a superclass object, or I may receive a subclass object.
[06:35] So if I don't have the concept of downcasting and instanceof operator, then I need to write this
[06:41] perform action methods multiple times accepting different data type like in total, I need to write
[06:48] three different methods one
[06:49] accepting the Animal object, the second one accepting the Dog object, and the third one accepting
[06:54] the Cat object, which will make your code complex and lengthy.
[06:57] So to handle these kind of scenarios, we can use the Downcasting.
[07:01] And whenever we are trying to perform the Downcasting with the help of instanceof operator, we can
[07:07] make sure the Downcasting is not creating any issues at runtime.
[07:11] I hope you are clear.
[07:12] Now I'll go to the DowncastingDemo.
[07:14] Inside this class I'm going to invoke the class which is AnimalUtility and post that I'm going to invoke
[07:22] the perform action and to this perform action I'm going to send these dog reference name.
[07:28] So what does this dog reference name holding?
[07:30] It is holding the data type of Dog.
[07:33] That's why when we execute this program, we'll be able to see a statement which is Dog is barking from
[07:40] the bark() method and Dog is eating from the eat() method.
[07:44] Similarly, if you try to pass a Cat object, then you'll get Cat is eating and Cat is meowing.
[07:51] So such kind of output you're going to get if you pass a Cat object.
[07:56] I hope you're clear about the instanceof operator
[07:58] and with the advantage of downcasting.
[08:01] Let's try to continue the discussion of instanceof operator in the next lecture as well.
[08:06] Thank you,
[08:07] bye.

----------------------------------------
