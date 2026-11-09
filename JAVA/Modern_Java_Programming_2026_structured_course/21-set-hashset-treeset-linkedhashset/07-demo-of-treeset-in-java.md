# 21.7 — Demo of TreeSet in Java

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] In the previous lectures, we discussed about HashSet, which is one of the most commonly used Set implementations
[00:07] inside real projects. But has it has some drawbacks or limitations
[00:13] one such limitation is whenever we store elements with the help of HashSet object, we cannot perform
[00:19] the sorting.
[00:20] That's why whenever you have a two primary requirements, one needs to store unique elements and the
[00:26] other one needs to store them in a sorted manner.
[00:29] In such scenarios, you can use the TreeSet.
[00:33] So this is another implementation of Set which is greatly inspired by TreeMap we know HashSet inspired
[00:40] from HashMap.
[00:42] Similarly tree set inspired from that TreeMap.
[00:45] Internally it is going to store the data in the form of TreeMap we discussed in the previous sections.
[00:51] TreeMap guarantees the sorting order by storing all the elements with the help of red black tree implementation.
[00:58] So let's try to understand more details about these tree set like you can see here,
[01:03] TreeSet is a collection that store elements in a sorted and ascending or natural order by default.
[01:10] So by default this tree set it is going to use the Comparable interface and the compareTo() method to
[01:17] perform the natural ordering.
[01:19] But if you are looking to perform sorting based upon your custom requirements, then you can define
[01:24] your own comparator implementation and the same can be passed as an input to the constructor of the
[01:30] TreeSet.
[01:30] Since the TreeSet is going to leverage the Comparable and Comparator interfaces to perform the sorting,
[01:37] the null elements are not allowed to store inside the object of TreeSet.
[01:42] So this is the hierarchy of the TreeSet at the top we have Set interface.
[01:47] The same is extended by SortedSet, followed by NavigableSet, and all these interfaces.
[01:52] They are implemented by TreeSet class.
[01:55] The important methods inside TreeSet are add to add a element clear to clear all the elements contains.
[02:02] To check if the specified element is present inside that TreeSet or not.
[02:06] Since the elements are sorted inside the TreeSet, we have some helper methods like first and last
[02:12] to get the first element and the last element, since by default the tree set is going to perform the
[02:19] sorting based upon the ascending order.
[02:21] When you invoke the first method, you are going to get the lowest element.
[02:24] Similarly, for the last method, you're going to get the highest element, and using the remove() method,
[02:30] we can remove the specified element from the TreeSet, and with the help of size, we can return the
[02:35] number of elements inside the TreeSet.
[02:38] Let's see the demo of this tree set by writing a Java program inside IntelliJ.
[02:42] Before we try to see the demo, first let's try to see what is there inside that TreeSet.java class.
[02:48] So this is the documentation
[02:50] and it says it's a NavigableSet implementation based upon a TreeMap.
[02:55] The elements are ordered using their natural ordering or by a comparator provided at a Set creation
[03:02] time depending on which constructor is used.
[03:05] So if you can scroll down, you will be able to see the class definition like
[03:09] this class extends the AbstractSet class and it is also implementing so and so interfaces.
[03:15] The interesting point that I want you to understand here is, if you can open the constructor of the
[03:22] TreeSet, you'll be able to see that whenever we are invoking these default constructor, a new object of
[03:28] TreeMap is going to be created.
[03:30] This conforms behind the scenes,
[03:32] the TreeSet
[03:33] it is going to leverage TreeMap.
[03:35] That is how it is going to achieve the sorting order of the elements by leveraging the red black tree
[03:41] approach.
[03:42] If you can scroll down, you'll be able to see other constructors as well.
[03:46] Whenever you want to pass your own sorting logic with an Comparator, you can pass your Comparator object
[03:52] as an input to this constructor.
[03:53] The same is going to be used to perform the sorting.
[03:56] Otherwise, the default comparable sorting logic is going to be leveraged.
[04:01] So let's see the demo of this TreeSet. For the same,
[04:04] I'm going to create a new Java class with the name TreeSetDemo. Inside this class,
[04:11] first let me create the main() method, followed by
[04:14] I'm going to create the object of TreeSet.
[04:16] For the same,
[04:17] I can mention TreeSet or Set
[04:20] I can mention var as well, but here
[04:22] this time let me mention the TreeSet itself and inside the angle brackets I can mention String.
[04:29] Since I want to store String data type elements inside my TreeSet object the variable name.
[04:34] I'll just keep it as TreeSet only, and on the right hand side I'm going to mention new TreeSet with
[04:40] a diamond operator.
[04:42] Here I'm trying to invoke the default constructor.
[04:44] That means I want to perform the comparison by the default Comparable.
[04:49] Here I'm trying to store the String data type elements.
[04:52] If you can open the String, you will be able to see that these class implementing the Comparable interface.
[04:58] That's why inside
[05:00] this class, you'll be able to see there is a method which is comparedTo().
[05:04] Inside this method only we have the logic on how to compare two different String objects.
[05:09] So using this logic only the sorting is going to happen inside my TreeSet object.
[05:14] Now to this TreeSet object I'm going to add the elements.
[05:18] The very first element I'll add here is India which is the country name followed by I'll try to add
[05:25] another country which is USA, followed by Germany.
[05:29] So first let's try to print out these TreeSet with the help of System.out.println().
[05:36] If I execute this program, you'll be able to see the output in an default ascending order.
[05:42] The letter G comes first, followed by I followed by u.
[05:46] So this output confirms that my elements are sorted based upon the default natural ordering or ascending
[05:53] order.
[05:54] Let's see that demo of few other methods that we can invoke whenever we are using the TreeSet.
[05:59] This time I'm going to invoke the remove() method and with the help of remove() method, I'm going to remove
[06:05] the country Germany from my TreeSet object.
[06:09] I can also confirm whether the removal is successful or not by using a System.out.println().
[06:15] And inside this I'm going to have a statement which is TreeSet after removal.
[06:22] After this statement, I'll just mention colon followed by space and to the same.
[06:26] I'm going to append that TreeSet object.
[06:29] With that we'll be able to see the what elements right now we have inside the TreeSet.
[06:34] After the removal, you can see we have India and USA in an ascending order.
[06:40] Similarly, we can invoke the size() method to know the size of our TreeSet object.
[06:45] What I can do here is with the help of System.out.println(), I can try to print out the size details
[06:51] by invoking the size() method with the help of TreeSet object.
[06:55] Here I'll try to change the statement to size of TreeSet.
[06:59] So if I execute this program, I'll be able to see the size which is two because Germany is removed
[07:05] as part of our business logic.
[07:08] Similarly, we can also use the contains() method to check whether a given element is present inside your
[07:14] TreeSet. This time
[07:15] also, I can try to copy the System.out.println() and try to update these statement to ease India present
[07:24] in TreeSet.
[07:25] So to confirm the same, I need to invoke the contains() method and to this contains() method
[07:31] I need to pass the element as India and we are going to get the output as true because as of now my
[07:38] TreeSet object, it has the element India.
[07:40] That's why we are getting the output as true.
[07:42] At last, let me show you the demo of the first and the last methods that you can invoke to get the
[07:47] first and last elements inside your TreeSet object. For the same,
[07:51] let me copy the System.out.println() statement and change this statement to first element of TreeSet
[07:59] to display the first element, I need to invoke the first() method.
[08:04] Similarly, to get the last element, I need to invoke the last() method.
[08:10] So if I execute this program, I'll be able to see what is the first element which is India, followed
[08:15] by what is the last element which is USA.
[08:17] Since TreeSet always guarantees the same order, we can use the SequencedSet related methods as
[08:24] well.
[08:25] For example, here, with the help of this TreeSet, I'll be able to invoke reversed() method to reverse
[08:31] the element.
[08:32] Similarly, I'll be able to invoke the addFirst() method to add the element at the first location and
[08:39] addLast().
[08:40] So this kind of SequencedCollection related methods.
[08:43] I can use them happily, because my TreeSet object is always going to maintain the same order.
[08:49] Even if you try to look at these TreeSet class definition, you will be able to see that it is implementing
[08:55] an interface NavigableSet and this Navigable interface
[08:59] it is extending SortedSet and this SortedSet it is extending another interfaces like Set and
[09:06] SequencedSet.
[09:06] So if you can open the SequencedSet it is extending the SequencedCollection.
[09:11] Under this we have so many methods using which we can perform the operations related to the boundary
[09:18] elements like first andLast().
[09:19] And we can also use these reverse() method to reverse the elements inside a
[09:23] TreeSet.
[09:24] I hope this makes sense to you.
[09:26] The sample program that we discussed, I have mentioned in this slide for your reference along with
[09:30] the actual output, please refer the same for any questions.
[09:34] You can also find this code inside the GitHub repo as well.
[09:38] Feel free to refer to the GitHub or to this slide.
[09:41] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
