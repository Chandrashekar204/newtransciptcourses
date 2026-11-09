# 10.22 — Method Overloading - Theory

> Section 10: Inheritance in Java

[00:00] As of now, we understand what is an method overriding in Java.
[00:05] As a next step, let's try to understand what is method overloading and how we can achieve static polymorphism
[00:12] with the help of method overloading.
[00:14] Inside Java, whenever we want to perform the method overloading, there is no mandatory that you need
[00:19] to implement inheritance even in a normal and independent class
[00:25] also, you can implement method overloading.
[00:27] So first I'm going to show you an example where I'm not following any inheritance post that I'll also
[00:33] show you another example on how to perform the method overloading.
[00:37] When we implemented inheritance between two classes.
[00:41] Coming to that definition of the method overloading, it is a feature in Java that allows a developer
[00:47] to define multiple methods with the same name in the same class.
[00:53] However, the methods must have different parameters list.
[00:58] Though the method names are same, but they are going to hold the different number of parameters or different
[01:04] data types of parameters, or both of them the return type and the access modifier and the Throws class
[01:10] of a method
[01:11] they are not going to play any role in making an method overloaded, and at the same time using different
[01:18] names for the method parameters does not going to make the method overloaded.
[01:23] I have an example class and this class
[01:27] it is not inheriting any superclass.
[01:29] If you closely look at the class body inside this example class, we have three different methods with
[01:36] the same name print and all of these methods
[01:39] they have different parameters as an input.
[01:42] For example, for the first print() method, I'm having the input parameter as int followed by double
[01:49] and at last
[01:50] for the last print() method, we are accepting the String data type as an input parameter.
[01:56] So this is a perfect example of method overloading.
[01:59] Though the name of the three methods is same, but they are having different method input parameters.
[02:06] So in this kind of scenario the Static Binding or compile time binding is going to happen.
[02:13] And that's why whenever we are implementing method overloading we are going to achieve Static Polymorphism.
[02:19] Here you can see I have given an example.
[02:22] First I'm trying to create the object of this Example class, followed by I'm trying to invoke all these
[02:28] three methods.
[02:29] When I'm trying to invoke these three methods, I'm passing the method input parameter value as per
[02:35] the method definition.
[02:36] If I pass the int value, the very first method is going to be invoked, whereas when I pass the double
[02:42] value, the second method is going to be invoked.
[02:45] And when I pass the String data, the last method is going to be invoked.
[02:49] So the compiler, it is going to take the decision about which method to invoke at the compile time
[02:55] itself.
[02:56] So you can see here the same print() method
[02:58] it is trying to behave differently based upon different input that we are passing at the compile time
[03:05] itself.
[03:06] That's why we can call this kind of Polymorphism as Static Polymorphism.
[03:10] So there won't be any confusion to the compiler to which method it has to call, because all your overloaded
[03:16] methods always they are going to have different method signatures.
[03:20] Now let me show you another example where we have the inheritance implemented.
[03:25] Here you can see I have a Person superclass and inside the Person superclass I have an eat() method and
[03:32] it is going to accept a String food as an input parameter.
[03:35] Now inside my subclass which is IronMan
[03:39] first I have a override method because you will be able to see that I have used the annotation at symbol
[03:44] followed by override.
[03:46] On top of that, this method signature is exactly same as the method signature that we have inside the
[03:53] Person superclass.
[03:54] Now coming to the last two methods inside the IronMan, you can see they are maintaining the same name
[04:00] like eat(), but the input parameters to these methods are different.
[04:05] For the second method, we are not accepting any method input parameter, whereas for the third method
[04:11] we are accepting String and the int as an method input parameters.
[04:16] So the last two methods that we have inside the IronMan, they are overloaded methods because they
[04:22] have different method input parameters compared to the parent method are inherited method inside the
[04:30] IronMan subclass.
[04:31] So whenever you have confusion to understand whether a method is overloaded or not, you can follow
[04:37] a simple rule.
[04:38] First, you can write down the method name followed by a separator like comma or percentage,
[04:44] whatever works for you.
[04:45] After mentioning the method name, you can also mention the data type of your method input parameters.
[04:52] So each of the data type
[04:54] also you can separate them with the help of a separator like comma.
[04:58] So once you have written all
[04:59] this method
[05:00] names and parameter data types.
[05:02] Using a separator, you can compare all of them.
[05:05] If they are having different values, then obviously it indicates method overloading.
[05:11] Otherwise it is going to indicate there is no method overloading inside your class.
[05:16] And here I also want to highlight a very important point.
[05:20] Think like inside your class you have a private non-static method or private instance method.
[05:27] This private methods
[05:28] they can always be overloaded by only a non-static method inside the same class.
[05:34] I hope you are clear about what is method overloading.
[05:37] I'm going to show you a demo of method overloading in the next lecture.
[05:41] Thank you,
[05:42] bye.

----------------------------------------
