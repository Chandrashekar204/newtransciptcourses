# 9.16 — Deep dive on POJO classes - Part 2

> Section 9: packages in Java

[00:00] As of now we have created a Pojo class with the name Person.
[00:04] How can we call this class as a Pojo class?
[00:07] Because it has only logic related to that data transfer.
[00:12] I only have the fields which I can use to transfer the data from one place to other place, but like
[00:18] I said before, we need to follow certain standards or best practices whenever we are trying to declare
[00:24] a Pojo Java class.
[00:26] So let's try to understand what are those standards.
[00:28] Before I try to explain those standards, first let me show you that drawback with this approach.
[00:33] With this approach, anyone can write a logic to create an object, and with the help of the object,
[00:39] they're able to access my variables directly.
[00:43] So there is a serious drawback whenever someone is able to access your Java fields directly.
[00:49] The drawback is think like instead of 25
[00:52] here
[00:53] if I mention the age as 125, do you think it is going to be valid?
[00:58] off course not.
[00:59] So I will not be able to enforce any validations or restrictions if I allow to populate data directly
[01:07] with the help of the Java fields that I have defined inside the person Pojo class.
[01:12] So how to overcome this issue?
[01:13] First, you should always make sure you are defining your fields as private.
[01:19] So always inside your Pojo classes, you should always define your fields as private.
[01:25] For that reason, let me try to replace all public with private keyword.
[01:31] So with this, no one can access my fields directly from other classes.
[01:37] That's why I'm going to get a compilation error here.
[01:40] The next question you may have is, then how can people can populate the data or fetch the data?
[01:46] So whenever a developer is trying to work with a Pojo class, they'll be only two scenarios he will
[01:52] be focusing.
[01:53] The very first one is he want to set some data into the Pojo object.
[01:58] The other scenario is he want to get information from the Pojo object.
[02:03] So to handle these kind of possible scenarios, we need to define the getter and setter methods for
[02:10] your Java fields.
[02:12] So how to define them.
[02:13] So there is an easy way to define getter and setter methods for your Pojo class
[02:18] java fields.
[02:19] The easier process is
[02:21] first, you need to highlight all your Java fields like this and post that right click
[02:26] and here there is an option of generate.
[02:29] And inside the generate option you have an option to generate the only getter methods or setter methods
[02:36] or getter and setter methods as well.
[02:39] So for now I'm going to select the option which is getter and setter.
[02:43] And here in this window it is asking you for which fields I want to generate the getters and setters.
[02:50] So let me select all of them and click okay.
[02:52] And with that you can see I have the getters and setter methods.
[02:56] But since my cursor is present just after the first name, all these methods are created in between
[03:03] my Java fields.
[03:04] So let me select all these fields and remove them.
[03:08] Post that
[03:08] just after this Java fields I'm going to paste again.
[03:12] So now you can see for each Java field like firstName, lastnName, age and salary I have a getter
[03:19] method and a setter method.
[03:21] So what is the purpose of a getter method?
[03:23] Whenever someone wants to read the data from my person Pojo object, they can simply invoke these
[03:30] getFirstName() method and this method is going to return the field firstName which is present inside
[03:37] the given object.
[03:38] That's why the return type of this method is always going to match with the data type that you have
[03:43] defined as part of the variable declaration.
[03:46] Now coming to the setter method.
[03:48] So the setter methods will be used only in the scenarios when someone wants to populate the data inside
[03:55] your Pojo object.
[03:56] So here I can write a logic inside this setAge() method, like in the scenarios, whenever someone want
[04:02] to populate the age data with the help of this set, I can write a if logic here saying that if age
[04:10] greater than 100, I'm going to throw an exception like we are ready to discuss about exceptions, but
[04:18] that's fine for now
[04:19] I'm just trying to throw an error or an exception if someone send me an invalid data.
[04:24] So the exception that I can throw here is runtime exception, and to this exception constructor I can
[04:31] pass the data which is invalid age details sent.
[04:36] But here I'm getting a compilation error because before we try to throw an RuntimeException, first
[04:42] we need to create the object of the RuntimeException.
[04:44] So how to create it with the help of new operator.
[04:47] So with this you can see I'm trying to throw an object of RuntimeException with this message.
[04:52] Like in case if someone is trying to send the age details which are greater than 100, I will throw
[04:57] this exception otherwise.
[04:59] I'll just try to write the logic, which is this.age = age, like whatever age that I'm going
[05:07] to receive as part of this setAge(), the same I'm going to set to the Java field that I have defined
[05:13] inside this Pojo class.
[05:14] This way we can also enforce some validations or conditions whenever someone tries to fetch your data
[05:21] as well.
[05:22] Think like for one of the person.
[05:24] I don't have the lastName details saved inside that database.
[05:28] And with that, whenever someone is trying to fetch the lastName from a given Person object, they'll
[05:34] get the value as null because the default value of String is null.
[05:38] So instead of returning a null value always in the scenarios where the lastName of a Person is not
[05:44] available in such scenarios, I can simply return a String value, which is unknown.
[05:50] So here first I'm going to perform the null check of the lastName.
[05:55] If null == lastName
[05:58] I'm going to return a String variable which is Unknown.
[06:04] Otherwise I'm going to simply return the this code which is written lastName.
[06:10] So these kind of control you will not have if you try to access the fields directly with the help of
[06:17] the variable names.
[06:18] That's why we need to always create the setter and getter methods for your fields present inside the
[06:25] Pojo class.
[06:26] So now if someone wants to populate the data, they can first invoke the setter method like setFirstName()
[06:32] and to this firstName method they can pass the data like John, and similarly they can also invoke
[06:40] the other method which is setLastName().
[06:43] And to this method we need to send Doe
[06:45] let me do the same for age and salary as well.
[06:49] So let me invoke the setAge() method.
[06:53] And to this I'm going to pass the data 25, followed by I'm going to invoke the setSalary() method and
[07:00] to this I'm going to pass the salary details which is 10,000 .00.
[07:06] So this is how you need to populate the data with the help of setter methods.
[07:10] If you have a scenario where you want to fetch the data, then in such scenarios you can simply use
[07:15] the getter method.
[07:16] For example, think like I want to display the first name of the person so I can use a person object
[07:23] post that I can invoke the getFirstName() method.
[07:26] So if I try to execute this program, you will be able to see the first name displayed on the console.
[07:32] I hope you are clear
[07:32] what is the purpose of getter method and setter methods.
[07:35] So always your getter and setter methods
[07:38] they are going to have the public access modifier that is the standard.
[07:42] Otherwise the other classes present inside other packages they will not be able to access.
[07:47] So always make sure you are defining your fields as private and you are getter and setter methods as
[07:53] public inside the Pojo class.
[07:55] So if you closely observe the logic present inside the Person Pojo class, we strictly write everything
[08:02] to store the data or to fetch the data.
[08:04] So these kind of classes we call them as Pojo classes.
[08:09] I have methods inside these Person class, but these methods, they don't have any other business logic
[08:15] other than storing the data or fetching the data.
[08:18] All the details that we have discussed around the Pojo class I have mentioned inside this slide.
[08:23] So there are some advantages that we are going to get if you transfer your data with the help of Pojo
[08:29] classes.
[08:29] So the advantages are Encapsulation, Data validation, Flexibility and Access control.
[08:35] With the help of Pojo class, you're not exposing your Java fields directly.
[08:39] You are encapsulating them or you are hiding them from the using class.
[08:44] So anyone who wants to access your Java fields, they need to come through the getter and setter methods.
[08:51] And if needed, you can perform some data validations like we discussed.
[08:54] And with the help of these getter and setter methods, we are also going to get some flexibility.
[09:00] For example, we can add additional logic to a setter method or a getter method, such as logging or
[09:06] triggering some other action without changing anything on the fields declaration.
[09:11] And at last, with the help of this Pojo classes, we are able to control the access of our Java fields.
[09:17] So always other Java classes, they have to come through the getter method and setter methods to access
[09:24] our Java fields.
[09:25] I hope you are clear.
[09:26] There are other names also for the Pojo classes.
[09:29] The other names are like DTO objects and Java beans.
[09:33] So if someone asks you to build a DTO or Java Bean, the process is going to be very similar to Pojo
[09:39] class.
[09:39] It's just a different naming convention that they are trying to use.
[09:43] So some projects they'll call it as DTO and some projects they call it as Pojo
[09:47] and some people they will call it as Java Beans.
[09:50] So regardless of whatever is the name, the concepts and the rules that we have discussed inside this
[09:55] lecture, always going to be the same.
[09:57] I hope you are clear.
[09:59] Thank you
[09:59] and I'll catch you in the next lecture bye.


########################################
