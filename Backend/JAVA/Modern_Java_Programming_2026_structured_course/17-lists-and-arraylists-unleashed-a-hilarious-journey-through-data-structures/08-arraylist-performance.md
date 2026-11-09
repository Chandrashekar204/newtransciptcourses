# 17.8 — ArrayList performance

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Performance is the important parameter that you need to consider whenever you are trying to select a
[00:06] particular data structure available inside the Java Collections framework. Based upon your business scenario,
[00:13] you may need to select various data structures available inside the Java Collection framework.
[00:18] That's why inside this lecture, let's try to understand under which scenarios ArrayList is going to
[00:24] perform better and under which scenarios.
[00:26] It is going to cry a lot to understand about the ArrayList performance.
[00:31] First, let's try to consider an ArrayList example like you can see here I'm trying to create an object
[00:37] of ArrayList, and this ArrayList object is capable of storing the Integer objects or int wrapper
[00:44] objects.
[00:45] You can see here with the help of add() method I'm trying to add various int values like one, two, three,
[00:51] four.
[00:52] And here if you can recall, I'm not doing any boxing.
[00:56] Like I'm not trying to convert this primitive data type values into a wrapper object.
[01:00] But behind the scenes, the auto boxing is taking care of converting my primitive data type values into
[01:07] the Integer wrapper objects.
[01:09] I hope you remembered the wrapper classes discussion that we have done previously.
[01:13] So based upon the data that I am trying to add, this is how the data is going to store inside the memory
[01:20] location.
[01:21] So at the zero index the value one is going to be stored followed by two, three and four.
[01:27] ArrayList is going to store the data very similar to array which means ArrayList also is going to
[01:33] store all your elements in an contiguous locations.
[01:37] With this clarity, let's try to understand how various operations is going to work inside the
[01:44] ArrayList.
[01:44] First let's try to talk about random access operations.
[01:48] So what do I mean by random access operation?
[01:51] Using random access operations, I want to randomly access any element inside my ArrayList object.
[01:58] So in this kind of operations, whenever you are trying to randomly fetch an element or randomly set
[02:04] an element inside an ArrayList object, it is going to work super fast.
[02:09] You're always going to have a constant time, regardless whether you're trying to fetch the first element
[02:15] or the thousand element or the 1 million element inside your ArrayList object, it is always going
[02:22] to have same time to fetch the element, or to set the element at a random given index location.
[02:29] Do you know the reason why the random access operation is always going to have a constant time, and
[02:35] why it is going to work super fast?
[02:37] It's very simple.
[02:38] If you try to think about it, think like you have 1000 elements inside your ArrayList object.
[02:44] If you are asking for the 999 element behind the scenes, Java is not going to look for each and every
[02:52] index location.
[02:53] Instead, from the first index, it will try to jump directly into the 999 location by adding zero plus
[03:01] 999, and with that, the memory location is going to be jammed very quickly.
[03:07] The same applies even if you try to access a random location like 666.
[03:11] Think like right now, the cursor inside your ArrayList object is present at the second index from
[03:17] the second index.
[03:17] If you want to jump to the 666 index, it's very easy.
[03:21] Just have to add 664 to this index, and with that it will easily jump into the corresponding index
[03:28] location.
[03:29] That's why the main reason why random access operation is fast inside the ArrayList is all your elements.
[03:36] They are stored in an contiguous locations or in an contiguous memory locations.
[03:42] So always whenever you are looking to read a lot of information, or whenever you have some business
[03:48] logic which is going to perform a lot of invocations around the get() method and set() the method, you
[03:55] can happily use the ArrayList object.
[03:58] Now let's try to understand how this ArrayList is going to perform around the insertion and removal
[04:04] of the element.
[04:05] As of now, we are only trying to read the data randomly or trying to set the element randomly, but
[04:12] the story is going to be different in the add and remove scenarios.
[04:15] Let's try to understand the same here.
[04:18] I'm trying to add a new element at the location, our index one.
[04:23] So when I'm trying to add I'm not trying to replace.
[04:26] Instead I want to introduce a new element at a given index.
[04:30] So when I'm trying to add a new element at a given index, what should happen to the existing value
[04:35] at the same location?
[04:36] We can't delete it.
[04:37] Instead, the shifting of that element to the right hand side is going to happen.
[04:42] So if you try to understand with an example, you can see initially we have this kind of ArrayList
[04:47] object inside the memory location.
[04:49] Since we want to add five at the index number one, whatever element that we have previously at the
[04:56] index number one, it is going to be replaced with the five and at the
[04:59] same time
[05:00] the previous elements like two, three, four, which are available at the index one and two three,
[05:06] they are all going to be right shifted by one index value.
[05:11] So if you see here just to add one element to our ArrayList object, the shifting operation of all
[05:18] the remaining elements has to happen.
[05:20] Think like your ArrayList object has 1 million element objects in this kind of scenarios.
[05:26] Definitely, if you try to randomly add an element at an index location like 5 or 10, all the subsequent
[05:33] elements, they have to shift by one index.
[05:36] And since the shifting has to happen for all the elements after the five index, it is going to impact
[05:43] the performance of your ArrayList object. In the similar lines
[05:47] if you try to understand the remove scenario, think like I'm trying to remove an element present at
[05:53] the index location.
[05:54] Three in this scenario, you can see initially this is how my ArrayList used to be
[05:59] look like.
[05:59] If I'm trying to delete the element at the third index, whatever elements that we have after this third
[06:06] index, they need to move to the left hand side by one index, because inside ArrayList, the way the
[06:13] elements are going to be stored is in an contiguous or in an contiguous memory locations.
[06:19] So that's why whenever you are trying to do the addition and remove operation inside your ArrayList
[06:25] object, the performance is going to be less.
[06:29] If you are dealing with 100 object or 1000 objects, you may not see much impact.
[06:33] But if you are trying to deal lakhs and millions of objects, then always in such scenarios don't go
[06:40] for the ArrayList object.
[06:42] If your business logic is going to do a lot of addition and removal operations for the addition and
[06:48] removal operation, we should always use the brother of ArrayList which is LinkedList.
[06:53] LinkedList will have its own advantages and disadvantages, which we are going to discuss in the coming
[06:58] lectures.
[06:59] For now, I'm assuming it is pretty clear for you if your code is doing a lot of random access operations
[07:05] to read an element, or to set an element in those scenarios, always prefer ArrayList.
[07:10] But if your code is going to do a lot of add() and remove() elements, then obviously the recommendation
[07:16] is to go with the LinkedList, because array list cry a lot while you're trying to perform addition
[07:22] and remove.
[07:23] So whatever I'm trying to say this performance impact you will be able to see only when you try to store
[07:29] thousands or lakhs or millions of elements inside your ArrayList object.
[07:34] If you are just dealing with ten objects or anything less than 1000, it should not have any great impact.
[07:40] You will not see any performance issues.
[07:43] You can happily use any kind of collection object.
[07:46] I hope you are clear around the ArrayList performance.
[07:49] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
