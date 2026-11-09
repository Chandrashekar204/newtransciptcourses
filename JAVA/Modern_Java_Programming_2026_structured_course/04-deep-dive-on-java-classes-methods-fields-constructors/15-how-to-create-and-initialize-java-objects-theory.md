# 4.15 — How to create & initialize Java objects - Theory

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now, we learned how to create Java classes, how to define Java fields and methods inside Java
[00:06] classes.
[00:07] As a next step, we should understand how to create and initialize objects from the Java classes.
[00:14] Because Java is going to follow object oriented programming paradigm inside all the business logic that
[00:21] we want to write inside the Java, we are going to populate data inside these objects with the help
[00:26] of fields that we have defined inside the Java class.
[00:28] Using these data and objects, we are going to write lots and lot of business logic throughout the course.
[00:34] That's why, as a next step, let's try to understand how to create Java objects from the Java classes.
[00:41] Whenever we want to create an object from a Java class, we need to use " new " keyword.
[00:47] Whenever we are trying to create an object with the help of new keyword behind the scenes, the memory
[00:53] allocation for your object is going to be done by the JVM, and it is also going to return a reference
[01:00] to your memory location.
[01:02] We're going to talk about memories and where these objects are going to store inside the JVM.
[01:07] So all those advanced topics we are going to discuss in the coming lectures.
[01:11] For now, let's try to understand what is the syntax that we need to follow whenever we want to create
[01:17] an object using a Java class and a new keyword. Like you can see here, I'm trying to create an object
[01:23] with the help of Employee class that we have created previously.
[01:28] So the syntax that we want to follow is on the left hand side
[01:32] first you need to mention what is your class name.
[01:34] The class name is Employee and post that you need to give the variable name or a reference name for
[01:41] your object.
[01:42] So here I have given a name which is myObj, obj indicates object.
[01:47] Using this variable only I can access my object.
[01:51] I can store the data with the help of Java fields.
[01:53] So this variable naming convention is going to be very similar to Java variables or Java fields.
[01:59] So here also we are going to follow the CamelCase style.
[02:03] After you have mentioned the class name and the object reference name on the left hand side you need
[02:08] to mention is equal to symbol and followed by " new " keyword.
[02:13] And after the new keyword you should mention that class name again, which is Employee after the class
[02:20] name,
[02:20] you should also mention parentheses like you can see on the screen.
[02:24] So this employee with the parentheses we are going to call it as constructor.
[02:29] Using these constructor only behind the scenes, the object of the class will be created.
[02:34] We are going to talk what is a constructor in Java in the coming lectures?
[02:38] For now, please note that this convention, which we are trying to follow on the right hand side,
[02:43] where after the class name, I'm trying to mention the parentheses.
[02:46] So this indicates the constructor inside Java.
[02:50] After the constructor I need to mention the semicolon.
[02:53] So if you follow these syntax, an object of your Employee class will be created behind the scenes.
[03:00] If I try to put these in a different perspective like you can see here
[03:04] first we have an Employee Java class.
[03:07] So it's a skeleton or a blueprint or a definition about your Employee from this Java class, which is
[03:14] Employee.
[03:15] I'm trying to create an Employee with his firstName, lastName, age and gender.
[03:21] So what is the syntax that I'm following here?
[03:23] Employee employee1,
[03:24] employee1 is the variable name is equal to new Employee().
[03:29] Once I have defined the employee 1 object it is going to have all the default values inside firstName,
[03:36] lastName, age and gender.
[03:38] Since I want to populate the unique data related to this particular Employee object, I am going to
[03:45] invoke the fields available inside my class with the help of dot operator.
[03:50] So employee1.firstName = John and lastName I'm trying to say to Doe and the age I'm
[03:57] trying to set to 30 and gender I'm trying to set as M, M indicates Male.
[04:02] This way I can create any number of employees with their own unique characters or properties like firstName,
[04:10] lastName, age and gender.
[04:12] Here there is also a common pattern regardless of how many objects you are trying to create from a given
[04:19] class, you're always going to use a new operator.
[04:22] Whenever you are using new operator, you are telling to the JVM to give a fresh object or a new object,
[04:30] and on top of this object you can populate the required data, which is unique and specific to your
[04:37] given object, and how we are populating the data inside the object.
[04:41] By using that dot operator.
[04:43] Using these dot operator, we can access the objects, states, properties like instance variables and methods.
[04:50] So whatever non-static methods that you have declared inside your Java class, you can invoke them with
[04:57] the help of dot operator
[04:59] itself.
[05:00] Let's see a sample Java example on how to create an object from the Employee Java class.
[05:07] So if you try to put class, objects, methods in action, this is how it is going to look like.
[05:12] First we are going to create an Employee class.
[05:15] Inside the class, we are going to mention all the required Java fields followed by Java methods.
[05:21] This we already completed in the previous lectures.
[05:24] As a next step, using this Java class, we want to create the Java objects for the same
[05:29] I'm going to create a separate EmployeeMain class, and inside this EmployeeMain class I'm going to
[05:35] create a main() method using which my JVM can start the execution of the business logic that I have defined
[05:42] inside the main() method of the EmployeeMain class.
[05:45] So here the very first line you can see.
[05:47] First, I'm trying to create Employee object with the help of Employee class and the new operator followed
[05:54] by I'm trying to populate the firstName, lastName, age and gender details at last
[06:00] I'm also trying to invoke the methods inside Employee class, which are getAge() and getGender() with
[06:07] the help of object reference, which is employee itself.
[06:11] So when I try to invoke these, getAge() and getGender(), I'm going to get the age and gender details
[06:17] which I have stored inside my Employee object.
[06:19] I hope you are clear on a high level on how to create objects from a given Java class.
[06:25] Let's try to implement these inside IntelliJ and see the object creation in action, so that it will
[06:32] be more clear for you as well.
[06:34] But before that, I want to highlight that whatever code that I have shown here, this is not a good
[06:40] code or a great code.
[06:41] This is a bad code.
[06:43] The reason why I'm calling this as a bad code is no where
[06:46] we are using modifiers for our fields and we are not following certain standards, which I'm going to
[06:53] teach you in the coming lectures.
[06:55] But for now, since we are getting started with Java, let's focus on how to create Java objects in
[07:01] the coming sections
[07:02] when we talk about the modifiers like public, private, protected, default, then we will be more clear
[07:09] about the standards that we need to follow and how to make our code as production ready.
[07:14] I hope this is clear.
[07:16] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
