# 15.5 — Deep dive on hashCode() in Object class - Part 2

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] In the previous lecture, we discussed that the default behavior of the hashCode() method inside Object
[00:05] class is to calculate the hash code value based upon the memory address of the object where it is stored.
[00:13] But sometimes we may want to override these hashCode() method to have our own logic to calculate the
[00:20] hash code.
[00:21] In such scenarios, if equals is returning output as true, then whatever hash code logic that we have
[00:27] written, it should give the same hash code value both for object to one and object to two.
[00:34] We are ready to discuss about the equals() method.
[00:36] We are going to discuss about the same in the next lecture, but I want to highlight here that both
[00:41] hashCode() and equals(), they are tightly coupled.
[00:45] They are like sister twins or brother twins.
[00:48] So there is a good history
[00:49] why this hashCode() and equals() are tightly coupled with each other, which I am going to discuss in the
[00:54] next lecture.
[00:55] But now please note that whenever you are trying to invoke the equals() method by using two objects like
[01:01] obj1.equals() and to the equals() method, I'm trying to pass obj2 as an input object.
[01:08] So behind the scenes this equals() method
[01:10] it is going to compare the content of these two objects.
[01:13] If they are same it is going to return true.
[01:16] Otherwise the equals() method is going to return false.
[01:19] So whenever this equals() method returns true in such scenarios, the hashCode() method of object one
[01:26] and object two, they should return the same hash code value or same Integer value.
[01:33] In other words, if two objects are equal using the equals() method, they must have the same hash code
[01:40] value.
[01:40] So that's a very first rule that you need to take care whenever you are trying to implement your own
[01:45] hash coding logic.
[01:46] The second rule is if the hash code values are same, that is not going to guarantee the equality of
[01:54] the objects.
[01:54] So this is the reverse of the rule number one, but in a negative way.
[01:58] Think like the object to one hash code and the object two hash code
[02:02] return the same integer value at the same hash code value.
[02:05] That doesn't mean both object one and object two
[02:09] they are equal and your equals() method is going to return true.
[02:13] So there is a good chance, even if the hash code values are same, the objects content may not be the
[02:18] same.
[02:19] So this is what rule number two conveys. Coming to the rule number three
[02:22] if you are trying to invoke the same hashCode() method on top of the same object multiple times in the
[02:28] same execution or in the same operating system or in the same mission, your hashCode() method should
[02:35] always give the same hash code value or same integer value as an output.
[02:41] For example, think like you are having the same execution environment, which means same laptop, same
[02:48] operating system, same Java project.
[02:50] With this kind of environment, if you are trying to invoke the hashCode() method on top of an object
[02:56] ten different times, in such scenarios, you should always get the same hash code value or same integer
[03:03] value as an output.
[03:04] Whereas if the execution environment changes like in a different laptop or in a different operating
[03:10] system, the hash code may vary.
[03:12] But generally, if you're trying to invoke the hash code method in the same execution environment multiple
[03:18] times, it should always give the consistent hash code value as an output.
[03:23] And at last, the rule number four says whenever you are trying to overwrite the hashCode() method inside
[03:30] your subclass, you should also make sure you are overriding the equals() method as well, because they
[03:37] both are closely tied with each other.
[03:40] If you try to override only the hashCode() but not the equals(), then you are going to get unexpected
[03:46] results from your Java program.
[03:48] On top of that, whatever parameters are or whatever instance variables of your object you are trying
[03:54] to consider to calculate and hash code, the same set of instance variables or the same set of object
[04:00] parameters
[04:01] you need to consider for overriding the equals() method as well.
[04:06] I know you may have some confusion here, but don't worry when I'm going to discuss about equals() method
[04:11] along with an example, it is going to be super clear for you.
[04:15] Before I try to close this lecture, I want to highlight that in java7, a utility class called
[04:21] java.lang.Objects was introduced.
[04:25] So please note that objects is a plural here.
[04:28] So inside this Objects class we have an hash method which is capable of calculating the hash code based
[04:36] upon the input data that you are trying to provide.
[04:39] So whenever you have a requirement to calculate your own hash code based upon your own requirements,
[04:46] you don't have to start from scratch to calculate the hash code
[04:50] you don't have to write the hashing algorithm.
[04:52] You can just invoke these hash method available inside the Objects class
[04:57] and to this hash method you can
[04:59] provide the input data that needs to be considered to calculate the hash code and behind the scenes.
[05:06] This hash method is going to take care of calculating the hash code and returning the same.
[05:11] So let's try to see this hash method inside IntelliJ.
[05:14] First we need to open the utility class with the name Objects.
[05:18] So please note that this is a plural form, whereas the superclass object it is a singular form.
[05:24] So I'm trying to open this Objects class.
[05:26] And inside this class we have a static method hash, which is going to return the int value as an
[05:33] output, which means it is going to return the hash code as an output.
[05:37] To this method, you can pass input data
[05:39] when I say the input data.
[05:41] This input data can be the instance variables available inside your current object.
[05:47] So based upon all these instance variables data that you're trying to provide behind the scenes, this
[05:52] hash method, it is going to invoke the hashing process.
[05:55] And it returns the hash code value based upon the input data that you are trying to provide.
[06:00] So here you can see we have three dots.
[06:02] So this indicates variable arguments.
[06:05] Long back I discussed about these inside the course.
[06:07] So whenever you have these three dots inside your method input signature that conveys we can pass any
[06:14] amount of input data as an input to this method I can pass one object or two objects or three objects
[06:22] so there is no limitation.
[06:23] I can send any amount of objects as an input data to this method.
[06:28] I hope you are clear.
[06:29] If something is not clear, don't worry, I'm there for you.
[06:31] I'm going to make it super clear for you around these.
[06:34] When we are discussing about the equals() method, I'm also going to show you an example on how to override
[06:41] hashCode() and equals() method in the coming lectures.
[06:44] For now, please make a note of all the rules that we need to follow whenever we are trying to override
[06:50] the hashCode() method.
[06:51] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
