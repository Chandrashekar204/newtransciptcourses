# 4.16 — How to create & initialize Java objects - Demo

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Inside this lecture, let's try to create our first Java object.
[00:05] I'm very excited for this.
[00:06] As of now, you can see we have a class with the name Employee
[00:10] and inside this class we have Java fields and Java methods.
[00:14] As a next step, I want to create Java objects by using the skeleton or blueprint that I have defined
[00:21] inside these Employee class.
[00:23] To get started around this, I'm going to create a separate Java class.
[00:28] The Java class name is going to be EmployeeMain.
[00:32] I have chosen this name because inside this class I'm going to write a main() method which will trigger
[00:39] the Employee functionality like object creation, populating the data and invoking the methods.
[00:46] That's why I felt like this name is very apt for this scenario.
[00:49] So let me create this class.
[00:51] Now my class is empty.
[00:53] As a next step, let me try to create the main() method for the same
[00:57] I'm going to type psvm inside my IntelliJ and press enter and you can see I got an main method with
[01:04] the syntax that my JVM is expecting, like " public static void main (String[] args)".
[01:10] Inside these main() method, the very first task that I want to accomplish is to create an object of Employee.
[01:18] For the same
[01:18] first I need to mention the class name, which is Employee, followed by what is the variable name
[01:25] or reference name that I want to give for my object.
[01:28] In future
[01:29] whenever I want to access something inside my object, I am going to use the same reference.
[01:35] Maybe I can give the variable name as Employee in all small letters.
[01:40] After this I am going to mention is equal to followed by new keyword followed by Employee
[01:47] but here we should not simply give the class name.
[01:50] This is not valid.
[01:52] Instead we need to mention the parentheses.
[01:55] This we call it as a Java constructor.
[01:58] We are going to talk about constructor in few minutes.
[02:01] So whenever we invoke the constructor of the class with the help of new operator behind the scenes,
[02:07] it is going to create an object, and it is going to assign a memory inside your JVM.
[02:13] And for that memory location it is going to give a name which is employee, same as your variable name.
[02:19] So whenever you want to access that data inside that memory location, you're going to use the same
[02:25] variable name.
[02:26] Now my Employee object will have all the default values.
[02:30] Because if I go and see inside my Employee class I have three names like firstName, lastName, age
[02:36] and gender.
[02:37] For firstName and lastName we are going to have null value and age
[02:41] we are going to have zero and gender
[02:43] we are going to have blank char because by default char data type is going to hold the blank space.
[02:49] So to provide the data which is specific to my object, I'm going to first use my object reference which
[02:56] is employee and dot operator.
[02:59] And you can see your IntelliJ is going to show you all the available options that you have when you
[03:06] try to invoke a field or a method.
[03:08] So first I want to invoke the firstName field.
[03:12] You can just type initial letters and press enter and post
[03:16] that user is equal to followed by
[03:19] try to assign a firstName.
[03:21] So I'll just give the firstName as John here, followed by I will try to invoke the next field, which
[03:28] is lastName.
[03:29] For the last name I'm going to give the value as doe, followed by semicolon.
[03:35] Please note that inside Java, each and every Java statement should be terminated with a semicolon.
[03:41] After the last name, I want to populate the age of the employee, so for the same I'm going to invoke
[03:47] the age field.
[03:49] So here, as soon as you type age you can see you are getting two options age and getAge.
[03:55] age is a field
[03:56] that's why you are able to see this f icon.
[03:59] Whereas getAge() is a method
[04:01] that's why you are able to see an icon with the m value.
[04:05] So please be always cautious since I want to populate the field value, I'm going to select the age
[04:11] and to this I'm going to assign some value which is 30, and followed by what is the gender of this
[04:18] employee.
[04:19] So the gender I want to populate it as M.
[04:22] With this I have populated all the unique data which is specific to this employee.
[04:26] Similar way you can create thousands of employee objects based upon your requirements and in real projects
[04:34] we're not going to repeat all these lines of code thousands of time.
[04:38] Instead, what we are going to do is we are going to write looping programming logic, which is going
[04:43] to execute continuously based upon your conditions.
[04:47] So all such advanced topics we are going to discuss in the coming sections.
[04:52] For now, let's focus on how to invoke the methods available inside the Employee object.
[04:59] So whatever
[04:59] methods that we have defined inside the Employee class,
[05:03] these are non-static methods or instance methods.
[05:07] That means in order to invoke these Java methods, we need to use a reference of object.
[05:12] So what is our reference of object?
[05:13] It is employee.
[05:15] And if I try to press Dot and you can see I'm getting so many options, let me type get and getAge()
[05:21] is one of the method which I want to invoke here.
[05:25] Let me press semicolon here
[05:27] I'm just trying to invoke the method, but I'm not catching the output that I receive from this method.
[05:33] So I want to catch the output from this method, and I want to print it onto the console.
[05:38] So for the same what I can do is I can first try to write System.out.println().
[05:44] Inside this println() method, I'm going to first mention employee object reference and invoke getAge() method.
[05:51] With this we are simply invoking the getAge() method, and this getAge() method is going to return the byte
[05:59] value, and that byte value is going to be accepted by the println() method, and it is going to print
[06:05] the same onto the screen.
[06:06] With that the upper line we don't need,
[06:10] let me delete this.
[06:11] Very similarly, let me copy this value and this time instead of getAge(), let me mention getGender().
[06:18] So with this we should be good.
[06:20] Let me save this changes and do a build.
[06:23] Build is a process which will initiate the compilation of your Java class by automatically.
[06:30] Your intelliJ is going to perform the same if you try to execute your Java program.
[06:35] In case
[06:36] if you want to manually trigger this build process, you can go to build and click on this build project.
[06:43] Otherwise, you can simply follow the shortcut mentioned here.
[06:46] For the mac, the shortcut is going to be command +F9.
[06:49] Similarly, inside windows operating system you'll be seeing the corresponding shortcut.
[06:53] So if I try to press command + F9 inside my system, you can see the build process triggered
[07:00] and behind the scenes the compilation might have completed and the .class might have triggered.
[07:05] Otherwise, if you don't do the build process manually, it should work perfectly without any issues.
[07:10] Because when you try to run your Java class at that time, the compilation will take care if the compilation
[07:16] is already not completed.
[07:18] But in some scenarios, if you have too many classes and dependencies between them, then you are going
[07:24] to get some compilation errors to resolve that you can do the build manually, so let me try to invoke
[07:30] the main() method present inside this class.
[07:32] For the same I can click on this button.
[07:35] You can see I got an output in the output
[07:38] the age and gender details are displayed.
[07:41] I hope this is clear.
[07:43] Now as a next step we need to understand what is a constructor in Java.
[07:47] Like I said here in this line, when we are trying to create an object from the Java class, we are
[07:53] invoking a constructor Employee with parentheses.
[07:56] But we have not defined this constructor.
[07:59] Nowhere inside my Employee Java class. But how your code is still working, because behind the scenes,
[08:05] the Java compiler is going to add a default constructor for every Java class that you are going to create.
[08:12] I can show you that as well.
[08:14] You can see this is a source file of my employee Java class.
[08:18] If I try to open the compiled file of Employee under out, you can see there is an Employee.class
[08:25] file is present.
[08:26] If I try to click on that, you'll be able to see there is a .class extension.
[08:30] My IntelliJ
[08:31] decompile the bytecode for my reference into the Java code.
[08:35] So here it is also showing some information that it decompile the .class file bytecode into the Java
[08:42] code.
[08:42] So what is a Decompilation?
[08:44] Decompilation is a reverse process of compilation.
[08:47] So in compilation a Java code will be transferred into the bytecode, whereas in the decompilation the
[08:54] bytecode will be transferred back to the Java code.
[08:58] So if you see here most of the code we have written like these fields we have written and these methods
[09:04] also we have declared.
[09:05] But this code we nowhere declared inside our Java code.
[09:09] So what is this?
[09:10] This is a constructor.
[09:12] Each and every Java class is going to have this default constructor.
[09:17] Using this default constructor, only a Java object is going to be created.
[09:22] There is a very good reason why we need constructors inside Java.
[09:25] From the next lecture, let's focus on understanding why we need constructors inside Java.
[09:31] I know you may have many questions around constructors.
[09:33] Don't worry, by the time we are done with the discussion of constructor, you are going to be the master
[09:39] of constructor inside Java.
[09:41] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
