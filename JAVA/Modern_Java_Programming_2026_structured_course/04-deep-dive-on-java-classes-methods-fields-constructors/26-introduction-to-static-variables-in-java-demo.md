# 4.26 — Introduction to static variables in Java - Demo

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture,
[00:01] let's see the demo of static variables that we have discussed in the previous lecture.
[00:06] As of now you can see I have three fields inside my Car class and all of them are instance variables
[00:13] are non static fields.
[00:15] How can I say that these are non static variables or instance variables because I don't see static
[00:20] keyword anywhere.
[00:21] Which means every object that we are going to create with the help of this Car class, they're going
[00:26] to have their own copy of data.
[00:29] Now after these three fields I want to create a new field which is of type static.
[00:35] For the same I need to mention static keyword.
[00:37] So static is a keyword inside Java.
[00:40] After the static we need to mention what is that data type of the variable that we want to create.
[00:46] I'll mention byte after the byte, we need to mention what is our variable name?
[00:51] The variable name,
[00:52] I'll keep it as numberOfWheels.
[00:55] So do you think the numberOfWheels are going to change for different, different objects?
[00:59] Off course not, because every Car object they are going to hold the same number of wheels.
[01:05] So what are the number of wheels that a car can hold?
[01:08] It can hold exactly four wheels.
[01:11] There is no car with three wheels or two wheels or six wheels throughout the world
[01:15] everyone is using four wheels car.
[01:17] So this is a very good field to consider as a static variable, since the data is not going to be changed
[01:24] for each object.
[01:25] Very similarly, I'll go to the Employee class, and here inside the Employee class, as of now we have
[01:32] firstName, lastName age, gender as instant fields.
[01:36] Just after these four fields, I'm going to create a static variable of type String and the name of
[01:42] the variable
[01:43] I'll give it as EmployerName.
[01:46] And the value that I want to store here is Google.
[01:50] After the Google I'll just do semicolon.
[01:52] This means all the objects that I'm going to create with the help of Employee class
[01:57] they're going to hold different, different firstName, lastName, age, gender.
[02:01] But all of them, they're going to have the same employerName which is Google.
[02:05] So this is a very common scenario, right?
[02:07] If you go and work inside a organization, all the employees inside that organization, they're going
[02:13] to have the same employerName.
[02:15] That's why this is going to be a good field to consider as a static field.
[02:19] So we need to follow this kind of strategy whenever we want to define static variables.
[02:24] Now let me go to the CarMain class inside the CarMain class
[02:28] as of now we are trying to create two objects of Car with the name car1 and car2.
[02:34] So what is the approach that we need to follow to access a static variable?
[02:38] We need to use the class name itself.
[02:40] So let me type System.out.println() post that I will give you the class name which is Car.
[02:47] After the Car I'll type that
[02:49] you can see I have only one field, which I can invoke with the name of class name and the field is,
[02:55] numberOfWheels.
[02:56] Here you can also see there is a f icon.
[02:59] F indicates field.
[03:00] So let me select this.
[03:02] So this is the syntax that we need to follow to access the static variable or static field.
[03:07] If I try to access it with the help of object name I'm going to get an error.
[03:13] Let me try to do the same here.
[03:14] So I'll copy this into the next line and I'll remove this Car.numberOfWheels.
[03:19] Now I'll do one of the object variable name that we have created like car1 or car2.
[03:26] Let me take car2.
[03:27] After the car2 I'm going to press dot and it is going to show me all the fields that I can invoke.
[03:33] I can invoke color, model horsePower, but there is no option for me to invoke numberOfWheels.
[03:41] So this confirms anytime you want to invoke a static variables.
[03:46] Always we need to use the class name, but not the object name.
[03:50] The reason is static variable is a variable that is common or specific to the Java class, but not for
[03:57] the Java objects.
[03:58] I hope you are clear.
[03:59] Let me delete this now as a next step, I'll go to the EmployeeMain.
[04:04] Inside the EmployeeMain, I will try to invoke the static field just after this System.out.println()
[04:09] statements.
[04:10] I'm going to introduce one more System.out.println() statement and here I will mention the class
[04:16] name which is Employee and I'll press dot
[04:19] using the dot operator.
[04:21] We can see all the fields that I can invoke
[04:23] there is only one field with the name employerName.
[04:26] Now let me execute this EmployeeMain program using this run button
[04:31] and you can see at the end I have my employerName getting displayed, which is Google anytime inside
[04:39] your business logic.
[04:41] If you want to understand what is the employer name of this particular object or a particular employee,
[04:47] you can always use this syntax which is Employee.employerName.
[04:52] So employee here is a Java class.
[04:54] Let me try to execute the CarMain also.
[04:57] But this time I'll try to execute in a
[04:59] debug mode.
[05:00] I keep a breakpoint here and remove other breakpoints that I have inside Car.
[05:05] I don't have any breakpoints inside Car.
[05:07] I can go to CarMain and try to run the program in a debug mode.
[05:11] You can see the breakpoint stopped at the line number6.
[05:14] Here I have two objects created with the name car1 and car2.
[05:19] If I try to open these car1 and car2, you'll be able to see there is no field inside these objects
[05:26] with the name numberOfWheels.
[05:28] Because numberOfWheels is a static variable.
[05:31] I hope with this it is very clear for you that static variables are meant for the class level, but
[05:36] not for the object level.
[05:38] Let me release this breakpoint and in the output we should be able to see the numberOfWheels, which
[05:44] is four.
[05:44] Now as a next step, I want to show you a problem with the approach that we have taken.
[05:49] So as of now I have created a static variable which is of type byte, and I have assigned a value 4.
[05:57] What if one of the developer will change this numberOfWheels to 6.
[06:01] I can change this.
[06:02] To change this, let me go to the CarMain and I'll try to execute the command which is Car.numberOfwheels.
[06:08] Number of wheels is equal to six.
[06:12] With this statement
[06:13] now all the Java objects they are going to get the latest value which is six.
[06:18] After making this assignment, if I try to print the same value, I'm going to get the six initially
[06:24] first I'll get the four later on
[06:26] after the change, I'm going to get the value as 6.
[06:29] So let me execute the program in a run mode by using this run button.
[06:34] You can see first I have four and later on there is six.
[06:37] So there is a good chance that static variables someone can change and if they change, the same updated
[06:43] value will be used by your entire application or all the objects.
[06:48] So that's why we need to be very cautious with the static variables.
[06:52] If you have a scenario where you don't want someone to change these values that you have initially initialized
[06:59] like four, then you need to tell to the JVM, saying that don't allow anyone to change the value that
[07:05] I stored inside the static field.
[07:07] So let's try to understand how to communicate that to the JVM in the next lecture.
[07:12] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
