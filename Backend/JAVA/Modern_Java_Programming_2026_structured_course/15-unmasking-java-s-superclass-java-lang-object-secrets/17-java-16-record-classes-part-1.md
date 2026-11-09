# 15.17 — [JAVA 16] Record classes - Part 1

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Creating Immutable objects is a very common requirement inside any Java project.
[00:06] Even when you start working in a real project, you will see a lot of immutable objects getting created
[00:13] inside your Java program.
[00:15] But whenever someone wants to create an immutable object, they have to follow certain standards and
[00:21] guidelines like we discussed in the previous lecture.
[00:23] First, they need to create a class by using the final keyword.
[00:27] Later on, they need to create the instance variables with the final, and they need to make sure there
[00:32] are no setter methods
[00:33] only getter methods are available.
[00:35] So if you see here, in order to create an ImmutableObject, someone has to write 20 lines of code,
[00:42] at least. Inside my class right now you can see there are 20 lines of code.
[00:46] What if I say we can create an ImmutableObject by just creating a class with only one, not two lines
[00:54] of code?
[00:54] You may be very angry at me at this point of time, because I have not showed this shortcut in the previous
[01:00] lecture.
[01:01] First, I'm trying to always explain the lengthy approach or the complex approaches.
[01:06] The reason is I want to teach you the concept.
[01:09] Think like if you are trying to learn the driving.
[01:11] There are two approaches.
[01:12] One approach is someone can try to teach you using shortcut approaches like you press the accelerator
[01:18] car will move.
[01:19] You can change the gear by using the gear handle and you can apply the brake which will stop the vehicle.
[01:25] So this way someone can teach you in 5 or 10 minutes.
[01:29] With that, you will only have very limited knowledge and you will be able to drive the vehicle only
[01:35] on empty roads or in a straight road.
[01:38] But you will not be able to handle the complex scenarios, like maybe if you want to drive in a heavily
[01:44] traffic road, you will fail in that scenario because you never understand the basics or the concept
[01:50] behind the driving,
[01:51] how to do that?
[01:52] What are the guidelines that you need to follow?
[01:54] What are the rules that you need to follow?
[01:56] So that's why always the better approach is to first understand the basics and the concepts around the
[02:02] topic.
[02:03] Post that we can look for the shortcut.
[02:05] I hope you are convinced with that.
[02:06] Now let me show you how to create the immutable classes with just 2 or 3 lines of code inside Java.
[02:13] For the same, I'm going to create a new Java class with the name Person record.
[02:21] So when I'm trying to create a class, you can see I have an option of record.
[02:25] So let me select this record option and press enter with that instead of class
[02:31] I have the record keyword inside my class definition.
[02:36] So what is a record?
[02:37] Record is introduced in Java 16.
[02:40] That is going to help you to create the immutable classes on the fly by writing few lines of code.
[02:47] So whenever you're trying to create a record class, you are going to get the parentheses after your
[02:53] class name this parentheses.
[02:55] In other words, we can call it as record header.
[02:58] Inside this record header, we can define the list of instance fields that your class is going to have.
[03:06] So the list of instance fields
[03:07] in other words we can call them as record components.
[03:11] So how to define my instance fields here.
[03:13] Just type String followed by name
[03:16] you don't even have to mention private and final behind the scenes
[03:19] Java is going to take care of it.
[03:21] Similarly, I'm going to mention String occupation.
[03:25] This way you can try to mention any number of record components or instance variables inside your record
[03:32] header.
[03:32] That's it
[03:33] we are done creating a class which is going to allow only immutable objects.
[03:38] I'm not joking here.
[03:39] Java team decided to make developers life easy with the help of these record feature, which is introduced
[03:46] in Java 16.
[03:47] I can also show you that demo.
[03:49] Like I can try to create a new Java class with the name RecordDemo.
[03:55] Inside this RecordDemo, I'm going to create the main() method.
[03:59] Inside this main() method, I'm going to create the object of PersonRecord class.
[04:05] So how to create it with the help of same new operator and the constructor of PersonRecord().
[04:11] So to the constructor of PersonRecord we can pass the name.
[04:15] I can pass the name as John followed by occupation as doctor.
[04:20] So now I will not be able to change the data inside this object.
[04:26] For example, I can't invoke the set() method, I can't invoke the variables, but they'll be getter methods
[04:33] which you can use to fetch the data.
[04:35] But the getter methods that are going to be generated by the record, they are not going to have the
[04:40] get to prefix.
[04:41] Instead, these methods are going to simply have the same name as your instance field.
[04:47] For example, I can try to print out what is present inside the name by invoking the name() method.
[04:54] So here this name method we can construct as a getter method why we don't have a get prefix in the senario
[04:59] of Record classes.
[05:01] It's quite simple.
[05:02] Anyway, since your classes is not going to have setter methods, there is no need to differentiate
[05:07] between getter and setter by maintaining the prefix like get and set.
[05:11] With that reason Java team they simply using the instance field name as method name to fetch the data.
[05:18] So this time I'm going to invoke the occupation() method.
[05:22] If I try to execute this program, you can see I'm getting the details
[05:26] John and Doctor. And I will not be able to change the data inside these ImmutableObject, because I
[05:33] have created these ImmutableObject from a Record class that we have created.
[05:38] Whenever you're trying to create a Record class behind the scenes, Java or JVM is going to take care
[05:43] of few things.
[05:44] Let me try to explain what are those?
[05:46] The very first thing that Java is going to take care of is making the class as final.
[05:53] So that's a very first thing post that it is going to make the fields as final and private, and the
[06:02] next thing that it is going to take care is, generate the getter methods without any getPrefix.
[06:10] In the similar lines, it is also going to generate a constructor with the fields mentioned inside the
[06:18] record header.
[06:20] Since we are trying to mention two different fields, the same fields are going to be considered to
[06:24] generate the constructor apart from these steps, which is going to make your object as immutable,
[06:30] the Record class, it is also going to overwrite the methods of toString(), equals() and hashCode(), based
[06:39] upon the instance fields that we are trying to mention inside the record header.
[06:43] For example, I can go to the RecordDemo here.
[06:47] I can try to print out the My PersonRecord object with the help of System.out.println().
[06:53] So let's try to understand how this object is going to be printed.
[06:56] You can see it is printed in an easily understandable format because behind the scenes, my Record class
[07:04] also override the toString() method, and similarly it also override equals and hashCode() method based
[07:11] upon the instance fields that we have defined inside the record header.
[07:16] If you try to see the list of elements present inside my PersonRecord, you'll be able to see there
[07:21] are fields like name and occupation, and apart from that, there is a constructor and it also override
[07:28] the equals(), hashCode() and the toString() method on top of that, it also has a getter methods with the
[07:35] name, name and occupation.
[07:37] So these are all the list of elements that are going to be generated behind the scenes.
[07:41] To make our life easy.
[07:43] As a developer, I just have to create the Record class by using this syntax.
[07:47] So first you need to mention public followed by record keyword, followed by your class name.
[07:52] And inside the parentheses you can mention the list of your instance fields.
[07:56] So please note that these parentheses is only allowed if you are trying to mention the record keyword.
[08:02] For normal class, you will not be able to use these parentheses.
[08:06] For example, inside my Immutable class.
[08:09] If I try to mention these parentheses, I'm going to get a compilation error.
[08:13] I hope this is clear next time
[08:15] whenever you are trying to create an Immutable object inside a project, don't follow this lengthy approach
[08:21] instead, always go with the record approach.
[08:24] But please note that this feature is only available from Java 16, so this can be a good interview question
[08:30] as well.
[08:31] I hope you're clear.
[08:32] Let's try to continue the discussion around record in the next lecture as well.
[08:36] Thank you,
[08:37] bye.

----------------------------------------
