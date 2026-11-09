# 4.3 — So, what is a Java class

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let me give a formal introduction about Java class.
[00:05] Many times people may ask you what is the purpose of a class inside Java?
[00:09] Why should we create a Java class?
[00:11] For all such questions, you should be prepared with an answer.
[00:14] So whatever we are going to discuss inside this lecture is going to provide some clarity on what is
[00:20] a Java class and why we should create.
[00:22] In the previous lecture we discussed Java follows object oriented programming paradigm.
[00:29] Anytime If you want to create an object inside Java, first we need a Java class.
[00:33] So what is a Java class?
[00:35] Java class is a blueprint or a template or a definition representing your objects.
[00:42] For example, if you want to create an object of a Person or a Customer, then you need to define a
[00:48] skeleton or a blueprint based upon your Customer attributes and behavior.
[00:54] Most of the times your Java classes, they are going to contain instance variables, which represents
[00:59] the state of the object and the methods which represents the behavior of the object.
[01:05] If you take the same Person or Customer scenario, a person can have a name, gender, age.
[01:11] These kind of details are properties we define with the help of instance variables inside the class,
[01:18] and the person can have various behaviors.
[01:21] For example, if I want to write a business logic to calculate the age of the person based upon his
[01:27] date of birth, then in such scenarios, I need to write a method inside the Person class or Customer
[01:32] class.
[01:33] So such kind of business logic
[01:35] we have to write inside the methods.
[01:37] So methods define the behavior of an object.
[01:40] We can define many other components inside Java class, but most of the times we will create instance
[01:46] variables and methods.
[01:48] I know you may still have some confusion about what is a Java class.
[01:52] Let me take a example and try to explain you the same.
[01:56] To make this explanation very easy, let's try to understand Java class by taking the car manufacturing
[02:02] analogy.
[02:02] Inside this analogy, we need to define a Java class, which is going to work as a blueprint or a template
[02:09] for building cars.
[02:10] All the cars, they are going to have some properties which defines them, and they are also going to
[02:15] have some behaviors.
[02:16] So such details we need to define inside the Java classes like you can see here.
[02:21] First we need to make sure we are creating a Java class by following public class Car.
[02:27] So Car is the name, class is the keyword and public is an access modifier.
[02:32] So we're going to discuss a lot about access modifier in the coming lectures.
[02:36] But for now please note that whenever we define a public just before the class keyword that represents
[02:42] any other class inside my Java project, they can invoke my class.
[02:46] They can invoke the methods inside my class.
[02:49] They can access the variables inside my class.
[02:52] So that is the purpose of public.
[02:54] So inside this example you can see I have taken some variables or attributes.
[02:59] So the variables are like model what is the model of the car.
[03:02] After the model I have a variable with the name color.
[03:05] So these model and color they are going to have that data in the form of String.
[03:10] That's why I need to make sure I'm defining these variables or attributes with the help of String data
[03:16] type.
[03:17] After these two variables I have horsePower variable.
[03:20] Since we are going to represent horsepower with the help of numbers, I have given int as a primitive
[03:26] data type for the horsepower variable.
[03:29] This way, based upon your business requirements, you can create any number of variables.
[03:34] So all these variables, they are going to have default values for model and color
[03:39] we are going to have null values.
[03:40] Whereas for the horsepower it is going to hold the default value zero.
[03:44] So as a developer, whenever you are trying to create an object based upon this public class Car, you
[03:50] need to provide these details, which is going to be unique data for your object.
[03:56] Think like from the same Car definition.
[03:58] You are trying to create three different objects of Car for all these three different objects,
[04:02] definitely you're going to provide different set of data like what is a model, what is a color, what
[04:07] is a horsepower?
[04:08] Very similarly, just like how we have defined variables or attributes, we can also define methods
[04:15] inside the class.
[04:16] So what is the purpose of methods, inside the methods only we are going to write our business logic.
[04:22] For example, for the car I may want to provide behavior like start, stop, accelerate.
[04:28] Since car is going to provide this kind of functionality, I need to define the business logic related
[04:34] to these functionalities
[04:35] inside the respect to methods, we are going to discuss in detail about Java methods in few lectures.
[04:40] So that's why I'm not going to talk in detail about the Java methods for now.
[04:44] So this is how we usually going to develop the class definition.
[04:48] So you can see here this is strictly a blueprint or template for the objects that I'm going to create
[04:55] in future.
[04:56] Without these blueprint or template Java cannot
[04:59] create any object.
[05:01] So that's why the very first basic component inside Java programming language is to create a class.
[05:07] So whatever variables you see.
[05:09] So these variables have various names.
[05:11] Some people they call it as variables.
[05:13] Some people they call it as fields.
[05:15] And few developers they call it as attributes.
[05:18] So regardless of whatever is the name, these variables help the objects to hold the data.
[05:23] So by the time I create the Car object, I can store some data with the help of these variables.
[05:29] Since these variables, we are going to build with the help of primitive data types and String data
[05:34] type.
[05:34] We put enough efforts in the previous sections to understand about them.
[05:39] Very similarly, we're also going to learn how to create classes, how to create methods throughout
[05:43] this section.
[05:44] So whatever I had discussed, I have highlighted here in order to retrain the properties or the characteristics
[05:50] of a particular Java class, we are going to create the instance variables, very similarly, in order
[05:56] to define the behavior of a class or an object, we are going to create the methods inside the Java
[06:03] class.
[06:03] Now let me show you more details about Java class.
[06:06] Inside Java classes we can create fields and methods like we discussed.
[06:11] So these fields we can also call them as variables and attributes.
[06:15] Apart from fields and methods we can write constructors,
[06:18] we can write static initializers and instance initializers.
[06:23] So if you see Java class is a basic component which is holding all your attributes, business logic
[06:30] and other supporting components.
[06:32] So throughout this section we are going to put enough efforts to understand what are fields, methods,
[06:38] constructors, static and instance initializers, these fields and methods that we defined inside the
[06:44] Java class.
[06:45] They are also known as members of the class.
[06:48] A class can have zero or more class members.
[06:51] That means it is not always mandatory to define a field or a method.
[06:56] You can write a empty class as well, or you can write a class with a single method, but without any
[07:02] fields, and vice versa is also possible.
[07:05] And in some scenarios, developers also define a class inside a class.
[07:09] That means inside a class we can write another class, and these classes that we have written inside
[07:14] the Java class, we call them as inner class or nested class.
[07:18] So these inner class and nested classes are advanced concepts.
[07:22] We are going to discuss them towards the end of the course, but for now let's focus on simply how to
[07:28] create a Java class.
[07:29] So the syntax to create a Java class is like you can see here.
[07:33] First we need to mention the modifier.
[07:35] So as of now we are mentioning the modifier as public.
[07:39] Even if you don't mention any modifier still your Java class is going to be valid.
[07:44] We are going to learn more about modifiers in the coming sections, but for now, let's continue to
[07:49] use the public as a modifier in front of the class keyword and after the modifier we have to mention
[07:56] the class.
[07:57] Class is a keyword inside Java, which we are going to use to define a class, and after the class keyword,
[08:03] we have to provide the class name that we want to define based upon our business logic.
[08:09] If I'm trying to build a business logic related to a Car, then the Car name is going to make more sense.
[08:15] And similarly, we can give any other name like Person, Customer, Loan, Card based upon our business scenario.
[08:22] Here I want to highlight about the case style that we have to follow
[08:26] whenever we are trying to define the class name, we have to follow the Pascal case style to define
[08:33] the Java class name.
[08:34] So for the fields or the variables inside Java, we need to use a camel case, whereas for the class
[08:41] name we need to use a Pascal case style.
[08:43] So inside Pascal case style all words has to start with a capital letter.
[08:48] Even your first word,
[08:50] first letter has to start with a capital letter.
[08:53] And since my class is going to hold lot of other components like fields, methods, constructors and
[09:00] initializers, we need to make sure we are putting some opening brace and curly brace.
[09:05] So whatever we want to write or whatever we want to define inside my class, we need to define all such
[09:12] components within this curly braces.
[09:14] So what are we write inside these curly braces.
[09:17] We also call it as body of the class.
[09:20] I hope now you are clear about what is a Java class. Inside the next lecture, let's try to create a
[09:25] sample Java class inside the IntelliJ IDE.
[09:28] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
