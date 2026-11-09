# 17.12 — Sorting ArrayList using sort() methods

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] When we try to store multiple objects or elements inside an Collection object, sometimes we may have
[00:07] requirement to sort them based upon ascending order or in a descending order.
[00:12] You might be storing simple primitive data type objects like Integer, String, Character, Double, Float,
[00:20] or you may also store complex data types like Person, Employee.
[00:25] Regardless of what kind of data that you're trying to store inside your Collection, object sorting
[00:29] is one of the common requirement that you may see inside your projects.
[00:33] That's why let's try to understand what are the options that we have to sort the elements inside an
[00:39] Collection object.
[00:40] To show you the demo of sorting, I'm going to create a new Java class inside the package
[00:47] com.eazybytes.List.
[00:48] The class name that I'm going to give here is SortingDemo. Inside this class,
[00:53] first we need to make sure we are creating the main() method post that I'm going to create an object of
[01:00] ArrayList, which is capable of storing the Integer objects.
[01:04] The variable name I'm going to mention as numbers followed by new ArrayList with the help of diamond
[01:11] operator.
[01:11] Now inside these numbers ArrayList object, I'm going to add few integer values for the same
[01:17] I'm going to paste few lines of code.
[01:19] You can see I have added multiple elements of type Integer.
[01:23] If I try to print out all these elements with the help of System.out.println(), and by passing these
[01:30] numbers as an input, I'm going to get the output in the same order of insertion that I have followed.
[01:36] But like I said, we need to look for options on how to sort these elements.
[01:41] There are multiple approaches.
[01:42] Let's try to understand what are those one by one.
[01:45] The very first approach is with the help of a static method available inside the Collections class.
[01:51] Inside this we have a sort() method.
[01:54] So there are two overloaded methods of sort().
[01:57] First, let's try to see the demo of very first sort() method which is going to accept the object of List.
[02:03] Here you can see I'm trying to pass the numbers object as an input to the sort() to static method, which
[02:09] is available inside the Collection class.
[02:11] So with this line of code behind the scenes, all the elements inside the same numbers object, they
[02:17] are going to be sorted in an ascending order after this line.
[02:22] If I try to print out all the numbers inside the Numbers Collection object, I will be able to see the
[02:28] output in an ascending order.
[02:30] You can see this is the original list.
[02:32] Later on, after the sorting is completed, you'll be able to see all the Integer elements
[02:37] they are sorted using ascending order.
[02:40] But what if you have a requirement to sort your elements in an descending order?
[02:46] The default order that is going to be followed by the collection framework is ascending order.
[02:51] If you want to follow that descending order, you need to invoke the same sort() method, but this time
[02:57] you should invoke the sort() method that is going to accept the two method input parameter.
[03:02] The very first input parameter is the Collection object itself, followed by
[03:06] you need to invoke the Comparator interface, and inside these we have a reverseOrder() method.
[03:13] You need to invoke the same with this extra input parameter, which is Comparator.reverseOrder().
[03:18] I'm telling to the collection, please sort my elements in an reverse order which is descending order.
[03:24] After this last statement, if I try to print out the numbers again this time, you should be able to
[03:29] see the numbers sorted in and descending order as a next step.
[03:34] This time, let's try to sort the list of String objects.
[03:37] As of now we are trying to use the numbers for sorting, so ascending order.
[03:42] Descending order for the numbers is very common.
[03:45] But coming to the Strings or Characters, you may have a question which is how the String objects are
[03:51] characters.
[03:51] They're going to be sorted all the String objects and the Character objects
[03:55] they are going to be sorted by using the lexicographically order we know inside English
[04:01] the very first letter is A, followed by B, followed by C, and it will continue till the end of the
[04:06] alphabetic letters using the same order
[04:09] A is going to be considered as the smallest compared to the B.
[04:13] Behind the scenes collections framework also is going to follow the same format or the same formula
[04:18] to sort the String objects or characters by using the Lexicographically order.
[04:24] So let me show you one demo on how to sort the String objects. For the same this time
[04:30] also, I'm going to create one more ArrayList object
[04:33] this time I'll use the var keyword and with the variable name as countries.
[04:38] And to this I'm going to assign the new ArrayList of type String.
[04:43] Inside this ArrayList object I'm going to store various country names like India, USA, Japan, France
[04:50] and Canada.
[04:51] If you try to print out all these elements without sorting whatever the order that you have followed,
[04:57] the same is going to be consider.
[04:59] While displaying these elements into the console, we should be able to sort the Countries object also
[05:06] by using the Collections.sort().
[05:07] So let me copy these lines of code and paste the same here.
[05:12] Instead of numbers, I'm going to pass countries in all the places so that we can see the output in
[05:18] the console.
[05:19] So you can see these are default insertion order.
[05:22] Later on when we try to sort based upon ascending order, you can see the very first character is C
[05:28] followed by F, followed by I, j and u.
[05:31] Whereas in the descending order, the very first element has the character as u, followed by j, I,
[05:38] f, and c.
[05:39] And here you may have a question which is what if two elements have the same first character?
[05:43] In those kind of scenarios, the Java collection framework is going to look at the second character.
[05:49] If all the characters in both the elements are same, then there won't be any sorting.
[05:53] The elements will be displayed next to each other, which is expected in any kind of sorting mechanism.
[05:59] So as of now, you can see we are trying to use the same approach, which is with the help of sort to
[06:04] static method available inside the Collection class.
[06:07] But there is one more approach
[06:09] let me show you the second approach.
[06:11] In the second approach, you can directly invoke the instance method available on top of your object.
[06:19] So the object here is Country.
[06:20] So on top of this I'm trying to invoke the sort() method.
[06:24] So whenever you are trying to invoke the sort() method using your List object, you need to make sure
[06:29] you are passing the comparator value as an input.
[06:32] So that's why after invoking the sort(), I need to invoke the Comparator followed by I need to invoke
[06:38] the method which is naturalOrder().
[06:40] So when we say naturalOrder, we are referring to the ascending order.
[06:44] The same kind of logic I can write by removing these line of code here.
[06:49] This time, instead of naturalOrder(), we are going to mention reverseOrder(), since we want to sort
[06:56] the country elements based upon the descending order.
[06:59] So let me execute this program and you'll be able to see the same output inside the console.
[07:05] So this is very simple data where we are trying to store numerical values and String objects.
[07:10] And we are simply invoking the sort() related methods available inside the JDK.
[07:15] But sometimes we may have some custom requirements to perform the sorting.
[07:19] So let's try to understand how to implement our own custom sorting requirements in the next lecture
[07:25] thank you,
[07:26] bye.

----------------------------------------
