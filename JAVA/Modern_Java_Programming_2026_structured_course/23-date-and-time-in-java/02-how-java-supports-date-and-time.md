# 23.2 — How Java supports Date and Time

> Section 23: Date and Time in Java

[00:00] As of now
[00:01] throughout this course we discuss on how to store various data.
[00:05] Like with the help of String object, we can store alpha numeric values and using primitive data types
[00:12] we will be able to store numbers, characters, boolean values, and for complex requirements we can
[00:19] create our own custom classes like Person, Employee, user and with the help of the objects of these
[00:26] custom classes, we should be able to store complex data related to a Person, Employee or and User.
[00:33] But we are yet to discuss about one important data type available inside Java.
[00:39] You might have questioned yourself as well many times throughout this course, when this fellow is going
[00:44] to discuss about how to store date and time inside Java.
[00:49] Date and time are very important.
[00:52] Even for real projects, you will face lot many scenarios on your day to day job.
[00:58] For example, inside an e-commerce application, if someone is buying a product, you should make sure
[01:03] you are storing the data.
[01:04] When an order is placed, at what time and what date the order has been placed, and what is the expected
[01:11] delivery time.
[01:11] This way you will have many scenarios inside real projects as well around date and time.
[01:17] That's why inside this section, we are going to put a good amount of effort to understand how to store
[01:23] date and time related data with the help of Java objects.
[01:27] Inside Java, there are two different distinct APIs that we can use to represent date and time values.
[01:35] The very first API, it is going to rely on the classes and interfaces present inside the package java.util
[01:43] and java.sql, whereas the other API, it is going to leverage the classes and interfaces present
[01:50] inside the java.time package.
[01:53] So let's try to understand what are these two different APIs and why we have these two different APIs.
[01:59] The very first API, which uses the classes from the Java.util and java.sql, we can call this as
[02:06] a legacy date API.
[02:08] The reason why this called as Legacy Date API is this API are the classes present inside this API.
[02:14] They have some design flaws, or they have some challenges to understand on how they work.
[02:20] Since these legacy date API and classes, they are present from day one of Java.
[02:25] Obviously they have some drawbacks because the people who develop these APIs, they didn't envision
[02:31] the future problems that developers may face.
[02:33] Like you can see here
[02:34] inside this API, we have these important classes like Date Calendar, GregorianCalendar, SimpleDateFormat
[02:41] and java.sql.Date.
[02:44] We're going to discuss about all of them in detail, but let's try to understand what do we have under
[02:49] the new API or under the java.time package?
[02:54] This new date API it is introduced in Java 8.
[02:58] The reason why this new date API introduced is to overcome the design flaws and the drawbacks of the
[03:04] Legacy Date API.
[03:05] You can see all the classes and interfaces available inside the new Date API.
[03:10] They are going to be present under the java.time package.
[03:15] These are the important classes that you can find inside this package.
[03:19] The class names are local date, local date time, instant duration period, and date time formatter.
[03:26] So these are very quick introduction about how Java is going to support to store date and time values
[03:31] inside a Java program.
[03:33] We are going to explore both legacy date API and New Date API throughout this section.
[03:39] In the next lecture.
[03:40] First, let's try to understand why the new date API introduced.
[03:43] What are the problems that we have with the Legacy Date API?
[03:47] I hope you are excited about these new topic.
[03:50] It is going to be super interesting and challenging.
[03:53] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
