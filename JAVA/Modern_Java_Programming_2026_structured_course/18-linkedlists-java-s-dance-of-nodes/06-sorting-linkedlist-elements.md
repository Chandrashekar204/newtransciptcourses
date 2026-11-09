# 18.6 — Sorting LinkedList elements

> Section 18: LinkedLists - Java's Dance of Nodes

[00:00] Let's try to understand how to perform sorting.
[00:03] Whenever we are storing elements inside a LinkedList object.
[00:07] This is going to be very similar to the ArrayList.
[00:09] That's why to make this explanation super fast, I'm not going to type the code.
[00:14] Instead, I'm going to copy all the code that we have developed in the previous section by using the
[00:19] ArrayList inside the GitHub repo.
[00:21] You can see under the section_17 we have a class name with the name SortingDemo.
[00:27] I'm going to create the same class inside my section_18 as well.
[00:32] So here inside my section_18 and at the package I'm going to create a new Java class with the name as
[00:40] SortingDemo.
[00:42] Inside this class I'm going to copy all the code that we have inside the GitHub repo.
[00:47] Here you can try to copy all the content and paste it inside this new class that we have created inside
[00:55] the section_18.
[00:56] So here all the code we have with respect to the ArrayList.
[01:00] So let's try to change all this code to LinkedList.
[01:03] So here instead of ArrayList I need to mention LinkedList.
[01:07] And here also I'll change the comment from ArrayList to LinkedList, followed by
[01:12] we're trying to add some random numbers.
[01:15] Post that we are trying to print them, and after printing the numbers, we are trying to perform
[01:20] the sorting with the help of Collections.sort() method, the sort static method available inside the Collection,
[01:26] it is going to perform the sorting in an ascending order.
[01:30] So to perform using descending order, we need to make sure we are passing two input parameters to the
[01:36] sort() method.
[01:36] One is what is your Collection object?
[01:39] It can be an ArrayList object, or it can be a LinkedList object.
[01:42] And under the second input parameter you need to invoke these reverse order with the help of these Comparator
[01:49] interface.
[01:49] So this is approach one.
[01:51] The second approach is you can invoke the sort() method directly on top of your LinkedList object.
[01:57] But before we try to explore this code, let me replace this ArrayList with LinkedList.
[02:03] After that LinkedList inside the angle brackets, we need to mention the data type as String.
[02:08] So now my countries is going to act as a LinkedList object.
[02:11] And inside this LinkedList object we are trying to store various country names and we are trying to
[02:16] print the same with this statement.
[02:17] After this System.out.println() statement, we are trying to invoke the instance method with the help
[02:24] of LinkedList object which is countries.
[02:27] And to this I'm trying to pass the input parameter by invoking the naturalOrder() method
[02:32] with the help of Comparator. Post search, we are trying to print the same, and at last I'm trying to
[02:38] invoke the reverseOrder() method of the Comparator interface to perform the sorting in and descending
[02:43] order.
[02:43] So this should give a confidence to you that there is no change compared to the ArrayList, even inside
[02:49] the LinkedList.
[02:50] In terms of sorting
[02:51] now let's try to understand how to perform the custom sorting by defining our own custom Comparator
[02:58] implementation class.
[02:59] Here we have a variable name with the name countries1 which is of type ArrayList object.
[03:04] I can try to replace this with LinkedList post that when we are trying to invoke the sort() to static
[03:10] method of Collections class, we need to make sure we are passing the object of our custom Comparator
[03:16] class.
[03:17] So as of now this class is missing in inside my project.
[03:20] So let me try to create this class with the name as LastCharComparator.
[03:25] Inside this class, we need to make sure we are implementing the Comparator.
[03:30] And after the interface name I need to mention the data type as String.
[03:34] With that, we are going to get an error to override the method.
[03:38] Let me hover on this compilation error and select these implement methods and override the compare() method.
[03:45] Inside these compare() method, I'm going to write the same logic that we have written during the
[03:50] ArrayList discussion.
[03:51] I'll try to copy the logic from the GitHub repo under this LastCharComparator.
[03:57] We have this logic which is we are trying to fetch the last char from both the Strings and the chars
[04:04] we are trying to compare with the help of these compare() method available inside the Character wrapper
[04:10] class.
[04:10] Here you can see the lastchar2 is the first parameter and the lastchar1 is the second parameter.
[04:16] That means the sorting is going to happen in an descending order.
[04:20] Let's try to use this inside our SortingDemo class.
[04:23] So here you can see we are trying to create the object of LastCharComparator with the new operator
[04:29] if needed
[04:29] instead of the static method.
[04:31] You can also invoke the instance method by using the LinkedList object and to the same
[04:36] you can try to pass the object of LastCharComparator.
[04:40] So let me execute this program and you'll be able to see the output.
[04:44] This is the initial data that we stored inside the LinkedList.
[04:47] And later on after the sorting in an ascending order, this is how it is going to look like followed
[04:52] by descending order sorting followed by these the LinkedList object with the countryNames without
[04:58] any sorting after
[04:59] this we have the ascending order sorting output followed by descending order output, and this is the
[05:07] output from the custom comparator that we have written. Like we have written LastCharComparator to
[05:13] perform the sorting in and descending order by considering the last char.
[05:17] So here you can see we have n, e, a, capital A.
[05:22] So this confirms all the sorting logic also working in a very similar manner inside LinkedList as well.
[05:29] I'm not going to show you the demo on how to store the Student objects inside a LinkedList, and how
[05:35] to sort the Student objects based upon their marks and rollNumber, because the same code that we have
[05:40] discussed as part of ArrayList is going to work very similarly here as well.
[05:45] Regardless whether you are going to use the Comparator approach or Comparable approach, it is going
[05:50] to work very similarly to ArrayList.
[05:52] So my humble request is please try to implement the same sorting logic using ArrayList object.
[05:59] So try to create some Student objects and try to store them inside a LinkedList object and post that
[06:05] try to sort them with the help of Comparable and Comparator interfaces.
[06:09] I hope this makes sense to you.
[06:10] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
