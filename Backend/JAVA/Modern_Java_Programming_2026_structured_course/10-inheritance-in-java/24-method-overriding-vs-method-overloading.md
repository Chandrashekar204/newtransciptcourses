# 10.24 — Method overriding vs Method overloading

> Section 10: Inheritance in Java

[00:00] Since method overriding and method overloading concepts are very important inside Java, let's try to
[00:06] put more efforts on trying to understand what is the difference between these two concepts.
[00:13] People may get confused very easily at these concepts and inside interviews.
[00:18] Also, the interviewer, he or she can try to confuse you very easily.
[00:22] So to avoid these kind of scenarios, let's try to put some efforts on understanding the differences
[00:29] between method overriding and method overloading.
[00:32] The very first difference is method overriding always happens if a class declares a method that shares
[00:39] the same name, along with the same number of method parameters and same parameter data types in the
[00:46] same order as specified by its superclass, whereas the method overloading is going to happen if multiple
[00:54] methods inside a class have a same name, and all these methods which are sharing the same method name
[01:01] if they have difference in at least one aspect, like it can be a number of method input parameters
[01:08] or their data types are in their order.
[01:11] So in such scenarios the method overloading is going to happen.
[01:15] So these are the definitions of method overriding and a method overloading.
[01:20] Moving on to the second difference.
[01:21] Whenever you want to perform the method overriding, you should always have followed the inheritance.
[01:27] That means you should always have at least two classes,
[01:30] one is superclass and the other one is subclass
[01:34] in order to implement method overriding concept. On the contrast side, you can try to implement method
[01:40] overloading in a single class without worrying about the inheritance.
[01:45] The third difference is the return type of the overridden method must be same as the superclass method,
[01:53] or it should be compatible with the return type of the superclass method.
[01:57] When I say compatible, it should be one of the subtypes of the return type mentioned inside the superclass,
[02:04] whereas inside the method overloading the return type of the method is not going to be considered,
[02:10] and it is not going to influence method overloading concept.
[02:13] On the similar lines, while you are trying to implement method overriding, you are not allowed to
[02:18] include any additional throws class compared to the overriding method.
[02:23] If needed, you can get rid of all the checked exceptions defined inside the superclass method, or
[02:30] you can maintain the same number of checked exceptions or less
[02:33] number of checked exceptions or
[02:35] if needed
[02:36] you can also maintain a different checked exception, but you need to make sure it is one of the subclass
[02:42] of the checked exception, which is defined inside the superclass method on the method overloading
[02:47] side
[02:47] the Throws class is not going to play any role, and it is not going to impact the process of overloading.
[02:54] And the last difference that we have is the method overriding is always applicable for the instance
[03:00] methods or non-static methods, whereas method overloading is applicable for any type of method, whether
[03:08] it is an static method or a non-static method, I can define multiple static methods in a same class
[03:15] with the same name, but with a different method input parameters.
[03:19] So that is perfectly possible with the method overloading.
[03:23] Whereas if you try to overload a static method present inside a superclass in the subclass, then it
[03:30] is not allowed or we cannot call that concept as method overriding.
[03:34] So there is a different concept called method hiding, which you are going to discuss in the coming
[03:39] lectures.
[03:40] And at last I want to highlight you that method overloading is always going to be resolved at compile
[03:46] time based upon the static binding or compile time binding or static polymorphism.
[03:52] And the other side method overriding is always going to be resolved at runtime based upon that dynamic
[03:58] binding or dynamic polymorphism.
[04:00] With this, I'm assuming you are clear about what is method overriding and method overloading.
[04:05] My humble request is please create some classes and inside these classes you can try to define multiple
[04:12] methods with the same name and in the same process, you can try to implement method overriding and
[04:18] method overloading so that you will get used to these concepts easily.
[04:22] Thank you,
[04:23] bye.

----------------------------------------
