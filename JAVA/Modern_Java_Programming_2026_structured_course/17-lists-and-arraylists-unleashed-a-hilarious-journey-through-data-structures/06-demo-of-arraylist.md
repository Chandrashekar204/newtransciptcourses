# 17.6 — Demo of ArrayList

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Now inside this lecture, let's try to add a few elements inside a ArrayList object.
[00:06] In the same process, we can try to explore many other methods supported by ArrayList.
[00:10] Think like I want to prepare a ArrayList object with the list of country names.
[00:16] So let me bring these country names to the last line.
[00:21] Now using these country names variable, I want to add multiple countries details, but before that
[00:27] I want to check what is the size of ArrayList object when we don't have any elements inside it for the
[00:35] same, using the country names variable, I'm invoking the method size.
[00:39] We know the purpose of size() method inside collection is to give the int value as an output, which
[00:45] represents number of elements that a given collection object has.
[00:49] So I'm trying to run this program, and you will be able to see zero inside the console because we just
[00:56] done only the initialization.
[00:58] But this time I'm going to add a new element inside my country names.
[01:03] So what is the method that we need to invoke.
[01:05] We need to invoke the add() method to this
[01:08] we can pass the element as an input.
[01:12] So if I try to pass a numerical value as an input, you can see we are getting a compilation error saying
[01:17] that required type is String
[01:19] but we are trying to provide int.
[01:21] So to resolve this issue we need to make sure we are sending the String object as an input.
[01:27] I will try to mention my country name as a very first country name.
[01:31] So it is India.
[01:32] You can try to mention your own country name in the similar lines.
[01:36] I'm also going to add few more countries.
[01:38] The second country that I want to add here is Canada, followed by I want to add USA as well.
[01:45] After the USA, I'm trying to mention Germany and at last I'll make sure I'm adding one more duplicate
[01:53] country name, which is India.
[01:55] I just wanted to show you the demo that ArrayList supports order of insertion and at the same time they
[02:00] also support storing duplicate values.
[02:03] After adding all the elements, I can try to print out the country names array list object and you'll
[02:10] be able to see the list of objects inside the ArrayList.
[02:14] You can see ArrayList is maintaining the same insertion order.
[02:18] At the zero index we have inserted India followed by Canada, followed by USA, Germany, and at last
[02:24] we have India, the country name India.
[02:26] We have mentioned at two different places, so it is a duplicate element
[02:31] still my ArrayList object
[02:33] it is storing it because we know any list implementation object.
[02:37] It is going to support duplicate values as well as a next step.
[02:41] What we can do is, we can try to explore other methods available as part of the ArrayList object.
[02:47] This time I'm going to invoke the add() method which is accepting two input values.
[02:54] The very first one is what is the index value followed by what is a country name?
[02:58] Maybe this time at the first index instead of Canada, I want to maintain another country name, which
[03:05] is France.
[03:06] So let me mention France as an element.
[03:09] After executing this program, you will be able to see that the array is adjusted based upon the new
[03:15] element that I'm trying to insert.
[03:17] So if I try to execute this program at the index one, we have France right now and all the elements
[03:23] like Canada, USA, Germany and India, they moved by one index.
[03:28] So right now Canada is available at the second index followed by 3, 4, 5.
[03:32] So these are purpose of add method which is going to accept the index value also as an input.
[03:39] Next I'm going to invoke the set() method.
[03:42] Using the set() method I'm going to replace one of the element.
[03:46] Maybe instead of Germany I can try to have Spain.
[03:49] So where is the Germany is going to be available.
[03:52] So we need to understand what is the index number of Germany.
[03:55] So this is 0, 1, 2, 3, 4.
[03:59] So it is available at the fourth index.
[04:01] That's why to this set() method I can pass the index number as four followed by Spain as a country name.
[04:08] Now if I try to execute this program this time you will not see Germany.
[04:13] The Germany is replaced with the Spain country name.
[04:16] We also have remove() method.
[04:18] Maybe what I can do is I can try to remove that duplicate India country name by using the index number.
[04:26] So here I need to pass the index number.
[04:29] The index number should be five I think like 0, 1, 2, 3, 4, 5.
[04:35] Yeah we are correct.
[04:36] We can try to mention five.
[04:38] So if I try to execute this program you will not see that duplicate India name.
[04:42] And the size of the ArrayList object also is reduced to five.
[04:46] As of now we are trying to invoke the remove() method by mentioning the index number.
[04:50] We also have other flavor of remove() method, which is going to accept the object itself as an input.
[04:56] So to this if I pass India as an
[05:00] object element.
[05:01] This is going to delete the very first occurrence of the given object.
[05:06] You can see the very first Indian object is deleted because if you try to read these documentation of
[05:13] this method, it is very clear removes the first occurrence of the specified element from the List.
[05:18] This way we can either remove an element using the index value, or we can remove based upon the element
[05:25] object.
[05:25] We also have removeAll() method, which is going to remove all the elements that you are trying to provide
[05:32] in an collection format.
[05:34] If you want to delete multiple elements at a single time, you can pass the array list object, which
[05:40] has the list of elements which you want to remove so that you can provide as an input to this method.
[05:46] For now, let's not try to remove multiple elements.
[05:48] That's why I'm simply rolling back to the previous method invocation, which is remove by passing the
[05:55] object element.
[05:56] Similarly, we also have get() method which is going to help us to get the element from a particular index
[06:03] or we can also get the element by invoking the getFirst() and getLast().
[06:09] So this getFirst() and getLast() methods are inherited from the SequencedCollection interface.
[06:15] So let me try to invoke the getFirst() method.
[06:18] And the return type of this method is going to be the type of the object that you have mentioned during
[06:24] the ArrayList declaration.
[06:26] Here I have mentioned the type of the object as String.
[06:28] That's why I need to make sure I'm mentioning the String as a data type.
[06:33] Whenever I'm trying to catch the element on the left hand side, on the left hand side, I'm trying
[06:38] to give a variable name as first element, followed by.
[06:41] I'll try to invoke the getLast() method as well, and on the left hand side I'll just mention the variable
[06:48] name as last element, and at last I'll also try to invoke the get() method with an index value, so I'll
[06:55] try to pass the index value as two.
[06:57] And here on the left hand side I'll just mention some random element.
[07:02] So if I try to keep a breakpoint here and try to execute this program, you'll be able to see.
[07:08] And at the first element we have an object name as France, followed by last element India.
[07:15] And the random element we have USA.
[07:17] You can also see the list of elements inside an ArrayList object by opening this at runtime, and you
[07:23] will be able to see the index number and what is the element is being stored.
[07:28] At the very first we have France.
[07:30] That's why we got the first element as France.
[07:32] And at last we also have India.
[07:34] At the second index we have USA.
[07:37] That's why the random element output we got as USA.
[07:41] I hope this makes sense to you.
[07:42] Let me release this breakpoint and at last I can also try to invoke the clear() method which will remove
[07:48] all the elements inside a ArrayList object.
[07:51] If I try to invoke this program by the end of this program, since we are trying to clear the country
[07:57] names inside the country names, you can see we don't have any elements and the size also became zero.
[08:02] So this confirms that the dynamic adjustment of the size is being taken care by the ArrayList at runtime,
[08:10] based upon the number of elements we are trying to add and we are trying to remove.
[08:14] Let me release this breakpoint and at the end you can see we have an empty ArrayList printed onto the
[08:20] console.
[08:20] This time instead of clear, let me invoke the reversed() method.
[08:24] But please note that whenever we are trying to invoke the reversed() method, it is not going to reverse
[08:29] the elements present inside the original ArrayList object.
[08:33] Instead, it is going to give the new ArrayList object as an output, and inside this new ArrayList
[08:39] object, we are going to have all the elements in an reversed order.
[08:43] So that's why whenever you are trying to invoke this reversed() method, please make sure you are catching
[08:48] the object on the left hand side by using List or ArrayList String as the data type and the variable
[08:56] name
[08:56] I'm going to mention reversedCountryNames at the end of the program, I can try to print out the
[09:04] ArrayList object with the name reversedCountryNames, so that we can validate whether the reversing is
[09:09] happening or not.
[09:10] Let me execute this program, and at the end you can see we have an ArrayList object in a reversed
[09:17] order.
[09:17] So the France went to at the end and India came to the very first place.
[09:22] So this confirms the reversing is also happening.
[09:26] And here I'm assuming you are seeing the beauty of SequencedCollection, which is introduced as part
[09:31] of Java 21 before Java 21 developers, they have to write a lot of complex logic to reverse the elements
[09:38] inside an ArrayList object, and at the same time, in order to get the first element, last element,
[09:43] they need to write some code.
[09:44] Now all this complexity is taken over by the JDK libraries itself.
[09:49] We as a Java developers, we simply have to invoke these methods and test them if they're working based
[09:55] upon our business requirements.
[09:57] So this way we can invoke any number
[09:59] of methods which are available inside the List and ArrayList object.
[10:04] We can see the demo of all of them, but throughout the course I will try to show you various methods
[10:09] demo as and when needed.
[10:11] Everything that we discuss around the ArrayList I have mentioned in these two slides, so please refer
[10:16] them if you have any questions.
[10:18] We are going to discuss more about the ArrayList in the coming lectures as well.
[10:22] I will show you how to iterate the elements inside an ArrayList object, how to sort the elements,
[10:27] all the advanced demos around the ArrayList we are going to see in the coming lectures.
[10:32] For now, I am assuming you are clear on how to create an object of our List and how to store the elements
[10:37] inside the ArrayList object, and how to invoke various methods with the help of ArrayList object.
[10:43] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
