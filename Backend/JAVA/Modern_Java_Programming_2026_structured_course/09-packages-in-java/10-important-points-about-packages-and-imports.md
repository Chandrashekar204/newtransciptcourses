# 9.10 — Important points about packages & imports

> Section 9: packages in Java

[00:00] Now let's talk about a few important points that you need to be aware while you are trying to use the
[00:06] import statements.
[00:07] The very first important point is import statements inside Java
[00:12] they don't support or allow recursive imports.
[00:15] What do I mean by recursive imports?
[00:18] Let me show you a demo here.
[00:19] For example, think like I'm trying to import the package which is java.util.
[00:26] And inside this util I'm mentioning the wild card.
[00:29] So with this I'm trying to import all the classes present inside the util package.
[00:35] So if I open this util package you'll be able to see under util
[00:40] there are so many classes, but inside the same util package there are other sub folders or other sub
[00:48] packages.
[00:48] For example, I have a reject sub folder a sub package under the util package.
[00:54] With this statement, please don't assume that you're going to get all the classes present inside these
[01:00] sub packages as well.
[01:02] That is not going to happen.
[01:03] You will be only able to access the classes present directly under this util package.
[01:10] Like for example, there is a class which is ArrayList.
[01:14] You should be able to access it without any issues, but if you try to access a class which is present
[01:19] inside regex, which is like Pattern or Matcher, you're going to get a compilation error.
[01:24] In this kind of scenarios, you need to specifically import the classes present inside the sub package
[01:31] of regex as well.
[01:33] Like just after the util you need to mention rejects.*.
[01:38] I hope you are clear about the point, which is Java does not allow recursive imports.
[01:44] On the similar lines
[01:45] java also does not support nesting package structure.
[01:49] Like I said before, this util package is completely different from the regex package, which is present
[01:57] as a sub package inside the util.
[01:59] You should not be under the assumption that regex and these util
[02:03] they both are related to each other.
[02:05] They are not going to be related.
[02:07] They will have completely different classes based upon the business requirements.
[02:12] Always note that Java does not support nesting package structure.
[02:17] Now to explain you about the next important point, let me create some classes inside the packages that
[02:24] I have created.
[02:25] Maybe inside the model package, I'm going to create a class with the name Class1.
[02:32] So this is a class name post that I'm going to create a Java class inside the service package with the
[02:38] same name, which is Class1.
[02:40] Right now you can see though we are using same name for these two different Java classes, the compiler
[02:46] is accepting it because they are present in two different packages.
[02:51] Think like I have a scenario where I want to use these two classes in one of my another class.
[02:58] For example, inside the Main class, I want to create the object of both of these Class1.
[03:04] For example, here I will try to type Class1 as soon as I type Class1,
[03:09] you can see it is showing me which Class1 I want to import.
[03:13] So first let me try to import the Class1 present inside the model package.
[03:17] So the object reference I'll give it as model post that I'll mention Class1 followed by semicolon.
[03:24] On the similar lines
[03:25] if I try to create the object of Class1 present inside another package, which is service in this
[03:32] scenario
[03:33] this time I need to mention the complete qualified name without the import statement.
[03:39] So here I'm going to mention the object reference name as service followed by new operator, followed
[03:44] by the Class1 present inside the service package.
[03:47] So this is how you need to handle in the scenarios where you're trying to access the classes with the
[03:53] same name inside a single class.
[03:56] So the class one that we have here is going to be referred with the help of these import statement that
[04:01] we have here on the top, whereas the second Class1 that we are trying to define, we cannot define
[04:07] the import statement.
[04:08] Because if you try to define the import statement for this one, and if you try to mention only class
[04:14] one here, my Java compiler will not know which Class1 you are trying to refer.
[04:19] So to differentiate that, you need to make sure for the second Class1 reference, you are providing
[04:25] a complete qualified name like you can see on the screen.
[04:28] I hope you are clear about this important point.
[04:30] So this is how you need to solve the name ambiguity that your compiler may face when you try to access
[04:37] the same class with the same name from two different packages.
[04:41] And at last, I want to highlight you that please don't try to overuse the import to static statements,
[04:48] because whenever you're trying to use this, import static statements.
[04:52] If some developer is looking at this code, he may think that this TAX_RATE is present inside the same
[04:58] class similarly.
[05:00] He may also think like this
[05:02] calculatedTotalCost() method is available inside the same class, so it may create some confusion
[05:07] until someone click on this method, they will not be able to figure out that so and so method is present
[05:14] inside another class in the static form.
[05:17] So to avoid this kind of confusion, don't try to overuse the import static statements, please use
[05:23] them only in the scenarios where you are trying to use a static variable or a static method multiple
[05:28] times.
[05:29] Otherwise, you can always refer the static methods and static variables with the help of the class
[05:34] name itself.
[05:35] All the four important points that we have discussed about the packages and import statements
[05:40] I have mentioned them inside this slide
[05:42] for your reference.
[05:43] Before I try to close this lecture, let me show you some funny meme images about the packages and import
[05:49] statements.
[05:50] So these are very first funny image I have.
[05:53] So whenever someone is saying to the Java developers like directory in a directory in a directory,
[05:59] they will immediately think about the packages because packages are nothing but directory in a directory
[06:05] in a directory.
[06:06] So we are trying to simply define the package name as com.eazybytes.model.
[06:11] Behind the scenes a directory inside a directory is going to be created based upon how many words you
[06:18] have defined inside your package name.
[06:20] Now moving on to the next image.
[06:22] So this is going to be funny.
[06:24] Like you can see someone is trying to use the import statement like java.util.Scanner, Java.util.Timer,
[06:31] java.util.ArrayList.
[06:34] If you closely observe from the same package, which is java.util, they are trying to import multiple
[06:40] classes like Scanner, Timer and ArrayList.
[06:43] So instead of this we can simply use import java.util.*.
[06:51] So using these statement is going to be like killing three birds with a single stone.
[06:56] So the same feeling that this girl is getting right now.
[06:59] Because with a single shot she is able to shot three different enemy planes.
[07:04] Now let me go to the next meme.
[07:06] So to understand this one, you may feel some difficulty if you are not from India.
[07:11] So let me try to explain you.
[07:13] Here you can see one of the Java fresher who just now landed into a project
[07:18] he's trying to use a statement which is import java.*.
[07:23] So this is like he's trying to import all the thousands of classes that we have inside the Java package.
[07:29] So in this kind of scenarios the compiler will say Bhosdike.
[07:33] So what is the meaning of Bhosdike,
[07:35] so this is a kind of bad word that we use in India.
[07:39] So Bhosdike means something like idiot.
[07:41] So the compiler may scold the fresher.
[07:43] You idiot
[07:44] why are you trying to import the entire Java package instead?
[07:49] Please mention like java.lang or java.util based upon the business requirements.
[07:54] Now let me show you the last funny meme image and this is my favorite.
[07:59] So here, instead of mentioning all these import statement like java.util.Array, ArrayList, Date, Logging,
[08:05] Math, Random, Scanner.
[08:06] So instead of all these, we can simply mention asterisk like java.util.*.
[08:13] So that is going to be super simple.
[08:16] And you're going to avoid all these import statements inside your Java program.
[08:21] I hope you like these fun images and you are enjoying this course.
[08:24] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
