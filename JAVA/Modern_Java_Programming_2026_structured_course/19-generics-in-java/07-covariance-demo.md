# 19.7 — Covariance Demo

> Section 19: Generics in Java

[00:00] As of now, we are building the generic classes or generic methods which are capable of processing any
[00:07] kind of data type objects.
[00:09] But in reality, the developer life is not going to be so easy and simple.
[00:14] Sometimes we may have a requirements to build a generic classes or generic methods which are capable
[00:21] of accepting or processing the objects which are inheriting from a particular superclass, or which
[00:27] are implementing from a particular interface.
[00:30] So these kind of complex requirements, you may get around the generics inside the real projects.
[00:36] As of now, we discussed the simplest flavor of generics, where you just mention the generic type as
[00:42] T and U, and with that, you are good to accept any kind of object.
[00:46] But there are more flavors around generics which are going to help you to impose some restrictions around
[00:52] that data type objects.
[00:53] We are going to discuss about those flavors in the coming lectures.
[00:56] But for now, before we try to explore about the other flavors of generics, first I want to teach you
[01:01] about an important concept inside this lecture, which is Covariance.
[01:06] For the same, I'm going to create a new Java class inside the same package that we have created previously.
[01:12] The class name I'm going to mention as CovarianceDemo.
[01:16] So Covariance is a concept inside Java which you need to understand to further explore about the other
[01:21] flavors of generics that we have inside Java.
[01:24] Let me create this class inside this class,
[01:27] first I'm going to create a main() method, followed by I'm going to write a static method which is capable
[01:34] of printing the array elements.
[01:36] So I'm just going to mention the method name as printArray().
[01:40] And inside this method I'm going to print all the elements present inside an array, which I'm going
[01:45] to receive as an input to this method, I'm going to add the method input parameter in few second.
[01:50] Before that, I want to create some model classes inside a new package.
[01:55] First, let me create a package with the name com.eazybytes.generics.model inside this
[02:00] model package, I'm going to first create a class with the name Employee.
[02:06] The same class I'm going to extend by other subclasses
[02:10] like
[02:10] first I'm going to create a Java class with the name Developer and this class it is going to extends
[02:16] the Employee superclass. In the similar lines,
[02:19] I'm also going to create one more Java class
[02:22] this time the name of the class is going to be manager and this manager class also going to extend the
[02:28] Employee superclass.
[02:29] For now, let's not worry about the code inside these classes.
[02:32] They can be empty classes.
[02:34] We don't have to implement any code inside them.
[02:37] Now let me go to the CovarianceDemo class here
[02:40] I'm going to update the printArray() method to accept an method input parameter of type Employee[] array
[02:47] and the parameter name I'm going to give as employees.
[02:50] Inside this method, I can write a logic, which is to iterate all the employees that we received inside
[02:57] the array employees the same
[03:00] I'm going to print them with the help of System.out.println().
[03:04] For now, let's not worry about what is the output that we are going to get.
[03:07] As of now, we are not storing anything inside these employee objects.
[03:11] That's why we are not going to get much useful information on the console when we try to print these
[03:16] objects.
[03:17] Now, inside the main() method I'm going to create an array of Employee[].
[03:22] First let me type employee followed by square brackets and the array name I'm going to mention as employees.
[03:28] And inside these I'm going to create a couple of employees with the help of constructor of employee
[03:34] class.
[03:35] So let me create two Employee objects.
[03:38] You can see the same I can send now to these printArray() method.
[03:42] I'm trying to send these employees as an input.
[03:45] If I try to execute this program I'll get some random output.
[03:48] You can see the objects are trying to be printed.
[03:51] Since we don't have any toString() method inside the Employee classes, we are getting these kind of information
[03:56] when we are trying to print the objects.
[03:58] What I can do is, I can try to generate a toString() method inside my Employee class.
[04:05] So as of now you can see I don't have any fields to consider inside the toString().
[04:10] I'm going to click on this okay.
[04:11] And with that I'm just going to get these statement whenever I try to print the object of Employee.
[04:17] So the same kind of logic I can try to do inside that developer as well.
[04:22] So let me try to generate the toString() method.
[04:26] And this time also I'm going to click on this okay button.
[04:28] Similarly I'm going to generate the toString() method inside the Manager class as well.
[04:34] Now if I go and execute this CovarianceDemo this time we are going to get some meaningful data.
[04:40] So it is an empty.
[04:41] We are getting at least whatever information we have mentioned inside the toString() method.
[04:46] As a next step, I want to create the objects of Developer and Manager the same I can try to create
[04:53] after this line of code.
[04:55] This time instead of Employee, I'm going to create the array of Developers
[04:59] with the variable name as developers.
[05:02] And inside this I'm going to create Developer objects, couple of Developer objects I'm trying to create.
[05:09] You can see I'm able to invoke the printArray() method with the developers as an input.
[05:15] In the similar lines, I should be able to do the same for manager as well.
[05:20] So let me try to create the Managers[] array, which is going to store a couple of manager objects.
[05:28] Once we create these Managers[] array, we can pass the same as an input to the printArray().
[05:33] If I execute this program, you can see I'm going to get a proper output based upon whatever I'm storing
[05:38] inside my objects.
[05:39] So this concept is called as Covariance.
[05:43] Inside the Java, whenever we write the code with a parent supertype, the same code can be used by
[05:50] the subtypes as well.
[05:52] So here I'm sending a subtype which is Manager and Developers.
[05:55] Still my code is working this kind of concept we call inside Java as Covariance.
[06:01] This Covariance exists throughout the Java.
[06:03] It's not only applicable for arrays.
[06:06] For example, I can try to create an String object with the name s
[06:10] and inside this I can try to store a value which is generics.
[06:15] Post that the same String object I will be able to assign to the variable of type object by using the
[06:23] code like you can see here, Object o = s, so this is perfectly is going to work inside
[06:30] Java due to the concept of Covariance.
[06:33] So String is a subtype of object.
[06:36] That's why this assignment is working without any problem.
[06:40] Let me show you one more example as well.
[06:42] This time I'm going to create an array of String [] with a variable name as sArray.
[06:48] And inside this array I'm going to store a couple of String objects which are generics followed by collections
[06:56] the same String object array
[06:59] I will be able to assign to the array of objects without any issues
[07:05] like you can see here, I am able to assign the String [] array object to the Object[] array.
[07:12] This is working perfectly due to the concept of Covariance.
[07:16] Let's try to implement the similar logic with the help of collections.
[07:20] Maybe what I'm going to do is instead of array object, I'm going to create an List object that is capable
[07:27] of storing the String objects.
[07:29] I'll just mention the name as sList, and to this on the right hand side, I'm just going to mention
[07:34] the ArrayList.
[07:35] And with that you can see I have an empty ArrayList object in the similar line.
[07:40] Let me try to create one more ArrayList object which is capable of storing object data type elements.
[07:48] So here I'm trying to mention object and the variable name I'm going to mention as oList, to this
[07:55] oList,
[07:55] if I try to assign the sList which is capable of storing Strings, I'm going to get a compilation error.
[08:02] Previously, the same code is working with arrays, but the same kind of concept is not working with
[08:08] the collections.
[08:09] This should give a confirmation to you that Covariance concept is not going to work inside collections.
[08:15] We should never try to do these kind of assignments because inside collections Covariance is not supported.
[08:22] With that, you may have a question, which is why collections does not support Covariance.
[08:28] Before I try to explain about the same, let me try to show you a drawback with the Covariance.
[08:33] As of now, we saw that Covariance is allowed inside array.
[08:38] So with that assumption, let me show you an example.
[08:41] Here I'm going to create an array of type number inside this numArray I can store any kind of numbers.
[08:49] For example I'm trying to store the numbers like one two, three. The same,
[08:53] I should be able to assign to the object array because Covariance is allowed inside arrays.
[09:00] So let me mention the variable name as objectArray is equal to numArray.
[09:06] So the Covariance is allowed.
[09:07] That's why you're not going to get any compilation error after this code,
[09:11] think like someone is trying to add an element into this array
[09:16] maybe at the zero index with an value called String.
[09:20] You can see my compiler is not complaining anything,
[09:24] it is trying to be dumb here.
[09:26] The reason is this is an array which is capable of storing objects.
[09:31] But if you try to see this array is originally created from an array which is capable of storing only
[09:38] the number objects.
[09:40] But my compiler is not able to detect that because inside arrays Covariance accepted.
[09:47] But if I try to execute this program, I'm going to get a runtime exception.
[09:51] You will be able to see I'm getting an exception which is ArrayStoreException.
[09:56] We are trying to fit a String object into array
[10:00] of type number.
[10:01] My compiler is not able to detect this issue at compile time just because covariance is allowed inside
[10:08] arrays.
[10:09] So Covariance has its own advantages, which is we can write the generic code like
[10:14] you can see here that I'm able to write the single method.
[10:17] And with the same single method I'm able to process all kind of array elements like Employees, Developers,
[10:24] and Managers.
[10:25] But with this advantage, we are also going to get a disadvantage like you can see here Java team when
[10:30] they build it arrays.
[10:31] Very first time they accepted the covariance since it supports writing lot of polymorphic code, but
[10:38] later on they realize it is going to have some runtime exceptions as well.
[10:42] That's why when they're trying to build a collections, they make sure that collections is not supporting
[10:48] Covariance.
[10:49] But that doesn't mean we can't write the polymorphic code like you can see here with the help of collections.
[10:55] There are other approaches which we can leverage to implement Covariance inside collections.
[11:01] We are going to discuss about the possible options that we have to implement covariance inside a collections
[11:07] object.
[11:08] But I'm assuming you're clear about what is a Covariance,
[11:10] why it is not allowed inside collections,
[11:13] what are the disadvantages that we have with covariance ?
[11:16] What kind of runtime exceptions that we are going to get with covariance?
[11:19] I hope this all makes sense to you.
[11:21] Before I try to close this lecture, let me show you a demo that collections are not going to accept
[11:26] covariance. For the same,
[11:28] I'm going to copy the same method inside the same class, but the method name I'm going to mention as
[11:34] printArray1().
[11:34] Post that I'll try to convert these array of Employee into the List of employee.
[11:41] And with that you can see we have a method ready which is capable of accepting the List objects of type
[11:48] Employee.
[11:48] Now I'll try to copy this code that we have and using the same kind of code, I'm going to write a logic
[11:56] to send the List of employee objects to the printArray()
[11:59] one method.
[12:00] So for the same first I need to mention List of Employee and I need to remove the square brackets,
[12:06] followed by
[12:07] I'll just mention this employees variable name as employees1.
[12:10] And after this I'm going to invoke the of static method available inside the List to create the couple
[12:18] of Employee objects.
[12:19] So let me copy these code and mention inside the off method and remove these curly braces.
[12:25] And with that, now I have a list which is storing couple of employee objects. The same,
[12:30] I should be able to send as an input to the printArray1() method.
[12:34] Now, as a next step, let me try to create one more List object which is capable of storing the developer
[12:42] objects.
[12:43] So here I'm going to mention List of developer and I'll change this variable name as developers one,
[12:49] followed by I'm going to create couple of developer objects and save them inside this List object which
[12:56] is developers one.
[12:57] Now you can see the surprise here.
[12:59] If I try to send these developer one as an input to the printArray1() and getting a compilation error
[13:04] saying that the printArray1() method is expecting a input of list employee, but I'm trying to send
[13:11] the list to developer.
[13:12] But according to us, this should work because developer is a subtype of employee.
[13:18] But why it is not working?
[13:19] It is not working because inside collections Covariance is not supported.
[13:24] We should never treat list of Employee as a subclass of list of Developer that is not allowed inside
[13:31] Java.
[13:32] I hope you are clear about Covariance concept from the next lecture,
[13:35] let's try to explore the other flavors of generics that we have inside Java.
[13:40] In the same process, we can try to understand how to overcome these covariance restrictions inside
[13:46] collections.
[13:46] I'm going to comment this line of code for your reference, and I'll check in this program for your
[13:51] reference as well inside the GitHub repo.
[13:53] Thank you and I'll catch you in the next lecture, bye.

----------------------------------------
