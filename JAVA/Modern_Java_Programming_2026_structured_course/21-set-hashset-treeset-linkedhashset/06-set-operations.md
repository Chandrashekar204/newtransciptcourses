# 21.6 — Set operations

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] The Set data structure, which is available inside the Java collection framework, is greatly inspired
[00:06] by MathematicalSet.
[00:09] If you can recall our school days inside mathematics, there is a concept with the name Set.
[00:14] So whenever we are using Set inside mathematics, we can perform various operations like union, intersection,
[00:21] difference, subset, the same kind of operations
[00:24] we can also perform with the help of the Set or its implementation classes.
[00:29] Let me show you a demo so that it is going to be clear for you.
[00:32] To show you the demo, I'm going to create a new Java class with the name SetOperationsDemo.
[00:40] Inside this class
[00:42] first I'm going to create the main() method, followed by
[00:44] I'm going to create couple of Sets, the two Set objects that we are going to create
[00:48] they are going to store the integer values.
[00:51] That's why I'm mentioning the integer data type inside the angle brackets, followed by I'll just mention
[00:57] hashSet1, and on the right hand side I can mention new HashSet with a diamond operator and a
[01:05] default constructor.
[01:06] Now inside this hashSet1 object I can try to add the integers like,
[01:12] first I'm going to add seven, followed by I'm going to add four.
[01:17] So these are the two integer values that I'm trying to store as of now
[01:20] inside this hashSet1.
[01:22] In the similar lines I'm also going to create one more hashSet object with the name as hashSet2.
[01:29] Inside this I'm going to store elements one followed by six.
[01:34] Now using these two hashSet objects, let's try to perform various Set operations.
[01:40] The very first operation that I want to perform is union operation.
[01:46] So whenever we try to perform union operation with the help of two hashSet objects, what is going to
[01:51] happen is, the elements present inside the second Set object
[01:56] they are going to be added to the first Set object.
[01:59] For example, we can try to perform the union operation by invoking the object to one which is hashSet1
[02:06] and post that we can invoke the addAll() method, and to this addAll() method, we can pass the
[02:12] second object which is hashSet2.
[02:15] With this, if I try to print out hashSet1, you'll be able to see all the elements present inside
[02:22] the hashSet2 they are added to the hashSet1 object.
[02:26] So let me execute.
[02:27] This program you can see hashSet1 object.
[02:30] Right now it has elements like one, four, six, seven.
[02:33] So the elements one and six they are added from the hashSet2.
[02:37] So this is a union operation.
[02:40] So to perform any time a union operation you can use these addAll() method.
[02:45] So with this union operation the hashSet2 is not going to be impacted.
[02:49] For example if I try to print out hashSet2() object I'll be able to see the data one and six inside
[02:57] the hashSet2.
[02:58] So it is not going to be impacted anyway.
[03:00] Only the first object which is hashSet1 is going to be impacted because using the same we are trying
[03:06] to invoke the addAll() method.
[03:08] Next I'm going to show you the intersection operation.
[03:12] Whenever we try to perform the intersection operation, only the common elements between the two sets,
[03:19] they are going to be retained in the very first object.
[03:22] Let me show you the demo around the intersection as well.
[03:24] But before that I want to comment these lines so that we can see that demo of intersection.
[03:30] So let me comment these followed by I'm going to mention the operation name which is intersection.
[03:38] So whenever we want to perform the intersection operation you need to first select the object in which
[03:43] you want to maintain the common elements.
[03:46] So first I'm going to mention hashSet1 here using the same.
[03:50] I'm going to invoke the retainAll() method.
[03:53] To this retainAll() method I'm going to pass the second object which is hashSet2.
[03:58] Now if I try to execute this program, my hashSet1, it is going to have empty values because
[04:06] there are no common elements between these two hashSets.
[04:10] So what I can do here is I can try to replace this 6 to 7 inside my hashSet2 object with that
[04:17] if we execute this program this time your hashSet1, it is going to have the element seven because
[04:23] it is a common element present inside, hashSet1 and hashSet2.
[04:27] Even with the retainAll operation, the second object is not going to be affected.
[04:32] Now let's see the operation of difference.
[04:35] Before I try to perform the difference operation, I will comment this line of code and post that I
[04:41] will mention the operation name as difference.
[04:44] So what is going to happen with this difference
[04:46] operation is, all the common elements between the two sets.
[04:51] They are going to be removed.
[04:52] Only the uncommon elements inside the hashSet1 object
[04:57] they are going to be retained.
[04:58] So let's see the demo for.
[05:00] I'm going to first mention the hashSet1 object.
[05:03] Using these, I'm going to invoke the removeAll() method.
[05:07] To this removeAll() method I'm going to pass hashSet2 as a second object.
[05:11] If I execute this program, we can expect the output as four, because the seven which is present inside
[05:18] both the sets, it is going to be removed.
[05:20] With that the uncommon elements inside the hashSet1, they are going to be retained.
[05:26] So what is that element?
[05:27] As of now we have only four.
[05:29] That's why the same we are able to see inside the console even with these operation.
[05:34] Also the second HashSet object
[05:36] it is not going to be affected.
[05:37] I hope this makes sense.
[05:39] Now let's see the last operation which is subset operation.
[05:43] We can check if a given set object is a subset of another Set object.
[05:49] Before I try to perform the subset operation, let me comment this line of code followed by.
[05:54] I'm going to mention the operation name as subset() in order to perform whether a given set is a subset
[06:00] of another set, we can first invoke the first Set object which is hashSet1, followed by
[06:06] we can invoke the containsAll() method.
[06:10] To this containsAll() method,
[06:11] we can pass hashSet2. The output from
[06:14] this containsAll() method is a boolean value.
[06:17] That's why on the left hand side I can type boolean followed by variable name as isSubset.
[06:22] So whenever we are using this containsAll() method, we are going to get a boolean value as true.
[06:28] If all the elements inside the hashSet2 are present inside the hashSet1.
[06:33] So this containsAll() method.
[06:34] It is going to check whether the hashSet2 is a subset of hashSet1.
[06:39] It's not like other way.
[06:40] Don't be under the impression that hashSet1 is going to be checked.
[06:44] If it is a subset of hashSet2, it is not going to work that way.
[06:48] It is going to work other way.
[06:49] So if we try to execute these program, we are going to get the output as false.
[06:53] I can try to confirm the same by printing the boolean each subset.
[06:58] So if I execute this program you can see I'm getting false because the seven element is present inside
[07:04] the first object, but one is not present.
[07:07] In order to get the output as true, what we can do is, we can add the element one to the first Set object.
[07:14] So here I'm trying to add one.
[07:16] If I execute this program this time I'm going to get the output as true.
[07:19] Because all the elements inside the second set object, they are present inside the first set object
[07:26] as well.
[07:27] So this confirms that my second hashSet object is a subset of my first hashSet object.
[07:34] So these are the operations that you can perform whenever you are trying to deal with the set related
[07:40] objects in real projects.
[07:41] Also you may get requirements around these operations.
[07:44] I hope this makes sense to you.
[07:46] All the Set operations that we have discussed so far inside this lecture, I have mentioned in this
[07:50] slide
[07:51] for your quick reference.
[07:52] There are examples and method code snippets as well for your quick reference.
[07:57] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
