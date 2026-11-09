# 18.5 — Iterate LinkedList elements

> Section 18: LinkedLists - Java's Dance of Nodes

[00:00] Inside this lecture, let me show you how to iterate the LinkedList elements.
[00:05] There are three different approaches that we discussed as part of ArrayList.
[00:08] The same approaches we can use with linked list as well.
[00:12] I would request you to pass the video and try to write the iteration logic of LinkedList with your
[00:19] own logic.
[00:20] Otherwise you can simply follow my discussion to show you the demo of LinkedList iteration.
[00:25] I'm going to create a new Java class with the name LinkedList iteration. Inside this class,
[00:32] first, let me create the main() method post that I'm going to copy the code related to creating the LinkedList
[00:39] object with the name countryNames along with these add() related logic.
[00:44] So let me copy these and paste inside my main() method.
[00:47] The very first approach is with the help of for each.
[00:51] So let me type for loop inside these parentheses.
[00:54] First I'm going to mention the temporary variable name for each country, so I'll just mention countryName
[01:00] followed by colon
[01:02] and after the colon I'm going to mention countryNames.
[01:05] And inside these for each loop we can try to print out each element.
[01:11] Maybe this time I'll try to print out each country name in an uppercase letter.
[01:16] So I just have to invoke the toUppercase() method with the help of the String variable that I have,
[01:22] which is country name.
[01:23] So if I try to execute this program, you'll be able to see the country names in the same order that
[01:28] we have inserted.
[01:29] But the country names are getting printed using uppercase letters.
[01:33] In the similar lines
[01:34] we can also try to use the iterator.
[01:37] So whenever you want to use the iterator, first you need to make sure you are invoking the iterator()
[01:44] method with the help of LinkedList object.
[01:47] On the left hand side, you need to make sure you are catching the Iterator object by mentioning the
[01:54] element data type as String and variable name as iterator.
[01:58] Using these Iterator object, I can try to write the while block, and whenever we are trying to write
[02:04] the while block, we need to invoke the hasNext() method to validate if there is any next element available
[02:11] inside my LinkedList object.
[02:14] If there is an element, then we need to make sure we are invoking the next() method available inside
[02:20] the iterator.
[02:22] And after that I'm going to print out the countryNames.
[02:26] This time maybe we can print out in an lower case values.
[02:30] So let me execute this program and you'll be able to see all my country names in an lower case letters.
[02:36] So this confirms the iterator is also working with the LinkedList object.
[02:41] But we know iterator has some drawback compared to ListIterator.
[02:45] Iterator can only navigate to a LinkedList element in an forward direction, but not in the reverse
[02:51] direction.
[02:52] On top of that, whenever you are using Iterator, we can only remove the element with the help of Iterator
[02:58] object. Whereas when we use the ListIterator, we can navigate the elements either in the forward
[03:03] or the reverse direction.
[03:05] On top of that, we should be able to add the elements, remove the elements, replace the elements,
[03:10] read the elements.
[03:12] So all kind of operations we can try to perform whenever we are using the ListIterator.
[03:18] But please use the ListIterator only whenever you need it, because it is going to come with an performance
[03:24] cost.
[03:25] To show you the demo of ListIterator, I can copy all this code related to Iterator and paste it inside
[03:31] the same method.
[03:32] This time instead of iterator() method, I'm going to invoke the listIterator() method.
[03:36] On the left hand side, I'm going to replace Iterator with ListIterator and the variable name
[03:43] also, I'm going to mention as ListIterator.
[03:45] So using this ListIterator I'm going to perform as
[03:48] next check.
[03:49] If this condition is met, then I'm going to invoke the next() method.
[03:53] So this time what I can do is, I can try to print out my country names without changing anything.
[04:00] So whatever we stored inside the LinkedList, the same country names is going to be displayed.
[04:05] Here
[04:05] we are trying to access the elements in an forward direction, but if needed, like I said, we can
[04:11] also access the elements in an reversed direction with the help of the methods like hasPrevious() and
[04:18] previous().
[04:19] But please make sure whenever you are invoking this hasPrevious() and previous() methods.
[04:24] You need to make sure at least you traveled in forward direction by one element.
[04:29] Otherwise you're always going to get the hasPrevious() output as false because there is no previous element
[04:36] when your ListIterator cursor is pointing to the very first element inside your LinkedList.
[04:41] So let me execute this program and we'll be able to see all our country names the first in the forward
[04:48] direction, followed by in the reverse direction.
[04:51] I hope this makes sense to you.
[04:52] Did you see all the code is working very similar to ArrayList.
[04:57] The same is applicable for the sorting as well in.
[05:00] Inside the next lecture, let's try to see the demo of LinkedList sorting.
[05:04] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
