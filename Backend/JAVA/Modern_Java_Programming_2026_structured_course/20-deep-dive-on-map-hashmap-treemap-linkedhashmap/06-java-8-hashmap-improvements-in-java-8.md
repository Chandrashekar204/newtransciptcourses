# 20.6 — [JAVA 8] HashMap improvements in Java 8

> Section 20: Deep dive on Map, HashMap, TreeMap, LinkedHashMap

[00:00] In the last two lectures, when we were trying to discuss about the internal working of the HashMap,
[00:05] I told you that whenever an hash collision happens, it is going to store the entries in a LinkedList
[00:12] format.
[00:13] But it is partially true because there are some enhancements or improvements introduced as part of the
[00:21] Java 8.
[00:22] So let's try to understand what are these improvements that are introduced inside the HashMap as part
[00:27] of Java 8.
[00:28] Inside Java 8, HashMap was improved to include a new data structure called TreeNodes.
[00:35] This was done to improve the performance in cases where HashMap contains a large number of entries with
[00:43] the same hash code, causing the hash collisions and the creation of long LinkedList.
[00:49] We know based upon our previous discussion, whenever the hash collision has happened, the new entry
[00:53] is going to be appended as an node to the existing LinkedList.
[00:58] If the HashMap, it is going to keep on adding more and more elements or nodes to the same LinkedList
[01:04] inside the same bucket.
[01:06] When you are trying to read the value based upon a given key, it is going to be slow because we know
[01:11] inside LinkedList the reading operation is going to be very slow.
[01:16] Think like there is a value present at the 11th node, but in order to read that 11th node value, the
[01:23] reading operation has to start from right from the very first node inside the LinkedList.
[01:28] So to overcome these kind of challenges, a new data structure which is tree nodes is introduced as
[01:35] part of Java 8.
[01:36] But this doesn't mean from Java 8 we are always going to store the elements in a TreeNode format.
[01:43] Whenever a hash collision happen, it is not going to work.
[01:46] HashMap is always going to start with the LinkedList data structure.
[01:50] When a number of nodes inside a LinkedList exceeds a configured number inside the JDK library, then
[01:57] that entire LinkedList data structure is going to be converted into a TreeNode format.
[02:03] Let's try to understand more details about this TreeNodes.
[02:07] They work by creating a self-balancing binary tree within the same bucket.
[02:12] When you are trying to add new entries to the same bucket, the tree is restructured as needed to maintain
[02:19] the balance and ensure that retrieval time always remains fast.
[02:24] How it is going to be fast.
[02:25] I'm going to explain you in few seconds.
[02:27] Hold your thought around this, but you may have a question here, which is if tree nodes are fast compared
[02:33] to the LinkedList, then why can't HashMap can use tree nodes right from the very first entry insertion?
[02:42] That's a great question.
[02:43] But tree nodes has a disadvantage, which is they are twice the size of regular nodes of LinkedList.
[02:50] That's why in order to get the benefits of TreeNodes, we need to make sure there are minimum number
[02:55] of elements or nodes inside your LinkedList.
[02:58] Then only it is worth replacing the LinkedList with a double size tree node inside a bucket.
[03:04] Think like
[03:05] once the benchmark is exceeded, a given LinkedList is converted into a tree node inside a bucket.
[03:11] So as of now, your bucket is going to hold all the hash collision elements in a TreeNode format.
[03:17] But at later point of time, there is a good chance that a developer may invoke remove() method to remove
[03:24] few elements.
[03:25] In this kind of scenarios, when the number of elements inside your tree nodes are getting reduced automatically,
[03:32] the TreeNode is going to be converted back into the LinkedList.
[03:36] This way, always behind the scenes LinkedList is going to be converted into a TreeNode.
[03:41] When the NF elements are stored under a single bucket, and vice versa is going to happen whenever we
[03:48] are trying to remove the entries which are present inside the same bucket.
[03:51] Let's try to understand all these concepts by taking an example.
[03:54] Think like you're trying to store the below key and values.
[03:58] And just for a second, imagine all of them have the same hash code which will make them to store at
[04:05] a same index or same bucket.
[04:08] I know it's a very hypothetical scenario, but let's imagine all these elements
[04:12] they are going to be stored in a single bucket because their hash code values are same.
[04:17] With this assumption, if we try to visualize how the same information is going to be stored in the
[04:23] LinkedList format is,
[04:25] like you can see here whenever the elements are getting stored in a LinkedList format, this is how they
[04:30] are going to be stored.
[04:31] So these are very first node which is pointing to the next node followed by third node,
[04:36] fourth node.
[04:36] Whenever we are trying to read the value with a key five, then the HashMap, it is always going to
[04:42] start the searching operation right from the first node.
[04:46] If it is not able to find the equal key inside the first node, then it is going to ask the first node
[04:51] what is the memory location of the second node.
[04:53] So this process is going to keep on continue until it reaches the node where the key is five.
[05:00] Since LinkedList has this kind of disadvantage whenever we are trying to perform the read operation,
[05:06] when there are good amount of nodes, this LinkedList is going to be replaced with a tree node due
[05:12] to the improvements introduced inside Java 8.
[05:15] Now let's see how the same information is going to be stored with a tree node like you can see here.
[05:22] First we have for it is going to be inserted as a very first parent or top node inside the tree node.
[05:30] The second key and its a value we are trying to store is one.
[05:33] Since four is less than one when the comparison is going to happen behind the scenes, it is going to
[05:39] be stored as a left node.
[05:41] Now coming to the seven.
[05:43] Since seven is greater than four, it is going to be stored on the right hand side.
[05:48] Coming to the two two is less than four
[05:50] it will go here and compare to one.
[05:53] Since two is greater, it is going to be stored as a right node.
[05:57] Next coming to the 15, 15 is greater than four.
[06:01] That's why it goes to seven.
[06:02] And since 15 is also greater than seven, it is going to be stored on the right hand side.
[06:08] Next we have 11 for 11
[06:10] you can see it is greater than four and seven but less than 15.
[06:14] That's why it is going to be stored as a left node under the 15 node. For nine,
[06:21] since it is greater than seven, it is going to come here, but it is less than 15.
[06:26] It is going to become here.
[06:28] And compared to 11 it is still less
[06:30] that's why it is going to be stored as the left node.
[06:34] After 9 we have 13 for 13
[06:36] since it is greater than 11, it is going to be stored as a right node.
[06:40] At last we have five, which is greater than four.
[06:44] That's why it will come here under 7
[06:47] since it is less than seven, it is going to be stored as a left node.
[06:50] So this is how a TreeNode is going to store the key and its value.
[06:54] So whenever a search operation is happening for a second think like you're trying to search for 15.
[07:00] So my HashMap it knows it don't have to check anything on the left hand side of the for node, it will
[07:07] straight away go on to the right hand side.
[07:09] It identified seven compared to seven
[07:12] 15 is greater than.
[07:13] That's why it will ignore all the left hand side nodes.
[07:16] It will keep on searching on the right node direction here, since it is able to find the same key,
[07:22] it will fetch the value and the same is going to be returned to the end user.
[07:26] Since the elements are already sorted using a sorting logic, accessing them will be much quicker compared
[07:34] to the LinkedList
[07:35] whenever we are trying to use the TreeNodes.
[07:38] I hope this makes sense to you.
[07:39] Why?
[07:40] The LinkedList is going to be replaced with a tree node in some scenarios from Java 8 version.
[07:46] Now here you may have $1 million question, which is when the transition between LinkedList to TreeNode
[07:52] and TreeNode to LinkedList is going to happen for the same.
[07:55] Inside the Map interface, we have certain static final variables declared the process of converting
[08:02] a LinkedList to the TreeNode is three five, whereas converting a tree node to the LinkedList, we
[08:09] can call it as UNTREEIFY.
[08:11] So the threshold for Trevor process is eight, whereas for the entry five threshold is six.
[08:17] Which means when your LinkedList is going to have minimum eight elements, then the tree five process
[08:23] is going to happen, whereas entry five process is going to happen only when your tree node is going
[08:29] to have a minimum of six elements.
[08:32] So based upon the above constant fields, the process of conversion from List to tree and vice versa
[08:38] is always going to happen.
[08:40] I hope it makes sense to you.
[08:41] Let's try to validate these two constants inside the Map interface.
[08:45] Inside HashMap class, we need to look for the static final variables that we have discussed previously.
[08:51] Previously, I said they are going to be available inside the Map interface.
[08:54] That is not correct.
[08:55] They are going to be available inside the HashMap because whatever we discuss, it is applicable only
[09:01] for the HashMap.
[09:02] Here I'm going to search for the variable with the name tree five threshold.
[09:08] You can see the value is eight.
[09:10] If you try to read these documentation, it says the bin count threshold for using a tree rather than
[09:17] List for a bin.
[09:18] So when they refer to the List, they mean LinkedList.
[09:21] Similarly, for the entry five threshold, if you try to read the documentation, it says the bin count
[09:26] threshold for entry flying a bin during a resize operation.
[09:31] So based upon these two constant values, always the TREEFY process and UNTREEIFY process is
[09:37] going to happen.
[09:38] I hope you are clear on how the HashMap is going to work internally, and what kind of improvements
[09:44] are introduced inside Java 8.
[09:46] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
