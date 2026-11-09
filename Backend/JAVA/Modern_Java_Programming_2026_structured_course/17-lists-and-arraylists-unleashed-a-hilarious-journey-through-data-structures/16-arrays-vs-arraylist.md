# 17.16 — Arrays vs ArrayList

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] We are at the end of our discussion around ArrayList.
[00:04] We discussed good amount of topics around ArrayList.
[00:07] Before I try to close this lecture around the ArrayList, let me spend a few minutes explaining you
[00:12] about the differences between arrays and ArrayList.
[00:16] I know most of these points you already aware and we discussed in the previous lecture, but there is
[00:21] no harm revising one more time because this is a very important Java interview topic.
[00:27] The very first point is arrays
[00:30] they have a fixed size, they support only a static size, and they cannot be automatically resized.
[00:36] Whenever you want to change the size of an array, a new array must be created and all the elements
[00:42] of the old array needs to be copied over.
[00:44] But coming to the ArrayList, they can be resized dynamically at runtime based upon the number of elements
[00:51] that we are trying to add and remove.
[00:53] The second difference also revolves around the first point, which is memory allocation for arrays is
[01:00] static and contiguous, whereas inside the ArrayList memory allocation is going to be dynamic and the
[01:07] elements they are going to be stored in a contiguous locations.
[01:11] The reason why ArrayList also store the elements in an contiguous manner is behind the scenes
[01:17] ArrayList follows the array data structure only.
[01:20] The only advantage that it is providing is it can be dynamically resized based upon the elements that
[01:26] we are trying to add or remove.
[01:27] Moving on to the next difference.
[01:29] Using arrays, we can store either primitive data elements or objects, whereas with ArrayList or with
[01:36] any Collection object we can only hold the objects, but not the primitive data types.
[01:41] But there is a workaround to this.
[01:43] Whenever we try to store the primitive data type values behind the scenes, auto boxing is going to
[01:48] happen with the help of wrapper classes, and the wrapper objects are going to be stored inside the
[01:53] collections eventually.
[01:54] The last difference that we have here is, whenever we want to understand the how many elements that we
[02:00] have inside an array, we should invoke the length variable available inside array.
[02:05] Whereas with ArrayList, whenever we want to understand the number of elements stored inside an ArrayList
[02:11] object, we should invoke the size() method.
[02:14] Apart from this, we also have one more difference.
[02:16] But don't try to tell about this difference.
[02:18] This difference is whenever we are dealing with the arrays, we use the square brackets.
[02:23] Whereas with ArrayList we are going to use the angle brackets.
[02:27] Not only ArrayList any Collection object that we are going to create, we are going to use the angle
[02:32] brackets.
[02:33] I hope you are clear with these differences.
[02:35] As a next step, let me explain you about how to convert an array into an ArrayList and ArrayList
[02:41] into an Array, because many times in real projects, you may have these kind of requirements to convert
[02:47] a given Array into an ArrayList, or to convert a given ArrayList object into an Array.
[02:53] But these kind of scenarios we have helper methods inside the JDK library like you can see here.
[02:59] First, I have a ArrayList object with the name country names.
[03:03] If I want to convert these country names ArrayList object into an Array, I just have to invoke the
[03:08] toArray() method with the help of ArrayList object.
[03:11] But if you are looking to convert an array into an ArrayList object or into an List object, you can
[03:18] always invoke the static method as List available inside the Arrays class.
[03:24] So this countrys array is going to be converted into a new List object.
[03:29] Let me show you the demo around this, so that it is going to be clear for you.
[03:33] Inside my project, I'm going to create a new Java class and the class name I'll just mention as a
[03:40] ArrayVsArrayList.
[03:42] I know this name looks very weird, but I just wanted to give some meaningful name here. Inside these
[03:49] class,
[03:50] first we need to create the main() method and inside the main() method,
[03:53] first let me try to create an ArrayList object.
[03:56] You can see I have created an ArrayList object with the name countryNames. Inside these countryNames,
[04:01] I'm trying to add various country names like India, Canada, USA, Germany and India.
[04:07] So first let me teach you on how to convert an ArrayList object into an Array.
[04:13] Like I said before, using the ArrayList object, we should be able to invoke the toArray() method.
[04:19] So if you try to invoke these toArray() method on the left hand side, we will be able to catch the
[04:25] output with the help of an array.
[04:28] So array name I'm going to mention as countries.
[04:31] With that you're going to get a compilation error
[04:33] saying that these two are eight is going to give the output in the form of Object[] array, but we are
[04:39] trying to store them inside an array that is going to store the String elements.
[04:43] So it is asking to perform the casting.
[04:46] So we can resolve this error by providing the new array object as an input to this method.
[04:52] Inside this new array object, we want to convert all the elements and the same
[04:56] we want to assign to these left hand side array variable.
[04:59] So how to create a new object of array
[05:01] we just have to mention new followed by String and after the String we need to mention the square brackets
[05:08] and inside the square brackets.
[05:09] I need to tell the size of my array. So how I can know the size of my array.
[05:14] It should be same as the size of my ArrayList object.
[05:17] So that's why I'm going to mention countryNames.size().
[05:20] With that we have our array ready.
[05:23] I can try to print out with the help of Arrays.toString() and to this toString() method I can pass
[05:32] the country's array name.
[05:33] So if I try to execute this method, you can see this is my array which I have created based upon my
[05:40] ArrayList object.
[05:41] In the similar lines, you may also have vice versa.
[05:44] Requirements like to convert your array into an ArrayList object.
[05:49] So this is going to be also easy.
[05:51] First you need to invoke the arrays class which is available inside the java.util package.
[05:57] Inside this class we need to invoke the static method which is as List.
[06:01] To this we need to pass your array object.
[06:05] So what is our array object
[06:06] it is countries. On the left hand side,
[06:08] we can try to catch the object with the data type as String, and with the variable name as new List.
[06:16] So now if I try to print out these new List, I'll be able to see the elements again inside my List
[06:24] object.
[06:24] So you can see here.
[06:25] This is my array and this is my List
[06:28] both of them
[06:29] they have the same kind of elements this way.
[06:32] Always use these two methods based upon your requirements toArray()
[06:36] method is going to help you to convert a List object into an Array.
[06:41] Similarly, as a List method available inside Arrays class, it is going to help you to convert your
[06:47] array into an List object.
[06:49] I hope this is clear to you.
[06:50] Before I try to close this lecture and this section, I want to spend few minutes explaining you about
[06:57] the Vector.
[06:58] So Vector inside Java collection framework is very similar to the ArrayList.
[07:04] So you can see it also implementing List and the same kind of interfaces and abstract classes.
[07:10] So this is going to work similar to the ArrayList.
[07:13] The way you create the object, the way you add the elements, the way you iterate, the way you sort
[07:18] the elements.
[07:19] So everything is going to work very similar to the ArrayList.
[07:23] But with that you may have a question, which is why Java team
[07:27] they provided two different data structure implementations like ArrayLists and Vector if they work
[07:32] in a very similar manner.
[07:34] The reason for this is Vector data structure is multithreading safe, whereas ArrayList object or
[07:42] ArrayList data structure is not safe
[07:45] for multithreading environment. All the code that is returned inside this Vector class is handled with
[07:52] the help of synchronization logic.
[07:54] So inside multithreading environment there is a concept called synchronization.
[07:59] This is going to make more sense to you when we start discussing about the multithreading in the coming
[08:04] sections.
[08:04] For now, please note that if you are working on a multithreading environment and you are trying to
[08:10] build a business logic which is going to be executed by multiple threads at a time, you should always
[08:16] consider Vector.
[08:17] Otherwise you can always go with the ArrayList.
[08:20] Most of the time these days developers, they are not writing multithreading code.
[08:24] With that assumption, you can always happily use the ArrayList.
[08:27] But if you have a some specific or rare scenario around the multithreading, then feel free to use the
[08:33] Vector to store your elements.
[08:35] Since Vector has a lot of logic to handle the multithreading issues, the performance of vector is going
[08:42] to be less compared to the ArrayList array.
[08:46] List is going to work very fast compared to the Vector.
[08:49] So that's why by default always prefer to use ArrayList until
[08:53] unless you have some special scenario around multithreading, then you can use the Vector the same I
[08:58] have highlighted around the Vector data structure inside this slide for your reference.
[09:03] If you are coming from the C++ background, then this vector may look very similar to what you
[09:09] have learned inside your C++.
[09:12] But inside Java, like I said, always prefer ArrayList because it is the most commonly used and it
[09:18] is going to have some performance advantages compared to the Vector.
[09:21] I hope it is clear
[09:22] finally, we are done discussing everything around the ArrayList.
[09:26] I'm super happy right now.
[09:28] We can conclude this section.
[09:30] Let's take a break and I'm going to catch you in the next section.
[09:33] Thank you,
[09:34] bye.


########################################
