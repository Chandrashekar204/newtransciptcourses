# 15.13 — Details about Shallow cloning & Deep cloning - Theory

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] In Java
[00:01] there are two types of cloning that we can perform.
[00:03] The very first one is Shallow cloning and the second one is Deep cloning.
[00:08] Let's try to understand what are these cloning and how they work.
[00:12] These are the very important topics.
[00:14] If you go to any Java related interviews, anyone can answer questions around the clone() method.
[00:20] But if someone wants to test your deep knowledge inside Java, they can ask some difficult questions
[00:26] around shallow cloning and deep cloning.
[00:28] That's why, my friend, my request is please pay attention and try to understand what is this
[00:34] Shallow cloning and Deep cloning.
[00:35] This shallow cloning and deep cloning only come into picture if a given object has some other embedded
[00:42] objects.
[00:43] In the previous lecture, we have a Person class, and inside this Person class we only have primitive
[00:49] data type instance fields along with that String object.
[00:52] Other than that, we don't have any other complex objects, but in real projects we always have embedded
[00:59] objects as an instance.
[01:01] Variables inside your own class, I'm going to show you what do I mean by embedded objects in few seconds.
[01:07] But before that, let's try to understand what is a shallow cloning.
[01:10] Whenever you're trying to perform cloning with the help of shallow cloning, it is going to create the
[01:15] new copy of your outer object only, but it is not going to create the copies of the embedded objects
[01:22] referenced by the original object.
[01:24] Instead, it is going to simply copy the reference of the embedded objects.
[01:29] For example, like you can see here, I have a Student class, and inside this Student class I have
[01:35] instance variables name and course.
[01:38] So this course is a instance variable which belongs to other class with the name course.
[01:44] So inside this course class I have another instance variable which is courseName.
[01:49] So with this code my Student class object it is going to have an embedded object of Course class.
[01:56] If you try to override the clone() method inside the Student class like you can see here, we simply override
[02:04] the clone() method and we are trying to invoke the clone() method with the help of super.clone().
[02:08] So this is a classical example of shallow cloning.
[02:12] So with this shallow cloning, what is going to happen behind the scenes inside the heap memory is you're
[02:17] going to have an original student.
[02:19] And if you try to clone this original student object, you're going to get another cloned student physical
[02:25] object.
[02:26] They both are stored in two different memory locations, but coming to the embedded objects, like course,
[02:32] both these original student object and the cloned student object, they are going to point to the same
[02:38] course object, because shallow cloning is not capable of copying the embedded objects.
[02:45] Instead, it simply copy the reference of the embedded objects into the objects of original student
[02:52] and the cloned student.
[02:53] This is because we are trying to go with the simple invocation of super.clone().
[02:58] With this, it should be pretty clear for you whenever your class has instance variables, which belongs
[03:03] to other class.
[03:04] In such scenarios, if you are going with the default logic of cloning, you are always going to end
[03:10] up with the shallow cloning.
[03:11] I can also show you an example of shallow cloning based upon these two classes,
[03:16] Student and Course.
[03:17] You can see here inside the main() method.
[03:19] First, I'm trying to create a Course with the variable name as math.
[03:23] Inside this math course, I'm trying to store the course name as math and post that I have created an
[03:29] original student by passing the student name and the course object later on
[03:34] if I try to perform the cloning with the help of original Student object, I'm going to get another
[03:40] object with the name cloned student.
[03:42] So both these original student and the cloned student, they represent two different physical objects.
[03:49] That's why if I try to compare the memory locations of these two objects with the help of these double
[03:54] equal to operator, I'm going to get the output as false because they point to the two different memory
[04:00] locations.
[04:00] Whereas if you try to check the memory location of the Course object which is present inside the original
[04:06] student and the cloned student, you're going to get the output as true, because the same course object
[04:12] is being maintained in both the original student and the cloned student object.
[04:18] I hope you are clear about the shallow cloning.
[04:20] Now let's try to understand what is deep cloning, which means whenever you want to copy the even the
[04:26] embedded objects, then in such scenarios, you need to override the clone() method with a different logic
[04:32] like you can see here
[04:33] first, I'm trying to invoke the super.clone() method, which is going to give me the cloned student
[04:39] object later on
[04:41] I should also perform the cloning of the Course object, which is available inside the same object.
[04:46] So that's why I'm trying to invoke the course.clone(), and the same I'm trying to assign to the
[04:52] clonedStudent.course().
[04:53] And with that, we will end up performing the deep cloning.
[04:57] And this is how it is going to look like inside the
[05:00] heap memory both the original student and the cloned student.
[05:03] They will point to the two different course objects.
[05:07] But before you try to perform this deep cloning, please make sure you also implement Clonable interface
[05:14] inside your Course class.
[05:16] On top of that, you should also overwrite the clone() method with the help of super.clone().
[05:21] Otherwise, when you invoke these clone() method with the help of Course object, you are going to get
[05:26] the CloneNotSupportedException.
[05:28] Let's try to understand the example of deep cloning like you can see here.
[05:32] When we try to perform the cloning of the original student, the student details along with the embedded
[05:38] course details, both of them, they are going to be copied into separate physical memories.
[05:44] That's why for these two statements, we are going to get the output as false because they are pointing
[05:49] to the two different memory locations.
[05:52] I hope you are clear about these theory discussion around the shallow cloning and deep cloning.
[05:57] In the next lecture, let's see the demo of these shallow cloning and deep cloning.
[06:02] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
