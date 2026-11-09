# 22.8 — Demo of EnumSet and it's important methods

> Section 22: Enums in Java

[00:00] Inside Java Collection Library, there is a Set which is built specifically to deal with the enums.
[00:08] The set name is EnumSet.
[00:11] If you can type EnumSet, there is an abstract class inside the java.util package.
[00:16] You can see this is a sealed abstract class which extends AbstractSet.
[00:21] There are good amount of methods inside these EnumSet class that we can leverage.
[00:27] Whenever we are trying to deal with the enums.
[00:30] Understanding these methods will give more power to you whenever you are trying to write business logic
[00:35] that handles lot of enums.
[00:37] So let's try to understand few of the important methods available inside this EnumSet.
[00:42] To show you the demo, I'm going to create a new Java class with the name EnumSetDemo.
[00:50] Inside this class I'm going to create the main() method.
[00:53] The very first static method that we can explore is allOf() method. Inside EnumSet abstract class
[01:00] there is a method which is allOf() to this
[01:02] if you pass your enum class like Day.class, we have a enum data type with the name day.
[01:09] Inside
[01:09] this day we have created days like Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday.
[01:15] Using these Day class,
[01:16] if you try to invoke this allOf() method, it is going to give you an object of EnumSet, which is
[01:22] going to hold all the enum constants that you have defined inside these Day.class.
[01:27] So on the left hand side I can try to catch the output with the help of EnumSet and inside the angle
[01:33] brackets
[01:33] I need to mention that enum data type which is day Post
[01:37] I am going to give the variable name as all days.
[01:41] Now using this test, I can try to understand what are the constants available inside my enum data type.
[01:48] For example, I can iterate all of them with the help of these all days.
[01:53] I'm trying to build an for each loop on the left hand side I need to catch the output, which is day.
[01:59] The temporary variable name as day, and inside these for each block
[02:03] I'm trying to print out that day details.
[02:06] So if I execute this program, you'll be able to see all the days that I have stored inside my Enum.
[02:12] So the order also is being maintained by my EnumSet.
[02:15] So whatever order I have defined inside my Day.java class, the same is trying to maintain inside
[02:21] my EnumSet as well.
[02:23] So this is one method which you can use whenever you are trying to convert your enum details into the EnumSet.
[02:29] Just like allOf() method, we also have of() method.
[02:33] So using EnumSet we can invoke the of() method.
[02:36] So there are overloaded of() methods.
[02:39] We can invoke any one of them.
[02:41] And to this of() method we can pass enum constants.
[02:44] For example, here I'm trying to pass day comma Monday followed by day comma Tuesday.
[02:52] And at last I am trying to pass Wednesday.
[02:54] So with these information that I'm trying to provide to the of() method, I'm going to get a new
[03:00] EnumSet object which is going to hold only the given enum constant objects on the left hand side.
[03:06] Let me catch the output with the help of EnumSet and by mentioning angle brackets and inside this angle
[03:12] brackets, I can mention day followed by
[03:14] I can provide the variable name as some days if the same, some days if I try to print out.
[03:20] With the help of this for each, I will be able to see the output only the days that I have passed to
[03:27] my EnumSet with the help of these of() method.
[03:30] So let me execute this program.
[03:31] This time you should get only three days like Monday, Tuesday, Wednesday, so you can always use this
[03:36] of() method whenever you want to process only a subset of enum constants, whereas allOf() method it
[03:43] will convert all your enum constants present inside a enum data type.
[03:47] The next important method that we can explore inside EnumSet is range method.
[03:52] So let's see what is the documentation of this range() method.
[03:55] So using these range() method we can create an EnumSet initially containing all of the elements in the
[04:02] range defined by the two specified end points.
[04:06] For example, whenever you are trying to process only a range of enum constants in all those scenarios,
[04:12] you can invoke these static method range() which is available inside the EnumSet class to show you the
[04:18] demo around the range.
[04:19] What I can do is I'm going to create a new enum type with the name grades.
[04:26] Inside this enum, I'm going to create constants representing various grades like A, B, C, followed
[04:33] by D, and at last I'll mention E.
[04:36] So what I'm going to do is I want to construct these first three gates as a pass grades, whereas the
[04:42] last two grades as failed grades.
[04:44] So whenever I have a requirement only to process the pass grades inside my business logic, then I can
[04:50] use a range() method to get these three grades, which are A, B, C.
[04:55] Let's try to invoke the range() method with the help of these Grades enum. For the same inside
[05:00] my EnumSetDemo class, I need to invoke the range() method to this range() method I need to pass what
[05:07] is the starting element and what is the ending element.
[05:10] So both of your elements are going to be inclusive.
[05:14] So the first element that I want to construct to calculate the range is a
[05:18] and the end element that I want to consider is C.
[05:22] Since these greats are also inclusive.
[05:24] So all the enum constants like A, B, C, they are going to be provided as a new EnumSet object.
[05:32] That's why on the left hand side let me type EnumSet and inside the angle brackets.
[05:36] This time I need to type grades followed by
[05:39] I'm going to mention the variable name as passGrades.
[05:42] Now think like for all these passGrades, I want to process them with a for each loop.
[05:48] So let me copy these for each loop.
[05:50] And here I'm going to use a passingGrades.
[05:53] And instead of Day we need to mention Grades.
[05:56] And the temporary variable name I'm going to mention as grade.
[05:59] The same
[06:00] if I try to print out, I'm going to get the grade details like A, B, C.
[06:05] Here
[06:06] I'm just trying to write a simple business logic which is just printing them.
[06:09] But in real projects you may have some complex requirements, like if someone has so and so grade,
[06:15] consider them as a passed.
[06:17] Otherwise consider them as fail.
[06:18] So to handle those kind of scenarios, you can use these kind of for each loop to iterate all the enum
[06:24] constants.
[06:25] The next important method that we have inside EnumSet is complementOf() method.
[06:31] So let me invoke these complementOf() method to these complementOf() method
[06:36] if you pass any of the EnumSet the enum elements which are not present inside these pass grades,
[06:44] it is going to give as an output.
[06:46] My compiler will note that these pass grades is built with the help of Grades enum, and inside these
[06:51] passGrades we have only three enum constants like A, B , C.
[06:55] Since we are using complement of the output EnumSet object from this method, it is going to hold the
[07:02] grades like D.
[07:03] So that's why on the left hand side I can mention EnumSet with the angle brackets as grades and with
[07:11] the variable name as failGrades.
[07:13] So if you try to print out these failGrades, you will get the failGrades which are D and E.
[07:19] So
[07:20] so let me execute this program and you'll be able to see at the end we have the fail grades which are
[07:26] D and E.
[07:27] So always use complementOf() method.
[07:29] If you are looking to get the remaining enum constants which are not present inside a given EnumSet
[07:36] object.
[07:37] So these are the four important key methods that you can use on day to day basis inside your projects.
[07:43] So there are more good amount of methods as well
[07:46] inside EnumSet.
[07:47] We can't discuss all of them, but I just wanted to give some inputs that there is a Collection Set
[07:53] class available focusing enum data types.
[07:56] So whenever you have some complex requirements to process your enum constants, always come to the enum
[08:02] set and try to look a method that is going to solve your business problem.
[08:06] I hope this makes sense to you.
[08:08] The details of the four important methods of enum set I have mentioned here along with the example code.
[08:14] Please refer to them for any questions.
[08:16] Thank you,
[08:17] bye.

----------------------------------------
