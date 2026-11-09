# 21.10 — List vs Set

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] One of the important question that you may face inside your Java interviews is, people may ask you to
[00:07] explain you about the differences between List and Set, and under which scenarios
[00:12] you need to choose one of them.
[00:13] To answer these kind of questions, you should have a good clarity about the differences between List
[00:18] and Set.
[00:19] That's why inside this lecture, let's put few minutes efforts to understand the differences between
[00:24] the List and Set.
[00:25] We know both List and Set are the interfaces inside the Java collection framework.
[00:30] However, there are good amount of differences between them.
[00:33] The very first difference is List can contain duplicate elements.
[00:37] If you have a requirement to maintain a collection of elements that can contain duplicates, you need
[00:43] to use a List.
[00:44] Whereas if you are looking for an option which will not allow the duplicates, then in that scenario
[00:49] you can happily use Set and its implementation classes.
[00:53] The next difference is around the order of insertion.
[00:57] By default List
[00:58] always maintain the order of insertion while Set.
[01:01] They do not maintain.
[01:03] If the order of insertion is important to you, always prefer List.
[01:08] The Set does not maintain the order of insertion by default.
[01:11] If you are looking for the order of insertion within the Set implementations, then you need to go for
[01:17] the LinkedHashSet.
[01:18] The third difference between List and Set is, List allows for positional access to elements, which means
[01:25] we have 1000 elements inside your List.
[01:27] You should be able to easily pick 200 element or 300 element, or 250 element without any performance
[01:35] issues, because we know by default List is going to maintain the elements in an sequential memory.
[01:40] Locations coming to the Set,
[01:43] Set does not going to provide the positional access.
[01:46] Instead, you can quickly check if an element is present inside a Set or not with the help of contains()
[01:54] method.
[01:54] Off course, List also have contains() method, but whenever you are using contains method on top of a
[02:00] List object, it is going to iterate all the elements one by one, whereas in the scenario of Set it
[02:06] is going to be very quick.
[02:08] It is going to calculate the hash code of your element and pick the corresponding bucket number inside
[02:13] the HashMap, and straight away will return you whether a given element is present or not.
[02:18] Moving on to the next difference list generally have better performance than sets for positional access.
[02:24] This is because List use an index to access the elements, which is faster than checking every element
[02:31] in a Set for membership.
[02:33] This means if you are looking for an option to randomly access the elements with the help of index,
[02:39] always prefer list because they are going to have better performance, whereas on the other side sets
[02:45] they are going to have better performance than List for testing the membership.
[02:49] When I say membership, we can test whether a given element is present inside a Set object or not with
[02:55] the help of contains() method.
[02:57] In summary, always prefer using List when you need to maintain duplicates and preserve the order of
[03:03] insertion, whereas you can prefer Set whenever you need to ensure uniqueness or test for membership
[03:10] of an element very quickly.
[03:12] I hope this is clear to you.
[03:13] We finally did it guys!
[03:16] We are done with the collection framework discussion.
[03:20] We had a very good discussion around the List, Map and Set and generics as well.
[03:25] I know this is a very big concept, but I'm very happy with the progress that we made.
[03:30] With this, we can conclude the discussion around the collection framework and move on to the other
[03:35] important Java concept.
[03:37] But here you may have a question which is, hey Madan there are good amount of other data structures as
[03:42] well inside Java collection framework like Queue, Deque, Stack.
[03:46] I agree with you, but I just wanted to highlight those are not commonly used by the developers on day
[03:52] to day job.
[03:53] That's why I'm not going to put efforts around those least used data structures.
[03:58] But if there is a requirement comes inside your real projects to use one of those least used data structures.
[04:04] I'm sure with all the knowledge that we have gained throughout this course, you'll be able to explore
[04:09] those data structures, their documentation, their methods, and easily able to use them inside your
[04:15] projects.
[04:16] I hope you agree with me.
[04:18] We are going to revisit the collections framework one more time when we are discussing about the functional
[04:23] programming, I'm keep telling throughout the course there is a beautiful concept of functional programming.
[04:29] Using the functional programming, we can make our collections framework even more powerful.
[04:35] With very less code we can try to achieve lot.
[04:38] So that's a power of streams and functional programming inside Java.
[04:42] So hold your thoughts around this.
[04:44] When we start discussing about the functional programming, you are going to become a fan of it, and
[04:50] I would strongly recommend you to use the same inside your real projects as well.
[04:54] Thank you and I'll catch you in the next section,
[04:57] bye.


########################################
