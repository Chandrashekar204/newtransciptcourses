# 26.16 — Demo of Streams collect() method

> Section 26: [JAVA 8] Streams API

[00:00] Collect is the another commonly used terminal operations by the developer on day to day work.
[00:06] Let's try to understand what is the purpose of this terminal operation and when to use these and how
[00:11] to use these.
[00:11] So all these details we can try to understand inside this lecture.
[00:15] So the purpose of collect() method inside the Java Stream API is to transform the elements of a stream
[00:22] into a different form, usually into a collection like a List, Set or Map.
[00:27] Think like you have an original list with 1000 different elements.
[00:31] By using these original List, you created a Stream object and after creating the Stream object, you
[00:37] executed a intermediate operation
[00:39] with the help of filter() method and using these filter() method, you have a new Stream object that is
[00:44] holding to the 200 different elements.
[00:47] But at the end of the day, whenever we want to process these filtered elements further inside the business
[00:54] logic, first we need to convert them into an another collection object like List, Set or Map.
[01:00] In this kind of scenarios, we can happily use the collect() method.
[01:04] For example, here I have a departmentList with the various department names.
[01:08] Using that department List object, I tried to create the stream by invoking the stream() method, followed
[01:14] by
[01:15] I'm trying to apply an intermediate operation, which is filter(), with the filter()
[01:19] I'm trying to filter all the departments that are starting with the letter s, so after my filter operation
[01:26] is executed, I'm going to get a new Stream object that is holding to the elements like Supply and Sales.
[01:32] If I want to convert these elements from stream to another data source like List, I can use that terminal
[01:39] operation which is collect().
[01:40] Like you can see, I'm trying to collect it into a new List object with the name new departmentList.
[01:46] And whenever we are invoking these collect() operation, we can leverage one of the utility class available
[01:52] inside the JDK, which is Collectors, and inside these we have a method called toList().
[01:57] So these toList() it is going to give the instructions to the collect() method and how to collect the
[02:03] elements with the toList().
[02:04] We are trying to convey that I want my elements to be collected in the form of a List object.
[02:09] That's why on the left hand side we have the variable name with the name new departmentList of type
[02:15] List.
[02:15] And at last it's up to me what I want to do with the elements present inside these new List object here
[02:21] to keep things simple, I'm just trying to display them by using these forEach() method.
[02:26] So if you see here we are trying to use a two list static method inside the Collectors.
[02:31] Very similarly we have other kind of methods like toSet(), toCollection().
[02:35] Basically what Java team they have done is instead of asking the developer to provide some lambda expression
[02:42] to create a List or to create any other data source, instead of making developer life complex, they
[02:47] try to provide all the static methods which we can use based upon our business requirements.
[02:53] So when you try to invoke these toLoist(), you're going to get a List object, whereas with toSet()
[02:57] you're going to get the elements inside a Set object.
[03:00] But coming to the two collection, inside collection, we know there are many implementations.
[03:06] That's why whenever we are using these toCollection() method to collect the elements, we need to convey
[03:11] which collection implementation class we want to consider to store the elements.
[03:17] I'm going to show you the demo of two collection in few minutes.
[03:20] Post that it is going to make more sense to you.
[03:23] Let me show you one more example here
[03:24] like you can see here
[03:25] think like I have some collection with the name persons. Inside this persons collection object.
[03:30] I have various person related objects stored.
[03:33] Maybe I have 100 different person objects.
[03:36] So using these persons variable name, I'm trying to invoke the stream post that I'm trying to invoke
[03:41] an intermediate operation which is map().
[03:44] With the help of map(), I'm trying to get the name details of each person, and at last all the names
[03:51] I want to collect into a list.
[03:53] That's why I'm trying to invoke the terminal operation, which is collect().
[03:56] And to this terminal operation I'm trying to provide the input which is Collectors.toList().
[04:01] With that, I'm going to get all the persons names into List
[04:05] That's what I'm trying to catch with this variable name person names the same.
[04:08] If I try to print out, I'll be able to see all the person names. Apart from toList().
[04:13] We have other methods inside the Cllector class, so these methods are like toSet(), which is going
[04:19] to help me to convert stream into a Set object, toCollection()
[04:22] like I discuss, it is going to help in converting Stream into a collection, toMap()
[04:27] it is going to help us to convert our Stream into a Map.
[04:29] But to these toMap() method, we need to provide the lambda expression that helps in determining the
[04:36] key and the values.
[04:37] And the counting() is going to help us
[04:39] number of stream elements.
[04:40] This is just like a count reduce operation.
[04:43] Similarly, joining() is going to help us to concatenate the stream of elements into a single stream.
[04:49] minBy() and maxBy().
[04:50] They are going to help us to identify the minimum or maximum elements based upon the given comparator
[04:57] logic.
[04:58] I'll be showing a demo of this
[04:59] minBy() and maxBy() in few minutes, and at last reducing also helpers to reduce the stream elements based
[05:07] upon the BinaryOperator function that you are trying to provide.
[05:10] So this is going to work very similar to the reduce() operation.
[05:14] I hope you are clear with this theory discussion.
[05:16] Now let's try to see the demo of this collect() method very quickly inside the IntelliJ.
[05:22] Here inside my project, I'm going to create a new Java class with the name StreamCollectOperationsDemo.
[05:29] Inside this class
[05:30] first let me create a main() method followed by
[05:32] I'm going to create a List object that holds all the department details.
[05:37] So let me copy this entire code and paste it here.
[05:40] So I have a List object that holds the name of four different department names.
[05:45] Now as usual using this departmentList, first I need to get the Stream object, followed by
[05:50] I'm going to invoke the filter() method to filter the departments only with the name that starts with
[05:58] S.
[05:58] So here I'm going to mention the input parameter name of lambda expression as word followed by
[06:03] I'll just use the same word, and using this word I'm going to invoke the method which is startsWith()
[06:09] and
[06:09] to this I'm going to mention s as the input value.
[06:13] After this, I'll try to invoke that terminal operation which is collect().
[06:17] To this collect(), we need to pass the input in the form of Collectors.toList().
[06:22] So if I try to invoke these toList() method available inside the collectors, basically what it is doing
[06:27] is it is trying to convert all your stream elements into a List representation.
[06:32] So that's what here you can also confirm in the documentation returns a collector that accumulates the
[06:38] input elements into a new list.
[06:41] So let me go to the main class.
[06:42] And here on the left hand side I'll try to catch the output with the help of List String and with the
[06:48] variable name as newDepartmentList.
[06:52] So using these newDepartmentList variable I can try to invoke the forEach() method.
[06:58] So here don't assume like this.
[07:00] forEach() is a terminal operation.
[07:02] We're not trying to invoke the forEach() by using a Stream object.
[07:05] Instead we are invoking this forEach() method with the help of List object itself.
[07:10] So this forEach() method is available inside the iterable interface.
[07:14] So basically this is also going to help us to iterate the elements based upon the consumer logic that
[07:21] we are trying to provide.
[07:22] That's why in this scenario we can't call this as a terminal operation.
[07:25] We can only call this as a terminal operation if it is used as part of the stream pipeline.
[07:30] So here I'll try to mention System.out::println().
[07:36] So if I execute this you know the output that I'm going to get I'm going to get an output with the name
[07:42] Supply and Sales.
[07:43] If you are looking for an option to count the number of elements inside the stream with the help of
[07:50] collect() method, then it is very simple.
[07:52] Instead of invoking the toList() method, what you can do is you can invoke the counting() method available
[07:59] inside the Collectors.
[08:01] So this counting() method,
[08:03] it is going to count the number of input elements.
[08:06] If there are no elements are present, the result is going to be zero.
[08:09] Since this is going to give me the count in the form of long, I need to accept the output with the
[08:16] help of long only on the left hand side.
[08:19] So let me create a variable with the name totalCount the same
[08:23] if I try to print out the help of System.out.println(), I'm going to get the output as two.
[08:29] So you can see I'm getting the output as two.
[08:31] Similarly, you can use the toSet() method as well instead of toList().
[08:37] So here I'm trying to catch the output in the form of List object.
[08:41] But if I try to change this to toSet(), then I need to catch the output with the help of Set on the
[08:47] left hand side, I just need to mention Set of String.
[08:49] You can see how easy it is to collect the elements with the help of these collect.
[08:54] But if you are looking to collect your elements with the help of Map, then you need to invoke that
[08:59] toMap() method to these toMap() method you need to pass two lambda expressions.
[09:04] One is going to help on how to calculate the key for your element, and the second lambda expression
[09:09] is going to help to calculate the value based upon your elements.
[09:13] For now, let's not complicate our life.
[09:16] We can go with that toList() or toSet() developers rarely use toMap() because why do you want to convert
[09:22] a normal data into a map?
[09:24] Just like toSet() and toList() ?
[09:26] We also have toCollection() static method.
[09:29] Whenever you are using these toCollection() method, you need to provide a lambda expression adhering
[09:34] to the Supplier.
[09:35] So basically your lambda expression should tell to that toCollection() method which collection implementation
[09:42] object you want to use to collect the elements.
[09:45] So here you can see the documentation says returns a collector that accumulates the input element into
[09:51] a new collection.
[09:52] If my intentions is to collect the elements using one of the collection implementation like a TreeSet,
[09:58] then
[09:59] I just have to provide a lambda expression which which is going to provide that TreeSet object.
[10:05] So in this kind of scenario I can use the constructor reference.
[10:08] So let me type TreeSet followed by colon colon followed by new.
[10:12] So my toCollection() method it is simply expecting what is a collection data type that I want to use
[10:18] to collect the elements.
[10:19] Since here I want to use the TreeSet, I need to provide the object of TreeSet as an input to that
[10:25] toCollection().
[10:26] With that, all the elements that are going to be stored with the help of TreeSet.
[10:30] And since on the left hand side I'm using the set which is a parent of this TreeSet, I'm not getting
[10:35] any compilation error. But if I try to use list I'm going to get a compilation error.
[10:40] So let me revert back to Set.
[10:42] This way you can always use the collect() method to collect the List of elements that are present inside
[10:48] a Stream.
[10:49] I hope you are clear,
[10:50] thank you and I'll catch you in the next lecture, bye.

----------------------------------------
