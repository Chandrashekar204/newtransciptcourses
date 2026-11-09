# 17.15 — Sorting ArrayList of custom data type using Comparator

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Inside this lecture, let's try to understand how to perform the custom data type sorting with the help
[00:05] of our own comparator.
[00:07] In the previous lecture, we tried to do the sorting of the student objects with the help of these comparable
[00:13] interface.
[00:14] So whenever we are trying to deal with the comparable interface, we need to override the compare to
[00:19] method inside the same class which we are trying to sort.
[00:23] Whereas with comparator we can write the comparison logic outside of our domain class or outside of
[00:30] the class, which we are trying to sort as a next step, what I'm going to do is I'm going to create
[00:35] a Java class with the name Student Comparator.
[00:39] Inside this class, I need to make sure I'm implementing the comparator interface, the data type,
[00:45] to this comparator.
[00:46] I need to pass student and post that.
[00:49] We are going to get a compilation error to override the compare method, let me implement the compare
[00:56] method.
[00:56] So whenever we are trying to implement the comparator and try to override the compare method, like
[01:02] you can see, it is going to expect two different objects as an input.
[01:07] That's why we have the compare method, whereas with the comparable we are going to override the compare
[01:13] to method, we want to compare our existing object with the other object.
[01:17] That's why this compare two method makes more sense here.
[01:21] And it is also going to accept single object as an input, because we already hold the other objects
[01:28] in the form of this keyword.
[01:30] I hope this makes sense.
[01:32] Now inside this compare method I need to write the same logic.
[01:36] So let me copy this logic and paste it here.
[01:40] But here I can't use these this dot marks because right now we are in a different class.
[01:46] That's why instead of that we need to use these 0101 indicates object one followed by 0202 indicates
[01:54] object two.
[01:55] The same kind of changes I have to do here as well.
[01:58] Let me try to mention 01. roll number followed by 02. roll number.
[02:03] That's it.
[02:04] We are done defining our own comparator as a next step I can use this comparator when I'm trying to
[02:10] sort my student object.
[02:12] Let me go to the student sorting demo here.
[02:14] I'm going to copy all this code and paste it again and override this variable name to students one followed
[02:21] by I'm going to replace student one variable name in all the subsequent code.
[02:27] Now I have two different ArrayList objects holding the same kind of data.
[02:32] So this is the very first approach where we are trying to compare with the help of comparable interface.
[02:38] The second approach that I want to show here is with the help of comparator.
[02:41] Whenever you are trying to use a comparator, you have two options.
[02:45] One is by invoking the static method, which is sort inside the collection class.
[02:51] To this sort method, first we need to pass what is the object name, which is student one, followed
[02:57] by what is the object of our comparator, which is new student comparator.
[03:03] So this is the very first option.
[03:05] The second option is you can directly invoke the sort method on top of students one object, and whenever
[03:12] you are invoking the sort method, you need to pass your comparator object with the help of this new
[03:18] student comparator.
[03:20] So these are the two options that you can follow whenever you have your own comparator.
[03:24] Whereas if you are going with the comparable option, you need to use the static method available inside
[03:31] the collection, which is sort.
[03:33] Here I'm going to comment these one of the approach, because we don't have to perform the sorting multiple
[03:38] times.
[03:39] Suppose that I'm going to print out the students one object content so that I can validate the output.
[03:47] Let me execute this program.
[03:48] You can see the sorting is done in an ascending order based upon the marks followed by rule number.
[03:54] This confirms the output from the comparator and comparable is always same, only the approaches are
[04:00] different.
[04:01] With these explanations you may have $1 million question, which is when to use the comparator approach
[04:08] and when to use the comparable approach.
[04:11] Let me share more details around this.
[04:13] It depends upon the scenario that you are into.
[04:16] Sometimes you may want to maintain your comparison logic inside your same domain class which you are
[04:22] trying to sort.
[04:23] So in such scenarios, you can happily implement comparable interface and override these compared to
[04:30] method and write your own logic.
[04:32] But in real projects, sometimes these domain objects will be provided by some other team members,
[04:38] or will be provided by some other organizations.
[04:41] In those scenarios, you will not have flexibility to change the content of your domain classes or the
[04:47] custom data type classes.
[04:49] In all these kind of scenarios, you can write the comparison logic outside of your domain class or
[04:55] the custom data type with the help of comparator.
[04:58] So here you can see all the logic is present outside of my student class.
[05:03] And one more difference between these comparable and comparator is whenever you are following the comparator
[05:09] approach, you can build as many comparators as you want and you can pass them under various scenarios.
[05:16] For example, I can create one more comparator, which is going to strictly follow the marks details
[05:22] as an sorting criteria.
[05:24] So whenever I want to perform the sorting based upon only the marks, I can create one more comparator
[05:29] and pass the same object as an input to the sort method.
[05:33] Whereas with the comparable approach you will not be having multiple options.
[05:37] Let me show you a demo around this so that it is going to more clear for you.
[05:41] Maybe what I can do is I will try to copy these student comparator inside the same package and rename
[05:47] this class name to student Mark comparator.
[05:50] So inside this class I'm going to perform the comparison based upon only the marks.
[05:56] So what I can do is I can remove all these logic and just simply return the output that I'm going to
[06:04] get based upon the comparison of the two student marks.
[06:07] Details.
[06:08] So this is the second comparator I have created.
[06:11] Similarly, I can create any number of comparators based upon the student name, based upon the roll
[06:16] number.
[06:17] All these comparators which I have created, I can use at various places in various methods and various
[06:23] classes based upon my own business requirement.
[06:26] Whenever I'm trying to perform the sorting of the student objects here inside the student sorting demo.
[06:32] As of now, we are trying to use the student comparator, which will sort the student objects based
[06:38] upon the marks and their roll number.
[06:40] This time, if I try to mention the student mark comparator object as an input, definitely the student
[06:47] objects details are going to be sorted based upon their marks.
[06:51] You can see here 9292, followed by 97, followed by 99.
[06:57] This way comparator has some advantages compared to comparable.
[07:02] So based upon your scenario, you can always choose one of the best option that works for you.
[07:07] There is no wrong and right here.
[07:09] If you have a flexibility of defining your comparison logic inside your own domain class or inside your
[07:16] own custom data type, then feel free to implement comparable and override the method.
[07:21] Why to create one more extra class inside your project.
[07:24] But please note that with this approach, you will be able to perform the comparison or sorting based
[07:29] upon a single logic.
[07:31] Whereas if you have a requirement where you want to perform the sorting based on multiple parameters
[07:36] under different scenarios, then you can create multiple comparator implementation classes for your
[07:43] custom data type class, and you can write multiple comparison logic inside all these comparators,
[07:49] and based upon your own requirement, you can create the corresponding object whenever you are trying
[07:55] to invoke the sort method.
[07:57] We discussed a lot around the sorting of elements inside an ArrayList.
[08:01] All these details I have mentioned in these slides for your reference, so please refer them.
[08:07] How to perform the sorting based upon the various concepts that we have discussed.
[08:12] And at last I also have a slide comparing between comparable and comparator.
[08:17] Here I have a request for you which is.
[08:20] Please read all the slides very quickly one time.
[08:22] So that concept of sorting inside collections is going to be super clear for you.
[08:27] Thank you.
[08:27] And I'll catch you in the next lecture.
[08:29] Bye.

----------------------------------------
