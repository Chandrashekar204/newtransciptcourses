# 21.8 — Demo of LinkedHashSet in Java

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] If you are looking for an Set implementation, which is going to maintain unique elements and the order
[00:06] of insertion for such scenarios, you can happily use the LinkedHashSet.
[00:11] So this LinkedHashSet is one of the implementation of Set interface.
[00:16] It provides all the features that you have from HashSet.
[00:19] And it is also going to implement the SequencedSet.
[00:22] Since the order is always guaranteed, it is going to implement SequencedSet how it is going to maintain
[00:28] the order of elements by leveraging the LinkedList concept.
[00:31] So this LinkedHashSet is a combination of both the Hashset and the LinkedList.
[00:37] Let me show you an example code.
[00:39] Here you can see I'm trying to create an LinkedHashSet object inside this
[00:44] I'm trying to store various country details.
[00:47] If I try to iterate all these details, you will be able to see the output with the country details
[00:53] with the same order of insertion.
[00:55] So India, USA, Dubai, Singapore, France the same is going to be printed inside the output.
[01:01] So when to use the LinkedHashSet ?
[01:03] If you have a business requirement to maintain the unique elements and the order of insertion in those
[01:09] scenarios, you can happily use LinkedHashSet.
[01:12] Let's try to write a small program around this so that it is going to be clear for you.
[01:17] Like you can see here, this is the LinkedHashSet class which I have opened.
[01:21] If you look at the class definition it is going to extend the HashSet.
[01:26] And it is also going to implement the SequencedSet apart from this class definition.
[01:30] If you can try to observe the code present inside the constructors of this class, they are invoking
[01:36] the super constructor which is available inside the HashSet.
[01:40] If you open any of the super constructor here, you will be able to see that behind the scenes it is
[01:46] using the LinkedHashMap to store the elements.
[01:49] So this is how it is going to maintain the order of insertion.
[01:53] I hope this makes sense to you.
[01:55] Now let me go back to the LinkedHashSet.
[01:58] And since this LinkedHashSet also implemented the SequencedSet interface, you will be able to see
[02:04] all the SequencedSet related methods like reversed(), addFirst() and similarly removeFirst().
[02:12] I hope you are clear.
[02:13] Now let's try to create the class with the name LinkedHashSetDemo. Inside this class,
[02:20] first I'm going to create the main() method followed by
[02:25] I'm going to write var visitedCountries and on the right hand side I'll type new LinkedHashSet and
[02:34] inside these angle brackets I can mention the String as a data type followed by semicolon.
[02:40] And now inside this LinkedHashSet object
[02:44] I'm trying to add various elements.
[02:46] The very first element I'm trying to add here is India, followed by USA and after USA Dubai and after
[02:56] Dubai, Singapore and after the Singapore.
[02:59] I'm going to mention France.
[03:02] So if you try to iterate them and display them onto the console, you will be able to see the country
[03:09] details in the same order of insertion.
[03:12] So first let me try to create a dummy variable name with the name country name, followed by visited
[03:19] countries.
[03:19] Inside this
[03:20] for each block, I'm going to write System.out.println() statement and print the country name details.
[03:27] So if I execute this class, you'll be able to see the output in the same order of insertion like India,
[03:33] USA, Dubai, Singapore and France.
[03:36] Now let me show you that demo of the reversed methods which inherited from SequencedSet method.
[03:42] So what I can do is with the help of these visitedCountries, I can try to invoke the reversed() method.
[03:49] The return type of these method is SequencedSet.
[03:52] On the left hand side, I can type SequencedSet and inside the angle brackets I can mention
[03:58] String followed by reversedVisitedCountries.
[04:02] So these are object name the same.
[04:05] If I try to print out all my country, details will be reversed.
[04:09] Let me execute this program and you'll be able to see all the country details are reversed like first
[04:15] France, followed by Singapore, followed by Dubai.
[04:18] And after Dubai we have USA and India.
[04:21] With this, it should be pretty clear for you under which scenarios you need to use
[04:26] LinkedHashSet. Majority of the times
[04:28] if your primary requirement is only about the unique elements, always go with the HasSet.
[04:34] Whereas if you are looking for sorting, you can go for the TreeSet.
[04:38] But if you are looking both for unique elements and order of insertion, then you can happily go for
[04:44] that LinkedHashSet.
[04:46] I hope this makes sense to you.
[04:47] Thank you,
[04:48] bye.

----------------------------------------
