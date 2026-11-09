# 4.9 — Demo of Java methods - Part 1

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's try to create Java methods inside the classes that we have created so far.
[00:06] Before we try to declare Java method, let me answer one of the burning question that you may have, in
[00:11] the previous section
[00:12] we have defined a main() method.
[00:14] Using this main() method only we executed Hello world program.
[00:17] If you see here
[00:18] for this main() method we have a static keyword. Just after public,
[00:23] we have a static keyword, but the same I have not discussed or highlighted in the previous lecture.
[00:28] The reason is inside Java we can write two different type of methods.
[00:32] One is static methods like main() method and non static methods like we discussed in the previous lecture.
[00:39] For non static methods we don't have to define these static keyword.
[00:43] So there is a clear difference between static methods and non static methods
[00:47] and we should also learn when to create a static method and when to create a non static method.
[00:53] So we are going to focus on static methods in the coming lectures.
[00:56] But for now let's simply focus on non static methods where we don't have to define the static keyword.
[01:03] I hope you are clear.
[01:04] First, I'll try to create two methods inside my Car class.
[01:08] Since I'm trying to create a method related to Car class, I need to make sure I'm defining the methods
[01:14] which are relevant to my Car class or the object that I'm going to create with the help of Car class.
[01:20] To get started with the method creation
[01:22] like we discussed previously, always at the top of the class, we should have Java fields.
[01:27] Under the Java fields we can create any number of methods.
[01:31] It is a standard that we need to follow.
[01:33] Even if you don't follow the standard, your compiler is not going to complain anything, but it will
[01:38] always make your class looks good.
[01:40] If you keep all your fields at the top and the methods in the down.
[01:44] So to create a method, first I want to mention the modifier which is public and my method is not going
[01:50] to return any output to the invoking entity.
[01:54] So what is the return type that I have to mention here it is going to be void.
[01:58] Void indicates that my method is not going to return anything after the return type we need to provide
[02:03] what is the method name.
[02:06] The name of the method that I want to choose here is startCar().
[02:10] So whenever I want to start my car I'm going to invoke this method.
[02:14] This is just an imaginary use case I'm trying to define with the help of a Java method.
[02:19] There's a very good chance in real projects you're not going to start your car with a Java method.
[02:26] Though it is possible to start a vehicle by integrating your Java code with the IoT devices.
[02:31] But that is a very rare scenario.
[02:33] But now let's keep this method very, very simple.
[02:36] So to keep this method very simple, I'm not going to accept any method input parameter.
[02:42] That's why I'm going to keep these parentheses as empty.
[02:46] So there'll be an open parenthesis and closing parentheses.
[02:49] After the parentheses I'm going to give a space followed by opening curly brace and closing curly brace.
[02:56] If you can see here inside these curly braces only we have to define all our business logic.
[03:02] The business logic that I want to write here is very simple.
[03:06] I just wanted to print a statement indicating that car started.
[03:10] So let me do the same with the help of System.out.println().
[03:14] So the shortcut that we need to use inside IntelliJ is, sout.
[03:19] So if you type sout and press enter you're going to get a statement which is System.out.println().
[03:26] To this println() method I'm going to pass a String which is Vehicle Started.
[03:31] So whenever someone invoke this method I'm going to print a message saying that vehicle is started.
[03:37] Now very similarly, let me create one more method which is going to stop the car.
[03:42] This time I want to return a String data from my method.
[03:46] That's why after public I have to mention the return type as String after String, I have to mention
[03:52] the name of the method.
[03:54] The name of the method is stopCar().
[03:57] After the method name, I'm going to give the parenthesis and this time also my method is not going
[04:03] to accept any input parameters.
[04:05] That's why I'm keeping this stopCar() input parameters as empty post that we need to mention the curly
[04:11] braces.
[04:12] And inside this method body, I'm going to write a logic to return a String as an output for the same
[04:18] first let me create a variable which is String output.
[04:22] The variable name is going to be output and to this output variable I'm going to assign a String which
[04:27] is vehicle stopped.
[04:29] Once I have mentioned this vehicle stopped String, I'm going to simply return this variable.
[04:35] Otherwise you can see I'm keep getting an error saying that missing return statement.
[04:40] So to resolve this first we need to type the return keyword followed by space
[04:45] and after the space you need to mention the variable which is matching your return type.
[04:50] After the variable, you need to give the semicolon.
[04:53] So here the output is matching with the return type variable which is String.
[04:57] If I try to change the return type of the
[05:00] to the int.
[05:01] Then again, I'm going to get a compilation error because the method is telling that it is going to
[05:06] return int, but inside the method body we're trying to return String, which is contradicting with
[05:12] each other.
[05:13] That's why we are getting an compilation error.
[05:15] So let me revert back to String and this will resolve the compilation error.
[05:21] So with this core is trying to invoke my stopCar() method.
[05:25] They are going to get an String as an output.
[05:28] And inside the String we are going to send a value which is Vehicle Stopped.
[05:32] With this value, they can do whatever they want, they can print it or they can further process it.
[05:37] So based upon their requirements, they can accept this output and process on their side.
[05:43] I hope you are clear with these two methods
[05:45] let's try to write more methods in the next lecture as well.
[05:49] I want you to get familiar with these syntax
[05:51] that's why I'm trying to build a lot of methods.
[05:53] In the next lecture, let's try to create some methods inside the Employee class.
[05:58] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
