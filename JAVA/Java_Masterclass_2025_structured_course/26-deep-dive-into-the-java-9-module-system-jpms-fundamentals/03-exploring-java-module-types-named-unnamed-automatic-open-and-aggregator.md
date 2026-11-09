# 26.3 — Exploring Java Module Types: Named, Unnamed, Automatic, Open, and Aggregator

> Section 26: Deep Dive into the Java 9 Module System: JPMS Fundamentals

All right. Let's talk about the various module types in project jigsaw. So project jigsaw defines two types of modules namely named modules and unnamed modules. So let's see a breakdown of each type. So you can see that we've got named modules and unnamed modules. Now named modules can be automatic or normal modules. And still further we can break down normal modules which can be basic modules or open modules. So let's discuss some named modules in more detail.

So firstly, for named modules each named module has a name. Now named modules can be normal or automatic. Now name modules are modules declared in the module- info.java file which is the module descriptor file. So that's actually a requirement for named modules. And all platform modules are named modules. Now normal modules don't officially exist in the in JDK 9. We just use the term normal for a named module that isn't an automatic module. And again, a normal module has a module descriptor file.

In other words, the module-info.java file while an automatic module doesn't have a module descriptor file. And a normal module is declared using the keyword module. A normal module doesn't export any of its packages by default. And finally, a normal module is divided into basic and open modules. All right. So contrast that to automatic modules. So an automatic module is created after adding a jar file to the module path. Now unlike a named module, an automatic module is not explicitly declared by the developer inside the module descriptor.

Rather it's automatically created when a jar file is placed into the module path. Now it requires by default all platform modules, all our own modules and all other automatic modules. And by default, it exports all its packages. Now these are useful for third-party code, and we'll be talking more about that later, and they're also used for migrating existing applications to java 9. And you'll see that in practice in the next section in this course.

Now basic modules don't officially exist in JDK 9 either. We just use the term basic for a module that is not an open module. Now in other words these are modules that are not automatic and not open. So it's got the same characteristics as a normal module except that it's not an open module. So let's talk about open modules now many third-party libraries like spring and hibernate use reflection to access the internals of JDK of the JDK at runtime.

Now these libraries won't work unless we have an open module. Now an open module is defined using the open keyword. Now an open module makes all packages inside the module accessible for deep reflection. Now the keyword open can be used to declare an open module or to declare specific packages as open. Now you will get to see this in action later in the course with a java fx application. We're going to see how to open some packages for the fxml loader and the application class.

All right. So unnamed modules which we talked about earlier in this video. Well, they don't have a name and also, we don't declare them. Now they export all their packages, and it actually reads all modules in the JDK and on the module path. Now an unnamed module is a module made up of jar files from the class path, and all these jar files form the unnamed module. And what we will do later is discuss the difference between the module path and class path.

And importantly a named module can't require an unnamed module. All right. So let's talk now about aggregator modules. Now these exist for convenience. Now usually they have no code of their own, they just have a module descriptor. And they collect and export the contents of other modules. This is the reason why they're named as an aggregator. Now it's an example here when a few modules depend on, let's say, three modules. What we can do is create an aggregator module for those three modules.

And that way our modules can depend on only a single module which would be that newly created aggregator model. And if you want to see an example of that in the JDK 9, there's several aggregator modules. Take a look in java.se that module for starters. All right. So module path and class path JDK 9 introduced a module path. Now a module path can represent a path to a sequence of folders that contain modules. It can represent a path to a modular java file, it can represent a path to a jmod file which if you're unfamiliar is an extended version of a jar file.

And we will discuss jmod files later in the course. Now a module path is used by the compiler here to find and resolve modules. Every module from a module path needs to have a module declaration and again is the module-info.java file. So contrasting that the module path to a class path, the class path, of course, just represents a sequence of java files. All right. So let's finish this video here, and we'll continue our discussion in the next video.


########################################
