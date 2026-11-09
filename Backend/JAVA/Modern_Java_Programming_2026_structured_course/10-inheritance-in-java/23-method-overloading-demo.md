# 10.23 — Method Overloading - Demo

> Section 10: Inheritance in Java

[00:00] Inside my IronMan subclass, I'm going to write multiple eat() methods so that I can show you a demo of
[00:08] method overloading.
[00:09] So just after this overridden method, I'm going to create one more eat() method.
[00:14] So this time I'll just try to mention private void eat().
[00:19] And I'm not going to accept any method input parameters.
[00:23] And inside this method I'm going to write a simple System.out.println() saying that method overloading
[00:31] one followed by I'm going to create one more method similarly with the same name eat().
[00:37] .
[00:37] But this time I'll try to give some different access modifier, and at the same time I'm going to accept
[00:44] different input parameters like first String food, followed by int quantity.
[00:49] So these are the two method input parameters that I want to accept.
[00:53] Post that I will change this System.out.println()
[00:56] from method overloading one to method overloading two.
[01:00] Now if we try to see the list of methods available inside this IronMan class, you'll be able to see
[01:07] three different eat() methods.
[01:10] So you can see these three methods are overloaded methods because they all have same method name, but
[01:18] they have different method input parameters.
[01:21] I can try to invoke any of them very easily.
[01:24] Let me show you the same.
[01:26] I'll try to create a one more Java class here with the name StaticPoly.
[01:32] So this name indicates Static Polymorphism.
[01:35] Now inside this class first I need to create the main() method followed by
[01:39] I'm going to create the object of the IronMan with the help of IronMan class itself.
[01:46] Once the object is created using the same, I'm going to invoke the eat() methods.
[01:51] You can see I can only invoke only one of the eat() method, which is accepting the String method input
[01:59] parameter.
[02:00] So to this I can mention pasta.
[02:02] The reason why I'm able to invoke only one from this class is if you closely look at these methods.
[02:08] One of the method I have defined as private, the other one I have defined as protected.
[02:13] Maybe here instead of protected, I can mention public so that now I should be able to access eat() method
[02:21] with the help of IronMan object.
[02:23] So here you can see now I'll be able to access other overloaded method which is going to accept two
[02:30] different method input parameters
[02:32] one is of type String.
[02:34] So I can mention the food name as pasta followed by quantity as one.
[02:39] So if you closely look at these two lines we are invoking the same method which is eat() but a different
[02:46] input method parameters.
[02:48] So this is a classical example of Static Polymorphism that we are able to achieve with the help of method
[02:55] overloading.
[02:56] I hope you are clear.
[02:57] Regardless of you have this override method inside your subclass or not
[03:02] still, you can perform the method overloading because even if you don't have this overridden method
[03:07] inside your subclass, still it is going to be inherited from the superclass.
[03:12] And like I said before, you need to follow a rule to identify whether we have overloaded methods inside
[03:19] a class or not.
[03:20] The rule is first you need to write what is your method name like
[03:24] eat() followed by a separator like comma and post that you can mention what is the method input parameter
[03:31] data type.
[03:32] So for the first method we have a method input parameter data type which is String.
[03:37] If you try to do the same exercise for the second method, the method name is going to be same and after
[03:43] the comma
[03:44] you can't mention any method input parameter data type because it is not going to accept anything.
[03:49] Very similarly, if you try to do the same for the third method, we are going to have two different
[03:55] method input parameter data types.
[03:57] First one is String followed by int.
[04:00] So with this you should be able to clearly understand that inside your class you have overloaded methods
[04:07] with the same name, but with the different method input parameters.
[04:11] Don't consider the method input parameter name values regardless of whatever name that you use, it
[04:18] is not going to impact the method overloading and method overriding.
[04:22] I hope you are clear with this demo.
[04:24] Now let me show you the list of rules and guidelines that you need to follow whenever you are trying
[04:30] to implement the method
[04:32] overloading inside Java.
[04:33] The very first rule is very obvious whenever you are trying to implement a method overloading all the
[04:39] methods, they should have the same method name coming to the rule number two.
[04:44] The overloaded methods must differ in the number of method
[04:49] input parameters or the order or the type of their input parameters.
[04:54] What do we mean by the order of the method
[04:56] input parameters.
[04:57] Let me show you a very quick example.
[05:00] As of now you can see I have a eat() method which is accepting String and int data type values.
[05:06] If I try to define one more eat method by reversing the order like first, I can try to mention int
[05:14] quantity followed by String food.
[05:16] So this is also a method overloading because if you try to write the definition here, first you need
[05:23] to mention the eat() method name followed by int comma String.
[05:27] So you can see these two are different.
[05:30] That's why even when the order of the method input parameters is changing, we can still consider it
[05:36] as method overloading.
[05:38] I hope you are clear with the rule number two.
[05:40] Now the rule number three says whenever you are trying to perform method overloading inside Java, you
[05:45] can have different return types or different access modifiers, and you can also have different checked
[05:52] or unchecked exceptions inside the method signature.
[05:55] Still, all these methods are going to be considered as overloaded methods, but the method overloading
[06:01] only the method name and the method input parameters are going to be considered.
[06:06] I hope you are clear about the method overloading concept and how we are able to achieve the Static
[06:12] Polymorphism.
[06:13] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
