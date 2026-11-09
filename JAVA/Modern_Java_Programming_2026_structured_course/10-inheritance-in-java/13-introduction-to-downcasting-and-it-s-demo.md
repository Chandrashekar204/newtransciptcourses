# 10.13 — Introduction to downcasting & it's demo

> Section 10: Inheritance in Java

[00:00] What is downcasting ? downcasting is the exact opposite of upcasting.
[00:06] Inside the upcasting, we are going to assign the object of a subclass to the superclass, but if you
[00:12] try to do the exactly opposite of it, which is assign an object of superclass to the object reference
[00:18] of subclass, then we are going to call it as downcasting.
[00:22] First, let me show you a demo of downcasting.
[00:25] Later on, we can discuss more details about downcasting. For the same here
[00:30] inside my app package, I'm going to create a new Java class with the name DownCastingDemo.
[00:37] Inside this DownCastingDemo.
[00:39] First I'm going to create the main() method inside my main() method
[00:43] first I'm going to create the object reference of superclass which is Animal pose.
[00:48] This Animal object reference I want to create the object of Dog class.
[00:53] So let me create it with the help of new operator and default constructor of Dog class.
[00:59] So now you can see we have a object reference of superclass.
[01:03] And we also have an subclass object.
[01:06] So if you try to type anm = dog.
[01:11] So this is perfectly acceptable inside Java because this is upcasting because we are trying to assign
[01:18] an subclass object to the superclass object reference.
[01:22] But if you try to do the opposite of it, we are going to get a compilation error.
[01:27] So let me type dog = anm.
[01:31] So you can see I'm getting a compilation error because inside Java by default downcasting is not allowed.
[01:39] So to resolve this compilation error we need to tell specifically to the compiler.
[01:44] I'm aware of the fact that I'm trying to downcast, and I'm sure that these Animal object reference
[01:49] is holding the Dog object, so we need to give an assurance to the compiler to resolve this error.
[01:56] So how to give that assurance just before your anm object reference we need to mention parentheses.
[02:03] And inside the parentheses we need to mention the subclass name which is Dog.
[02:07] And with that you can see the downcasting
[02:10] right now it is allowed.
[02:11] So here we are trying to assign a superclass object reference or superclass object data type to a subclass
[02:19] object to reference.
[02:21] So this is called downcasting.
[02:23] So why Java is not allowing this automatically is by default we can't say that every Animal is a Dog.
[02:30] It is going to be invalid because under Animal we may have cat, we may have horse, we may have elephant.
[02:35] So since it is invalid to call every Animal as a dog, your compilation is going to stop you with a
[02:41] compilation error.
[02:42] So you as a developer, you need to give a assurance or confidence to your Java compiler saying that
[02:49] that these anm is holding the object of Dog.
[02:52] So how to give that confident or assurance by mentioning the subclass name within the parentheses just
[02:59] before this name.
[03:00] So the same kind of syntax we also followed for primitive data types casting as well.
[03:05] So with this syntax we are able to manually perform the downcasting.
[03:10] But whenever we are trying to perform the downcasting we need to be very careful.
[03:14] We need to perform the downcasting only if we are 100% sure that these anm is going to hold the object
[03:22] of Dog.
[03:22] Otherwise we are going to get a RuntimeException which is ClassCastException.
[03:28] So let me show you a demo around this.
[03:30] For the same I'm going to first create the object reference of Cat subclass, followed by I'm going
[03:37] to assign the a anm object reference.
[03:40] And with that I'm going to get a compilation error because by default downcasting is not allowed.
[03:45] So to resolve this issue I can simply say Cat within the parentheses and my compilation error is resolved.
[03:53] But if I try to execute this program at runtime, I'm going to get a ClassCastException.
[03:59] I can show you that as well by running my program in a debug mode.
[04:03] You can see I got a ClassCastException saying that inside my anm object reference we are holding the
[04:10] Dog object, but we are trying to assign that to the Cat.
[04:13] So since they are representing two different classes, the casting is not going to be allowed.
[04:19] That's why we are getting the ClassCastException at line number 16.
[04:25] So that's why always please make sure you are 100% sure that your object reference is holding the actual
[04:33] object of your subclass whenever you are trying to perform that downcasting.
[04:38] Otherwise, you're going to get the surprises like we discussed.
[04:41] I hope you are clear what is downcasting.
[04:43] I know you may have a question here, which is what is the advantage of downcasting?
[04:48] Why a developer will try to perform the downcasting.
[04:51] I'll explain about the advantages of downcasting in the coming lectures.
[04:55] First, we need to discuss about the instance of operator.
[04:58] So once we discuss about
[05:00] the instance of operator post that I'm going to show you the advantages of downcasting, but
[05:05] I'm assuming with all the discussions that we have done, you are pretty clear about what is Upcasting
[05:11] and Downcasting.
[05:12] All the data points that we have discussed around the Upcasting and Downcasting
[05:16] I have mentioned all of them in these three slides, so please refer to them for any questions.
[05:22] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
