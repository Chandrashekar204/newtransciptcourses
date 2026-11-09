# 16.4 — Introduction to Wrapper Classes

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] Inside Java, we have wrapper classes which are going to help us to convert a given primitive data type
[00:07] value into an corresponding object.
[00:10] The reason why these classes are called wrapper classes is they wrap your primitive value into an object,
[00:18] just like how this cover is wrapping the chocolate.
[00:21] Very similarly, these wrapper classes, they are going to help us wrapping your primitive data type
[00:27] values into an object inside Java
[00:30] under the java.lang package, we have eight different wrapper classes representing each of the primitive
[00:39] data types that we have in Java.
[00:41] For example, for byte we have a Byte wrapper class.
[00:45] So here B is capital.
[00:47] Similarly, for short, we have a Short wrapper class with the S capital.
[00:51] For int, we have Integer for long Long for float Float, double Double, boolean Boolean, char Character
[01:00] only.
[01:00] For int and char, you'll be seeing a different class name like Integer and Character.
[01:06] For all the remaining primitive data types, the wrapper class is going to be the same, except the
[01:12] naming convention, which is the first alphabetic is going to be uppercase value.
[01:17] So why do we need these wrapper classes like we discussed in the previous lecture, the collections
[01:23] that only accept the objects to store inside them.
[01:27] That's why whenever we want to store a primitive data type value inside collections, first we need
[01:32] to wrap them and convert the primitive data type values into an wrapper object.
[01:37] For example, I can convert these into primitive data type value into an Integer object.
[01:44] So the same Integer object I can use to store inside the collections.
[01:49] Apart from collections, you can also use this wrapper classes in one more scenario, which is to pass
[01:56] a primitive data type as an argument to a method that expects an object.
[02:01] Think like you have written a method which is going to accept any object.
[02:06] So in this kind of scenarios, you can't simply send the primitive data type value.
[02:10] Instead, we need to send an wrapper object representing a given primitive data type value.
[02:16] So in these two scenarios, we can use the wrapper classes to convert the primitive data type values
[02:21] into wrapper objects.
[02:23] Apart from wrapping your primitive data type value into an object, these wrapper classes, they also
[02:29] have so many useful methods that we can use to perform operations like converting and primitive data
[02:36] type value into an string representation, or parsing a String into an given primitive data type value
[02:43] are comparing two different primitive data type values, so there are good amount of utility methods
[02:49] available inside these wrapper classes.
[02:51] We're going to explore most two commonly used methods in the coming lectures.
[02:56] But for now, let's try to understand on a high level how these wrapper classes they are going to look
[03:00] like inside IntelliJ IDE.
[03:03] Since we are into the new section, I have created a project with the name section_16, and
[03:09] at this project inside the source folder, we don't have any Java classes.
[03:14] Using these projects, I'm going to search for the one of the wrapper class, which is integer.
[03:20] Since this wrapper class is available inside the JDK library, I should be able to search for it and
[03:26] open it like you can see here.
[03:28] This integer class available inside the java.lang package.
[03:33] Very similarly, if you try to look for another wrapper class like double, it is also present inside
[03:39] the java.lang package.
[03:41] For now, let's try to open the Integer wrapper class.
[03:45] If you try to read the documentation of this class, you'll be able to see the same information that
[03:50] we have discussed, which is,
[03:52] The Integer class wraps a value of the primitive type int in an object.
[03:58] An object of type Integer contains a single field whose type is int.
[04:03] So inside this wrapper class there are so many static methods and utility methods which is going to
[04:09] help us while dealing the integer values.
[04:13] So whenever you have some requirements around the int values to convert them into a String, or to convert
[04:19] them into any other format, my humble request is always to come into this wrapper class and search
[04:26] for any method that is going to help you around your scenario.
[04:30] Otherwise you can build your own method.
[04:32] Similarly, there will be seven more other wrapper classes inside the java.lang package.
[04:37] I would request you to search for them inside the Java library and open them, and try to read their
[04:44] documentation so that it will be clear for you.
[04:46] Before I try to close this lecture, let me show you a funny meme around the wrapper classes.
[04:51] So this is a funny representation of a primitive data type value and its wrapper class or its wrapper
[04:58] object.
[04:59] If you take
[05:00] int as an example.
[05:01] So this is how a primitive data type value is going to look like.
[05:04] Whereas it's a wrapper class or it's a wrapper object, it is going to look like more polished or more
[05:10] professional.
[05:11] Why it is becoming more professional because it needs to work with collections like we discussed.
[05:16] Collections is like a professional party where only the guys who were a professional court is allowed.
[05:24] That's why you can see the same inter primitive data type value
[05:27] it is getting converted into a wrapper object with a proper dress code.
[05:32] I hope you like this comparison.
[05:34] In the next lecture, let's try to understand how to convert a primitive data type value into a wrapper
[05:40] class object.
[05:41] Thank you and I'll catch you in the next lecture, Bye.

----------------------------------------
