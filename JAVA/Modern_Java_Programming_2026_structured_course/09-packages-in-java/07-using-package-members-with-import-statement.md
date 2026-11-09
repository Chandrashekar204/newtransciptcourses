# 9.7 — Using package members with import statement

> Section 9: packages in Java

[00:00] When we start creating many packages inside our Java application and inside all these packages, we
[00:06] are going to define lot
[00:07] many Java classes think like one of the Java class which is present inside package one.
[00:14] Want to access the other class present inside the package two.
[00:18] In this kind of scenarios, if the class one is trying to access to the class two, it is going to get
[00:24] a compilation error because accessing a class present inside another package is not going to be straightforward.
[00:32] You should first import that class two details inside your class one.
[00:37] Post that only the class one can access the class two present inside another package.
[00:43] I know it might be super confusing.
[00:45] Let me show you a demo of it very quickly.
[00:48] For the same, I'm going to create some classes inside packages that we have created so far.
[00:53] So inside my model package I'm going to create a class which is Vehicle for now
[01:00] don't worry about the content of the classes.
[01:02] So you can see here.
[01:04] This class is an empty class and it is tagged to a package which is com.easybytes.model.
[01:10] Now inside my service package
[01:13] also I'm going to create a new Java class which is VehicleService.
[01:19] So these are class and post that I'm going to create a new package which is com.eazybytes.app.
[01:28] Inside this app package only, I'm going to create the main class that is required for my application.
[01:35] So let me right click on this package and create a Java class with the name Main class.
[01:41] And inside my Main class I'm going to create the main() method. Think like from these Main class which
[01:48] is present inside the app package.
[01:50] I want to access the classes present inside the other packages like model and service.
[01:56] For example, let me try to create the object of the Vehicle class.
[02:01] So as soon as I start typing vehicle, you can see my IntelliJ is giving me the automatic recommendations
[02:09] based upon what I type.
[02:10] So as soon as I type Vehicle, it is giving me two options whether I want to use the Vehicle or VehicleService
[02:16] class.
[02:17] So if I select the vehicle and press enter, you can see there is an import statement came at the top
[02:25] which is like com.eazybytes.model.Vehicle.
[02:30] So this Vehicle class is present inside so and so package the same
[02:35] we need to import it with the help of this import keyword.
[02:39] So this is the complete qualified name of my Vehicle class.
[02:43] Once you have mentioned these import you should be able to create the Vehicle object without any issues
[02:51] because your Main class is able to access the Vehicle class present inside another package with the
[02:58] help of this import statement.
[03:00] Now I'm going to disable the intelliJ feature, which is helping me to recognize the class and importing
[03:06] the package details automatically.
[03:09] For the same, I'll go to IntelliJ Idea preferences and under the editor I'll go to code completion.
[03:15] Here I'm going to uncheck this box for now just for demo like this option which is show sessions
[03:23] as you type I'm going to uncheck it and press okay.
[03:26] This time I'm going to create the object of the other class which is Employee.
[03:30] So let me try to create the object of the Employee class by typing Employee.
[03:36] So you can see my compiler is throwing an error because it searched for this Employee class inside the
[03:42] same package where your main class is present.
[03:45] Since there is no such class, it is throwing an compilation error.
[03:49] So as a next step, we need to tell to the compiler where this Employee class is available with the
[03:55] help of this import statement.
[03:57] So instead of import statement, there is also another approach which is we can mention the complete
[04:02] name of Employee here like com.eazybytes.model.Employee.
[04:09] So these are complete name.
[04:11] After mentioning the complete name I can mention what is the object reference name followed by is equal
[04:17] to followed by new operator, and after the new operator, I need to mention the complete name of the
[04:23] class, followed by the constructor parentheses.
[04:26] So this is another approach which you can follow to access the class which is present inside another
[04:32] package without mentioning the import statement.
[04:36] But do you think this is the correct approach,
[04:38] off course not, because every time we want to access the Employee class inside this Main class, we
[04:44] need to type this entire qualified name.
[04:47] Instead, we can simply mention these qualified name with the help of import statement.
[04:53] So after the import statement, I'm going to mention the Employee and post that I can remove this complete
[05:00] qualified name
[05:00] simply I can mention what is the class name which is Employee here.
[05:05] So this is the correct way of referring other classes present inside other packages.
[05:11] I hope you are clear.
[05:12] Let me bring back the IntelliJ Idea Autocompletion feature.
[05:17] So let me go to preference and make sure under the code completion you are selecting these show suggestions
[05:23] as you type.
[05:24] So by default this is going to be checked.
[05:26] So I'm trying to bring back this into my Java project.
[05:30] So let me click on this apply okay.
[05:32] Now I'm going to create the object of another class which is VehicleService for the same
[05:39] the object reference I'm going to mention is VehicleService itself.
[05:42] So as I type you can see I'm getting the VehicleService class name details.
[05:47] The same are added at the top with the help of the import statement.
[05:52] So there are no restrictions on how many import statements you are going to add inside your Java class.
[05:58] So the more and more Java class that you are trying to refer which are present inside another packages,
[06:04] the more and more import statement you may end up writing. In real projects,
[06:08] you may see hundreds of import statements as well inside your Java classes, but please make sure always
[06:14] only one package statement is allowed inside a single source file.
[06:19] The other kind of approach that you can follow whenever you are trying to import a class from a package
[06:25] is instead of importing the class by class using this import statement separately, you can try to import
[06:33] the entire package.
[06:34] As of now you can see inside model package,
[06:37] I have two different classes, both of them I'm trying to refer inside my main class and that's why
[06:43] I have mentioned these two import statements inside my Main class.
[06:47] Think like from the same model package,
[06:50] If I'm trying to refer ten other Java classes, then I need to mention this import statement ten more
[06:56] times with the complete class name details.
[06:59] So that is going to increase the number of lines of Java code that you are going to write.
[07:04] So to reduce the number of lines that you're going to write in this kind of scenarios, instead of importing
[07:09] the Java classes individually, you can import the entire package.
[07:15] So to import the entire package just after the model you can mention the asterisk.
[07:21] So with this wildcard asterisk we are telling we want to access all the classes present inside this
[07:28] model package.
[07:29] There might be 100 different Java classes.
[07:32] I may end up accessing only ten Java classes or 20 Java classes, but still, this should be fine because
[07:39] instead of writing 10 different or 20 different import statement, having a single import statement
[07:44] with a wildcard asterisk is recommended inside real projects.
[07:49] So with this wildcard asterisk, you can see I'm still able to access the Vehicle and Employee class
[07:55] which are available inside the model package.
[07:58] I hope you're clear.
[07:59] IntelliJ is also can help you in more ways while you are trying to deal with the import statements.
[08:05] For example, think like here
[08:07] I'm trying to delete the code related to the VehicleService.
[08:10] As soon as I delete this line of code, you can see this import statement is going to be unused import
[08:17] statement.
[08:18] So to resolve this error, I need to go to this import statement and delete this manually.
[08:24] Instead we can let intelliJ to help us in these kind of scenarios.
[08:29] So let me show you how to do that.
[08:31] Before that, let me bring back the VehicleService related code
[08:34] and with that you can see the warning is resolved.
[08:36] Now I'll go to IntellIJ, Preferences,
[08:39] and inside the editor general you can search for auto import option.
[08:45] Inside this auto import option, select all the check boxes that you see here.
[08:51] So that intelliJ is going to perform all these actions like it is going to optimize imports on the
[08:56] fly.
[08:56] That means whenever I'm trying to delete the code related to a Java class, the imports related to that
[09:02] class is going to be deleted.
[09:03] And very similarly, it is also going to help me to add unambiguous imports on the fly, so you don't
[09:10] have to add the import statements manually.
[09:12] The intellIJ idea is going to take care of it.
[09:15] So please make sure you are selecting all these options and post that click on this apply okay.
[09:21] So now this time you can see as soon as I try to delete this VehicleService, the import statement
[09:27] related to the VehicleService is also going to be deleted.
[09:30] I hope this is clear.
[09:31] And Intellij is also is going to do some optimizations here.
[09:36] Previously I mentioned the wild card, but right now you can see I got two different import statement.
[09:41] The reason is Intel is felt like we have only two Java classes inside this package
[09:46] there is nothing wrong mentioning two different import statements, but if you end up having good amount
[09:52] of classes inside your package, and if you are trying to refer them individually with the separate
[09:57] import statement in such scenarios after
[10:00] a certain benchmark or after a certain amount of individual import statement, intelliJ is going
[10:06] to perform the optimization by going back to the wild card import statement with the help of asterisk
[10:12] symbol.
[10:13] So if you are using Ides like IntelliJ, you don't have to worry much about the import statement as
[10:18] and when we are trying to type your code based upon the class that you are trying to access, the import
[10:24] statements will be automatically added and the same applies whenever you are trying to delete the code.
[10:30] The import statements will be automatically deleted. For your reference
[10:34] I have mentioned all the three approaches that we have discussed so far regarding import statement inside
[10:39] the slide, so please refer them if you have any questions and similarly inside the next slide
[10:44] also, I have mentioned the screenshot on how to enable the IntelliJ Idea auto import management, so
[10:52] please refer to this screenshot if you have any questions.
[10:55] I hope you are clear about the import statement.
[10:57] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
