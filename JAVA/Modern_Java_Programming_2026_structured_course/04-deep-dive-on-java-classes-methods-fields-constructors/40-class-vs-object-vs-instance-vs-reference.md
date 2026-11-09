# 4.40 — Class vs Object vs Instance vs Reference

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] As of now
[00:01] throughout the course I'm trying to use the jargons like class, object, instance, reference.
[00:08] With these jargons you may have some questions or confusion.
[00:11] What is this instance?
[00:13] What is the reference?
[00:14] What is this object?
[00:15] What is the class?
[00:16] To clear your confusion, I want to put some efforts inside this lecture.
[00:20] These jargons like class, object, instance reference, they are going to be used interchangeably by
[00:27] most of the developers.
[00:28] But do you know they have distinct meanings?
[00:31] Let's try to understand what are those meanings, so that you can be a good developer who are going
[00:36] to always use the correct jargon with the correct meaning.
[00:40] You might be very clear about what is a class and object.
[00:43] Class is a blueprint or a template to create the objects.
[00:47] With the help of a class, we can define the Java fields that are going to act as properties for the
[00:52] objects.
[00:53] And similarly, we can define the Java methods that are going to provide the behavior for your objects.
[00:59] So it is pretty clear
[01:00] and and this should not be any confusion around class.
[01:03] Very similarly, when I say object, object is an instance of a class with the help of the blueprint
[01:10] that is available inside the Java class, we can create an object with the help of new operator along
[01:16] with the constructor of the class.
[01:18] Whenever we create an object, it is going to hold the unique data inside its properties.
[01:23] Now the confusion will start with the instance and reference.
[01:27] So what is an instance?
[01:28] Instance is nothing but another name for the object.
[01:32] You can either use object or instance.
[01:36] Regardless of if you use object or instance, you are referring to the object of the class.
[01:41] Using object and instance interchangeably is always valid.
[01:45] There is no wrong in it.
[01:47] Now moving on to the last jargon which is reference.
[01:50] So what is a reference?
[01:51] Reference is a variable that holds the memory address of the object.
[01:56] With the help of this reference, we can only refer to the object and access it
[02:01] properties and methods.
[02:02] But please note a reference does not hold the object itself, because the object is going to be stored
[02:09] somewhere in the Heap memory.
[02:10] With the help of reference, we are going to point to the memory location inside the Heap memory.
[02:16] Let me give you a real example
[02:18] by taking all these four jargons so that it is going to be super clear for you.
[02:22] I'm making a promise,
[02:23] it is going to be clear when I discuss about this example.
[02:26] Let me go to the next slide.
[02:27] Let's take the analogy of house construction to better understand these four jargons. Inside the house
[02:33] construction
[02:34] first, we are going to have a blueprint at the construction plan.
[02:38] So the blueprint at the construction plan, which is going to have all the details about the structure,
[02:44] design, features of your house, this blueprint, we can consider it as a Java class when you have a
[02:51] blueprint for your house.
[02:53] With the help of this blueprint, you can construct any number of physical houses, just like how you
[02:58] are going to build a physical houses inside Java
[03:01] with the help of Java class, we can create objects are instances by using the new operator and the
[03:08] constructor of the class.
[03:09] Each object is going to have its own set of unique properties.
[03:13] Here you can see there are three physical houses.
[03:16] Each have its own color like black, blue and red.
[03:20] Very similarly your Java objects
[03:22] also they are going to hold unique data, so they are created from the same blueprint or from the same
[03:29] Java class here.
[03:30] Please note I have used object our instance to refer to a physical house or a physical object, but
[03:37] coming to the reference, reference is like a GPS coordinate that points to your particular house.
[03:43] So inside the Google Maps or Apple Maps, when I try to search for your location, it is going to give
[03:50] me latitude and longitude GPS coordinate.
[03:53] Does that mean it is providing me a physical house?
[03:55] Off course not,
[03:56] it is only going to help me to reach your physical house by following that directions.
[04:02] Very similarly, a reference in Java is a variable name using which I can always access the physical
[04:09] object which is present inside the Heap memory.
[04:11] I hope this clears your confusion.
[04:14] Especially I want you to be aware about the reference.
[04:17] Sometimes people always interchangeably use object and reference which is invalid.
[04:23] But with this discussion, I am assuming from now onwards you are going to use these jargons correctly.
[04:29] Let's also discuss a scenario by taking a Java code as an example for the same,
[04:35] let me go to the next slide.
[04:37] Inside this slide I'm going to show you the code.
[04:39] Here you can see we have a four lines of Java code. Based upon these lines of code
[04:45] the objects inside the Heap memory are created, and all these objects can be accessed with the help
[04:51] of references.
[04:52] But this is not a straightforward code.
[04:54] Let me try to explain the same.
[04:56] In the very first two lines we are trying to create an object
[04:59] Of house1 and house2, with the color value as red and black.
[05:04] With that there'll be two houses are physical objects will be created inside my Heap memory.
[05:11] The reference name you can see house1 which has red color, and house2 which has black color.
[05:16] Now moving on to the third line, which is I'm simply trying to assign the reference, which is house1,
[05:23] to the new reference with the name as houseOne, which is houseOne.
[05:28] So let's try to understand what is going to happen with this third line of code.
[05:33] When we try to assign a reference to other reference, both these two references, they're going to
[05:39] point to the same physical object inside the Heap memory.
[05:44] Your Java is not going to create two different objects just because you're trying to assign this house1
[05:50] to a new reference.
[05:51] That is never going to happen in Java.
[05:54] Java follows this strategy just to save some space inside the heap, since right now the same physical
[06:00] object is being referred by two variables.
[06:03] Any change that you make with one of the reference will impact other reference as well.
[06:08] For example, with the help of this first variable, which is house1, if you try to change the color,
[06:14] the same color will be also reflected when you try to access the color details with the help of other
[06:20] reference like houseOne.
[06:22] This is obvious because they both are pointing to the same physical object.
[06:27] I hope this is clear to you.
[06:28] Now, moving on to the last line of code where I'm simply trying to use a new operator and the constructor
[06:35] of the house class.
[06:36] And to this constructor, I'm passing the color green as an input.
[06:40] But you are not seeing this house created inside the Heap memory.
[06:44] This is because you're only creating the object, but you are not telling to the Java how to refer it.
[06:50] What is a variable name that you have to use it.
[06:53] Since those details are missing, it is going to be clear for JVM or Java that this fellow is never
[07:00] going to use this object.
[07:01] With that assumption though, Java is going to create an object inside Heap memory.
[07:06] You will not be able to access it or see it inside the Heap memory, because you have not assigned this
[07:13] object to any reference variable.
[07:15] That's why inside Heap memory I'm not able to see it because somewhere it is present and I don't know
[07:20] where it is.
[07:21] That's why I'm not showing any green house inside this Heap memory.
[07:24] With this, I'm assuming you are super clear about what is a reference instance, object and class.
[07:30] Please always be clear with all these basics.
[07:33] If you are strong at your Java basics, then all the advanced topics that we are going to discuss in
[07:37] the coming sections.
[07:38] They are going to be easy for you.
[07:40] Otherwise you're going to struggle because many times I'm going to use these jargons until unless
[07:45] what is the meaning of a particular jargon?
[07:47] You're going to scratch your head.
[07:49] And with that you may feel Java is very difficult.
[07:52] I hope you are enjoying the course.
[07:54] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
