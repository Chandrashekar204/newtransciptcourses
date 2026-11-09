# 15.15 — Mutable and Immutable objects - Theory

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Since we are discussing everything about the objects inside Java inside this section, I think it would
[00:06] be a wise decision to discuss about one more important concept around objects, which is creating mutable
[00:14] and immutable objects in Java.
[00:16] So what are mutable and immutable objects ?
[00:20] In java mutable and immutable terms refer to describe the ability of an object to be modified after it has been
[00:29] created.
[00:30] Immutable objects are the objects whose state or whose data cannot be changed once they are created.
[00:37] If you need to modify an immutable object, it is not going to be possible.
[00:41] The only option is you must create a new object with the required modified state or with the required
[00:50] new data. Whereas on the other hand, we have mutable objects whose state or
[00:55] data can be changed once they are created. With mutable objects
[00:59] we should be able to add new data, modify the existing data, delete the existing data inside the objects
[01:06] without worrying about creating a new instance.
[01:09] So these are basic definition about mutable and immutable objects.
[01:14] First, let's try to understand how to create mutable objects.
[01:18] Later on, we can focus on the immutable objects. Like you can see here
[01:23] whenever you want to create a mutable object, you need to create a Pojo class.
[01:29] And inside this pojo class you can create any number of instance variables.
[01:34] But please make sure your instance variables are of type private.
[01:38] So to access that data inside your object and to update the data inside your object, we should always
[01:44] use the getter and setter methods.
[01:46] So that's a standard approach.
[01:48] And similarly, whenever you are trying to create an object of your mutable object, you should be using
[01:54] the constructor.
[01:55] And just like how you have these fields, getter and setter methods, it is also recommended to have
[02:00] a constructor inside your class that is going to accept the required number of input parameters.
[02:06] These kind of Pojo classes we have created a lot throughout this course, so whenever you are following
[02:11] this approach to create a Pojo class inside Java, you are going to end up creating the mutable objects
[02:18] because once the object of this class is created, anyone can change that data by invoking the setter
[02:25] method.
[02:26] For example, like you can see here
[02:28] first, I'm trying to create a Person object with the help of new operator and with the help of constructor.
[02:34] To the constructor,
[02:35] I'm trying to pass the name as Elmer Raymond and the occupation as Software Engineer.
[02:41] So once this object is created, I'm trying to change the occupation of this person by invoking these
[02:48] setOccupation() method.
[02:50] So to the setOccupation() method, I'm trying to send the occupation name as chef.
[02:55] That means with the help of setName() and setOccupation() methods, we should be easily able to modify
[03:01] the values of the properties present inside the Person object.
[03:06] So this makes the Person class or the Person object as mutable, because it is allowing us to change
[03:13] the data inside it once the object is created.
[03:16] You can see here I also have a representation about the mutable objects.
[03:21] Think like there is a person
[03:22] initially we created this Person with the occupation as software engineer.
[03:27] Later on, we can change the occupation to whatever we want like a chef, pilot, nurse, doctor,
[03:34] It's up to us. This way
[03:35] based upon your own business requirements, you can keep on changing the data inside your objects.
[03:42] But please note that your class should have the setter methods, along with the other guidelines that
[03:47] we have followed here.
[03:48] Now let's try to understand how to create immutable objects.
[03:52] To make the same Person class as immutable.
[03:55] We can make few changes inside the Person class.
[03:58] The very first change that you need to do is you need to remove the setter methods.
[04:03] With that, no one will be able to set new data inside your object once it is created.
[04:09] And after removing the setter methods, you should also make your properties as final.
[04:15] Like you can see here just after the private.
[04:18] I'm trying to mention the final keyword with this
[04:21] once the data is assigned to this name and occupation with the help of this constructor, during the
[04:27] object creation, no one will be able to change that data inside them.
[04:32] The only way to change the data is to create the new object with the required new data.
[04:38] So this is the approach that you need to follow to make your class as immutable.
[04:43] This time
[04:44] if you try to see the sample code that I'm trying to provide, I'm trying to create the object of the
[04:49] Person with the name as Chitra mansi and the occupation as doctor.
[04:54] With this, an immutable object of Person is going to be created and
[04:59] no one will be able to change the data present inside this object, because there is no way for others
[05:06] to change the data, either with the help of setter method or by accessing the variables directly.
[05:12] No other class or method
[05:13] they should be able to access my instance variables, because we have defined them as private.
[05:18] And on top of that, we also declared these instance variables as final.
[05:23] Apart from removing the setter method and making your instance variables as final, it is also a good
[05:29] practice to mark your class as final, because this is going to prevent any other subclass from modifying
[05:37] the behavior of your class.
[05:39] When we mention the keyword final in the class definition, no other subclass can extend your immutable
[05:46] class.
[05:46] And with that, we will be closing the loophole of inheritance as well, so that no other subclass can
[05:52] modify the behavior of my immutable class.
[05:55] So you can see this Person object right now it is an immutable object.
[06:00] No one can change her designation or name.
[06:02] I hope you are clear on how to create immutable objects in Java.
[06:06] Here you may have a question which is why should I create immutable objects?
[06:11] What is the advantage that I'm getting by making my object as immutable?
[06:15] That's a great question.
[06:17] There can be some scenarios where you don't want your object to be modified at later point of program.
[06:23] Maybe think like you have created an object inside method1(), and you are trying to send the object
[06:30] as an input for the other methods like method2(), method3(), method4().
[06:34] So regardless of how many methods your object is going to be passed, you don't want the other methods
[06:40] to change the content of your object.
[06:43] In such scenarios, we can go with the immutable objects and apart from this, we also have another
[06:49] great reason on building the immutable objects.
[06:53] The reason is due to security reasons.
[06:55] Think like inside your Java application, you are dealing with some sensitive logic or sensitive information.
[07:01] You don't want any other method or any other API inside your project to be able to modify a given object
[07:08] once that is created. If the object can be modified, then you may have some serious implications inside
[07:14] your business logic.
[07:15] So to handle these kind of scenarios, we can also use immutable objects. These immutable objects
[07:22] in other words, we can call them as data carrier classes.
[07:27] The reason why they are called as data carrier classes is, they primary purpose is to store the data
[07:33] and provide the methods to access the data. So how others can access the data inside an immutable object
[07:39] using the getter methods.
[07:41] But there is no way to change the data.
[07:43] That means this is going to act like a post card.
[07:46] Once someone returns something on the post card, it can be only be carried or sent over to other person
[07:53] and the other person
[07:54] he should be able to read the post card, and he will not be able to update any content inside the post
[08:00] card.
[08:01] Similarly, immutable objects are also going to work in the similar fashion.
[08:05] Think like your frontend layer or frontend application.
[08:08] It is trying to send some data from browser to the backend server.
[08:12] So these kind of data can be sent in the form of immutable objects.
[08:17] And the backend
[08:18] it can simply accept the data and process the same based upon the business logic written inside a Java
[08:25] program, or if needed, the same data carrier object or immutable
[08:29] object can be transferred between multiple layers of the backend system.
[08:34] Inside backend system we are going to have multiple layers like controller layer, service layer,
[08:39] persistent layer or DB layer.
[08:41] To all these layers, we can try to send the same immutable object, and since it is an immutable object,
[08:47] we can happily sleep with an assumption that no one will be able to change the data inside this object.
[08:53] Now let's try to understand the differences between mutable and immutable objects very quickly.
[08:59] The very first difference between mutable and immutable objects is mutable objects requires synchronization
[09:06] whenever they are trying to be used inside a multithreading environment.
[09:11] So what is a synchronization?
[09:13] Synchronization is a process that developer has to implement that at a time
[09:18] a single thread can access a given object.
[09:21] If you don't implement the synchronization, then different threads inside your Java program.
[09:27] They will be able to manipulate the data inside mutable objects very easily.
[09:32] And with that you will end up race conditions.
[09:35] So what is a race condition?
[09:36] Race condition is a scenario where different threads have different set of data in their own hands.
[09:44] So one thread may have the designation as doctor, whereas other thread may have the designation of
[09:49] software engineer.
[09:50] And at the same time one more thread can come into picture and it can also try to manipulate the data.
[09:56] So with all these simultaneous manipulation of the data
[09:59] inside a mutable objects, it will result into the inconsistent state of your object.
[10:05] So that's why to overcome these kind of issues inside multi-threading environment synchronization has
[10:11] to be implemented.
[10:12] Whereas with immutable objects we don't have to worry about the synchronization, race conditions.
[10:18] Regardless of how many threads I have inside my program, all of them, they will be able to access
[10:24] the data inside these immutable objects without the need of synchronization.
[10:29] Since all threads they can only read the data.
[10:32] I don't have to worry much because no thread can change the data inside a immutable object.
[10:38] So that's why we can call these immutable objects as thread safe.
[10:41] So whenever you're trying to build a logic for multi-threading environment, you can consider the immutable objects.
[10:47] We are ready to discuss about
[10:49] what is a thread,
[10:50] what is multithreading inside Java ?
[10:52] This advanced topic we are going to discuss towards the end of the course.
[10:56] The next difference is mutable objects are going to provide more flexibility and they are going to be
[11:02] more efficient.
[11:03] The reason is once the object is created, the same object can be used multiple times by changing the
[11:11] data any number of times.
[11:13] Since we are not going to create the object from scratch with the new data, they are going to be efficient
[11:18] because already the object creation might have happened long back inside your program.
[11:24] But these mutable objects require careful handling to avoid issues related to concurrent access, especially
[11:32] in the multi threading environment.
[11:34] Whereas immutable objects may require more memory and potentially they may work slowly compared to the
[11:42] mutable objects.
[11:44] The reason is, every time you want to store new data, you need to create a fresh objects.
[11:49] And as you are trying to create more and more immutable objects, you're going to occupy more memory
[11:55] and it may potentially slow the performance of your application compared to the mutable objects.
[12:02] That's why most of the times Java developers, they will end up creating only the mutable objects.
[12:08] But if they have some special requirement where they don't want the object content not to be modified
[12:14] once the object is created in such scenarios, they are going to build the immutable objects.
[12:20] So the choice between mutable and immutable is always going to depend on the specific use case and the
[12:27] performance requirements of your application.
[12:30] I hope you are clear about mutable and immutable objects.
[12:35] In the next lecture, let's see the demo on how to create a mutable and immutable object.
[12:40] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
