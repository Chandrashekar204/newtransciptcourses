# 4.5 — Declaring fields in a Java class - Theory

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now we know how to create Java classes, and in the previous lecture we also created a couple
[00:06] of classes.
[00:07] But we can't simply create classes and keep them empty forever.
[00:11] Because to get started with the Java programming language, we need to populate certain components inside
[00:17] your Java classes.
[00:18] These components like fields and methods.
[00:21] Inside this lecture, let's try to understand how to declare fields in a Java class.
[00:26] So what are these fields?
[00:27] The other names for these fields is variables,
[00:30] attributes or instance variables.
[00:33] So there are many names that usually developers refer inside the Java programming language.
[00:39] Regardless of whatever name that the developer tries to use,
[00:42] these fields represents the properties or the attributes that you want to store as data inside your
[00:49] objects that you're going to create with the help of a given class.
[00:53] For example, in the scenario of Car scenario, when you start creating objects with the help of Car
[00:59] class, you may want to hold some data related to your Car.
[01:03] For example, you want to store the data like model, color, horsepower, year of manufacturing,
[01:10] who is the manufacturer, how many kilometers driven?
[01:13] So all these kind of properties you are going to define with the help of Java fields inside a Java class.
[01:21] By the time you try to create a Java object of a Car class, the developer will try to populate all
[01:27] the data with the help of fields present inside a Java class.
[01:31] So there is a syntax that we need to follow to create our declare fields.
[01:35] Inside a Java class, we need to always make sure we are defining our fields, always inside a class
[01:41] body.
[01:41] That's why you can see
[01:42] first, you need to make sure you are defining a class.
[01:45] And inside the curly braces you can start defining the field declarations.
[01:50] So for the field declarations the syntax that you need to follow is,
[01:53] first you need to mention the modifier like public, private, default, protected.
[01:59] And these modifier is going to be completely optional for the next few lectures
[02:04] we're not going to worry about the modifier for the fields, we're going to simply define them without
[02:09] any modifier. In the coming sections,
[02:11] when we start discussing about the modifiers, then I'll teach you what are the best practices that
[02:16] we need to follow, under which scenarios we need to use which modifier.
[02:20] So all that discussion we are going to do in the coming sections. After the modifier, you need to mention
[02:26] what is the data type of your field.
[02:29] So the data type can be a primitive data type, or it can be a reference data type like String or any
[02:35] other complex data type which is represented by a Java class.
[02:39] After the data type, you need to mention the field name our variable name by following the camel case
[02:45] standards, the same standards that we have discussed in the primitive data type section,
[02:49] the same standards are going to be applicable for the Java fields that we are going to create inside
[02:54] a Java class as well.
[02:56] And after the field name, if required, you can also try to initialize your field name with an initial
[03:03] value, but this is not a mandatory,
[03:05] it is completely optional.
[03:06] Most of the times we as a developers, we will not try to initialize the values inside a Java class,
[03:13] because every object that we are going to create with the help of a Java class, it is going to have
[03:18] its own unique values.
[03:20] So that's why there is no meaning of providing an initial value.
[03:24] Anyway whatever value that developer provided during the object creation will be considered and the initial
[03:30] value will be overrided.
[03:31] That's why in the most scenarios, we're not going to initialize any value.
[03:36] But in some rare scenarios, developers will also try to initialize the field with an initial value.
[03:44] And at the end of this Java statement, you need to mention the semicolon.
[03:48] So this is the syntax that we need to follow whenever we are trying to create fields in a Java class.
[03:54] I hope you are clear with this theory discussion.
[03:57] In the next lecture, let's try to create some fields in the classes that we have created so far.
[04:03] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
