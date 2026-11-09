# 15.14 — Details about Shallow cloning & Deep cloning - Demo

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Let's see the demo of shallow cloning and deep cloning.
[00:03] First, I'm going to create a new Java class with the name Course.
[00:08] Inside this class I'm going to create a single instance variable which is private String courseName.
[00:16] Post that
[00:17] for these instance variable, I'm going to generate the getter and setter method
[00:22] with that, we should be good with these Course class.
[00:25] As an example, let me try to create another Java class with the name Student. Inside the Student
[00:32] first, I'm going to have an instance variable of type String with the variable name as name, followed
[00:39] by
[00:39] I'm going to define another instance variable of data type course with the variable name as course.
[00:46] You can see my Student class has an embedded instance variable which belongs to the other class.
[00:54] In this kind of scenarios, only shallow cloning and deep cloning come into picture.
[00:58] First, let's try to perform the shallow cloning for the same
[01:02] I'm going to implement Clonable interface inside my Student class, followed by
[01:09] I'm going to generate the constructor and the getter and setter methods for my Student class.
[01:15] So let me select the constructor and select both of these parameters, followed by
[01:20] I'm also going to generate the getter and setter method.
[01:24] With this we should be good.
[01:26] At last we should override the clone() method.
[01:29] So let me copy the clone() method that we have inside the Person class.
[01:34] The same we can use inside the Student as well.
[01:36] Since I have implemented cloning related logic only inside the outer object which is Student, this
[01:42] is going to help me only to perform the shallow cloning.
[01:45] Let's see the demo of the same by creating an example class with the name ShallowCloneExample.
[01:53] .
[01:54] Inside this class
[01:55] first I'm going to create the main() method, followed by
[01:59] first I'm going to create the Course object with the help of default constructor.
[02:05] And at last I'm going to set the course name with the help of setCourse() name method.
[02:10] The course name is going to be Math.
[02:12] After this, I'm going to create the Student object with the object reference variable name as oirginal
[02:20] Student.
[02:21] On the right hand side, I'm using the new operator, followed by the constructor of the Student.
[02:26] To this constructor of the Student, I'm going to pass the Student name as Alice, and the second parameter
[02:33] is the object
[02:34] of course, we need to pass.
[02:36] Now I can try to perform the cloning with the help of original student.
[02:41] The same I'm going to assign to the clone Student object reference name.
[02:45] So how to perform the cloning?
[02:47] First we need to mention original Student Object reference name, followed by
[02:51] we need to invoke the clone() method and we are going to get the compilation error to handle the
[02:57] CloneNotSupportedException.
[02:58] Let me add the throws keyword later on, we should perform the casting manually by mentioning student
[03:06] within the parentheses.
[03:08] So with this only the shallow copying is going to happen.
[03:12] We can also confirm the same by having a System.out.println(), and comparing the memory locations
[03:19] of the two Student objects that we have.
[03:22] So this statement is going to print false as an output, because this original student and the clone
[03:28] student, they're going to be two different physical objects.
[03:31] Whereas if I try to compare the address of the course objects which are available inside the original
[03:39] student and the cloned student, I'm going to get the output as true because they both point to the
[03:46] same course object.
[03:48] So let me try to execute this program.
[03:50] You can see first I'm getting false, followed by true.
[03:52] I hope you're clear with that demo of ShallowClone.
[03:55] As a next step, let's try to perform that deep cloning.
[03:58] To perform that deep cloning, first, we need to make sure that the embedded objects also supports
[04:04] cloning.
[04:04] So what is the embedded object?
[04:06] It is a Course class.
[04:07] So here first I need to make sure I'm implementing Cloneable followed by I need to override the clone()
[04:13] method like we did inside the Student class.
[04:16] So let me mention the same here.
[04:18] As a next step, we need to update the cloning logic that we have inside the Student class.
[04:23] So first we need to perform the cloning of the Student object by having a object reference name which
[04:30] is clonedStudent followed by I can try to invoke the super.clone(), and after this I can try to perform
[04:38] the casting with the help of Student.
[04:41] With this only the student details will be cloned.
[04:44] But we decided to do the deep cloning by cloning even the embedded course objects.
[04:50] That's why we need to invoke the Course.clone() followed by
[04:55] we need to copy the new Course object into the clonedStudent
[05:00] by mentioning the field name, which is course.
[05:03] So with this the cloning is going to happen even for the course object.
[05:08] But before that I need to make sure I'm doing the down casting, and at last we can return these clonedStudent
[05:15] from this method.
[05:17] I hope you are clear with the logic that we have written inside this clone() method of the Student class.
[05:22] Now, if I try to execute this shallow clone example, I'm going to get the different output.
[05:28] Let's see the output.
[05:29] This time I'm going to get the false and false for both the System.out.println() statements.
[05:35] So this is the power of deep cloning.
[05:37] The name itself is self-explanatory.
[05:39] Whenever we are trying to perform the deep cloning, even the embedded objects present inside your original
[05:45] object, they are also going to be copied this way based upon your requirements
[05:49] you can try to clone any number of embedded objects inside your Java program.
[05:56] I'm not creating any other class with the name DeepClone example, because the same class you can use
[06:03] to check the output of shallow clone and deep cloning.
[06:06] Maybe what we can do is we can rename these class name to CloneExample.
[06:10] After renaming the class name, we should also rename the file.
[06:13] That's what I'm trying to do here.
[06:15] With this we should be good.
[06:17] And we discussed pretty good amount of methods inside object to super class.
[06:23] The only methods that we are add to discuss is notify() notifyAll() and weight related overloaded methods.
[06:31] So these methods we can use in the scenarios of multi-threading environment.
[06:36] So whenever you are trying to write a Java program that is going to create multiple threads, in those
[06:41] scenarios, only we can use notify(), notifyAll() weight related methods.
[06:46] So what is the purpose of notify() method?
[06:49] Using this notify() method, we can notify the thread which is waiting on top of my object.
[06:56] So you can see wake up a single thread that is waiting on these objects moniter.
[07:00] If any threads are waiting on this object, only one of them is chosen to be awakened.
[07:06] Whereas if you want to awake all the waiting threads, then in that scenario you should use the notifyAll().
[07:13] .
[07:14] So that's the purpose of notify() and notifyAll() method.
[07:17] But coming to the wait method using the wait() methods, we can make a current thread to wait until it
[07:25] is awakened.
[07:26] So whenever we are using this wait() method without any input parameters, the thread is going to wait
[07:31] continuously until it is awakened with the help of notify() or notifyAll() method, whereas with the help
[07:37] of other wait methods where we are trying to pass the number of milliseconds as an input parameter.
[07:43] So based upon how many number of milliseconds that you are trying to mention accordingly, your thread
[07:49] is going to wait.
[07:50] For example, if you pass 1000 milliseconds as an input, then this wait method it is going to make
[07:56] your thread wait for one second.
[07:58] After that, automatically your JVM is going to notify it and awake the thread which is waiting.
[08:06] More details about these notify() and wait() related methods we are going to discuss in the coming sections
[08:12] when we are talking about advanced concepts like multithreading.
[08:15] For now, you should be good with whatever short discussion that we have done just now.
[08:19] Before I try to close this lecture, let me show you an image which conveys the importance of Object
[08:25] class
[08:26] inside Java ecosystem.
[08:28] You can see Object class is the most important class inside Java ecosystem.
[08:33] Because every class that we are going to create inside Java, they are going to have object as a super
[08:39] class.
[08:40] On top of that, this Object class, it is providing lot many important methods like hashCode(), equals()
[08:47] cloning(), finalize(), notify(), waitAll(), toString().
[08:51] So there are good amount of methods available inside the Object, which are going to be super helpful
[08:56] to the developers whenever they are trying to deal with the object of any class.
[09:00] I hope you agree with this image.
[09:02] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
