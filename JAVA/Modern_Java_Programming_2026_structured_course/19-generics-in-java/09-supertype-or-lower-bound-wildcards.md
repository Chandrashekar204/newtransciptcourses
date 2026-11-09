# 19.9 — Supertype or Lower Bound Wildcards

> Section 19: Generics in Java

[00:00] Inside this lecture, let's try to understand another flavor of generics, which is Supertype are lower
[00:06] bound wildcards.
[00:07] This syntax is exactly opposite to what we have discussed in the previous lecture.
[00:13] Just like how we have covariance in the similar lines, we also have contravariance.
[00:19] Contravariance refers to the ability of a type to accept a more generic, broader types. With the help
[00:26] of Upper bound wildcards that we have discussed in the previous lecture, we are going to restrict the
[00:31] unknown type to be a specific type or a subtype of that type, whereas with the help of lower bound
[00:37] wildcards, we can restrict an unknown type to be a specific type or a super type of that type.
[00:42] How to define this lower bound wildcards.
[00:45] It's very simple.
[00:46] Inside the angle brackets after the question mark, you need to mention super, whereas for the upper
[00:51] bound wildcard we used to mention extents, but coming to the lower bound of wildcards, we need to
[00:56] mention the super.
[00:57] And what is the generic type.
[00:58] So here I'm trying to mention the type as A.
[01:00] We can only specify either an upper bound for a wildcard or a lower bound, but we can't specify
[01:07] both of them.
[01:08] So that's an important note that you need to be aware.
[01:10] Now let's see an example to understand more details about the lower bound wildcards usage.
[01:16] Like you can see here, there is a method with the name addNumbers.
[01:20] This method is going to help me to add the elements inside a List object.
[01:26] My business requirement is to add the integer numbers inside this, but I want to make this method more
[01:32] flexible by making these.
[01:34] To be able to add elements that belongs to Integer object are its super class.
[01:39] Integer class has super class like number and the number has a super class object.
[01:45] Since I want to have a flexibility to store the objects of integer or number or object, I can use lower
[01:52] bound wildcards like you can see here.
[01:54] First I need to mention the question mark, followed by super followed by integer. With this
[01:59] now my List is going to allow me to add the objects of Integer or number
[02:04] or Object class.
[02:05] Whenever we are using lower bound wildcards, there is no restriction around adding the elements.
[02:10] In the previous lecture, while we were discussing about the upper bound wildcards, we saw that there
[02:15] is a restriction, which is we will not be able to add any element inside the collection, but with
[02:20] the lower bound wild cards, there is no such restriction.
[02:23] We should be able to add an object inside the collection, but the only constraint you have is you should
[02:30] try to add an object which is of Integer or it's a super type.
[02:34] Let's see the demo of Lower bound wild cards inside the IntelliJ here.
[02:38] This time I'm going to create a Java class with the name LowerBoundWildCardDemo.
[02:45] So let me update this to lower bound. Post that inside the class
[02:50] I'm going to create the main() method.
[02:53] After the main() method I'm going to create a static method.
[02:55] So let me type public static void followed by method name, which is addNumbers().
[03:02] Inside this method parentheses I'm going to mention List followed by angle brackets.
[03:08] Inside the angle brackets, I'm going to mention question mark, followed by super keyword followed
[03:14] by Integer. And post that I'm going to give a name to the parameter, which is List itself.
[03:20] If you try to open this Integer class, it has a super class which is number, and this number has a
[03:27] super class which is Object.
[03:29] We know every class inside Java has a super class which is Object.
[03:33] So with the lower bound wild cards that we are trying to use here, my List is only going to accept
[03:39] the objects of Integer, Number or Object inside this method.
[03:43] Let me write a for loop with the logic int I is equal to zero, followed by i < 10, semicolon
[03:52] i++, and inside the for loop I'm going to write List.add() and what is the index
[03:59] so here autoboxing is going to happen.
[04:01] And this i value is going to be stored as an Integer wrapper object.
[04:06] The same addNumbers() method I can try to invoke from the main() method to this method I can pass an
[04:13] ArrayList object.
[04:14] So let me invoke new ArrayList. Here just after the ArrayList inside the angular brackets.
[04:20] If I try to mention Integer, you can see I'm getting a warning saying that it is an redundant why are
[04:25] trying to mention because based upon the method input parameter, these ArrayList is going to be inferred
[04:31] to store either Integer or it's a super class objects.
[04:34] So in the place of Integer, if I try to mention some other data type like double, I'm going to get
[04:42] a compilation error because based upon these method input parameter, we are only restricting to use
[04:48] the List object that is only capable of storing integer or its super class objects.
[04:53] But this Double class does not have any relationship with this Integer.
[04:57] That's why we are getting a compilation error.
[05:00] So let me remove this,
[05:01] after making this change, we should be able to run this program.
[05:04] But before that let me try to add a System.out.println(),
[05:08] to print the List objects.
[05:10] So if I execute this program, you'll be able to see that these are the elements or objects added inside
[05:16] my list
[05:16] based upon the code that we have written here.
[05:19] Let's try to validate some negative scenarios here.
[05:22] You can see as of now we are trying to add Integer object.
[05:25] Maybe what I can do is I'll try to add and Double object by invoking the add() method.
[05:32] And to this add() method I can pass 3.14 as a value.
[05:36] You can see I'm getting a compilation error because I'm trying to provide a Double object, but the
[05:42] required type is this question mark super Integer.
[05:45] That means it is only going to accept either integer or its superclass.
[05:49] I hope this makes sense to you.
[05:50] Let me comment this code so that it is going to be available for your reference inside the GitHub repo.
[05:57] I hope you are clear about the Lower bound wild card.
[05:59] The reason why we call this syntax as Lower bound is, we are at max,
[06:04] we are restricting the data type to be a minimum of Integer.
[06:08] So that's a lower boundary.
[06:10] They can't go anything below the Integer class inside the interface hierarchy.
[06:16] So that's why we call this as Lower bound wild card.
[06:19] Lower bound wild card come into picture with the concept of Contravariance, whereas Upper bound wild
[06:25] card is associated with the concept of covariance.
[06:29] I hope you are clear with all the concepts that we have discussed so far.
[06:32] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
