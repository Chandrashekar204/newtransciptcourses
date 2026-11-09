# 4.29 — Introduction to static methods in Java - Theory

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Just like how we can create static fields inside Java, we can also create static methods as well in
[00:07] Java.
[00:08] Inside this lecture, let's try to understand how to create the static methods.
[00:12] What is the purpose of them when we already have non static methods?
[00:16] In Java, a static method is a method that is associated with a class, rather than with an instance
[00:23] or object of the class.
[00:25] This definition you may find it very similar to static variables.
[00:29] There is a lot of similarity between static variables and static methods.
[00:33] The way we define the way we invoke you will see a lot of similarity when we discuss about the static
[00:39] methods.
[00:40] When we declare a method as a static method, that means we can invoke that method without creating
[00:46] an object of the class we already experienced one static method.
[00:51] What is a static method?
[00:52] Yes, it is the main() which we have created previously, and we are able to run our Java programs
[00:59] with the help of this main() static method
[01:01] my JVM is not going to create any object of the class to invoke the main() method.
[01:07] So how to define a static method?
[01:09] We just have to mention the static keyword in the method declaration.
[01:14] For example, you can see here inside the ArithmeticOperations class, I have defined an method with
[01:20] the name addition().
[01:21] The only difference between a static method or non static method is the static keyword. After the public
[01:27] modifier
[01:28] you can see I have mentioned the static keyword.
[01:30] That's the only difference
[01:31] and apart from that the syntax is going to be very similar to like a normal method.
[01:36] So how to invoke this method?
[01:38] If someone wants to invoke this method which is addition(), they need to mention what is the class name
[01:45] like ArithmeticOperations.addition().
[01:47] And they need to pass the arguments like 20, 5.
[01:51] And this method is going to perform the addition() and return the result to the caller method.
[01:56] This you may find very easy because there is a lot of similarities with the static variables, but there
[02:01] might be a burning question for you, which is why do we need to define static methods when we can define
[02:07] instance methods or non static methods inside a Java class?
[02:11] That's a great question
[02:12] let's try to understand that. The purpose of static methods inside Java is to define the utility functions
[02:20] that can perform a specific operation and do not require an access to the instance variables or a
[02:27] instance methods.
[02:28] That means inside your Java project or inside your Java business logic
[02:32] if you have a requirement where you want to write a logic that is going to be used by many of the classes
[02:40] inside your project, then such logic, you can keep them as static methods.
[02:45] For example, previously we saw we created an method with the name addition().
[02:49] So addition() is a utility logic which is going to be required by many of other classes that I may have
[02:56] inside my Java project.
[02:58] So such kind of utility logic, we can define inside the static methods.
[03:03] So anyone they can simply invoke the static method without worrying about the object creation.
[03:09] They can simply mention what is a ClassName.
[03:12] what is a static method?
[03:13] And they will pass the input data and they'll get the output data.
[03:17] So this gives a flexibility for the developers to invoke the utility logic in many places without creating
[03:26] the object.
[03:26] So that's the main purpose of static methods.
[03:29] Whereas if you define this utility logic inside a normal method or instance method or non static method,
[03:37] the developer has to go through the painful process of object creation and post that using the object
[03:43] variable
[03:44] he need to invoke the method. So we have an advantage with the static methods
[03:49] in the scenario of utility logic inside programming, when someone says utility function or utility logic.
[03:55] It is an piece of code that is going to be execute a specific operation which is going to be
[04:02] required or invoked by the majority of the other classes in the project.
[04:07] But whenever we try to create a static method, we need to be aware about certain limitations of the
[04:13] static methods.
[04:14] From a static method, we cannot access the instance variables or the instance methods of a class.
[04:21] I can only access other static variables or other static methods inside the same class are in another
[04:27] class.
[04:28] I'll also show you this limitation in few minutes.
[04:31] In Java, whenever we define a static method or a non static method, all of these methods are going
[04:37] to be stored inside the same memory area
[04:40] this memory area we call it as method area or class area.
[04:44] This area is going to be allocated whenever the class is being loaded by the JVM and inside this memory
[04:50] like we discussed previously
[04:52] static variables,
[04:52] static methods, non static methods, metadata about the class class fields.
[04:57] Everything is going to be stored and
[04:59] here, you may have a question why the non-static methods or
[05:03] the instance methods are also going to be stored inside the method area or class area, but not in the
[05:09] heap memory. Because previously we discussed all the objects, they are going to be stored inside the
[05:14] heap memory.
[05:15] That's a great question
[05:16] let me try to answer that.
[05:18] Inside the heap memory, we are going to store the objects along with their instance variables along
[05:23] with the instance data, whereas the instance methods or the normal methods
[05:28] we are still going to store them inside the method area or class area along with the static methods.
[05:33] The reason is, regardless of how many objects you try to create for all of them, the logic that we
[05:39] have written inside the instance method is going to be always the same.
[05:44] There is no need of maintaining separate, separate copies of method, but different, different objects.
[05:50] Because if I try a logic of calculating the age of a person or calculating the speed of an vehicle in
[05:57] all such scenarios, regardless of how many objects I create from these classes, the logic is going
[06:03] to be same for all the objects.
[06:04] That's why inside Java always all type of methods and classes, class metadata, static variables,
[06:11] everything is going to be stored inside the method area or class area.
[06:15] Only the objects and their instance variables along with their instance variables data will be stored
[06:22] inside the heap memory.
[06:24] I hope this is clear.
[06:25] At last, I want to highlight the famous main() method that we have discussed previously.
[06:30] It is a static method.
[06:32] What is the reason that we need to define it as a static method?
[06:35] Because we want our JVM to be able to start the program and invoke the main() method, without the need
[06:42] of creating the object of the class.
[06:45] To give that flexibility
[06:47] java people
[06:48] they set an expectation that always the main() method has to be a static method.
[06:52] Very quickly, let's try to understand the differences between a static method or an instance method.
[06:58] So what is an instance method?
[07:00] All the normal methods a or non static methods.
[07:03] We are going to call them as instance method, because we can only invoke them with the help of objects
[07:09] or instances.
[07:10] So the differences are going to be very similar to the static and the instance variables.
[07:14] So here also to create a static method we need to use the static keyword.
[07:18] And with the help of static methods we cannot access the instance variables or the instance methods
[07:24] directly.
[07:24] We can only access the other static variables and other static methods.
[07:29] So what is the syntax that we need to follow
[07:30] to invoke a static method, we need to use the ClassName. followed by what is a static method?
[07:36] Coming to the instance method, whenever we are not using the static keyword inside the method declaration,
[07:42] then that method is going to be considered as a instance method or a non-static method or an normal
[07:49] method.
[07:49] The beauty of the instance method is, they can access both instance variables, instance methods, static
[07:56] variables and static methods.
[07:58] Whereas static methods have a limitation, they cannot directly access the instance methods and instance
[08:04] variables.
[08:05] Moving on to the next point, which is related to how to invoke the instance methods.
[08:09] So what is the syntax?
[08:10] To invoke the instance method,
[08:12] first we need to create an object reference.
[08:14] Using the object reference our object variable.
[08:17] We need to invoke the instance method with the help of dot operator.
[08:22] So here you can see I have an Example class
[08:25] and inside the example class I have an instance method without any static keyword.
[08:30] That's why I have to first create the object reference and using the object reference, I am trying
[08:36] to invoke the instance method. Throughout your programming career
[08:40] many times you may have a confusion when to create a static method or when to create an instance method.
[08:46] It's going to be very easy.
[08:48] First, ask yourself a question
[08:50] does your method need to access any instance variables, or whether it needs to invoke any other instance
[08:58] methods?
[08:58] If the answer to this question is yes, then please go with the instance method, because instance method
[09:05] have super power where they can invoke all types of variables and all types of methods.
[09:11] Otherwise, if you are looking for a convenience where you want to define some utility logic and you
[09:17] don't have a requirement to access the instance variables and to invoke the instance methods, then
[09:23] always you can go for the static methods
[09:25] and the static methods have some limitations, but they provide a convenience to the developers where
[09:31] we can easily invoke the static methods with the help of class name without creating the object of the
[09:37] class.
[09:37] At the end of the day, you need to ask all these questions to yourself based upon your answer
[09:42] please choose either instance method or static method.
[09:46] I hope you are clear about the quick introduction about the static methods inside Java.
[09:51] In the next lecture, let's try to explore more about the static methods by building some static methods
[09:57] inside the
[09:59] IntelliJ.
[09:59] Thank you
[10:00] and I'll catch you in the next lecture bye.

----------------------------------------
