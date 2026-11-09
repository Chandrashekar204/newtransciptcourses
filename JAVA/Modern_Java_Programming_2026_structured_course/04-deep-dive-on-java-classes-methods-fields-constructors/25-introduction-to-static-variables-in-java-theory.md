# 4.25 — Introduction to static variables in Java - Theory

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now we are trying to create the Java fields inside the class.
[00:05] Here you can see we have fields like model, color and horsePower.
[00:09] So what is the purpose of these fields?
[00:11] These fields allow us to store the unique data, which is specific to each object that we are going
[00:18] to create with the help of a given class.
[00:20] But sometimes you may want to create a field or a variable, which is going to hold the data that is
[00:27] common for all the objects that you are going to create.
[00:30] For example, for my Car vehicle, I want to create a variable to hold the how many wheels my car is
[00:38] going to have.
[00:39] Obviously the car is going to have four wheels regardless of how many objects that I try to create
[00:45] with the help of Car, I want to have each and every object to have the same data, which is four wheels.
[00:52] So how to handle these kind of data with the help of a Java field?
[00:57] Let's try to understand the same inside this lecture.
[00:59] Inside Java we can create static variables or fields.
[01:03] As of now we are trying to create normal fields
[01:06] we can also call them as instance fields or non static fields.
[01:10] Because with the fields that we have created so far, we can store the unique data which is specific
[01:16] to each and every instance or object that we are going to create.
[01:20] But with the help of static variables or static fields, we can store the data that is common for all
[01:26] the instances or the objects.
[01:28] So what is a static variable?
[01:30] In Java, a static variable is a variable that belongs to a class rather than a particular instance
[01:38] or object of the class.
[01:39] How to declare a static variable.
[01:41] We just have to use the ' static ' keyword.
[01:43] For example, if I want to create an variable with the name employer name, I should follow this syntax
[01:51] which is static String EmployerName = Google.
[01:53] equal to Google
[01:55] As of now, we have a class called Employee inside our Java project, and with the help of Employee
[02:01] class, we are trying to create the objects representing various employees.
[02:05] Like their name, like their firstName, lastName, age, gender, but for all the employees, since
[02:11] they are going to work for the same company like Google, we can create an employer name as a static
[02:18] field.
[02:18] And with that, all the Employee objects that we are going to create, they are going to have the same
[02:23] data under the employerName field.
[02:25] This is very similar to the four Wheeler example that we have discussed for the car scenario.
[02:31] So with the help of static variables, we can store the data that is common to all the objects, such
[02:37] as a constant value or a read only value.
[02:39] In case if you want to access the static variable, we don't have to create an object.
[02:45] We can simply access the static variable with the help of class name itself.
[02:50] Like what is your class name dot and what is your static field name?
[02:54] We're going to see the demo in few seconds.
[02:56] Whenever we try to create the static variables inside the Java classes, behind the scenes, all the
[03:02] static variables are going to be stored inside a memory called method area
[03:08] or class area.
[03:09] This is an area inside the JVM memory which is going to be shared by all the threads.
[03:15] So what is a thread inside a Java programming?
[03:18] For example, think like you have deployed your code into a production server and your code is going
[03:24] to be invoked by the thousands of requests coming from the thousands of end users using their own laptops.
[03:30] So each and every user, when they initiate the request to your code, the back end server is going
[03:36] to assign a thread for them.
[03:38] So Java supports multi-threading execution as well.
[03:42] We are going to discuss about threading and multi threading in the coming sections.
[03:46] Whatever data that we are going to store inside the static variables, it is going to be shared across
[03:52] all the threads.
[03:53] When we try to execute a Java program, JVM first loads the Java class into the memory and it will look
[03:59] for any static variables are present inside the class.
[04:03] If they are present, then it is going to initialize and store them inside the memory called method area
[04:08] class area and the static variables that we store inside these memories, they are going to
[04:14] be remain and available until the program terminates.
[04:18] Like I said before, since the static variables can be accessed or shared by all the objects of the
[04:25] class, we can access these static variables with the help of the class name without creating any instance
[04:32] or object of a class, the JVM behind the scenes
[04:35] it will ensure that only a single copy of the static variables exist inside the memory, and all the
[04:41] instances are the objects that we create.
[04:43] They will refer to the same single copy available inside the JVM memory.
[04:48] And here I want to provide an important note.
[04:51] All the objects that we create inside the Java, they are going to be stored inside the heap memory.
[04:55] Whereas the static variables that we are going to create will be stored inside the
[04:59] method area or class area.
[05:01] This method area or class area is very limited in nature compared to the heap memory because usually
[05:08] inside the Java programs we are going to create thousands of objects
[05:12] that's why we will get a lot of heap memory compared to the method area or class area.
[05:17] So if you try to create too many static variables inside your classes, it may cause out of memory error.
[05:24] But you don't have to worry.
[05:26] This error you will face only if you try to create thousands and thousands of static variables, which
[05:32] will never be a scenario in real projects as well.
[05:35] We are going to talk about the JVM memory, where this objects, variables are going to be stored in the
[05:40] coming lectures.
[05:41] For now, if you try to visualize all this information first like I said, all the static variables
[05:47] are going to be stored in a memory called class area or method area.
[05:51] So you can see there is only a single copy is going to be maintained by the JVM.
[05:55] If you try to create multiple objects like employee1, employee2, and employee3 all of
[06:01] them, they are going to refer to the same copy of employer name which is available inside the class
[06:06] area.
[06:07] You can see I have created three objects and all these three objects
[06:10] they are going to be stored inside the heap memory.
[06:12] And these objects, they are also going to have unique data under firstName, lastName, age and gender.
[06:17] But coming to the employerName field, they're not going to store that employerName field and its
[06:22] value inside the heap memory because it's unnecessary and it will be repeated in all the objects.
[06:28] Since it is a common data, a unique copy of this data is going to be maintained in a memory location
[06:35] of class area or method area.
[06:37] The same will be referred by the objects which are created inside the heap memory.
[06:42] I hope you are clear with this theory discussion.
[06:45] In the next lecture, let's try to create static variables inside the Employee and the Car class so
[06:51] that it is going to be clear for you.
[06:53] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
