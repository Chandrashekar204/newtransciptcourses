# 17.10 — Iterate ArrayList using for-each and iterator()

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] When you are dealing with the ArrayList of objects, or any other List objects, one of the primary
[00:05] requirements that you may have on day to day basis is processing the elements inside the ArrayList
[00:11] object or inside the List object.
[00:13] That's why it is very important to understand what are the various options that we have to iterate the
[00:19] list of elements inside a Collection object.
[00:22] There are three most commonly used different approaches.
[00:25] I'll try to show you all of them one by one.
[00:27] The very first approach is with the help of for each loop.
[00:31] That's why I'm trying to mention the class name as ArrayListForEachExample.
[00:37] So this is the class name inside this class
[00:39] first, as usual, we need to create the main() method post that
[00:43] inside this main() method, I want to create a ArrayList object that is capable of storing various String
[00:49] objects. For the same,
[00:51] let me go to the ArrayListDemo here
[00:53] we already have a code related to creating an ArrayList object and storing various country names,
[00:59] so let me copy these code and paste it inside the ArrayListForEachExample class.
[01:06] First, let me remove this String data type because we don't need to mention on the right hand side
[01:11] if we are already mentioning on the left hand side this is called diamond operator, which we already
[01:16] discussed previously.
[01:17] Post creating these ArrayList object I'm trying to add various country names into my ArrayList like
[01:23] India, Canada, USA, Germany and India.
[01:26] The process of iterating the elements with the help of for each is very similar to what we have done
[01:33] with the arrays.
[01:34] We just have to mention for and inside the for
[01:38] we need to mention colon and to the left hand side of the colon
[01:41] we just need to mention what is the data type of your element which is String.
[01:45] And after that we can give a variable name which is going to act as a temporary variable name for each
[01:51] element that we are going to iterate with the help of
[01:54] for each loop. And after the colon, we need to provide
[01:57] what is your List object name
[01:59] or ArrayList object name.
[02:01] It is going to be country names, and inside this for loop we can write any kind of processing logic
[02:07] it can be converting your country names into and capital letters
[02:12] or it can be simply printing and country name.
[02:14] The business logic can be anything, but I just wanted you to understand the process that you need to
[02:20] follow to iterate the elements of an List object.
[02:22] So here I'll just go with the simple business logic, which is to display the each element that is available
[02:28] inside my ArrayList.
[02:29] So if I try to execute this program, you will be able to see the list of countries that I have printed.
[02:35] The elements are going to be printed based upon the same order that we have inserted.
[02:40] On top of that, duplicate elements are also going to be allowed inside ArrayList.
[02:45] That's why we're able to see this India as a very first element and the last element.
[02:50] So these are very first approach which is the basic approach.
[02:53] Now let's go to the second approach.
[02:56] For the same I'm going to create a new class.
[02:59] The class name I'm going to mention as ArrayListIteratorExample.
[03:04] .
[03:05] Inside this class let me copy the code that we have inside this
[03:09] ArrayListForEachExample. I'm going to copy the entire main() method here instead of for each loop
[03:15] this time I'm going to use the iterator.
[03:18] So whenever you want to use the iterator to iterate the elements of your Collection object, first using
[03:23] the Collection object which is country names, you need to invoke the iterator() method.
[03:29] This iterator() method is available inside the List.
[03:32] It is going to give the Iterator as an output, which is capable of iterating a given data type elements.
[03:41] That's why on the left hand side, I need to make sure I'm catching the output with the help of iterator
[03:47] and mentioning the element data type, which is String.
[03:50] And after that I'm going to give the name to my iterator, which is iterator itself.
[03:55] This is just like a variable name.
[03:58] Now using these iterator I can invoke various methods to identify whether I have the next element to
[04:06] invoke with the help of hasNext().
[04:08] And similarly, whenever I want to fetch the next element inside the iterator, I need to invoke this
[04:13] next() method.
[04:14] So whenever you are trying to use this iterator, you have to use the while block
[04:19] using the while block
[04:20] first, we need to make sure to define a condition which is iterator.hasNext().
[04:26] So this condition is going to check during the each iteration whether your iterator has any element
[04:32] in the next index.
[04:34] If there is an element, then only the logic inside the while loop is going to be executed.
[04:38] So inside my while loop I can try to fetch the element with the help of next() method.
[04:45] But before that, let me try to create a variable country and invoke the next() method post that I can
[04:51] try to print out the country details.
[04:54] If I try to execute this program, you can see I'm going to get the same output here.
[04:58] You may have a question which
[04:59] is if for each also capable of doing the same.
[05:02] Then why should I use the iterator and why should I use these hasNext() and fetching the element manually
[05:09] with the help of
[05:10] next().
[05:10] I agree with your question.
[05:12] It's a great question.
[05:13] Whenever you have a simple requirement just to iterate your elements, you can happily go with the for
[05:18] each loop.
[05:19] But compared to for each loop, iterator has one more advantage, which is with the help of iterator.
[05:25] You can remove the element inside your List at runtime.
[05:30] For example, here, if you try to remove with the help of like countryNames.remove() and providing
[05:37] these country name as an input.
[05:39] In this kind of scenario, you're going to get a runtime exception.
[05:42] Let me confirm you that by running the program you can see we are getting ConcurrentModificationException.
[05:48] So this exception you're going to get while you are trying to iterate.
[05:52] And at the same time you are trying to delete or modify the elements inside your ArrayList object.
[05:58] But there is a workaround to remove the elements with the help of iterator.
[06:02] What you can do is you can invoke the remove() method with the help of iterator.
[06:08] So here I can mention iterator.remove().
[06:11] Maybe what I can do is I can write a condition, which is if country.equals() India I'm going to invoke
[06:20] the iterator.remove().
[06:21] This if condition is capable of removing the element if it is matching with the name India,
[06:28] maybe what I can do is to prove you that the element is removed outside the while loop.
[06:34] I can try to print out the ArrayList object with the name countryNames.
[06:38] So if I try to execute this program this time, I'm not going to get any runtime exception.
[06:43] You can see first I have displayed all the elements and after the while loop is executed my ArrayList
[06:49] object.
[06:50] It has only three countries and all the elements with the name India are removed.
[06:55] So these are great advantages that we are getting inside the iterator compared to the for each loop.
[07:01] Apart from removing, we can't perform any other operations like if you try to look for the list of
[07:07] methods inside the Iterator, there is only a remove option, but I cannot invoke other methods like
[07:13] add(), so there are no option.
[07:15] That means Iterator is only going to support only the reading operation and the remove operation.
[07:22] You can't add and modify at runtime with the help of Iterator object.
[07:27] So these are second approach.
[07:29] In the next lecture, let's try to understand the third approach and why it is better than second approach
[07:35] which is iterator approach.
[07:37] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
