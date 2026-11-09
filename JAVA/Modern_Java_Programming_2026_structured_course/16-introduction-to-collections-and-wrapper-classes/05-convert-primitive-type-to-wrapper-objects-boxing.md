# 16.5 — Convert Primitive Type to Wrapper Objects (Boxing)

> Section 16: Introduction to Collections & Wrapper Classes

[00:00] Inside this lecture, I'm going to show you a demo on how to convert a primitive data type value into
[00:07] its corresponding wrapper class object.
[00:10] The process of converting a primitive data type value into its corresponding wrapper class object
[00:16] we call it as boxing.
[00:18] That's why I'm going to create a Java class with the name BoxingDemo.
[00:22] Before that, let me create a package with the name com.eazybytes.wrapper.
[00:29] So inside this package I'm going to create a Java class with the name BoxingDemo.
[00:36] As usual, first we need to create the main() method inside this class.
[00:41] Now inside this main() method, we can try to explore what are the various options that we have to convert
[00:47] a primitive data type value into its corresponding wrapper class object.
[00:51] So to show you the demo, I'm going to consider the inter primitive data type value.
[00:56] For the same, I'm going to create a inter primitive data type variable with the name num.
[01:02] And inside this I'm going to store the value 16.
[01:05] So this is a primitive data type value.
[01:07] Now in order to convert these primitive data type value into an wrapper class object, there are multiple
[01:13] approaches.
[01:14] The approach one is, with the help of constructor.
[01:19] So just like how we are going to create the object of a normal class, very similarly we need to create
[01:25] the object of Integer wrapper class.
[01:27] And here I'm going to mention the object reference name as Integer, followed by
[01:33] I need to mention new, followed by constructor of Integer.
[01:37] To this constructor of Integer, we need to pass what is our primitive data type value.
[01:43] We can either directly mention 16, or we can try to mention the int data type variable name which is
[01:50] num.
[01:50] So these are approach one.
[01:52] But this approach is not recommended because using the constructor of wrapper class for the boxing process
[02:00] is not recommended.
[02:01] And it is deprecated from Java 9.
[02:04] So if you try to open this constructor, you will be able to see an annotation saying that that the
[02:10] usage of this constructor is deprecated from Java 9, and this is going to be removed in the coming
[02:16] versions of Java.
[02:18] That's why even IntelliJ it is also highlighting, as with the warning saying that Integer is deprecated
[02:24] and marked for removal.
[02:25] But I just wanted to show you a demo.
[02:27] That's why I'm not going to delete these line of code.
[02:30] Similarly, you can try to create any other wrapper class object.
[02:35] For example, I can try to create the Double wrapper class object with the same approach by using the
[02:43] new operator along with the constructor to the constructor of the Double wrapper class, we need to
[02:49] definitely pass the double value.
[02:52] So here I'm going to directly mention the literal value.
[02:55] I'll try to mention 3.14 as an input, but I'm getting a compilation error because double is a reserved
[03:03] keyword inside Java.
[03:04] That's why instead of double keyword, maybe I can try to mention doubleObj which indicates Double
[03:12] object.
[03:12] So these are approach one which is not recommended.
[03:15] So anytime if you're seeing someone using this tell them that this is not a recommended approach.
[03:20] So whenever you are using this approach you can also pass your primitive data type values in a String
[03:26] format.
[03:27] For example, this time I'll try to create the object of Long with the same constructor approach.
[03:34] So here I'm trying to invoke the long constructor, and to this constructor of long we can either pass
[03:41] a long value either by mentioning the literal value directly, or we can also pass the String format
[03:48] of a Long.
[03:48] For example, here I'm going to mention some long value.
[03:52] So if you see here the value that I'm trying to mention here, it is going to be converted into a Long
[03:57] object.
[03:58] If you try to run this program by keeping a breakpoint, you'll be able to see all these objects which
[04:04] are going to be created.
[04:06] So let me move my execution point to the next line.
[04:10] So now you'll be able to see all three objects like under Integer we have 16.
[04:15] Under Double object we have 3.14.
[04:18] And similarly under the Long object we have 95657 value.
[04:23] So this confirms we can either pass that direct literal value of an primitive data type, or we can
[04:29] pass the variable
[04:30] or we can also pass the String representation of a primitive data type value here instead of number.
[04:37] If you try to pass some invalid value, like maybe I'll try to mention some Character as well.
[04:43] This time I should get a NumberFormatException as soon as I execute this program
[04:49] You can see I'm getting a runtime exception which is NumberFormatException.
[04:53] That's why whenever you are trying to pass the input data to the constructor of the wrapper classes
[04:58] in the form of String.
[04:59] Please make sure you are passing a valid numerical values or valid expected values.
[05:05] Otherwise, obviously you're going to get a runtime exception which you need to handle inside your code.
[05:11] Now let me show you the second approach, which is the recommended approach that you need to use whenever
[05:17] you are trying to perform the boxing process, which is converting a primitive data type value into
[05:23] a wrapper class object.
[05:25] So let me copy the same lines of code, and I'm going to mention the comment as approach two with the
[05:31] help of valueOf() method.
[05:34] So each of the wrapper classes, they have a static method with the name valueOf().
[05:39] To this method you can pass your primitive data type value, and it is going to convert that primitive
[05:45] data type value into an wrapper class object.
[05:48] So let me show you how to do that.
[05:50] For the same I'm going to update the variable names to integerObj1, doubleObj1, and longObj1.
[05:56] .
[05:56] So this time instead of constructor approach, I'm going to first mention the wrapper class of Integer,
[06:02] followed by
[06:03] I'm going to mention the valueOf().
[06:06] To this valueOf() method I can pass the num variable with that.
[06:11] This num primitive data type value is is going to be converted into an Integer wrapper class object.
[06:17] The same I can do for double as well.
[06:20] Let me remove this constructor code and mention double.valueOf() method.
[06:26] When you try to invoke the valueOf() method, you can see you can either pass the input in the actual
[06:31] representation of a primitive data type value, or you can also pass the input in a String representation
[06:37] value as well.
[06:38] So this time I will try to invoke the second valueOf() method.
[06:41] And to this I'm going to pass the 3.14 in a String format.
[06:46] Let me do the same for Long value as well.
[06:49] For the same, I'm going to mention Long.valueOf() and to the same
[06:54] I'm going to pass the input as 95657.
[06:59] Let me remove this unnecessary code here
[07:01] also, I'm going to remove the M because otherwise we are going to get a runtime exception.
[07:06] This time
[07:07] also, you will be able to see the three different objects created with the name integer1, doubleObj1
[07:12] and longObj1.
[07:15] Inside this we have corresponding values like whatever values we are trying to store inside them.
[07:21] So you can see we are trying to wrap our actual values inside an object.
[07:26] So that's why we call them as wrapper classes.
[07:28] And this process is called as boxing.
[07:31] I hope you are clear.
[07:32] We discussed two different approaches
[07:34] one is with the help of constructor and the other one is with the help of valueOf() method.
[07:40] Always please use the valueOf() method approach because this is the recommended approach and the constructor
[07:46] approach is deprecated.
[07:47] Apart from supporting the boxing process wrapper classes, they also have many utility methods that
[07:54] are going to help us.
[07:55] While we are dealing with the primitive data type values.
[07:58] I will show you the demo of most commonly used method in all the wrapper classes around the passing
[08:05] process.
[08:06] What is a parsing?
[08:07] Parsing is a process which will convert a String representation of your primitive data type value into
[08:14] its actual primitive data type value.
[08:17] For example, think like I have an Int value in an String format.
[08:21] If I want to convert that into an primitive data type value.
[08:25] In such scenarios, I need to invoke the parse related method available inside the corresponding wrapper
[08:32] class.
[08:33] Here since I'm trying to deal with the int primitive data type, I need to use the Integer wrapper class,
[08:39] and using this I need to invoke the static method which is parseInt().
[08:45] So to this parseInt() method, we can pass the String representation of your int value.
[08:51] Here I'm going to mention the value as 18.
[08:55] The output from these parseInt() method is going to be the actual int value.
[09:00] So that's why on the left hand side I'm going to mention a variable name of type int.
[09:06] So the variable name I'm mentioning as num1.
[09:09] Now I'll try to print out these num1 variable.
[09:12] And let's see what do we have inside this variable.
[09:15] Before that let me remove this breakpoint and execute this program.
[09:19] And towards the end you can see we have the same value
[09:22] but in a primitive data type format.
[09:25] Each of the wrapper classes they have these parse related method.
[09:29] For example, inside the double we have a method with the name parseDouble() because it is going to parse
[09:38] a given String value into an double primitive data type.
[09:42] So here you can see the return type from
[09:44] this method is double primitive data type.
[09:46] Similarly, inside long you will have parseLong() method.
[09:49] Inside short you will have parseShort() method.
[09:52] So always when you want to convert your String representation of your primitive data type values into
[09:58] their actual primitive data
[09:59] type values, then in such scenarios always use the parsing related method.
[10:05] Whereas for the boxing process which is converting your primitive data type values into their corresponding
[10:12] wrapper class objects, you should use the valueOf() method.
[10:16] Off course, you can also use these constructors, but these constructor approach is deprecated.
[10:20] I hope you are clear with all the topics that we have discussed inside this lecture.
[10:24] For your reference, I have mentioned all the details that we discussed inside this slide along with
[10:29] the code that we have discussed.
[10:31] Please refer the same if you have any doubts.
[10:33] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
