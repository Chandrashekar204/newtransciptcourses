# 9.4 — Creating a package - Part 1

> Section 9: packages in Java

[00:00] Inside this lecture, let's try creating a package and once the package is created, we can try to attach
[00:07] a given Java class to the same package like we saw in the previous lecture demo
[00:12] whenever we want to attach a given class to a package, we need to make sure we are creating a package
[00:18] inside our Java project.
[00:19] I'm going to show you how to create a package in few seconds.
[00:23] It is going to be super simple.
[00:24] Once the package is created, we can attach our Java class to the given package by using the package
[00:32] keyword.
[00:33] For example, think like I have a Java class with the name MyClass.
[00:37] If I want to attach this my class to the package com.example.myapp, I can simply mention
[00:45] package keyword followed by space, followed by my package name.
[00:50] So the package name can be a single word or multiple word.
[00:53] But always make sure you are separating each word off your package with the help of a dot.
[01:00] And also, please make sure your package name has only the small case letters.
[01:07] Once
[01:07] we define this package statement as a very first statement inside our Java class, then our Java class
[01:14] is going to be attached to the given package.
[01:17] So whenever you are using this package statement, make sure it is a very first line inside the source
[01:23] file.
[01:23] If you try to mention this package statement after the first line, you're going to get a compilation
[01:28] error.
[01:29] Apart from mentioning the package statement as a very first line, you should also make sure you are
[01:34] mentioning only one package statement inside your Java class.
[01:38] If you try to mention multiple package statement, you're going to get a compilation error regardless
[01:44] of how many classes you're trying to create within the same source file, you should only have a single
[01:50] package statement.
[01:51] Like I said before, Java allows you to define multiple classes inside a single Java source file.
[01:58] Like I can have a outer Java class, and inside this outer Java class I can have inner Java class as
[02:04] well.
[02:04] Regardless of how many Java classes you have inside your source file, you need to make sure the package
[02:10] statement is a very first statement, and there should be only one package statement in each source
[02:15] file.
[02:16] With this, you may have some clarity on how to assign a Java class to a given package.
[02:22] As a next step, let's try to create some packages inside our Java project.
[02:28] But before we try to do that, you may have some burning question, which is how can I provide a name
[02:34] to my package for the same
[02:36] let me show you some examples.
[02:38] There are multiple approaches used by the real projects, but I'm going to show you two of the most
[02:44] commonly used approaches.
[02:45] The very first approach is whenever you want to define packages inside your Java project.
[02:51] You can do that by considering your business functionality.
[02:55] Think like you have a Java project, and inside this Java project, you're going to build a business
[03:00] logic around the Employee, Vehicle, User.
[03:04] So in these kind of scenarios you can create packages focusing Employee, Vehicle and User.
[03:11] For example here you can see I have a package which is com.eazybytes.employee.
[03:17] So it is a good standard to always mention the domain name of your organization in and reverse order
[03:25] as a starting prefix of the package.
[03:27] For example, I own that domain name which is eazybytes.com.
[03:32] If I'm building some Java classes for the easybytes organization, I can first try to mention the domain
[03:38] name of the organization.
[03:39] But when you are trying to mention the domain name we should mention in and reverse form.
[03:44] So instead of easybytes.com, we need to mention com.easybytes post that you can try to mention
[03:51] Employee or Vehicle or user based upon your business logic.
[03:56] Here I'm going up to three levels like com is going to be a folder.
[04:00] And inside this folder there will be another sub folder will be created with the name eazybytes.
[04:05] And inside the eazybytes folder we are going to have another folder which is employee.
[04:09] So I'm going up to three levels.
[04:11] But if needed you can go to any levels.
[04:14] For example, after employee you can try to mention one more word or one more folder name, like maybe
[04:21] if you have a separate business logic for permanent employee and temporary employee.
[04:25] In such cases after employee you can mention dot temporary, dot permanent.
[04:30] This way you can create any number of packages inside your application based upon your business requirements.
[04:36] So inside my employee package you can see I have all employee related classes like Employee, EmployeeService
[04:43] EmployeeUtility.
[04:46] Similarly inside vehicle package I have all the classes which are related to Vehicle only followed by
[04:52] user related classes inside user package.
[04:55] So this is a very first approach.
[04:57] The second approach is based upon the
[05:00] Architectural patterns.
[05:01] Usually any Java project, when they're trying to build a business logic for a production application,
[05:08] they're not going to write all the business logic inside a single method or inside a Java class.
[05:14] Instead, they are going to build the logic in different layers.
[05:17] For example, we may have model layers, service layer, utility layer, control view layer, and presentation
[05:24] layer.
[05:25] So these are the most commonly used layers inside the Java applications.
[05:30] For example, inside the model layer we are going to create all the Java classes which are going to
[05:36] hold the data of an application.
[05:38] Here I can also give an example.
[05:40] Think like you have an UI application, and there is a back end logic written with the help of Java.
[05:46] If the UI application wants to send the data of a person from UI browser to the backend, it is going
[05:53] to send that with the help of a Java class.
[05:55] Like we can create a Java class with the name Person.
[05:58] And inside this Person we can create all the fields related to the person, like what is his firstName,
[06:04] what is his lastName, and what is his mobileNumber.
[06:07] So we are going to have simply fields, but no other Java methods.
[06:11] So these kind of classes we are going to call them as Pojo classes are entity classes.
[06:17] When I say Pojo, Pojo, plain old Java objects, we are going to discuss about Pojo classes in the
[06:24] coming lectures, but for now, please note that Pojo classes are entity classes which you are going
[06:30] to write inside the model layer.
[06:31] They are simply going to have the fields to hold the data that we get from the UI.
[06:37] And similarly, whenever the back end layer want to send the data to the UI in such scenarios
[06:43] also we are going to use these kind of Pojo classes, all these Pojo classes
[06:47] we are going to write inside the model layer.
[06:49] Similarly we also have service layer.
[06:51] Service layer is responsible for implementing the actual business logic, processing the data received
[06:58] from the model layer.
[06:59] It typically contains classes and methods that performs data validations, transformation of the data,
[07:07] and other business logic.
[07:09] In the similar lines, we also have utility layer.
[07:11] Utility layer is a layer where we are going to maintain all the common functionality that can be reused
[07:18] across the application by all the Java classes.
[07:21] It typically contains helper classes, constants, helper methods.
[07:25] So all these kind of helper classes, helper methods we are going to maintain inside a utility layer.
[07:31] And after the utility layer we have controller our view layer.
[07:35] So this layer is responsible for handling the user input that we are going to receive from the UI.
[07:41] And similarly from this layer only we are going to send the data to the UI.
[07:46] So it typically contains classes that handles and accept the HTTP request map the URLs that are invoked
[07:53] to the service methods and the render views for displaying to the end user.
[07:57] So all such logic we are going to write inside the controller view layer.
[08:02] And at last we also have presentation layer.
[08:04] Presentation layer is responsible for presenting the data to the user in a format that can be easily
[08:11] understand.
[08:12] It typically contains the HTML pages or HTML code that is going to help to display the mobile web pages
[08:19] or mobile app screens.
[08:20] So if you see here there are multiple layers where we are going to separate our business logic for easier
[08:27] maintenance or better maintainability.
[08:30] So based upon these layers also you can create the packages.
[08:34] For example here I have created three packages co.eazybytes.model.
[08:39] Inside this package I'm going to maintain all the model classes of my application.
[08:45] For example Employee, Vehicle, User.
[08:47] So these are the model classes which will simply have Java fields but not any methods which hold the
[08:55] business logic.
[08:56] Similarly for service layer we can create a service related package.
[09:01] And inside this service related package we can maintain all the classes like EmployeeService, VehicleService
[09:07] UserService.
[09:09] The same applies for the utility package as well.
[09:12] So these are the most commonly used approaches for now.
[09:15] If something is not clear, don't worry.
[09:18] For now, just focus on how to create the packages and how to assign the Java classes to the given package.
[09:25] When you start working in real projects, you will get some guidance from your senior developers or
[09:31] from your team lead on what is the approach that you need to follow while creating a package name.
[09:37] I hope you are clear with this discussion.
[09:39] In the next lecture, let's try to take this knowledge and create a package and post that we can tag
[09:44] a Java class to the newly created package.
[09:48] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
