# 20.8 — Iterating HashMap using values()

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] Before I try to show you the third approach, I want to highlight about an important point, which is
[00:06] whenever you are trying to iterate the entries of HashMap and try to display them on your console,
[00:11] it is very clear that HashMap is not maintaining the order of insertion inside the code.
[00:17] You can see first we try to insert India and its capital, followed by USA and France.
[00:23] But inside the console when you are trying to iterate them.
[00:26] First we received the entry related to USA, followed by France, followed by India.
[00:31] So this should give an assurance to you that HashMap is never going to maintain the order of insertion.
[00:38] On top of that, whenever we are invoking these entrySet() and the keySet() methods, we are going to
[00:45] get the keys and the entries inside a Set data structure.
[00:49] We are going to discuss about Set in the coming lectures.
[00:52] But I want to highlight you about a point related to Set which is Set are also they are not going to
[00:58] maintain the order of insertion.
[01:00] That's why inside the set we don't have a method to invoke the List iterator.
[01:06] Using ListIterator, we can iterate the elements both in forward and reverse direction, but the ListIterator
[01:11] is only available in the List interface and its implementation classes.
[01:17] Since the List is going to maintain the order of insertion, it makes sense to have ListIterator and
[01:22] its implementation.
[01:23] But coming to the Set since it is not going to maintain the order of insertion, we don't have any method
[01:29] around the ListIterator.
[01:31] We should always use the iterator or for each loop.
[01:34] I hope this makes sense.
[01:36] Now let me show you the third approach that we can follow to iterate the values inside an HashMap.
[01:42] Sometimes you may have a requirement which is to process only the values present inside an HashMap.
[01:49] You're not going to worry about the keys, you just wanted to process all the values.
[01:53] In such scenarios, you can always happily use the third approach.
[01:57] So let me copy this approach2() method and rename this method name to approach3().
[02:02] Inside this approach3() instead of entry set, we need to invoke the method which is values.
[02:09] So this values() method is going to give you the A collection of your values.
[02:15] So what is the data type of your Value object.
[02:18] It is String
[02:18] that's why you can see it is giving collection of String.
[02:22] And we can change this variable name to values.
[02:25] Since the return type of values() method is of type collection, I will not be able to invoke the iterator()
[02:32] method with the help of these values().
[02:34] You can see it is not available.
[02:36] So that's why whenever you are using these values() method to get all the values, the only option is
[02:42] to iterate them with the help of for each loop.
[02:45] So here let me mention values and post that on the left hand side I can mention String value.
[02:52] The same value I can try to print out directly with the help of System.out.println().
[02:58] Here I will not be having any access to my key.
[03:02] It is also not going to make sense to get a key from a value, because we discussed we can have duplicate
[03:08] values.
[03:09] So if you are trying to get a key from a value, your HashMap is going to be clueless whenever your
[03:15] HashMap has multiple duplicate values.
[03:18] That's why there is no option inside HashMap to get a key from a value.
[03:23] I hope this discussion making sense to you.
[03:25] Now let me try to invoke this approach3() method from my main() method.
[03:31] With that, if you try to execute this program, you will be able to see the values like Washington,
[03:37] Paris and New Delhi.
[03:38] So these are the most commonly used approaches.
[03:42] Whenever you want to iterate the entries inside your HashMap, you can see with the help of approach1()
[03:48] we can only iterate the keys.
[03:51] So from the keys we are able to get the value.
[03:53] But with the approach two we can get the set of entries.
[03:57] Using these entries, we can try to iterate them to fetch both key and value, whereas the third approach
[04:04] is going to give you the A collection of values.
[04:07] So based upon your scenario, you need to use one of these three approaches.
[04:12] There are few more approaches as well, but these three are the most commonly used
[04:17] as long as you aware about these three approaches, you should be good for your real projects or for
[04:23] any interview question around this.
[04:25] The three approaches that we have discussed around iterating HashMap.
[04:30] I have mentioned all of them in these two slides for your reference along with the example code.
[04:35] Feel free to refer them for any questions.
[04:38] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
