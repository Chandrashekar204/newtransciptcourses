# 19.2 — Introduction to Generics in Java

> Section 19: Generics in Java

[00:00] As of now, we discussed about List and few of its implementations like ArrayList and LinkedList.
[00:07] We are ready to discuss about other important collection data structures like Set and Map.
[00:12] But before we try to discuss about other type of collection data structures, inside this section,
[00:17] we are going to discuss about one important topic inside Java, which is very close to collections.
[00:23] And this topic is Generics.
[00:25] So we are going to take a break from collections.
[00:28] And inside this section we are going to completely focus on generics.
[00:32] Do you know what is this?
[00:33] This is a Swiss Army knife.
[00:36] It has so many tools that are embedded into this small knife.
[00:40] That's why this Swiss Army knife is going to be carried by many of the travelers, and even the army
[00:46] people.
[00:47] From this small knife, we are going to get a lot many functionality and at it is so simple to carry.
[00:54] If you have to replace this Swiss Army knife with the specialized tools, then obviously you will end
[01:01] up having more than 20 different knifes are tools which is going to make your life tough, whether in
[01:08] terms of using them or carrying them or storing them.
[01:12] In the similar lines inside Java, we have Generics.
[01:15] Using generics, we are going to write a a true polymorphic code.
[01:20] Let me give one more scenario to make you comfortable around generics in Java.
[01:24] Think like you have a problem with your refrigerator or television or washing machine.
[01:30] You will call to the support center and raise a complaint saying that so and so product is not working
[01:36] with so and so problem.
[01:37] The supporting staff who attended your call is going to take your complaint, and he's going to tell
[01:43] you tomorrow a person will come to your house to address the problem.
[01:48] In this scenario, you are going to anticipate a person to solve your problem.
[01:53] And this individual ah person could be of any race, gender or name.
[01:58] In a similar manner, whenever you are trying to create a business logic inside Java that can be applied
[02:04] to any data type or object, in such scenarios we can leverage generics.
[02:10] So what are generics?
[02:11] Generics in Java is a feature that allows us to create reusable classes and methods that can work with
[02:20] the different data types.
[02:21] With the generics, we are going to write a true polymorphic code that is going to work with any data
[02:28] type.
[02:29] When we started discussing about the collections and started creating the objects of ArrayList and Linkedlist,
[02:34] we used a lot of these angle brackets.
[02:37] So whatever code developed with these angle brackets inside the class or inside the methods, we call
[02:44] such code as generics in Java.
[02:46] So you can see the List interface which is present inside the collection library after the class name
[02:51] it has this angle brackets and it has a char which is capital E.
[02:55] So this E indicates the type of elements that we are going to store in this List.
[03:02] It can be a Person object.
[03:03] It can be a String object.
[03:04] It can be an Integer object, regardless of whatever data type that you are trying to store inside the
[03:10] List
[03:10] the code is going to be generic.
[03:12] For example, if you try to look for the method add()
[03:16] inside this List, you can see this method is going to accept an object of type E, and the same is
[03:23] going to be added and stored inside the List.
[03:26] Entire code inside this List interface is written by considering this E.
[03:32] So whenever you are trying to create an object of List with the help of ArrayList or LinkedList, we
[03:38] are going to mention inside the angle brackets which type of objects we want to store.
[03:43] It can be a String or it can be a Person.
[03:45] Accordingly, after the compilation, all the code that is written with the help of this element e is
[03:50] going to be replaced with the data type that you have provided while you are trying to create the object
[03:57] of an List.
[03:57] So if you have mentioned person inside the angle brackets while you are trying to create an object of
[04:02] ArrayList, in such scenarios, this E is going to be replaced with the Person data type after the compilation.
[04:09] So the same kind of generic code is being used extensively inside the collections library.
[04:15] You can see array list also has these and similarly LinkedList also using the same generics.
[04:21] If you go to the Set set also using the same generics inside the Map, you will see K, and V, because
[04:28] Map is a different kind of data structure, which is going to store the objects in the form of key and
[04:34] value.
[04:35] So the char K represents the type of keys maintained by this Map, and V indicates the type of mapped
[04:42] values.
[04:43] Just like how collections are using generics extensively.
[04:47] Sometimes inside our real projects, we may end up into the scenarios to develop the code with the help
[04:54] of generics.
[04:54] That's why understanding these generics is very important.
[04:58] We're going to focus a lot
[05:00] on generics inside this section.
[05:01] Once you learn everything about the generics, how they work, then it is going to make your job easy
[05:08] in future.
[05:08] Because lot many times the framework code like JDK libraries, they are going to write with the help
[05:14] of generics.
[05:15] If you know the concepts of generics, you will be able to understand the logic that they have written
[05:20] inside the libraries.
[05:21] For example, inside the List previously, we saw that add() method is accepting a data type of E.
[05:27] If you don't know about generics, you might be scratching your head.
[05:31] What is this class E know where I'm able to find this?
[05:34] So all such questions may rise for you.
[05:37] If you don't know about the generics.
[05:39] But don't worry, we are going to discuss everything and you will be in safe hands.
[05:42] I hope you are clear with the agenda of this section.
[05:45] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
