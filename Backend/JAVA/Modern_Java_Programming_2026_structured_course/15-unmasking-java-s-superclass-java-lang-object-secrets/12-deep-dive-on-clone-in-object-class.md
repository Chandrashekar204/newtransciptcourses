# 15.12 — Deep dive on clone() in Object class

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Now let's try to discuss about an interesting method available inside the Object
[00:05] superclass.
[00:06] The method is clone(). In layman language or in non-technical language
[00:11] clone is a process of making a copy from a original.
[00:15] So the same definition you can consider even for Java cloning process as well.
[00:21] Why do we need a clone() method inside Java?
[00:23] Because inside Java, there is no automatic mechanism for cloning an object or creating a copy of an
[00:30] object.
[00:31] With the help of this clone() method, we should be able to easily create a copy of an given object.
[00:37] And here you may have a question which is
[00:39] as of now, we are able to assign a object to other object reference with the help of is equal to operator.
[00:47] But I want to highlight an important note here.
[00:50] Whenever you are trying to assign an object to another object to a variable with the help of is equal
[00:56] to operator.
[00:57] In that scenario, you're not going to physically copy the data from one object to other object.
[01:03] Instead, the same physical object is going to be referred by two different object reference variables.
[01:10] Let me show you a demo around this very quickly.
[01:13] Here inside my package, I'm going to create a Java class with the name CloneDemo.
[01:19] Inside this class, as usual, first we need to write the main() method to execute our program.
[01:25] Post that, I'm going to create a person p1 object by invoking the constructor, and to this constructor
[01:33] I can pass data like John, followed by 25, followed by gender, which is Madan at last I can also
[01:41] mention his ssn number.
[01:44] Let me type some random SSN number.
[01:47] So these are random SSN number.
[01:49] With this code, a Person object is going to be physically created behind the scenes inside the heap
[01:55] memory.
[01:56] With the data that we are trying to provide the same Person object, memory, location is going to be
[02:01] pointed with the help of these p1 object reference variable.
[02:06] As a next step, I can try to assign the object to p1 to another object to reference variable, which
[02:14] is p2.
[02:15] With this, you might be under the assumption that we are able to copy the p1 object into the p2 object,
[02:23] the reference variable, but this is not going to copy the p1 object into the p2 reference variable.
[02:29] Instead, they both point to the same physical Person object present inside the same memory location.
[02:37] I can also confirm you this by writing a small logic.
[02:40] Think like I'm trying to change the name of the person with the help of p2.setName().
[02:47] And here I'm trying to change the name to John Doe.
[02:51] Later on, I'm going to print the name of the person using the p1.getName().
[02:58] You can see the change happened inside the p2, but the same change is going to be reflected inside
[03:04] the p1 object as well.
[03:05] The reason is both the p1 and p2 objects.
[03:08] They are pointing to the same object inside the same memory location.
[03:12] Let me try to execute this program.
[03:14] You can see we are getting the output as John Doe, so there is no direct automatic mechanism inside
[03:20] Java to physically copy the contents of an object from one object to other object.
[03:26] So to efficiently copy an object into another object, we have clone() method.
[03:30] So let's try to understand how to use the same to copy an object to enable cloning of an object belong
[03:36] to a class.
[03:37] First we need to manually re-implement the clone() method within the class.
[03:42] For example, if you want to clone the objects of Person, then inside the Person class, you need to
[03:48] override the clone() method. So that whenever someone is trying to clone() the Person object, whatever overridden
[03:55] clone() method that you have written inside your class, the same is going to be invoked. By default.
[04:00] the clone() method that is provided by the Object class.
[04:03] It is going to have all the logic that is required to clone an object physically.
[04:09] So all the logic of cloning is going to be written in the native code format.
[04:13] That's why we are able to see the native keyword inside the method signature of clone.
[04:18] As a developer, you just have to override this clone() method, and from your clone() method, you need
[04:24] to invoke the clone() method in the superclass
[04:27] with the help of super.clone(), you're not going to take the responsibility of copying the content by
[04:33] writing your own code.
[04:35] Instead, you just have to invoke the clone() method available inside the Object of super class from your
[04:41] own class.
[04:42] The actual copying process is going to be taken care by the Java library.
[04:47] Apart from overriding this clone() method inside your Person class or inside your any other class, you
[04:54] should also take care of implementing a Marker interface which is Clonable.
[04:59] What is a Marker interface?
[05:01] Marker interface is an empty interface, which is not going to have any body inside the interface.
[05:06] The purpose of this Marker interface is to communicate about a special information, or about a metadata
[05:12] information to the JVM.
[05:14] With the help of Clonable Marker interface, we are communicating to the JVM.
[05:19] Please allow the cloning of my objects belongs to a given class.
[05:24] If you don't implement this Clonable Marker interface inside your Person class, and if you try to perform
[05:29] the cloning with the overridden method that you have implemented, in such cases, you are going to
[05:35] get the CloneNotSupportedException.
[05:37] Since these CloneNotSupportedException is a checkered exception.
[05:41] Whenever you are trying to perform the cloning process, you need to either handle these checkered exception
[05:47] with that try and catch block, or you can propagate the exception by using the throw keyword.
[05:53] I hope you're clear.
[05:54] Let's try to implement these clone() method inside our Person class.
[05:59] Inside our Person class, I'm going to mention override annotation followed by public, and the return
[06:05] type from this method is going to be object, and the method name has to be clone followed by throws
[06:12] CloneNotSupportedException.
[06:15] So inside these method I need to invoke super.clone() method and the return type from the
[06:23] super.clone() method.
[06:23] I can return from these method as well, which I'm trying to override.
[06:28] With this, we have implemented our own clone() method inside the Person.
[06:32] As a next step, let me try to do the cloning process inside the CloneDemo class.
[06:37] This time I'm going to create Person Object reference variable, which is p3 to this p3 object reference
[06:45] variable.
[06:46] I'm going to assign the return type that I'm going to get from the clone() method, which I'm trying to
[06:52] invoke with the help of p1.
[06:53] With this code, whatever data that we have inside the p1, the same is going to be copied into the
[06:59] p3, and they both will point to the two different objects inside the memory location as well.
[07:05] We are getting a error saying that we have not handled the CloneNotSupportedException.
[07:11] Like I said before, since this is a checked exception, we need to either handle it with the help of
[07:16] try block, or we can simply add throws statement to the method signature.
[07:20] For now, let's try to add exception to the method signature with the help of throws, and with that,
[07:26] the compilation error related to the checked exception is resolved.
[07:29] But we still have one more compilation error, which is the casting from object to person is not allowed
[07:35] by default.
[07:36] We are going to do the casting manually by mention person inside the parenthesis.
[07:43] As a next step, I can try to print out what do I have inside my p3.getName(), followed by
[07:51] I'm going to change the name inside the p3 object to some different name like Will Smith.
[07:58] And after that I'm going to print the name present inside the p1 followed by p3.
[08:05] So this is going to give a confirmation to you that both p1 and p3, they are pointing to that two different
[08:12] objects.
[08:13] So let me execute this program.
[08:14] You can see we are getting a runtime exception which is CloneNot SupportedException.
[08:19] The reason is inside our Person class we have not implemented the Marker interface which is Clonable.
[08:26] So let me try to implement the same.
[08:29] Once I implemented this interface, we should be good this time.
[08:32] They should not be any exceptions.
[08:34] And you can see we got the output.
[08:36] So initially the name inside the p3 is John Doe.
[08:39] Later on I have changed this to Will Smith.
[08:41] That's why when I am printing the p3.getName(), I'm getting the output as Will Smith, whereas the
[08:47] name present inside the p1 object, it is not affected in any way.
[08:52] The reason is both p1 and p3 are two different objects.
[08:56] This way we can try to perform cloning with the help of clone() method.
[09:01] Believe me, in real projects there will be some situations where you want to create a copy of an object.
[09:07] Because creating an object sometimes require a lot of efforts.
[09:11] You may need to write a lot of code.
[09:12] Instead of doing that, you can simply rely on the clone() method, which is going to give an exact copy
[09:17] of your object in a different memory location in the form of different object.
[09:23] I hope you are clear about the initial discussion that we have done around the cloning process, but
[09:28] there is more to discuss about the cloning which which we are going to discuss in the next few lectures
[09:33] as well.
[09:33] Thank you, and I'll catch you in the next lecture, bye.

----------------------------------------
