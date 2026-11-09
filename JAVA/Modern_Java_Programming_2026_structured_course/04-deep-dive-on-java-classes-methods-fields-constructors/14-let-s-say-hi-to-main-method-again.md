# 4.14 — Let’s say hi to main method again

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00:00] Now, since we have gained some good amount of knowledge on Java methods, let's revisit
[00:00:06] our main method that we have discussed in the previous sections.
[00:00:10] So we are going to say hi to the main method again.
[00:00:13] Like we know the syntax of main method is public static void main array of string as
[00:00:19] an input parameter and inside the method body we can write our business logic.
[00:00:24] So now it should be pretty clear for you what is the purpose of each word inside your
[00:00:29] main method declaration.
[00:00:31] The purpose of public is it is going to act as a modifier for your method.
[00:00:37] So mentioning public is very important and mandatory for your main method.
[00:00:42] This public allow my JVM to access my main method without any issues.
[00:00:48] If you don't define public for your main method, then your JVM cannot access it since
[00:00:54] you have not made your method as public.
[00:00:57] And after public, we should also mention static because we want our JVM to invoke the main
[00:01:03] method without creating the object of the class.
[00:01:07] Like we discussed previously, whenever we want to invoke a static method, we can simply
[00:01:12] invoke it with the help of class name.
[00:01:15] So behind the scenes, when we start our Java program where we have a main method declared,
[00:01:20] the JVM is going to invoke this static main method with the help of class name itself.
[00:01:26] It does not have to create the object of the given class where the main method is present.
[00:01:31] This is one of the standardized approach that is implemented by the Java team for the JVM
[00:01:37] because JVM cannot create the object before invoking a method.
[00:01:42] So how come JVM can create an object of a class without invoking a method?
[00:01:48] So to give that convenience to the JVM, we need to make the main method as static.
[00:01:53] That means this method can be invoked by your JVM with the help of class name itself and
[00:01:58] without the need of writing the Java statement to create the Java object.
[00:02:03] And the return type of the method is void.
[00:02:05] So void means your method is not going to return anything and the input parameters that
[00:02:10] we need to send to the main method is array of string values.
[00:02:14] So we are going to discuss what is an array in the coming sections.
[00:02:17] Array of string means we can send multiple string values inside an array and this parameter
[00:02:24] name is a placeholder.
[00:02:25] So instead of args, you can define some other parameter name like myArgs.
[00:02:30] So any name should be fine for your method parameters.
[00:02:34] As a thumb rule, we just have to make sure the same name we are using inside the method
[00:02:38] body to refer to the method parameters.
[00:02:41] Otherwise you are going to get a compilation error.
[00:02:44] So with this knowledge, now let's try to create the public static void main method again and
[00:02:49] let's try to answer some tricky questions.
[00:02:51] So to create a main method, first I'm going to create a class like we discussed in the
[00:02:57] previous sections.
[00:02:58] The class name is going to be HelloWorld.
[00:03:01] Inside this HelloWorld class, I'm going to create a main method.
[00:03:05] So to create a main method, the shortcut in IntelliJ is psvm, the public static void main.
[00:03:12] So once you type this psvm, you can press enter.
[00:03:16] And with that, you can see you have an empty main method.
[00:03:20] And inside this, I want to print the HelloWorld statement.
[00:03:24] So what is a shortcut for System.out.printerln? S-O-U-T.
[00:03:30] So if you press enter, you'll get System.out.printerln statement.
[00:03:34] And inside this, you can simply write HelloWorld string value.
[00:03:37] So if I try to execute this Java class, you can see I'm going to get an output, which is HelloWorld.
[00:03:44] Now the tricky question that you may face in interviews is, the interviewer person can
[00:03:49] ask, can I remove static for my main method or can I remove the public for my main method?
[00:03:55] So these kind of tricky questions you may face.
[00:03:58] So let's try to understand what is going to happen.
[00:04:01] If I try to remove this static from my main method definition, you can see this is completely
[00:04:06] a valid method, but my JVM cannot use this main method to start the program.
[00:04:12] That's why right now you can see the start button also disabled.
[00:04:16] As soon as I try to bring back the static, you will be able to see that these buttons are enabled.
[00:04:22] That means my JVM always is going to look for the exact method signature like public
[00:04:27] static void main string of array.
[00:04:31] Here this time I can also show you that I'll try to remove this public and with that you
[00:04:35] will be able to see all these buttons will be disabled or disappear.
[00:04:40] So let me remove this.
[00:04:41] You can see right now this method cannot be used by my JVM to start the program.
[00:04:46] So let me bring back public.
[00:04:48] This time I will change this aux to some other name.
[00:04:51] Instead of aux, I'll just keep it as my aux.
[00:04:55] With this, it is perfectly fine because parameter names are going to be simply placeholder.
[00:05:01] You can give any name.
[00:05:03] So I can also try to execute this program and you are going to get the same output which is hello world.
[00:05:09] I hope you are clear with the signature of the public static void main.
[00:05:13] This is very very important inside Java.
[00:05:17] Interviewers can confuse you a lot around this method.
[00:05:20] So please be very very clear around this method.
[00:05:23] The next question that interviewer may ask you is, can I write multiple main methods
[00:05:29] inside a same Java class?
[00:05:31] The answer is, of course we can write the multiple main methods, but we need to make
[00:05:36] sure the method signature is not same.
[00:05:40] For example, if I try to copy the same method, the method signatures are going to be same.
[00:05:46] That's why I'm getting an error.
[00:05:48] So what I can do?
[00:05:50] I can try to create main methods which are not matching with the original main method signature.
[00:05:56] So here what I can do is, I can try to introduce one more parameter for the same.
[00:06:01] Let me mention comma followed by float num.
[00:06:05] This time you can see there is no compilation error and for this main method, there is no
[00:06:10] start button, whereas for this main method, there is a start button because this is matching
[00:06:15] with the main method signature that JVM is expecting.
[00:06:19] Very similarly, I can also create any number of main methods with different different method signature.
[00:06:25] Maybe here this time I will try to mention public double main and this main method is
[00:06:32] not going to accept anything.
[00:06:34] It is simply going to return a double value, which is 3.14.
[00:06:39] So you can see this is perfectly fine.
[00:06:41] I hope this is clear.
[00:06:43] Even if interviewer is trying to trick you or trying to confuse you, don't get confused.
[00:06:47] You can tell him or her confidently saying that, yes, it is absolutely possible to define
[00:06:53] multiple main methods, but different different method signatures.
[00:06:58] I hope this is clear.
[00:06:59] For your reference, I have mentioned the details about these tricky questions around the main
[00:07:03] method inside this slide.
[00:07:05] So please refer the same whenever you have some questions.
[00:07:08] I hope you are liking the progress that we are making throughout the course.
[00:07:11] Thank you and I will catch you in the next lecture. Bye.

----------------------------------------
