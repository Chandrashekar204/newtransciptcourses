# 9.6 — Rules & standards to name a package

> Section 9: packages in Java

[00:00] While we are trying to give a name to a Java package, we need to follow certain standards along with
[00:07] rules and regulations.
[00:08] Inside this lecture, let's try to understand what are those.
[00:11] Like I said before, there is a very good chance that two different developers from two different organizations
[00:18] are from two different teams.
[00:19] They may end up choosing the same name for a Java class or an interface.
[00:24] So to avoid name conflicts inside a Java project, we have packages and inside two different packages
[00:31] we can have two different classes with the same name.
[00:34] That is completely acceptable by the Java compiler.
[00:37] But what if two different developers, they end up creating the same package name and the same Java
[00:43] class name?
[00:44] So how to prevent these kind of problems?
[00:46] To prevent these problems, we need to follow a convention or a standard.
[00:51] Before I try to share more details about the standard, first, let me show you a problem that we may
[00:57] face where two developers they are trying to create the same package and same class name.
[01:02] Think like there is a developer who is working at Oracle and he wants to create a Java class which is
[01:09] User.
[01:10] And very similarly there is another developer who is working in Mozilla.
[01:15] So Mozilla is an open source community where they develop a lot of libraries for Java projects.
[01:21] In real projects, we will be using lot of third party libraries or open source libraries.
[01:27] Think like you have a scenario where you want to generate a PDF from your Java code.
[01:32] For that, you don't need to build the library from scratch.
[01:36] There are certain good amount of third party libraries
[01:39] or open source libraries available.
[01:42] You're going to leverage them inside your project and using them based upon your business logic
[01:47] you can generate a PDF.
[01:49] Very similarly
[01:50] you want to generate an XML or an Excel.
[01:53] You have some third party libraries.
[01:55] If you want to send an email, you have some third party libraries.
[01:58] Since there are good amount of third party libraries, we will end up using many third party libraries
[02:04] inside our real projects.
[02:06] For example, in our scenario, the developer who is working at Oracle, he wants to use an library
[02:13] from the Mozilla.
[02:14] So someone at Mozilla might have developed these library.
[02:18] When I say library, it is a kind of Java project which is compressed in an Jar format.
[02:23] So what is Jar?
[02:24] Java archive is the complete name for the jar.
[02:28] So while developing these third party library, even the developer from Mozilla also end up creating
[02:35] a class User.
[02:37] So if Oracle developer tried to use a library from Mozilla, he will end up two user classes inside
[02:45] his Java application.
[02:47] And with that he's going to get a compilation error.
[02:50] So to resolve these issue we have Java packages.
[02:53] Think like the developer from Oracle.
[02:56] He created a package which is user.model.
[03:01] And the same package name is also considered by the Mozilla developer as well.
[03:07] Like he also considered the package which is user.model.
[03:11] And with this you are back to the same problem.
[03:14] Two different developers
[03:15] they are trying to create two different packages with the same name, and inside these two different
[03:20] packages which has the same name, we have two different classes with the same name user.
[03:24] So to avoid these kind of conflicts, we have a standard that needs to follow.
[03:29] The standard is always make sure your package name starts with the domain name by completely reversing
[03:36] it.
[03:36] For example, the domain name of Oracle Company or Oracle app is oracle.com.
[03:44] So this is the domain name for
[03:46] similarly for Mozilla there is a domain name which is mozilla.org.
[03:53] Since these two developers are working in two different organizations, they can create the package
[03:59] name with the standard which is com.oracle.user.model.
[04:05] So we need to reverse that domain name.
[04:07] So please make sure the package name completely is mentioned in the small case letters.
[04:13] So here also I can change to small case letter.
[04:15] So now by following the same strategy the developer from Mozilla company he can use the package name
[04:23] as org.mozilla.user.model.
[04:28] And with that you can see we have two different packages with the two different names.
[04:33] This way, based upon to whom you are going to build the application, choose that domain name of that
[04:39] particular company.
[04:40] If you are working in Google and if you are trying to build a product for Google, then you're going
[04:45] to start your package name as com.google and post that
[04:49] you can mention whatever you want based upon your business requirements.
[04:54] So the same rules I have mentioned here, the very first rule is you need to make sure the package name
[04:59] always
[04:59] has all lowercase letters to avoid conflict with the names of Classes or Interfaces, because while
[05:07] giving names to the Classes and Interfaces, we follow the naming convention of Pascal case.
[05:13] Whenever we are following Pascal case standard, we will make sure every word starts with a capital
[05:18] letter.
[05:19] So to avoid conflicts with the names of Classes and Interfaces, it is always recommended to write your
[05:25] package names in complete lowercase letters.
[05:28] And the second rule
[05:29] like we discussed, we need to follow the revised internet domain name to begin the package names based
[05:36] upon to which organization you are building a Java application, and sometimes two different developers
[05:42] in the same organization,
[05:44] they may create the same package name like developer one
[05:48] he might be working in the sales department, whereas the developer two he might be working in an marketing
[05:55] department.
[05:56] In this kind of scenario, the domain name for both these two developers will be same, because they
[06:00] both are working in the same company like Oracle to handle these kind of scenarios
[06:05] after the domain name like com.oracle, they can mention the department name like sales or marketing.
[06:12] And after this complete com.oracle.sales they can mention whatever package name that they want.
[06:19] But coming to the packages that are present inside the JDK library or Java library, they are always
[06:26] going to start or begin with java or jakarta or javax.
[06:32] So these are the prefix words that are reserved for the JDK library or Java library.
[06:38] So anyone who wants to create their own package, they can avoid these names.
[06:42] Otherwise it is going to create a lot of confusion to other developers whether the class that you have
[06:48] created belongs to the JDK library or the package that you have created.
[06:52] So to avoid that kind of confusion, you can avoid mentioning the package names that start with java,
[06:59] jakarta, javax.
[07:00] Based upon the rule number two that we have discussed, you may try to give that reversed domain name
[07:06] as your package name, but sometimes your domain name may contain invalid character or special characters
[07:14] that are not allowed as part of the package name in Java.
[07:18] So to handle these kind of scenarios, it is always advisable to replace the special character or invalid
[07:25] character which is not allowed with the underscore value.
[07:29] For example, think like some organization
[07:31] they have a domain name which is for-ever.example.org.
[07:37] So the developers who are working at these organization, if they try to create a package which is org.example.for_ever,
[07:43] it is not going to work because hyphen is not allowed as part of the
[07:50] package name.
[07:51] So how to resolve this?
[07:52] Instead of hyphen, the developers they can consider underscore. Very similarly
[07:57] think like
[07:58] there is one more domain name which is 123. example.com for this domain name,
[08:03] ideally, the package name should be com.example .123, but complete numbers are not allowed as
[08:10] part of the package name.
[08:12] So to resolve the compilation error, we can mention underscore just before the 123.
[08:18] So let me show you these examples inside IntelliJ as well.
[08:22] Think like I'm trying to create a Java package with the name org.example.for-ever.
[08:32] So you can see hyphen is not allowed.
[08:35] That's why I'm getting an invalid package name.
[08:37] So instead of hyphen if I mention underscore we're not going to get any error.
[08:43] Similarly, if I try to mention org.example.123, I'm going to get again a compilation error.
[08:50] So to resolve this you can mention the underscore before you try to start the 123 value.
[08:57] I hope you are clear.
[08:58] So always follow the rules and the standards that we have discussed,
[09:02] while you are trying to create the package names inside your Java projects.
[09:06] As of now, you can see we have only a single Java package.
[09:10] So let me try to create more packages this time
[09:13] the package name that I'm going to provide is com.eazybytes.service.
[09:19] Inside this package I'm going to write all service layer related Java classes.
[09:24] So as soon as I try to create this package this time you can see under the com.eazybytes,
[09:30] we have two different folders like model and service.
[09:33] Since the prefix for this model and service is same, the representation of the package is also going
[09:39] to change like you can see on the screen.
[09:41] Very similarly
[09:42] this time let me create a one more package with the same prefix com.eazybytes.
[09:47] So in this kind of scenarios, instead of you right clicking on the src folder, you can directly right
[09:52] click on the com.eazybytes.
[09:54] And if you select the new package option, the prefix com.eazybytes is going
[09:59] to be automatically populated for you.
[10:02] You can simply mention what is the next folder name like
[10:06] here I can mention utility.
[10:08] If I press enter, the same package is going to be created inside my project.
[10:13] I hope this is clear.
[10:14] Now I can create the same employee class inside another packages.
[10:18] For example, I can create the Java class inside the service package with the same name like Employee.
[10:26] But still, I'm not going to get any compilation error because they belongs to the two different packages.
[10:33] For example, this time I'm going to create the same class Employee inside the same package, and you
[10:39] can see the error that you are going to get.
[10:42] So let me press enter here and you can see I'm getting an error that I cannot create the class because
[10:48] it is already exist inside my package.
[10:51] I hope you are clear.
[10:52] What are the advantages that we are getting with the packages?
[10:55] So let me remove this Employee, which is unnecessary right now.
[10:59] So I'm not going to focus a lot about creating classes methods fields.
[11:03] Throughout this section I'm going to focus a lot about the packages.
[11:07] Since we are discussing about packages inside this section.
[11:11] I hope you are fine,
[11:12] thank you and I'll catch you in the next lecture bye.

----------------------------------------
