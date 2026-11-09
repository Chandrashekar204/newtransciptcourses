# 21.5 — Iterating HashSet

> Section 21: Set, HashSet, TreeSet, LinkedHashSet

[00:00] As of now
[00:01] we saw the demo on how to add the elements to the HashSet, and how to remove the elements from the
[00:06] HashSet.
[00:07] As a next step, let's try to understand one more common operation that we can perform with the HashSet
[00:12] object.
[00:13] This common operation is iterating or looping the elements present inside a HashSet object.
[00:20] There are a couple of approaches that we can use to iterate the elements present inside an HashSet object.
[00:27] To show you the demo around the same, I'm going to create a new Java class with the name
[00:35] HashSetIterationDemo. Inside this class,
[00:37] first, let me try to create the main() method, followed by
[00:40] I'm going to create the object of HashSet with the variable name as super powers, and on the right
[00:48] hand side I'll just mention new HashSet.
[00:51] So inside this HashSet object, I want to store various super powers that our super heroes will have,
[00:58] and similarly, villains also will have some super powers.
[01:01] So let's try to store some super powers of our super heroes and villains.
[01:05] So the very first super power I want to add here is invisibility.
[01:10] For the same, I need to use the Super Powers variable name.
[01:14] Using the same, I need to invoke the add() method to this
[01:17] I need to pass the value which is invisibility.
[01:20] So this is one kind of super power that usually heroes may have.
[01:25] Similarly, I'm going to add few more powers very quickly, but I'm not going to type in front of you
[01:31] just to save some time here.
[01:32] Instead of this line, I'm going to paste a few lines of code like you can see here
[01:37] these are all the super powers that usually super heroes will have invisibility followed by teleportation.
[01:44] Teleportation means they will be able to travel from one location to other location without any traveling.
[01:51] Similarly, mind reading, super strength, time travel, coming to the villain, super heroes
[01:56] they may have powers like laser vision, weather manipulation, telekinesis.
[02:01] Telekinesis is a super power using which you can move the objects from a distance.
[02:07] After telekinesis, we have shapeshifting followed by Chaos Induction.
[02:12] You can add your favorite superhero super powers or your favorite villain Super powers as well.
[02:18] But coming to our agenda of this lecture, we want to understand what are the options that we have whenever
[02:24] we are looking to iterate the elements inside a HashSet and process them.
[02:28] The very first approach is with the help of for each.
[02:31] So here what I can do is, first I'm going to create a temporary variable name with the variable as String
[02:38] superPower, followed by HashSet object which is superPowers.
[02:43] So now all my elements inside my HashSet object, they are going to be iterated and the same can be
[02:48] accessed with these variable, which is super power.
[02:51] For example, if I'm trying to build a business logic to display all the super powered details by converting
[02:58] them into completely capital letters, I can write the code which is System.out.println(), followed
[03:04] by superPower.toUppercase().
[03:08] So if I execute this program, we'll be able to see all the superPowers in completely capital letters.
[03:15] Obviously the order is not going to be guaranteed, but whatever elements that we stored here, you
[03:21] can see we're able to convert them into capital letters and print them inside the console.
[03:27] This way you can write any kind of processing logic or business logic inside these for each loop.
[03:32] Similarly, we can also use the iterator.
[03:35] So how to create an iterator object using the HashSet object which is superPowers, we can invoke the
[03:42] iterator() method.
[03:43] We know behind the scenes this iterator() method.
[03:46] It is going to invoke the Map.keySet() method to give the Iterator object.
[03:52] So on the left hand side I can create Iterator object variable by typing iterator and inside the angle
[04:00] brackets I can mention String followed by variable name as iterator.
[04:04] So now using these iterator I can build an while loop.
[04:08] Inside these
[04:09] while loop I can write a condition which is iterator.hasNext().
[04:13] Then in such scenarios I want to read the next element with the help of iterator.next().
[04:22] .
[04:22] After reading the element, we can do whatever we want.
[04:26] Maybe what we can do here is we can try to copy the same code present inside the for loop, but instead
[04:31] of toUppercase() we are going to invoke the toLowercase(), but the variable name.
[04:36] I have mentioned the country name due to my confusion with the previous program, so let me rename this
[04:41] to superpower and this toUppercase() I can replace with toLowercase().
[04:47] So now if we execute this program this time you'll be able to see the superpowers printed in an completely
[04:54] lowercase letters.
[04:55] So these are the two approaches that you can use whenever you are looking.
[04:59] To iterate the elements inside a HashSet object.
[05:02] We don't have list iterator option like ArrayList.
[05:05] The reason is very simple HashSet does not maintain or guarantee the order of insertion.
[05:12] The details of the two approaches that we discussed to iterate the HashSet elements I have mentioned
[05:17] inside this slide, along with the example code.
[05:20] Please refer the same whenever you are trying to quickly refresh your knowledge around the HashSet.
[05:26] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
