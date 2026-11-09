# 4.30 — Demo of static methods in Java - Part 1

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's try to create some static methods and see them in action.
[00:06] To create a static method, I'm going to open the ArithmeticOperations class that we have created previously.
[00:12] Inside this method
[00:13] as of now we have a single non static method or an instance method with the name sum().
[00:20] Let me try to copy the same method and paste it inside the same Java class.
[00:25] Since the method signature and method definition is same, we are getting a compilation error in order
[00:31] to create a static method like we discussed previously, we need to mention static keyword inside the
[00:37] method declaration
[00:38] or method definition.
[00:40] So let me mention the static keyword just after the public keyword till you can see we are getting the
[00:46] compilation error because the method signature is going to be same for them, which means your Java
[00:53] compiler is not going to accept a static and non static method to have the same method signature
[01:00] that's why we are facing this error.
[01:02] To resolve this issue, I can change the name of this method from sum() to addition().
[01:07] So right now you can see I have a static method with the name addition() which is going to perform the
[01:13] addition().
[01:14] Similarly, I also have another non static method which is going to perform the same business logic
[01:20] but with a name as sum().
[01:22] I hope you are with me till this point.
[01:24] As a next step, I'm going to create two variables or two fields inside this class.
[01:30] The very first variable that I want to create is double piValue = 3.14.
[01:39] So this is a non static variable or instance variable.
[01:43] Very similarly I want to create a static variable to create a static variable,
[01:47] first I need to mention static followed by final.
[01:51] Since I want to create a constant static variable and giving the final keyword here, post that I'll
[01:58] give double, followed by what is a variable name?
[02:01] the variable name
[02:02] I'll just give it as same as piValue, but I'll follow the snake case because this is a final and constant
[02:08] value to this constant,
[02:09] I'm trying to give 3.14 as an value.
[02:13] So with the same value we have a instance variable and we also have static variable.
[02:18] The reason why I'm trying to create these variables is, I want to show you the limitations of static
[02:23] variable.
[02:24] To demo you the same I need all these variables.
[02:27] As a next step I'm going to create the public static void main() method inside these ArithmeticOperations
[02:33] class.
[02:34] So let me create main() method here.
[02:36] From the main() method I'm going to invoke the addition() static method which is present in the same class.
[02:42] Previously we discussed the syntax that we need to follow whenever we want to invoke a method which
[02:47] is present inside the same class is we just have to invoke the method name along with the method arguments.
[02:54] So the method name that
[02:55] here we have is addition() to this method, I want to pass two arguments.
[03:01] The very first one I'll just mention as 20, 5.
[03:06] So I want to add these two numbers.
[03:08] The result from this method I'm going to catch inside a variable called result the same
[03:14] I can also try to print them on the console so that we can validate if the operation is being successful
[03:20] or not.
[03:21] First, let me try to execute this program.
[03:23] You'll be able to see the output 25, which means it is working without any issues.
[03:28] So from a static method which is a main() method, I invoked another static method which is addition().
[03:35] Now let me try to invoke the instance method or a non-static method available inside the class, which
[03:41] is sum().
[03:42] So instead of addition(), I want to keep it as sum().
[03:45] As soon as I try to invoke the instance method, you can see the compiler is throwing an error saying
[03:50] that non static method cannot be referenced from a static context.
[03:55] That means from a static method we cannot invoke the instance method which is sum().
[04:01] So this is one of the limitation that you need to be aware.
[04:04] But this doesn't mean there is no way to invoke the instance method from a static method.
[04:10] There is a way in order to create the instance methods from the static method, we need to create the
[04:15] object of the class, and using the object, we should be able to invoke the instance method.
[04:21] So here let me create the object of the class to create the object of the class
[04:25] first I need to mention the class name, followed by what is the object reference name.
[04:30] I'll just mention the variable name as ArithmeticOperations only, but I'm following the camel case
[04:36] letter here.
[04:37] Post that I'll mention new followed by ArithmeticOperations
[04:41] default constructor.
[04:42] Now using these object reference, I can invoke the sum() method, and to this sum() method I can pass the
[04:51] 20, 5 value.
[04:53] The result I can catch it inside the result variable.
[04:57] Post this I'm going to delete the next line and
[05:00] now, if I try to execute the program, we are going to get the same output, which is 25.
[05:05] So do you see there is a way to invoke the instance methods from the static methods.
[05:10] The solution is,
[05:11] first, we need to create the object of the class, and using the object of the class, we need to invoke
[05:16] the instance method.
[05:17] Now let's move on to the fields that we have.
[05:20] So there is a field called piValue.
[05:22] This is a static field.
[05:24] I should be able to access the static field very easily from my static method.
[05:28] So what I can do is I can try to print the piValue by accessing it.
[05:34] And you can see I'm able to access it without any issues.
[05:37] If I try to run this program able to see the value also, which is 3.14.
[05:42] But if I try to do the same to access the normal variable, I'll get an compilation error.
[05:49] You can see there is no way for me to access the piValue, which is an instance variable from an static
[05:56] method.
[05:56] So this is not going to be acceptable by your compiler, whereas I can invoke this piValue instance
[06:04] variable from an instance method very easily.
[06:07] So you can see here if I try to mention the System.out.println(), piValue, I'm able to access
[06:14] it without any issues.
[06:15] So this confirms from instance methods we can access instance variable without any restrictions.
[06:21] If I try to access the static variable from my instance method, I should be able to access it without
[06:28] any issues.
[06:29] You can see there is no compilation error.
[06:31] The other approach that we can follow to access an instance variable from an static method is,
[06:37] using the object reference, we should be able to access the instance variable.
[06:42] So here what I can do is I can try to mention System.out.println() post
[06:48] using the object reference I can invoke the piValue field.
[06:52] So you can see this is one of the approach that we can follow.
[06:55] Let me try to execute this program.
[06:57] But before that I'll try to keep a breakpoint here and run the program in a debug mode.
[07:02] First an object is going to be created and using the object I'm trying to invoke the sum() method.
[07:09] So let me put a breakpoint inside the sum() method as well and release the breakpoint
[07:13] this time the breakpoint is going to stop inside the sum() method.
[07:17] You can see
[07:18] first I'm able to access the piValue, which is an instance value, and there is a value inside it
[07:24] which is 3.14
[07:26] the same is going to be displayed on the console post that I'm going to print the value of piValue
[07:32] with the help of the static variable.
[07:34] So let me move on to the next line.
[07:36] Here I can release a breakpoint and that will complete the execution of the program.
[07:41] You can see at many places we are trying to print the so many System.out.println() statements.
[07:47] The same we are able to see inside the output.
[07:49] As a next step, let me add one more method inside these ArithmeticOperations class.
[07:54] This time I'm going to create a non-static method.
[07:58] So let me copy this sum() method and paste it.
[08:01] Just after that
[08:02] and I'm going to mention the method name as subtract(), which means I want to perform the subtraction
[08:08] of the two numbers.
[08:09] So what I can do is first let me remove these System.out.println() statements.
[08:14] Here instead of class I can use the minus symbol, which is going to take care of subtracting the given
[08:20] two numbers.
[08:21] So from the sum() method which is a non-static method, I can invoke subtract() method.
[08:27] So let me do the same.
[08:29] So how to invoke the subtract() method?
[08:30] Since the method is present inside the same class, I can simply use the method name like subtract().
[08:37] And after that I'm going to pass the whatever values that I have received to this method, which is
[08:43] num1 and num2.
[08:45] So let me mention a semicolon.
[08:46] Also, let me remove the System.out.println() statements.
[08:50] We no more needed these values because we are already clear with these concepts.
[08:54] Now you can see what I'm trying to tell with these statement is from a instance method you can invoke
[09:02] another instance method just by using the method name.
[09:05] If the methods are present in the same class, and very similarly if needed from the instance method,
[09:11] you can also invoke the static method with the name addition() and pass the num1, num2.
[09:20] This confirms the instance method does not have any restrictions.
[09:24] It can invoke all type of methods which are present in the same class.
[09:28] The method can be a static method or a non-static method.
[09:31] The limitations only will come into picture if you try to invoke the instance method directly from the
[09:38] static method.
[09:40] We can't invoke the instance method from a static method by using the name
[09:45] first, we need to make sure we are creating an object post that only we should be able to invoke the
[09:50] instance method.
[09:51] So please be aware about all these limitations.
[09:54] So if you have a scenario where you don't have any requirement to access the instance
[09:59] method and instance variables, you can always happily go with the static methods.
[10:04] Otherwise always go for the instance method.
[10:07] But please note that there is also a way to invoke the instance method and the instance variables from
[10:14] the static method.
[10:15] The way is to first create the object of the class, and using the object of the class, we need to
[10:22] invoke the instance method or instance variable.
[10:25] I hope you are clear
[10:26] with this demo, I want to discuss more about the static method in the next lecture as well.
[10:31] So more to come about this in the next lecture.
[10:33] Thank you.
[10:34] Bye.

----------------------------------------
