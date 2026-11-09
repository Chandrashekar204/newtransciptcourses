# 9.2 — Introduction to the structuring of code in Java projects

> Section 9: packages in Java

[00:00] Welcome to the new section.
[00:02] Inside this section we are going to talk about a new topic inside Java which is packages.
[00:09] Before I try to deep dive into what are packages in Java, first let me show you a couple of videos
[00:15] to provide you some background on why we should use packages in Java.
[00:20] Like you can see here, someone is doing hydroponics farming as part of this farming, you can see they
[00:27] have planted a same set of plant in a single row.
[00:32] That means they are trying to organize different plants into different rows.
[00:37] This will allow them to maintain these plants easily, because every plant may have different food requirements,
[00:45] or different nutrition requirements or water requirements.
[00:49] To handle these kind of scenarios, they have planted a same plant in a same row like you can see here.
[00:56] Very similarly
[00:57] let me show you some other examples where people try to organize the products or items to make their
[01:04] life easy.
[01:04] So this is one of the fruit selling shop.
[01:07] Inside this shop, all the fruits are segregated or organized in different, different baskets.
[01:13] So this will give some convenience to the buying customers to look for the fruits and pick one of them
[01:19] based upon their requirements.
[01:21] Very similarly, you can see here in this shop also the fruits are arranged in different, different baskets.
[01:27] And finally, this kind of organization you might be seeing inside your home also where we'll try to
[01:33] store all the fruits and vegetables inside a fridge with the help of these plastic baskets or plastic
[01:40] covers.
[01:40] So why are we doing all this?
[01:42] We are doing all this to make our life easy.
[01:46] If you don't store the products or the goods in different, different baskets, then it is going to
[01:52] make our life tough.
[01:53] Whenever we want to access these products or use them on our day to day basis.
[01:58] Now let's try to take the same analogy into our Java projects.
[02:02] As of now, you can see we are trying to create all our Java classes in a single folder called src.
[02:10] So what is c, s r c indicates source, but this approach may work to some extent when you are trying
[02:18] to learn Java very first time, or when you're trying to build some small applications with the help
[02:23] of Java.
[02:24] But in real projects we will have thousands of Java classes.
[02:28] If you try to create all those thousands of Java classes under src folder, then it is going to make
[02:34] your life tough because all these thousands of classes, they are not properly organized.
[02:39] So the maintainability of the code is going to be tough as you are trying to create more and more number
[02:45] of classes.
[02:45] So to resolve this problem, we need to learn how to structure our Java classes or other data types
[02:52] inside Java projects.
[02:54] Whenever we are looking for an option to structure our Java code, we have various options inside Java
[03:01] ecosystem like you can see here
[03:03] first, we need to create a module.
[03:05] Inside a module we can create any number of packages.
[03:09] And inside the packages we can create any number of user defined data types like Java Classes, Java Interfaces,
[03:18] Enums, Annotations.
[03:20] So as of now we know about what are Java classes.
[03:23] We are ready to discuss about Interfaces, Enums, Annotations.
[03:27] But now don't worry about them.
[03:28] We're going to talk in detail about Interfaces, Enums, and Annotations in the coming sections.
[03:34] First, let's try to focus on how to structure our code with the help of the options that we have.
[03:41] The very first obvious question you may have here is why should I structure my code?
[03:45] Why should I maintain my classes in different packages or in different modules?
[03:51] There are two reasons for it.
[03:52] The very first reason is if you try to logically group your classes based upon your business logic,
[03:58] then it is going to make your life easy
[04:01] in future
[04:02] whenever you want to maintain your code or whenever you want to make some changes to your Java class.
[04:07] More details about this I'm going to share in coming lectures.
[04:10] The second benefit that we have when we structure our Java code is sometimes inside real Java projects
[04:16] you may end up using some third party libraries or the libraries that are developed by other organizations
[04:23] or other team members or other developers.
[04:26] So in these kind of scenarios, think like you have created a Java class with a name like Document or
[04:33] Person, or User.
[04:35] Very similarly, if the other Java developer or other team member or other organization, if they develop
[04:41] a class with a name like Person or a Document or User, then you're going to get a conflict because
[04:48] there are two Java classes with the same name.
[04:50] So to avoid these kind of issues, we are going to use packages and modules.
[04:55] I hope you are clear with the benefits.
[04:57] If something is not clear, don't worry, I'm going to
[05:00] talk in detail about these benefits in the coming lectures.
[05:03] For now, let's try to understand what are these module and package modules were introduced with the
[05:09] JDK 9 or Java version nine.
[05:12] Prior to the JDK 9 or Java 9, only packages and types existed within the packages.
[05:19] When I say types, I'm referring to the classes, interfaces, Enums, and Annotations, whereas packages
[05:26] are present inside Java from day one.
[05:29] With this, it should be pretty clear for you.
[05:31] Module serve as an optional means of organizing code complementing the existing packages.
[05:38] That means you can build a Java projects without using module, whereas building the Java classes with
[05:45] the package is a mandatory.
[05:47] Without that, you cannot build a real time production applications.
[05:51] So the projects they may have one or more modules.
[05:54] You should not be under the assumption that we can only have one module.
[05:58] It's not going to work that way.
[05:59] You can create any number of modules, and inside each module you can have zero or more packages.
[06:07] Within a package, you can define one or more types.
[06:11] When I say type, I'm referring to the user defined data types like Classes, Interfaces, Enums, and
[06:18] Annotations.
[06:19] Since packages are present from the day one of Java understanding packages is mandatory and every
[06:26] real project they will group their classes interfaces into various packages for various benefits.
[06:33] That's why we are going to focus on packages alone inside this section.
[06:37] Since using the modules are optional inside Java, we are going to learn about modules towards the end
[06:44] of the course
[06:45] once we are clear about all the mandatory basic skills of Java.
[06:49] Why modules are optional because modules are introduced as part of JDK 9.
[06:54] When Java team introduced these modules in JDK 9, they didn't mandate them as a mandatory to use
[07:01] inside the Java projects, because if they make modules as mandatory, when someone trying to upgrade
[07:06] from Java 8 to Java 9 or to any of the latest versions, they need to regroup or organize all
[07:13] their thousands of classes into multiple modules, which is a heavy task for any real time projects.
[07:19] Since they don't want to enforce these kind of rules, they made modules as optional.
[07:25] That's why even today, many projects, they are still building the Java classes by grouping them with
[07:32] the help of only packages, but not the modules.
[07:35] But as a Java developer, you should also learn about module because modules also provide certain advantages.
[07:42] We're going to discuss more details about module in the coming sections with this discussion I am
[07:48] assuming you are clear what is the agenda of this section?
[07:51] Why we should learn about packages in Java.
[07:54] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
