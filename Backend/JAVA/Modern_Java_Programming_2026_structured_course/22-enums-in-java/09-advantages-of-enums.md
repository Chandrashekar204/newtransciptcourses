# 22.9 — Advantages of Enums

> Section 22: Enums in Java

[00:00] By this time, it should be pretty clear for you that enums are the clear winner compared to the traditional
[00:07] Java constants.
[00:09] Inside this lecture, let's try to discuss about the advantages of enums so that it is going to help
[00:15] you inside your Java interviews.
[00:16] Because inside Java interviews, many times people may ask you, why should we use enums when we can
[00:22] achieve the same job with the help of Java constants?
[00:26] That's why let's try to understand the advantages one by one, the very first, and a major advantage
[00:31] that we are going to get with the help of enums is type safety.
[00:35] Enums provide type safety by allowing developers to define a fixed set of named values.
[00:41] So this will stop other developers to use invalid values or wrong data types as an input to the business
[00:49] logic, like we saw in the previous lectures demo.
[00:52] Whenever we are using enum as an input parameter, other developers, they will be able to invoke my
[00:58] method only if they are passing a valid value of enum.
[01:02] The second advantage is around the readability.
[01:04] Enum makes our code more readable by providing a clear and concise way to represent a fixed set of related
[01:12] constants.
[01:13] I saw many projects in my career where they are not using enums.
[01:17] What they are going to do is, they are going to put thousands of constants inside a single Java file,
[01:22] and it is going to make developers life tough.
[01:25] Whenever someone is looking for a particular scenario constant, they need to end up searching that
[01:31] entire file.
[01:32] And sometimes they may have constants with very similar names as well.
[01:37] Whereas with enums we can build multiple enum data types which are going to hold the constants based
[01:43] upon a particular scenario.
[01:44] For example, if someone is looking for the constants which are related to the task priority, they
[01:50] can find all the constants related to the task priority inside the PriorityEnum class.
[01:55] As a standard, we know developers
[01:57] they are not going to maintain other scenario constants inside the PriorityEnum class.
[02:02] So that's why using enums is always going to improve the readability of your code.
[02:07] The next advantage is around the robustness enums.
[02:10] They are going to make your code more robust by providing a centralized and consistent way to handle
[02:17] a set of related constants.
[02:19] If the help of enums, we are going to make our life easy to modify the code in future without introducing
[02:26] bugs.
[02:26] So whenever I want to introduce a new constant, or whenever I want to change a value of my constant
[02:32] or date of my enum constant, the change is always going to be in a single place.
[02:37] We don't have to worry about compiling the multiple dependent files.
[02:41] After robustness, we have the advantage around the code organization.
[02:45] Like we discussed previously.
[02:46] With the help of enums, we can group related constants together in a particular file.
[02:52] In all the previous lecture, we have created so many enum classes one to store the priority related
[02:57] constants, other to store the day related constants, and the other one related to the size related
[03:03] constants.
[03:03] So whenever you are following enums, you will end up organizing your code and constants based upon
[03:09] your scenario.
[03:10] And the last advantage is around the switch statements we saw in the previous lectures
[03:14] how easily we can use the enums along with the switch statements or switch expressions.
[03:20] By combining both enum and switch blocks, we can write business logic to handle a set of related cases.
[03:27] So these are the advantages on using the enums.
[03:30] So my humble request always is to implement the constant logic with the help of enums wherever possible.
[03:37] I hope this makes sense to you.
[03:38] And now you have a good understanding around the enum concept.
[03:42] Thank you and I'll catch you in the next lecture, bye.


########################################
