# 10.20 — Demo of dynamic polymorphism using method overriding

> Section 10: Inheritance in Java

[00:00] As of now, we are able to successfully override a method inside the IronMan subclass based upon the
[00:07] method overriding concept that we have discussed.
[00:10] Now, using the same override method, I'm going to show you the demo of Dynamic Polymorphism for the
[00:17] same
[00:18] let me create a new class under the app package.
[00:21] The class name is going to be DynamicPoly
[00:24] is a class name.
[00:25] So this represents Dynamic Polymorphism.
[00:27] So now inside this class I'm going to create a main() method here.
[00:32] First I'm going to perform the Upcasting by using the Person and the IronMan class.
[00:38] So Person is a superclass.
[00:40] So first I'm going to mention the object reference with the name Person.
[00:45] And to this I'm going to assign the object of the IronMan which is a subclass of the Person superclass.
[00:53] So this is a Upcasting.
[00:55] So since this is an upcasting my compiler is not complaining anything.
[01:00] Now using the Person object reference, if I invoke the walk() method, which method do you think is going
[01:08] to be invoked?
[01:09] We have a walk method inside the Person superclass, and we also have a walk() method inside the IronMan
[01:16] class as well.
[01:17] So we already discussed about this scenario a lot many times in the previous lecture.
[01:21] So this should be easy,
[01:22] come on you should tell me.
[01:24] Yes you are correct.
[01:25] The walk() method present inside the IronMan is going to be invoked.
[01:31] So let me highlight the same here inside the comments.
[01:33] So IronMan walk() method is going to be invoked.
[01:39] I can also confirm you the say by running this program.
[01:42] So here you can see we are getting the output which is IronMan walking with his suit.
[01:48] Now here the Dynamic Polymorphism is happening.
[01:52] Do you know how
[01:53] so based upon what I'm assigning to this Person object reference the behavior of the walk() method is
[02:00] going to change.
[02:01] So if I'm trying to assign the IronMan object, then the walk() method present inside the IronMan subclass
[02:09] is going to be invoked.
[02:10] Whereas if I simply assign the Person object, then the walk() method available inside the Person class
[02:17] is going to be invoked.
[02:18] Very similarly, if I try to assign object of any other subclass accordingly, the walk() method is going
[02:25] to be invoked.
[02:26] So this confirms the same piece of code which is present at the line
[02:30] number ten is greatly influenced based upon the object that we are trying to assign to the Person object
[02:39] reference at the line number nine.
[02:41] So this is the classic example of Dynamic Polymorphism.
[02:46] And this is completely possible with the help of method overriding.
[02:51] So the Java compiler is going to decide which walk() method it has to invoke based upon the Dynamic Binding.
[02:58] Since the Binding is happening dynamically.
[03:00] So the Polymorphism is also going to happen dynamically.
[03:04] Whatever we discussed around the Dynamic Polymorphism I have mentioned the same inside this slide for
[03:10] your reference, along with the example that we have discussed.
[03:13] So please refer to this slide for any questions.
[03:16] Before I try to close this lecture, let me show you a meme related to the method overriding.
[03:22] So whenever a subclass is overriding a superclass method, it is going to tell to the superclass saying
[03:28] that look at me, I'm the captain
[03:31] now you need to listen to me because the subclass feels like it has its own power due to the overridden
[03:38] methods.
[03:39] I hope you like this meme.
[03:40] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
