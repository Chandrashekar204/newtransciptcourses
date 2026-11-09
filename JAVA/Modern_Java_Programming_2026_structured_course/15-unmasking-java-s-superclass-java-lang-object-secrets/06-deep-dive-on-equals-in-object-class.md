# 15.6 — Deep dive on equals() in Object class

> Section 15: Unmasking Java's Superclass(java.lang.Object) Secrets

[00:00] Have you ever seen identical twins?
[00:02] They are going to look very similar, but physically they are two different persons.
[00:08] On a similar lines, inside Java also we may have different objects, but they may store same kind of
[00:17] data.
[00:17] So whenever you have some scenarios where you want to identify whether two objects are same or not.
[00:24] In such scenarios you can use the equals() method.
[00:28] By default, the equals() method it is going to return the output as true if the two different objects,
[00:35] they are pointing to the same memory location.
[00:38] So whenever you are trying to invoke the equals() method, you're going to use an object reference.
[00:43] So the object that you are trying to invoke your equals() method, that is going to be considered as the
[00:48] object one.
[00:49] And whatever object you are trying to pass an input to these equals() method that is going to be considered
[00:55] as the second object by default
[00:58] this is the logic that equals() method is going to have behind the scenes.
[01:02] So it is going to simply compare the current object with the object that we are trying to pass as an
[01:09] input with the code.
[01:10] Like you can see this is equal to is equal to object.
[01:13] So this default code is going to check if both objects they are referring to the same memory location.
[01:19] In such scenarios it is going to give the value as true.
[01:22] Otherwise it is going to give the value as false.
[01:24] But this default behavior may not be useful if you have your own custom requirements, because with
[01:31] this default behavior will only get the output as true if you're trying to compare the same single object
[01:38] with the help of equals() method.
[01:40] Because we know whenever we are using the new operator inside Java to create an object, it is definitely
[01:47] going to create at a different memory location.
[01:49] With that, we are always going to get the output as false with this default behavior, but sometimes
[01:56] we may have requirement to not compare the objects by referring to their memory location.
[02:01] Instead, we want to compare the objects by looking into the content of the objects.
[02:06] So inside objects we know we have various attributes or various instance fields.
[02:12] If those instance fields, if they hold the same data, we want the equals() method to return as true,
[02:19] otherwise false.
[02:20] In such scenarios, overriding that default equals() method is going to be more meaningful
[02:26] to compare your objects based upon the content of them are based upon the attributes present inside
[02:32] them.
[02:32] Let me show you a demo around this, so that it is going to be super easy for you to understand.
[02:37] As of now, we have a Person class which is empty.
[02:41] Inside this I want to create various instance fields like private String with the variable name as name.
[02:49] Similarly, I will also create another variable with the data type as int followed by private char gender.
[02:58] And at last I'm going to create an int variable with the name ssn.
[03:03] So what is SSN,
[03:05] in United States
[03:06] SSN means Social security number.
[03:08] This is a unique number that each person staying in United States is going to have very similarly inside
[03:15] your country
[03:15] also, you may have unique number like tax identification number or passport number.
[03:21] It can be any number.
[03:22] But for now let's consider this SSN, which is going to be unique for each and every person who is going
[03:28] to stay in a country.
[03:29] For these four variables, I want to generate a parametric constructor and the getters and setters.
[03:35] So how to do that?
[03:36] We just have to place the cursor at the end and right click on it and post that
[03:41] we can click on this generate followed by I'm going to select constructor and to the constructor
[03:47] I want to consider all the instance fields as the input parameters.
[03:51] That's why I have selected all of them.
[03:53] And I'm clicking on this okay button.
[03:55] And with that you can see I have an constructor which is going to accept the four different variables
[04:02] as an input.
[04:03] The same is going to be assigned to these variables present inside the class.
[04:07] With the help of these, this.name and this.age and this.gender and this.ssn.
[04:13] After this constructor, I also want to generate the getters and setters method.
[04:18] So let me right click on this.
[04:20] Click on the generate button.
[04:21] Post that I'll select this getter and setter followed by I'm going to select all the fields and post
[04:27] that I'm clicking on these okay button.
[04:29] And with that you can see for each instance variable I have a getter method which which I can use to
[04:35] fetch the data from an object.
[04:37] And similarly I have a setter method which I can use to set the data or to override the data inside
[04:45] an object.
[04:46] So this is a classical representation of Pojo object that we have discussed long back.
[04:51] So the purpose of Pojo classes is to carry the data from one location to other location, like from
[04:58] UI application to the backend
[05:00] or from the backend code to the database layer.
[05:02] So the purpose can be anything.
[05:04] These Pojo classes, we can treat them as simple data carrier classes.
[05:09] So inside this I'm not going to define any other business logic.
[05:12] With the help of static or instance method, I'm going to simply have the methods, which is going
[05:18] to help me to store the data or to fetch the data.
[05:21] So with this Person class, first let's try to see the how the hashCode() and the equals() method is going
[05:27] to work by taking that default behavior from the Object class. For the same, I'm going to create a new
[05:33] Java class.
[05:34] The class name I'm giving here as HashCodeEqualsDemo inside this class
[05:41] first, as usual, I'm going to create main() method
[05:45] inside this main() method I'm going to create two different Person objects.
[05:49] So let me create a Person one object with the object variable name as p1 and followed by I'm going
[05:57] to invoke the constructor of the Person.
[05:59] So we don't have default constructor inside the Person class, because we have declared the parametric
[06:05] constructor.
[06:06] Like you can see.
[06:07] That's why we are getting a compilation error.
[06:09] If you are trying to invoke that default constructor which is not present inside our class.
[06:13] So to these constructor I can pass input data saying that the name I'll pass as John, followed by the
[06:21] age I'm going to mention as 25, followed by the gender I'm going to mention as M, which is a single
[06:27] char, and at last I'm going to mention the SSN number as 564323456.
[06:34] So this is a SSN number.
[06:36] So with the same data I want to create one more Person object.
[06:41] This time I'm going to give the object to reference variable name as p2.
[06:46] Since we are using this new operator definitely these two different Person objects.
[06:50] They are going to be created with the two different memory locations inside the heap memory.
[06:56] So they are physically representing two different Person objects.
[07:01] We can also confirm the same by printing the hash code of the Person one with the help of
[07:08] p1.hashCode().
[07:09] And similarly I'm going to do the same for p2 object also.
[07:13] So in this scenario, definitely we are going to get that two different hash code values, because the
[07:18] default behavior of the hashCode() method is to generate the hash code value based upon the memory location
[07:25] of the object.
[07:25] Since these p1 and p2, they are stored at a two different memory locations, we are going to get the
[07:31] two different hash code values.
[07:33] Similarly, if I try to invoke the equals() method with the help of p1 like you can see after p1,
[07:40] I'm trying to invoke the equals() method, and as an input to the equals() method, we can pass the second
[07:47] object that we are trying to compare.
[07:49] So from these equals() method
[07:51] also I'm going to get the output as false because by default the equals() method it is going to compare
[07:58] the memory locations of the two different objects.
[08:01] That's why we are going to get the output as false.
[08:05] Let me execute this program.
[08:06] But before I try to execute this program, I'm getting a compilation error in a GetclassDemo because
[08:12] we don't have any default constructor inside the Person class.
[08:16] So to resolve this I can try to create a default constructor.
[08:21] So let me mention public person with a empty parentheses followed by curly braces.
[08:27] So I'm not going to do anything with these
[08:29] default constructor I just created these to resolve the compilation error that I'm getting inside this
[08:35] GetclassDemo.
[08:36] So now I'll go to the HashCodeEqualsDemo class.
[08:40] And here I'm going to execute my program.
[08:42] And you will be able to see in the output the hash code values of the p1 and p2 objects are different.
[08:48] And we are also getting the output from the equals() method as false.
[08:52] So this is that default behavior.
[08:54] But like I said in real projects you don't want to consider these two different Person objects as two
[09:00] different objects.
[09:01] Because if you see the content, it is representing the same person.
[09:06] Maybe behind the scenes, Java has created two different objects at two different memory locations,
[09:12] but they have a same content like they are representing same person.
[09:17] John with the age 25 who is a male and with so and so SSN.
[09:21] Logically, for your business logic, you should treat these two different objects as equal, otherwise
[09:28] you will end up in unexpected results.
[09:31] Think like you are writing a business logic to process a payment for a person.
[09:36] So if you are going with the default equal and default hash code logic, you're going to make the two
[09:42] time payment for two different objects, but you will end up paying the same physical person who is
[09:48] staying in a country.
[09:49] To overcome these kind of challenges, we can communicate to the JVM saying that whenever a Person object
[09:55] who is having the same name, same age, same gender
[09:59] and same SSN.
[10:00] So the combination of these four parameters, I want to consider them as a same Person.
[10:06] So to communicate these two JVM we can overwrite the equals() and hashCode() method.
[10:13] I hope you are clear on why we should override these default provided equals() and hashCode() method.
[10:19] So let's try to continue this discussion in the next lecture as well.
[10:23] Thank you,
[10:24] bye.

----------------------------------------
