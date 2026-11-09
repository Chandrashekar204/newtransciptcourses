# 4.6 — Declaring fields in a Java class - Demo

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's try to create some Java fields inside the Java classes that we have created.
[00:06] As of now, you can see we have two empty classes, one with the name Car and the other one with the
[00:12] name Employee.
[00:13] First, let's try to create the fields inside the Car.java.
[00:17] Whenever you are trying to create a Java fields or variables are the instance variables for your
[00:22] Java class.
[00:23] You need to think about what kind of data that your object, which you are going to create with the
[00:30] help of this class is going to hold.
[00:32] So usually for Car scenario, what kind of data we are going to store, we are going to store some data
[00:38] like what is the model of the Car?
[00:40] What is the color of the Car?
[00:42] What is the horsepower?
[00:44] What is the manufacturing year, whether the Car is an automatic car or a manual car.
[00:49] So all such details we are going to store inside the objects of the Car class.
[00:54] That's why before you try to create fields inside a class, you need to put some efforts and you need
[01:00] to do some imagination around your business use cases and accordingly, you need to create the Java
[01:06] fields.
[01:07] The very first Java field that I want to create is model.
[01:10] Since my car is going to have some model details, I want to create a variable or a field with the name
[01:17] model, but we need to follow a syntax.
[01:19] First,
[01:19] we need to mention that what is the modifier of your Java field.
[01:24] So the modifier is going to be public.
[01:26] But like I said before, as of now we have not discussed in detail about the modifier,
[01:31] that's why we can ignore the modifiers for now since it is completely optional.
[01:36] After the modifier, we need to mention what is the data type of your field?
[01:40] Since inside the model we are going to store some text data, we need to use that data type of String.
[01:47] So let me type String.
[01:49] As you type, you can see your intelliJ is going to give some recommendations.
[01:54] After you have mentioned that data type details, you need to mention what is a field name?
[01:58] The field name that I want to use here is model.
[02:01] So for the fields we need to follow the camel case.
[02:04] Since here there is only a single word, I have mentioned everything in the lower case letters.
[02:09] After that if needed, you can try to initialize this with a initialized value like you can see here.
[02:16] I'm trying to initialize this with some model details like Crysta, but this is not a good practice
[02:23] of defining the initial values for your Java fields or instance variables, because not every Car object
[02:32] that you are going to create is going to belong to the same model.
[02:35] Off course, if you have some scenarios inside your project where you are going to always create an object
[02:42] related to a model Crysta then definitely you can initialize that value.
[02:47] But here, since we don't have such business requirements, we can delete this initial value and simply
[02:54] mention what is a field name followed by semicolon.
[02:57] So this is a way of declaring a Java fields very similarly, you can try to create any number of Java
[03:03] fields based upon your business requirements.
[03:06] So let me try to create one more field by copying this variable String model.
[03:11] Now I'm going to paste the same inside the next line.
[03:14] You can see we can't have multiple fields with the same name.
[03:18] Every field inside your Java class has to be unique.
[03:22] So that's why we are seeing here a compilation error.
[03:25] The second variable are the field that I want to store inside my Car class is color.
[03:30] So since every Car object is going to have some color, I'm going to store that data with the help of
[03:36] this Java field.
[03:37] And here also I cannot initialize with some color like red or yellow or orange or white, black because
[03:44] every Car is going to have its own color.
[03:47] That's why I don't want to go with an initialized value.
[03:50] When we are trying to create objects for this Car class, we are going to populate all this data.
[03:55] I'm going to show you that in the coming lectures.
[03:57] But for now, let's create one more variable here.
[04:01] This time I want to store the horsepower data.
[04:04] Usually we are going to represent the horsepower with the help of numbers.
[04:08] So that's why here I'm going to mention the data type as int and post that I'll define the field name
[04:15] as horsePower.
[04:16] And since hourse and Power are two different words, I'm going to make the P as capital letter by following
[04:23] the camel case standards.
[04:24] This way we can create any number of fields inside a Java class.
[04:29] And all these fields are going to help us to store the data related to the object that we are going
[04:34] to create
[04:35] with the help of this Car class as a standard, we should always put our Java fields at the top of the
[04:42] body of the class after the fields only
[04:44] we should define the methods.
[04:45] So these are standard that every developer follows.
[04:48] I would recommend you also to follow the same standard.
[04:52] Now I want you to pause the video and try to create some variables inside the Employee class as well.
[04:59] I will give a clue here.
[05:00] The data that we want to store with the help of this Java fields is what is the firstName, lastName,
[05:06] age, gender of the employee.
[05:09] So please pause the video and try to declare these fields inside the Employee class.
[05:14] I hope you're successful at declaring the fields.
[05:17] If not, don't worry, you can follow my instructions here and post that you can try again.
[05:23] The very first field that I want to create here is firstName.
[05:26] With the help of this firstName field, I want to store the first name of an given employee.
[05:32] With the help of this Employee class, we are going to create thousands of Employee objects based upon
[05:37] how many Employees are there inside an organization.
[05:40] So for each employee, we are going to store what is his first name, last name, age and gender.
[05:45] So first name how you are going to store with the help of text data or with the help of words.
[05:50] So that's why here also we need to use String.
[05:53] And after that data type you need to mention the variable name or field name as firstName, followed
[05:59] by semicolon.
[06:00] The next variable is going to be String lastName.
[06:04] I hope you are seeing that I'm following the Camel case style, and the next field that I want to create
[06:09] here is related to the age.
[06:11] I want to store the age of an employee who is working.
[06:14] I know at max, the age of a person is going to be 100 or 120.
[06:20] That's why bite should be fine for me here
[06:23] instead of int, I can go with the byte and mention the field name as age, after age
[06:29] I also want to store the gender details of an employee.
[06:33] So whenever we store the gender details we can go with various options.
[06:37] I can store like male or female, or I can simply store M or F, M indicates male, F indicates female.
[06:45] Inside real project you will see many times developers will go for the short values like M and F so
[06:52] that they can save some space inside the database, because at the end of the day, all the details
[06:57] of the employees, they are going to be saved inside the database.
[07:00] So if I try to store the gender details as male or female, then it is going to take lot of space inside
[07:09] my database.
[07:10] Instead, I can simply go with the convention like M, M represents male and F indicates female.
[07:17] So whenever we want to store a single char, what is our data type that we need to follow?
[07:21] It is the char itself.
[07:23] After char I'm going to mention the field name as gender.
[07:27] So here you can see we have created four fields inside the Employee, but in real projects you may have
[07:34] more than 2030 fields as well based upon your business requirements.
[07:39] Since we are trying to learn Java, let's keep it simple so that we can focus more on learning Java
[07:45] programming language.
[07:46] Even if I try to create 100 fields, the process is going to be always same.
[07:51] I hope you are clear with the process on how to create the fields inside Java class, and what is the
[07:57] purpose that we need to create fields inside a Java class?
[08:01] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
