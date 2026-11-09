# 12.8 — Arrays advantages and disadvantages

> Section 12: Arrays in Java

[00:00] Let's try to understand what are the arrays advantages and disadvantages. Before we try to focus on
[00:07] advantages and disadvantages.
[00:09] First, we need to understand how arrays are stored behind the scenes
[00:14] inside memory.
[00:15] Whenever you try to create an array behind the scenes, all the elements of an array are stored continuously
[00:22] inside memory.
[00:23] What do you mean by continuously or consecutively?
[00:27] So let me show you an example.
[00:28] Think like I have declared an array which is going to store the int numbers.
[00:34] That's why I have defined that type of this array as int.
[00:37] So inside this you can see we have five different int values.
[00:41] So when these statement is being executed behind the scenes my JVM or Java
[00:47] they are going to look for a space where five continuous are consecutive memory locations are available.
[00:55] For example think like my JVM identified a space which is of type five continuous memory locations.
[01:02] The memory location
[01:04] they are going to start from 3415 to 3419.
[01:08] So this is just a random memory location value that I'm trying to mention here.
[01:13] So if you see all the contents of my array like 1, 2, 3, 4, 5 they are stored at
[01:20] the continuous memory locations.
[01:23] The behavior will not be the same if you try to create an array which is capable of storing an object
[01:30] of String or other custom data type.
[01:33] For example, think like I have an array which is capable of storing three different Person objects.
[01:40] In this scenario, whenever we try to create an Person object, we know it is going to be created inside
[01:46] the heap memory.
[01:47] If we end up creating three different Person objects, the same three different objects, they are going
[01:53] to be created at some random location inside the heap memory.
[01:58] For example, for each of the Person object, think like we have variable names as person1, person2
[02:05] person3.
[02:06] So these objects, they are not going to be physically stored inside my array.
[02:11] Instead, my array is going to store the object references in a continuous memory location like you
[02:18] can see.
[02:19] So this time my JVM or Java, they looked for an memory location which starts at 4016, followed by
[02:27] 4017.
[02:28] And at last we have 4018.
[02:30] At these three continuous memory locations, we are going to store object references of three different
[02:38] objects.
[02:39] So person1,
[02:40] person2,
[02:41] person3.
[02:41] When we try to access the very first element inside my array of persons behind the scenes, my Java
[02:49] at JVM, they are going to look for what this person1 is pointing to
[02:55] since this person1 is pointing to an physical object inside the heap
[03:00] memory, the same is going to be fetched, and on top of that we can do modifications or we can run
[03:06] some business logic.
[03:07] The main point that I want you to be aware here is, always inside arrays
[03:12] the elements are going to be stored in an continuous memory location of fixed length.
[03:20] So since we are going to give what is the length or size of an array during the initialization, my
[03:26] JVM at Java, they're going to look for the continuous memory location.
[03:30] So with this approach there are certain advantages and disadvantages.
[03:35] So let's try to understand what are those.
[03:37] The very first advantage or disadvantage that we have is around the size of the arrays.
[03:43] We know arrays in Java they are going to have a fixed size, which can be advantageous when you know
[03:50] the exact number of elements you need to store.
[03:53] If you know inside your business logic that you want an array to store five different person objects
[03:59] or five different String objects, then arrays is a great advantage.
[04:04] But in the scenarios where you are looking for a dynamic data structure that can grow or shrink during
[04:10] the runtime based upon the amount of data or the amount of elements you are trying to add or delete.
[04:16] So if you are looking for a dynamic data structure that can adjust automatically at runtime, then arrays
[04:23] is not an option.
[04:24] In this kind of scenarios where we are looking at dynamic data structure, we need to look for advanced
[04:30] options which are available inside the Java Collections framework.
[04:34] For example, we have a data structure with the name ArrayList
[04:38] inside the collection framework we can use the same, and when we are using the ArrayList, we don't
[04:43] have to mention any size during the initialization based upon how many elements we are trying to add
[04:49] or based upon how many elements we are trying to delete at runtime, the size is automatically going
[04:54] to grow or shrink based upon data manipulation, but for now, let's
[04:59] focus on address only.
[05:01] We're going to talk in detail about the collections framework in the coming sections.
[05:06] So please always use arrays only if you have a scenario where you know how many exact number of elements
[05:13] you're going to store.
[05:14] Since arrays have a fixed size, and since arrays store the elements in a continuous memory location,
[05:21] arrays provide a constant time access to the elements using their index.
[05:26] When I say constant time, the amount of time it is going to take to retrieve the first element, or
[05:33] to retrieve the 100th element, or to retrieve the 1000 element, or to retrieve the 10,000
[05:39] element inside your array is always going to be the same,. Because since all the elements are stored
[05:45] continuously inside the memory location, accessing them randomly is going to be super efficient.
[05:51] That's why whenever you are using arrays, random access operation of your elements is always going
[05:59] to be super fast and efficient.
[06:01] You can simply ask your array, I want the 1000 element or I want 9990 element.
[06:09] You can just ask and the array is going to give you very quickly.
[06:13] But coming to the insertion and deletion operations in the middle of the array, they can be inefficient
[06:20] or they can perform slowly inside arrays because in this kind of scenarios, the elements needs to be
[06:26] shifted in order to accommodate your new request for random insertion or random deletion LinkedList.
[06:34] They're always going to be super fast.
[06:37] So that's why based upon what is your business requirement, you need to choose the correct data structure.
[06:43] As of now we are simply focusing on arrays.
[06:45] So use these arrays when you have a requirement where you want to access the elements randomly, very
[06:51] fastly.
[06:52] On top of that, if you also have a requirement where you know the exact number of elements that you're
[06:58] going to store in these two kind of scenarios, you can happily use the arrays.
[07:03] Other than these two scenarios, if you have a requirement where you want to randomly insert an element
[07:08] or randomly delete an element inside an array, in such scenarios, you need to look for other data
[07:14] structures.
[07:15] We are going to discuss about all the other data structures available inside the collections framework
[07:20] in the coming sections.
[07:22] For now, let's focus on arrays only.
[07:24] Coming to the last point, arrays are memory efficient because elements are stored in contiguous memory
[07:32] locations, but in the scenarios where you're trying to create an array of large size, and if you don't
[07:38] populate the elements inside all the index, then in such scenarios you are going to waste a lot of
[07:45] memory.
[07:45] Think like I have created an array of persons which is capable of storing the thousand different Person
[07:53] objects.
[07:53] But if I end up storing only 200 or 300 Person objects at runtime, then the remaining space we are
[08:01] going to unnecessarily waste.
[08:03] Because inside arrays, regardless whether you are going to use it or not JVM, it is always going to
[08:09] look for an memory location that is available continuously.
[08:13] So the dynamic adjustment of the size is not going to happen in arrays.
[08:18] I hope you are clear with the arrays advantages and disadvantages and how they store that data.
[08:24] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
