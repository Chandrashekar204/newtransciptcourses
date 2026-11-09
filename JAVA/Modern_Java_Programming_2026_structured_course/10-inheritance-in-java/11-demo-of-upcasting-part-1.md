# 10.11 — Demo of upcasting - Part 1

> Section 10: Inheritance in Java

[00:00] Let's try to see the demo of Upcasting along with its advantages inside this lecture. For the same,
[00:07] first we need to make sure there is a superclass and subclass like you can see here
[00:11] we already have a superclass with the name Animal, inside this superclass
[00:15] first I'm going to create a String variable with the variable name as name.
[00:20] So let me try to create the same like private String
[00:23] and the variable name is going to be name.
[00:25] Post that I'm going to create a setter method and getter method to set the name value into this variable
[00:32] and to get the name value from this variable.
[00:34] So there is a shortcut to create a setter and getter methods.
[00:37] So what is that you need to perform
[00:39] right click and go to the option generate and select Getter and Setter.
[00:44] And here you can select for which variable you want to generate the getter and setter.
[00:50] So I'm trying to select the variable name and click okay.
[00:53] And you can see I have a getter method and setter method.
[00:57] So whenever someone is trying to invoke the set name they need to pass
[01:00] what is a name as an input.
[01:02] The same name is going to be assigned to this variable, which is present inside the object of the Animal.
[01:08] So that's what we are trying to achieve with the help of this code
[01:11] like this.name = name. After that getter and setter methods
[01:15] I want to create one more method inside my parent class.
[01:19] So the method name is going to be public void eat().
[01:22] And inside this eat() method I'm simply going to put an System.out.println() statement saying that
[01:29] Animal is eating.
[01:32] So this is the statement that I want to print whenever someone is trying to invoke the eat() method inside
[01:38] my Animal class.
[01:39] So we have superclass ready.
[01:41] Now let me go to the dog subclass and inside this we already have
[01:45] this extends Animal.
[01:47] And with this we should be good.
[01:49] We don't have to write any other logic inside that Dog class for now.
[01:53] As a next step, I'll go to the package of app and inside this package I'm going to create a Java class
[02:02] which is UpcastingDemo.
[02:05] Inside this UpcastingDemo class
[02:07] first I'm going to create the main() method.
[02:09] Inside this main() method,
[02:11] first I'm going to create the object of the Animal class.
[02:15] So let me try Animal anm is equal to new operator Animal constructor.
[02:22] Now using the anm object reference, I'm going to invoke the method setName().
[02:28] And to this I'm going to pass a name which is Scooby.
[02:32] So now if I try to print the name available inside the anm object with the help of getName() method,
[02:40] obviously I'm going to get the output as Scooby
[02:42] like you can see here.
[02:44] Inside the console I have the Scooby as an output.
[02:47] So till this point there is nothing new.
[02:49] But as a next step I'll try to perform the Upcasting.
[02:52] So what is an Upcasting?
[02:54] Upcasting is a process of assigning the object of a subclass to the object reference of the superclass.
[03:01] So what is a object reference of the superclass,
[03:04] it is anm.
[03:05] After that, I'm going to assign the object of child class or subclass which is Dog.
[03:11] So you can see I'm not getting any compilation error.
[03:15] So this line confirms the Upcasting is going to be always allowed inside Java automatically, because
[03:23] we can safely say that every subclass is a superclass.
[03:27] Like Dog is a animal, Cat is a animal.
[03:29] So anytime if you want to understand whether the up casting is happening, always check what do you
[03:34] have on the right hand side.
[03:35] So if you have on the right hand side a subclass object, and the same if it is being assigned to the
[03:42] superclass object reference which is present on the left hand side, then it is always going to represent
[03:48] upcasting in Java.
[03:49] So now using anm, I can invoke the setName() method.
[03:55] And this time I'll give a different name, which is Charlie, and post that I'll try to print the same
[04:01] with the help of anm.getName().
[04:05] So if I try to execute my program right now, you can see this time we'll get two outputs.
[04:10] One is Scooby and Charlie.
[04:12] So now you should be familiar with the upcasting process.
[04:16] But the next question that you may have is what is the advantage that I'm getting with this upcasting.
[04:21] Why do developers try to perform upcasting inside Java?
[04:25] So it's a very valid question.
[04:26] So to demo you the advantage of upcasting in Java, first let me create an utility class inside my
[04:35] app package.
[04:36] So the class name is going to be Animal Utility.
[04:40] Inside this utility class I'm going to create a static method with the name public static void
[04:48] and the method name is going to be printName().
[04:52] And to this printName() method, the input is always going to be the object of data type Animal.
[04:59] So
[04:59] I'm trying to mention the same here.
[05:02] And inside this method, the logic that I'm going to write is always print the name of the Animal object
[05:08] that we have received.
[05:09] So with the help of animal.getName().
[05:12] Now using these utility logic present inside my AnimalUtility, I'm going to build a common logic that
[05:19] is going to be executed regardless if I'm going to pass an object of Animal or object of a Dog class.
[05:26] So let me go to the UpcastingDemo class.
[05:29] So inside this class,
[05:30] so as of now, you can see we are trying to print the name manually by using this System.out.println().
[05:36] Instead
[05:37] what I'm going to do is I'm going to invoke the AnimalUtility class.
[05:42] And inside this utility we have a name which is printName()
[05:47] and to this I'm going to pass anm.
[05:50] And very similarly I'm going to mention the same just after that Dog object as well.
[05:56] So here if you see the same utility code is working for two different types of objects.
[06:03] One is the object of Animal, the other one is the object of Dog.
[06:08] Though I'm sending a two different objects with the help of the superclass object reference name.
[06:15] It is going to work because each subclass is going to inherit the method getName() present inside the
[06:22] superclass.
[06:22] So this is a great advantage that we have with the Upcasting inside Java.
[06:28] So you can write a common code that is going to be executed regardless
[06:33] you're going to pass an object of superclass or subclass.
[06:37] I can also show you a demo of this by creating one more subclass.
[06:41] So this time I'm going to create a one more subclass with the name Cat.
[06:46] So let me create the class here.
[06:48] The class name is going to be Cat.
[06:50] And inside this I'm going to extend the Animal.
[06:54] So let me mention the Animal superclass name.
[06:56] So now you can see my Cat is a subclass of Animal superclass.
[07:00] So now I'll go to UpcastingDemo.
[07:03] And here I'm going to write a new logic.
[07:06] The logic is going to be create the object of Cat with the help of Cat
[07:11] new cat here I'm not performing any upcasting.
[07:15] I'm simply trying to create the object of the Cat, which is a subclass.
[07:19] Now, using the Cat.setName() method, I'm going to assign a name to my Cat.
[07:26] The name can be Snoopy, and for that I'm going to invoke the AnimalUtility.printName().
[07:34] And to this I'm going to pass the object of Cat.
[07:36] So now if you see I'm going to get the proper output like inside the console Scooby, Charlie, Snoopy.
[07:43] So here, if you closely observe, I'm trying to send the object of cat to my printName().
[07:49] So inside the printName() method we are accepting a object of type Animal.
[07:55] So behind the scenes Java automatically is going to perform the Upcasting
[08:00] in this scenario.
[08:01] Though I'm sending an object of subclass my Java behind the scenes
[08:05] it is going to perform the Upcasting.
[08:07] And with that the logic present inside this method is going to be executed.
[08:11] I hope you are clear.
[08:13] So here the upcasting is happening automatically, whereas in the Dog scenario we perform the Upcasting
[08:20] with the help of this line of code, regardless of who is performing the Upcasting, Upcasting is always
[08:25] going to give the benefits to you where you can write a single piece of code, which is going to be
[08:31] executed for all the subclasses and superclass.
[08:35] So in future, whenever you are trying to introduce a new Animal as a subclass to the superclass, in
[08:41] that scenario, you don't have to worry about these logic.
[08:44] It is going to work perfectly without any issues.
[08:47] I can also show you a negative scenario here.
[08:49] For example, think like I'm not extending the Animal superclass in that scenario
[08:55] obviously I'm going to get a compilation error here.
[08:58] You can see I will not be able to send the Cat object as an input to the printName() method.
[09:04] I hope you are clear.
[09:05] Let me bring back this extends keyword.
[09:08] Now the compilation error should get resolved.
[09:11] I hope you are clear with the demo of Upcasting and the advantage of it.
[09:15] Let's try to continue discussion around Upcasting in the next lecture as well.
[09:20] Thank you,
[09:20] bye.

----------------------------------------
