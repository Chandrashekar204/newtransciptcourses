# 19.8 — Subtype or Upper Bound Wildcards

> Section 19: Generics in Java

[00:00] We had a very good discussion around what is a covariance and why it is not allowed inside collections.
[00:07] Whatever we discuss in the previous lecture around covariance, along with the examples, I have highlighted
[00:12] all of them inside these three slides.
[00:15] Now, as a next step, let's try to understand about one of the flavor inside generics. Which is subtype,
[00:22] or upper bound wild cards.
[00:24] Using these flavor of generic, we should be able to achieve covariance kind of functionality inside
[00:30] collections.
[00:31] So let's try to understand how to define these subtype or
[00:35] Upper bound wild cards.
[00:36] Whenever you are trying to define a generic inside your class or inside your method, you can follow
[00:42] these syntax which is question mark extends T.
[00:46] This means your class or your method
[00:48] it is only going to accept the elements which belongs to either T class or a child of T.
[00:56] Here T is a type used as the generics of collection.
[00:59] For example, you can see here I have a method with the name printEmployeeNames().
[01:04] To this method, we are trying to pass a Upper bound wild card or subtype generic after the collection
[01:11] name like ArrayList.
[01:12] I'm trying to mention question mark extends Employee.
[01:15] With this my method
[01:17] it is going to accept the ArrayList object, which is going to store either Employee objects or the
[01:23] subtypes of Employee like manager and developer.
[01:26] And inside this method we can write the generic code with the help of the superclass, which is Employee.
[01:32] The reason why this generic syntax is called as Upper bound wild cards is, with the help of this syntax,
[01:39] your method or your class at a max or at a upper bound
[01:43] it is going to accept only the Employee object, or it can accept the child elements.
[01:48] But you can't store or use the objects which are above the Employee inheritance hierarchy, like object
[01:55] or any other superclass.
[01:57] So we are trying to restrict the boundary up to a maximum of Employee.
[02:01] That's why this kind of syntax we can call it as upper bound or subtype wild card.
[02:07] Why this is called as subtype wild card.
[02:09] It is very simple,
[02:10] with this syntax, you are going to accept the subtypes of a given type that you have defined.
[02:15] So either the subtypes are allowed or the same data type objects also allowed. The question mark that
[02:21] we have inside the syntax like question mark extends Employee.
[02:24] It indicates some unknown subtype of Employee can be used inside this method or inside a class where
[02:32] you are going to use this syntax.
[02:33] So the question mark indicates wild card type, which is unknown.
[02:37] You can call this method with an Employee or an subtype like developer or manager.
[02:44] Whenever we are using this Upper bound wild card or subtype wild card inside our Java program, there
[02:50] is a restriction that you need to be aware.
[02:52] The restriction is we can't add a new element or object inside the collection.
[02:58] For example, here we have received a Collection object which is Employee and once this employees is
[03:04] received as an input to this method, inside this method or inside this for loop, I can't add a new
[03:09] element or object inside this class.
[03:12] The object can be belongs to employees or manager or developer.
[03:16] Still, I will not be able to make any changes to my Collection object.
[03:21] If you try to do the same, we are going to get a compilation error.
[03:23] We are going to see the demo in few seconds.
[03:25] The reason why we have this restriction inside collections is think for a second that we can add a element,
[03:32] or we can add an object whenever we are using these syntax.
[03:36] If adding an element is allowed, it may result into an heap
[03:40] pollution.
[03:41] There is a concept of Heap pollution inside Java.
[03:43] What is going to happen is think like your method received an ArrayList object which is capable of
[03:48] storing the subtype of employee like Manager.
[03:52] In such scenarios, it is not going to make sense to allow to add a developer object into the ArrayList
[03:58] of manager, because they both are different subtypes and they are independent on each other,
[04:03] and there is no direct relationship between them.
[04:06] To avoid these kind of heap pollution scenarios, adding an element whenever you are using the upper
[04:12] bound wild card or subtype wild card is not allowed.
[04:16] I hope this makes sense to you.
[04:17] Let's see the demo of these Upper bound wild cards inside IntelliJ.
[04:22] Inside my project, I'm going to create a new Java class with the name UpperBoundWildCardDemo.
[04:30] Inside this class I'm going to create the main() method and after the main() method, I'm also going to
[04:36] create a method which is going to developed with the help of Upper bound Wild card.
[04:41] We already have a similar method inside CovarianceDemo.
[04:45] So let me copy these method into my UpperBoundWildCardDemo class.
[04:51] Post that I'm going to rename this method to printEmployeeNames().
[04:56] Now as a next step, I'll change this list to ArrayList.
[05:00] And inside these angle brackets I'm going to mention question mark followed by extends keyword followed
[05:07] by Employee superclass.
[05:09] With this Upper bound wild card syntax.
[05:12] Now my method is capable of accepting an ArrayList object that can store Employee objects or its subtype
[05:21] objects.
[05:21] Let me copy the code present inside the CovarianceDemo around the ArrayList object creation.
[05:27] So here what I can do is, I can try to copy this code and paste it inside this main() method.
[05:33] Instead of printArray() method, I'm going to invoke the printEmployeeNames() method.
[05:38] I'm getting a compilation here because this method is only accept the object of ArrayList, but we
[05:44] are trying to send the object of List.
[05:46] What we can do is instead of this ArrayList, we can try to mention List.
[05:50] And with that the compilation error is going to get resolved.
[05:53] So let me rename this variable name to employees.
[05:56] And the same I'm going to mention here.
[05:58] As a next step I'm going to invoke the same method this time with that developers object as well.
[06:06] Let me rename this variable name to developers, and the same I'm going to pass as an input to the print
[06:12] employee names.
[06:13] This time you can see the covariance behavior we are able to get with the help of these Upper bound
[06:20] wild card syntax.
[06:21] In the similar lines, I should be able to create the List object which is going to store manager related
[06:29] objects.
[06:30] So let me use the manager constructor to create the objects and post that
[06:36] on the left hand side I'm going to mention List of manager and the variable name I'm going to mention
[06:42] as managers, the same managers I can try to send to the printEmployeeNames.
[06:48] If I execute this program, I'll be getting the same output based upon what we have inside the toString()
[06:54] method.
[06:55] Coming to that drawback, or the limitation that we have whenever we are using the Upper bound wild
[07:01] card, is we can't add an object into this Collection object inside this method.
[07:06] For example, if I try to invoke employees.add() to this add() method, I can try to pass an object
[07:14] of Manager.
[07:15] You can see I'm getting a compilation error saying that
[07:18] similarly in staff manager, if I try to mention developer as well, I'm going to get a compilation
[07:22] error.
[07:23] The same applies for Employee object as well.
[07:26] So this confirms whenever we are using the Upper bound wild card, we can't add a new element or object
[07:33] inside the collection.
[07:34] I hope you are clear on how to use our implement Upper bound wild card inside your generics code.
[07:40] Please use this generics flavor where you want to accept the objects of a class or its subtypes
[07:46] only in such scenarios, you can happily use this flavor of generic.
[07:50] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
