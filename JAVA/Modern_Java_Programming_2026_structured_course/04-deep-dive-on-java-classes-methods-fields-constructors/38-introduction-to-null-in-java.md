# 4.38 — Introduction to null in Java

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Null has a very important significance inside Java,
[00:04] let's try to understand the same inside this lecture.
[00:07] So what is a null, in Java
[00:09] null is a reserved keyword that denotes a variable or a attribute, but does not reference to any object,
[00:17] which means you only declared a variable by providing a reference data type, but you have not created
[00:23] an object or you have not assigned any object to that variable.
[00:27] In such scenarios, we can say that variable or attribute is going to hold the null value.
[00:33] So null indicates an absence of an instance or an object associated with a given variable or field.
[00:41] This might be very confusing.
[00:42] Let me give you an example.
[00:44] Here you can see I'm trying to create two variables or attributes or Java fields by using the reference
[00:51] data types.
[00:52] So what are the reference data types I'm trying to use here String and Employee.
[00:56] How I'm saying these are reference data types because String and Employee they both are Java classes.
[01:03] Whenever I try to assign these reference data types to a given variable or attribute or Java field,
[01:10] then there is a chance that variable is going to hold the null value.
[01:14] So when the null value is going to be hold by the variable, if you don't initialize the object or
[01:19] if you don't assign the object to the given variable.
[01:22] Here you can see the very first one,
[01:24] I'm simply declaring my String variable, and I'm trying to assign a value called null, which means
[01:30] my String is going to hold the null value which I have assigned specifically.
[01:35] The same can happen even with the second line of statement, where I'm trying to declare only the variable
[01:41] name but not initializing.
[01:42] I just mentioned what is the data type and what is the variable name which is Employee object.
[01:47] In this scenario, also, the Employee object is going to hold the null value.
[01:52] Usually inside the Java developers, they are going to declare the variables at the starting of the
[01:57] method later on inside the method, by using the same variables, they're going to create an object,
[02:04] or they're going to assign an object to these variables.
[02:07] As we try to create more and more examples inside this course, then it is going to make more sense
[02:12] to you.
[02:13] One important point that we need to aware in terms of null keyword is whenever a null value is assigned
[02:20] to a variable or a attribute, there is a good chance that NullPointerException may happen at runtime
[02:27] if you try to access the fields with the help of that object reference.
[02:31] So here you can see I have an object reference with the name Employee object.
[02:35] I know using the e\Employee object I can access the instance fields like firstName, lastName, age
[02:41] and gender.
[02:41] So if I try to do that with this Employee object which is going to hold the null value, since null
[02:46] indicates absence of an instance or object, I'm going to get an error or RuntimeException which is
[02:54] NullPointerException.
[02:55] To avoid this, always developers, they are going to do a null check before they try to access
[03:00] the fields or before they try to invoke the methods with the help of object references, we are going
[03:06] to talk more about what is an exception, how to avoid that, and what are NullPointerExceptions in
[03:11] the coming sections.
[03:12] For now, I just wanted to give this quick information.
[03:15] So whatever we are talking right now regarding null keywords, this is only applicable for the reference
[03:21] data types, but not for the primitive data types.
[03:24] In the case of primitive data types like int, boolean, float, double.
[03:28] When we try to create a variable with these primitive data types, they are going to hold a default
[03:34] value like zero false 0.0.
[03:37] That's why there is no concept of null for primitive data type variables.
[03:41] If you try to forcely assign a null value to the primitive data type variables like here, you're going
[03:48] to get an compilation error.
[03:50] Let me show you a quick demo about these null keywords.
[03:53] Here inside my IDE, I'm going to create a new class.
[03:57] The class name is going to be NullDemo inside this class,
[04:01] first I'm going to create a main() method.
[04:04] First, let me try to assign a null value to the primitive data type variable.
[04:09] So here I'm going to mention int and I'm going to mention the variable name as number.
[04:14] We can mention semicolon and leave this statement.
[04:17] And now my number is going to hold the default value which is zero. Because this is a variable belongs
[04:23] to the primitive data type.
[04:24] If needed I can try to assign some value like 34 and it is going to be completely fine.
[04:30] But if I try to assign the null value to this variable, you can see I'm going to get an compilation
[04:36] error saying that I'm trying to provide a null value, which is not accepted for the primitive data
[04:41] types.
[04:42] So this is not allowed always.
[04:44] So let me delete this code.
[04:46] Now as a next step let me try to create a variable of data type String.
[04:52] So String is a reference data type.
[04:54] I can mention the variable name as myString.
[04:57] If I leave this myString like this
[04:59] the myString
[05:00] variable is going to hold the value as null, because the default value for all the reference
[05:06] data type variables is null itself. But leaving the myString variable like this is not recommended.
[05:12] We should at least mention is equal to null.
[05:15] This will tell to the JVM that right now I'm trying to reserve a variable with the name myString of
[05:22] data type String.
[05:23] That's why I'm trying to assign a null value.
[05:26] So if you declare this code, your JVM is going to reserve a variable myString for your future use.
[05:33] So very similarly, I can also create Employee object with the variable name as Employee object itself
[05:40] to this one
[05:40] also, I'm going to assign the null keyword if I try to execute this program by keeping a breakpoint,
[05:47] you will be able to see the variables.
[05:49] The very first variable is myString, which is holding a null value.
[05:53] Let me execute this line also by using the step over and you can see right now I have two variables
[06:01] myString and the Employee object with the value as null.
[06:04] So null indicates there is nothing present.
[06:07] I can quickly show you a demo of NullPointerException
[06:09] also for the same, let me release this program execution.
[06:13] We know with the help of Employee object we can invoke many methods like
[06:18] if I try to mention the dot operator post that I can invoke the age field.
[06:22] So let me invoke this.
[06:24] After invoking these, I can assign the output to an another variable with the name age of type int
[06:32] primitive data type.
[06:33] So you may think like this is going to give zero value, because the default value inside the age is
[06:39] going to be zero, because we have used the byte as the primitive data type here.
[06:44] But that is not how it is going to work, since the Employee object is going to hold the null value
[06:50] with the help of null,
[06:51] if you try to access anything, you're going to get a NullPointerException.
[06:55] So let me show you that in the demo.
[06:57] Before that, let me remove this breakpoint and I'm going to execute this program using run option.
[07:03] And you can see I'm getting a NullPointerException
[07:05] .
[07:06] cannot read field age because Employee object is null.
[07:10] The same applies for the method invocations
[07:12] also, if I try to invoke the method getAge(), which is going to give me the age details of the Employee
[07:19] object, I'm also going to get the NullPointerException the same confirmed here.
[07:23] That's why always developers, they have to be very careful when they're dealing with the objects.
[07:28] They should not blindly invoke the methods, and they should not blindly try to access the instance
[07:34] fields.
[07:34] They should always make sure that a given object is not null.
[07:38] Then only they need to perform all these operations like invoking the method.
[07:43] We are going to discuss about how to avoid the NullPointerExceptions in the coming sections.
[07:47] For now, please note about this information.
[07:50] With this, I'm assuming you have some good introduction about the null keyword from now onwards.
[07:55] Whenever I say null, please always recollect whatever we have discussed inside this lecture.
[08:00] If you have any questions, you can also refer to the slide that we have discussed.
[08:05] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
