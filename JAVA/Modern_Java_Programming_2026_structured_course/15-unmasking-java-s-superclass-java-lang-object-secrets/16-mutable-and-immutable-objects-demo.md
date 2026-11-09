# 15.16 — Mutable and Immutable objects - Demo

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] First, let me try to create a mutable Person object. For the same
[00:05] I'm going to create a new Java class.
[00:08] The class name is going to be MutablePerson inside this class
[00:13] first, we need to create the instance variables with the help of private access modifier.
[00:19] As a standard, we should not allow other classes and their methods to directly access our instance
[00:25] variables.
[00:26] Instead, they should always access our fields with the help of getter method, and similarly they can
[00:31] use the setter method to update the data.
[00:34] So that's why we need to create the instance fields with the help of private access modifier.
[00:40] The first field I'm trying to create here is name, followed by
[00:44] I'm going to create one more variable which is occupation.
[00:49] After this, we can try to create the constructor with the help of generate option and selecting this
[00:55] constructor and post that you can select both the fields.
[00:58] And with that you're going to get a constructor inside your class, followed by
[01:03] we can try to generate the getter and setter methods.
[01:07] So you can see there is nothing new that I'm trying to do here.
[01:09] It's a simple normal Java Pojo object.
[01:12] So whenever you try to build a class by using the same standards that I'm trying to follow here, you
[01:19] will end up creating a class that is going to allow building the mutable objects.
[01:24] As a next step, I can try to create a new Java class, the Java class name I'm going to mention as
[01:31] MutableDemo. Inside this class
[01:34] first I'm going to create the main() method, followed by
[01:37] I'm going to create the object of MutablePerson with the help of constructor available inside the
[01:45] MutablePerson class to the constructor, I can pass the name, which is John, followed by occupation.
[01:51] I can mention as software engineer.
[01:55] You can see at this point of time, while we are trying to create the object, we are trying to assign
[02:00] the occupation as software engineer and the name as John.
[02:03] That's why if I try to print out the occupation details of this person, I will get the software engineer
[02:11] as an output.
[02:12] Let me try to execute this program.
[02:14] You will be able to see the software engineer.
[02:16] But now, like I said, since this is a mutable object, we should be able to update that data even
[02:23] once the object is created.
[02:25] So let me try to update the occupation details by using the same MutablePerson object.
[02:31] So this time I'm going to invoke the setOccupation() method.
[02:35] And to this I'm going to pass the occupation as doctor.
[02:39] So whenever I see this code, I recall my teenage days
[02:43] during my teenage days, every one month, I used to have different goal of becoming a doctor, or becoming
[02:50] a pilot or becoming a software engineer.
[02:52] So my goals, they used to change a lot during teenage.
[02:55] I'm assuming it might have happened for you as well.
[02:59] The same is happening right now because we have created the mutable object.
[03:03] Initially the person occupation is software engineer, but later on we changed the person occupation
[03:10] to doctor.
[03:10] So that's why this time if I try to print out the occupation details, I'm going to get the output as
[03:16] doctor.
[03:16] So you can see first we have the software engineer followed by doctor.
[03:20] So this is how you can build the classes that are going to allow you to build the mutable objects.
[03:26] As a next step, I'm going to copy the MutablePerson class inside the same package, but I will rename
[03:33] this to ImmutablePerson.
[03:36] So let me create this class.
[03:37] Later on we can try to make the class as final, followed by
[03:43] I need to mention the final before my instance variables as well.
[03:47] After this you can see we are getting an error inside the setter methods, because inside the setter
[03:52] methods we are trying to modify them.
[03:54] That's why we need to remove them.
[03:56] And with that, no one will be able to update the data inside my immutable object.
[04:03] You can see it is very easy to create a class that will allow to build only immutable objects.
[04:09] Let's see that demo of ImmutableObjects as well.
[04:13] For the same, I'm going to copy this MutableDemo into the same package and rename this to ImmutableDemo
[04:20] .
[04:21] Post that inside the main() method, I'm going to create the object of ImmutablePerson and the object
[04:28] reference name
[04:29] also, I'm going to mention as ImmutablePerson.
[04:32] This time you can see with the help of this ImmutablePerson object reference, there is no option for
[04:38] me to change the occupation or the name by any means.
[04:43] That means there is no way for me to modify the data inside this object once it is successfully created.
[04:51] So this is how you can build the immutable objects inside Java.
[04:56] So now these objects I can send to any layer of my backend
[05:00] or even I can send to other methods inside another classes, and I can be pretty confident that no one
[05:07] can be able to modify the data inside my ImmutableObject.
[05:11] I hope you are clear with this demo.
[05:13] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
