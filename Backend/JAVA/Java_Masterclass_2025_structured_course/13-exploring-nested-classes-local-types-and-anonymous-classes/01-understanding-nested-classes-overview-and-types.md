# 13.1 — Understanding Nested Classes: Overview & Types

> Section 13: Exploring Nested Classes, Local Types & Anonymous Classes

Kind: captions Language: en So far in the course, I've shown you static and instance members on a class, but they've only been fields and methods. In addition to these, A class can contain other types within the class body, such as other classes, interfaces, enums, and records. These are called nested types, or nested classes. You might want to use nested classes when your classes are tightly coupled, meaning their functionality is interwoven. The four different types of nested classes you can use in Java are: the static nested class, the inner class, a local class and an anonymous class.

A class that uses the static modifier is called a static nested class. It's declared in the class body, and access to it is through the class name, not an instance variable. We also have non-static nested classes, declared in the class body, that are called inner classes. You have to access this kind of class through an instance of the outer class. A local class is an inner class, but it's not defined at the class level, but usually inside of a method block.

An anonymous class is like an inner class, but it's declared and instantiated at the same time, and has no name. This section will cover all four of these nested classes, as well as additional nested types, like the enum & record (which are just classes at their core) and the interface. Before JDK16, only static nested classes were allowed to have static methods. As of JDK16, all four types of nested classes can have static members of any type, including static methods.

In the next video, I'll start out talking about static nested classes. There's a lot to cover, so let's get started.

----------------------------------------
