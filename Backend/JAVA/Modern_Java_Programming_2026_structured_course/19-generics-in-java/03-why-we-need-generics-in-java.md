# 19.3 — Why we need Generics in Java

> Section 19: Generics in Java

[00:00] You may argue with me,
[00:02] why do we need generics when we are able to write the generic code with other approaches that we have
[00:08] inside Java?
[00:09] One such approach is instead of this
[00:11] E why can't we keep the object ?
[00:14] We know there is a class with the name Object, which is going to act as a superclass for all classes
[00:21] that we are going to create inside Java.
[00:23] So this is going to be your first question.
[00:26] And the second question that you may have here is using inheritance
[00:30] we are able to write the polymorphic code.
[00:33] So with the help of same inheritance can't we write the generics.
[00:36] You may have these kind of questions and you may argue with me a lot
[00:41] why should we need generics in Java?
[00:43] I understand your concern and question.
[00:45] Let me try to show you an example inside this lecture, where I am going to build a generic code without
[00:51] the help of generic concept.
[00:53] In the same process, I'll also show you the drawbacks that we are going to have if you don't follow
[00:59] these generics in Java.
[01:01] Since we are into the section_19, I have created a Java project with the name section_19
[01:07] to make all the code changes that we are going to discuss inside this section. The same
[01:12] I'm also going to upload into the GitHub repo for your reference.
[01:15] As of now you can see this project is empty and at the source folder first I'm going to create a package.
[01:21] The package name is com.eazybytes.generics.
[01:27] Inside this package I'm going to create a new Java class with the name per the purpose of this pair
[01:34] class is,
[01:35] it is going to allow me to store two different objects.
[01:38] Apart from storing two different objects inside this pair class, I will be able to read them or I will
[01:44] be able to update them first.
[01:46] Inside this class, I'm going to create two instance fields with the access modifier as private, followed
[01:53] by object and the field name I'm going to mention as first.
[01:57] In the similar lines,
[01:58] I also want to declare one more instance variable with the name second.
[02:03] Whenever you want to copy the same line of code into the next line, you can press command D
[02:09] inside the Mac, whereas inside the window it is going to be CTRL + D.
[02:14] So here you can see the line of code is copied.
[02:17] But here instead of first I want to change this variable name to second.
[02:22] So now I have instance variables using which I can store two different kinds of objects inside this
[02:28] class.
[02:29] As a next step, I'm going to generate the constructor that is going to accept these two parameters
[02:34] as an input, followed by
[02:36] I'm also going to generate the getters and setters.
[02:39] The shortcut is command and inside Mac, whereas inside windows I believe it is CTRL + N.
[02:46] You can also confirm what is the shortcut inside your operating system by right clicking here.
[02:50] And you can see next to the generate I have a shortcut.
[02:53] So the same I'm trying to press.
[02:55] And in these options I'm going to generate the getter and setter for both these two instance fields.
[03:00] You can see now I have a getter method setter method.
[03:02] As of now I have a class which is capable of storing two different objects, and at the same time I
[03:10] will be able to read those objects.
[03:11] I'll be able to update those objects with the help of getter and setter methods.
[03:15] You may argue that this class is also providing a generic code, because it is capable of handling or
[03:22] storing any kind of object.
[03:25] You throw Integer object, String object or Person object any kind of object you throw at this class.
[03:31] It is going to accept it because the data type of these instance fields we have mentioned object which
[03:38] is a superclass for all Java classes inside Java.
[03:41] I agree with you to some extent, but there are some disadvantages.
[03:44] Let's see what are those disadvantages.
[03:46] To show you these drawbacks, I will try to use these class inside another class.
[03:51] So let me create one more class with the name NonGenericCodeDemo.
[03:58] Inside this class I'm going to create the main() method post that I'm going to create the object of Pair.
[04:06] And to this I'm going to give the name as StringIntPair, because I'm going to store two different
[04:12] objects of type String and int.
[04:15] On the right hand side,
[04:16] I'm going to mention new operator followed by Pair constructor.
[04:19] I'll just try to store hello, which is a String object followed by
[04:24] I'll also try to store a random Integer variable which is 42.
[04:28] So this 42 is also going to be converted as a wrapper object with the help of the auto boxing concept.
[04:34] Now here you can see I'm able to store any kind of object without any issues.
[04:39] In the similar way, I will be able to store a float object or char object or Person object, Employee
[04:46] object, any data type object.
[04:48] But let's see what is going to happen if we try to read these objects with the help of getter method.
[04:54] So to read the very first object, I need to invoke the getter method, which is
[05:00] getFirst().
[05:01] And similarly, I should also invoke the second method, which is getSecond().
[05:06] The very first line of code that we have written here, it is going to return a String object.
[05:11] That's why on the left hand side I'm going to type String myString.
[05:16] But this is not going to work because the return type of these getFirst() is Object.
[05:22] And I'm trying to catch it in the form of String.
[05:25] So there is a casting issue
[05:27] that's why I'm getting a compilation error.
[05:28] But here you can see we stored the String object, but we are not able to directly fetch it and use
[05:34] it.
[05:34] Whenever we want to fetch the first object, we need to typecast it with the help of casting
[05:40] like you can see here. The same kind of logic I have to write with the second object as well.
[05:47] So here, if I type int myInt is equal to, I'm going to get a compilation error because the casting
[05:54] is failing.
[05:55] To fix this compilation error I need to type Integer.
[05:58] And with that the unboxing is going to happen automatically.
[06:02] The value inside the second object is going to be available inside this variable, which is myInt.
[06:07] I can also try to print out them.
[06:09] First I'm going to print myString, followed by I'm going to print myInt variable as well.
[06:15] If I execute this program you know what is the output that we are going to get.
[06:19] First we are going to get hello followed by 42.
[06:21] So the main drawback that we have here is, whenever you try to build these kind of generic code without
[06:27] the help of generics, you need to do the casting a lot.
[06:31] And this is a very simple program and you know what you have stored.
[06:35] That's why you're able to cast it with the String or Integer.
[06:38] Sometimes when your program is super complex, or when you're trying to read the object of pair which
[06:45] is received from another program, then in such scenarios, you never know what Pair of objects are
[06:51] stored inside these Pair object.
[06:53] It may be a Person object, it can be a Employee object,
[06:56] it can be a Character object.
[06:58] So it is going to be super tough to write these kind of logic by manually casting.
[07:04] So these are very first drawback.
[07:05] I can also mention a comment here saying that requires casting.
[07:10] The same applies for the second object.
[07:13] Let me show you another drawback with these kind of approaches.
[07:17] Think like maybe once the object of this Pair class is created, someone overrided the object to present
[07:25] inside the Pair object.
[07:27] For example, I can try to invoke the setter method for the first object with the help of the setFirst().
[07:34] Here
[07:35] this time, instead of String, I'm going to pass an Integer value
[07:39] maybe I'll try to pass 16, and you can see I'm not getting any compilation error because the setter
[07:45] method which is setFirst(), it is going to accept the Object.
[07:48] And since I'm passing an Integer object, it is not throwing any compilation error.
[07:53] But now if I try to execute this program, I'm going to get a ClassCastException.
[07:59] Because here in this line of code, we're trying to cast the first object into a String format.
[08:05] That's why we are getting a ClassCastException.
[08:08] So this is another serious second drawback that we have.
[08:12] If you try to build that generic code with the help of Object, the reason why we have these two drawbacks
[08:19] that we have discussed is there is no compile time check.
[08:23] My Java compiler is not able to enforce any kind of rules during the compilation time about what kind
[08:30] of objects and user can store.
[08:33] With the help of List, you can see while you are trying to create the object of list, we will tell
[08:38] to the compiler.
[08:39] Please allow only the String objects by mentioning the String data type inside the angle brackets.
[08:45] And with that, the Java compiler is going to enforce rules during the compilation time only the String
[08:51] objects are allowed.
[08:52] This kind of flexibility are advantage we are not going to get if we try to build a generic code with
[08:58] the help of these object data type. In the similar lines,
[09:01] if you try to build a generic code with the help of inheritance concept, you're also going to face
[09:06] same kind of drawbacks.
[09:08] With all these drawbacks and limitations, it is very important in Java to create that generic code
[09:14] with the help of generics.
[09:15] I hope you are clear.
[09:17] Whatever example that we discuss inside this lecture, I have mentioned this inside this slide along
[09:21] with the drawbacks.
[09:22] In the next lecture, let's try to develop the same program with the help of generics.
[09:27] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
