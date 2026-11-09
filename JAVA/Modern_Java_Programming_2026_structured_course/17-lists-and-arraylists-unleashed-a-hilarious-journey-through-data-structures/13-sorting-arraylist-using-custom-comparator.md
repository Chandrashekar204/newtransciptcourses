# 17.13 — Sorting ArrayList using custom Comparator

> Section 17: Lists and ArrayLists Unleashed – A Hilarious Journey through Data Structures

[00:00] Let's think like I have a my own custom requirement to perform the sorting.
[00:05] For example, think like these countries that we have inside these countries ArrayList object.
[00:09] I want to sort them based upon their last char value.
[00:13] So here the last char value is a, here capital A, here and here E and here a.
[00:19] So based upon these last char value I want to perform the sorting.
[00:23] So for these kind of custom requirements we can't use the two approaches that we discussed previously
[00:28] with the help of this naturalOrder() and reverseOrder().
[00:31] Because how do we communicate to the JDK library about our custom requirements.
[00:37] That's why these two approaches we can't use them for any custom sorting requirements.
[00:41] So whenever you have these kind of custom sorting requirements, first you need to make sure you are
[00:46] creating your own comparator interface implementation class.
[00:51] Here inside my project, I'm going to create a new Java class.
[00:55] I'll mention this class name as LastCharComparator, inside this class, like we discussed, we need
[01:02] to implement the interface which is Comparator.
[01:06] Since we are going to sort the String data objects, we need to make sure we are mentioning the String
[01:11] data type as a element inside the angle brackets of Comparator.
[01:15] If you open this Comparator interface, it is going to expect what is a data type objects that you are
[01:21] trying to sort.
[01:22] That's why inside the angle brackets we need to mention that String as a data type, because the country's
[01:28] ArrayList object that we have created, it is using the String data type the same we need to mention
[01:33] inside the Comparator angle brackets as well.
[01:36] As soon as you try to implement this Comparator interface, you are going to get an compilation error
[01:42] saying that we need to override the abstract method with the name compare().
[01:46] So let me click on these implement methods and implement these compare() method.
[01:52] So you can see that Javadoc comments are also copied.
[01:55] Let me remove all of them for now.
[01:57] We don't need them and post that
[01:59] you can see I got a default implementation logic inside this compare() method.
[02:04] So the purpose of these compare() method is we need to write our own logic, how the JDK or how the Java.
[02:12] It has to compare two string elements inside your collection.
[02:16] Inside our collection we have various String elements like total.
[02:20] We have five different String elements.
[02:22] Behind the scenes, whenever we are trying to invoke the sort() methods, it is going to compare each
[02:27] and every element with the other elements, and it will keep comparing till the entire sorting is completed.
[02:34] Since right now we have our own custom sorting requirements, we need to mention that inside this compare()
[02:40] method, the same is going to be leveraged by the JDK library inside this method.
[02:45] First, let me get the last char value from the object to one.
[02:50] So here using o1, I'm going to invoke the method which is charAt(), and to this I will pass the index
[02:57] as o1.length()-1.
[03:01] Similarly, let me try to get the last char value present inside the second String object.
[03:07] So here instead of o1, I need to mention o2.
[03:10] And similarly here also I need to mention o2.length().
[03:13] So now I have last char one and last char two.
[03:16] So based upon these last char values I want to perform the sorting.
[03:19] If you closely look at these compare() method return type, it is going to return the Integer value.
[03:25] So let's try to understand what is this inter value conveys by opening the Comparator and looking at
[03:31] the compare() method documentation. Here if you closely look, returns a negative integer, zero or positive
[03:39] integer as the first argument is less than, equal to or greater than second.
[03:44] So what is this statement conveying to us?
[03:46] So this statement is conveying that our compare() method should return a negative value.
[03:52] It can be -1 or it can be any other negative value.
[03:56] It should return this negative value.
[03:58] If your first object is less than the second object.
[04:02] If both the objects content is same, we need to return the output as zero
[04:06] otherwise, if the first object content is greater than the second object content, we need to send
[04:12] the positive number like one.
[04:14] So right now we are trying to perform the comparison based upon these last char values.
[04:19] So what I can do here is I can invoke the wrapper class of char which is Character.
[04:25] And inside this I have a compare() method. To this compare() method,
[04:28] I can pass lastChar1 and lastChar2 as an input.
[04:34] So if I try to open this compare(), you'll be able to see the value zero is going to be returned if both
[04:40] char are same.
[04:41] Otherwise, if x less than y is a negative number is going to be returned, whereas if x is greater
[04:47] than y, I'm going to get a positive number.
[04:50] The same matches with the compare() method expectations as well.
[04:54] So with this we're trying to convey our own custom sorting logic.
[04:58] Now as a next step I need
[04:59] to use this Comparator while I am trying to perform the sorting of my ArrayList object.
[05:04] So what I can do is I can go to the sorting demo, and here I can try to copy the same ArrayList object.
[05:12] But this time I'll give the variable name as countries1.
[05:16] So the same countries1 I'm going to use in all the remaining places.
[05:21] So right now I have a brand new ArrayList object.
[05:24] Now as a next step, let's try to perform the custom sorting based upon our own comparator.
[05:29] So what I can do is I can use the same countries1 variable name and using the same I can invoke the
[05:36] instance() method which is sort() and you can see sort() method.
[05:40] Here it is expecting object of comparator as an input.
[05:44] So we have created our own custom comparator which is LastCharComparator.
[05:49] It is implementing the Comparator interface and override the compare() method.
[05:54] I can try to pass the object of LastCharComparator by writing new LastCharComparator() with this line of
[06:02] code
[06:03] this time the sorting is going to happen based upon the last char value.
[06:07] I can also confirm you the same by printing out countries1 collection object.
[06:12] So let me execute this program and this time you can see all the elements are sorted based upon the
[06:18] last character here capital A followed by small A, small A, then yi followed by N.
[06:23] I hope this is making sense to you.
[06:25] Just like how we are invoking the sort() method by using the object of ArrayList.
[06:30] Similarly, we can use the same LastCharomparator when we try to invoke the static method available
[06:37] inside the Collections class.
[06:39] So let me show you the demo of the same as well.
[06:42] For the same, I'm going to comment this line of code, and this time I'll try to invoke the static
[06:47] sort() method available inside the Collections.
[06:50] So here we have two types of sort() method.
[06:52] We need to invoke the second method which is accepting two input parameters.
[06:57] First we need to mention what is our Collection object or ArrayList object followed by what is the
[07:03] object of our custom comparator.
[07:05] So I'm trying to pass LastCharComparator object as an input this time
[07:10] also you should see the same output.
[07:12] You can see the sorting is happening in an ascending order based upon the last char value.
[07:18] If you are looking for that descending order, it's going to be very easy.
[07:21] You just have to swap these elements here instead of lastChar1 we need to mention lastChar2,
[07:27] followed by lastChar1.
[07:30] So this time if you execute the program, you should be able to see the sorting in an descending order.
[07:36] You can see first we have n, followed by E followed by small a, small e and capital A.
[07:43] I hope it is clear for you on how to define your own custom sorting logic.
[07:49] Whenever you are dealing with the primitive data type objects or String objects.
[07:54] As a next step, we should also learn on how to sort custom data type objects. Like in real projects
[08:01] you may store objects of Students, Persons, Employees with their own data.
[08:07] You should also understand how to sort these kind of custom data type objects with the help of Comparator
[08:12] and other options.
[08:14] So let's try to explore all of them in the next lecture.
[08:17] Thank you,
[08:18] bye.

----------------------------------------
