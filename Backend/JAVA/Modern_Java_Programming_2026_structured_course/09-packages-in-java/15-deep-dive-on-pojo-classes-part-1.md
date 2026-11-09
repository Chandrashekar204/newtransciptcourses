# 9.15 — Deep dive on POJO classes - Part 1

> Section 9: packages in Java

[00:00] Once you join an organization and started building the real applications with the help of Java programming
[00:06] language, you will hear a jargon lot many times from the senior developers or tech lead inside your
[00:13] project.
[00:14] The jargon is Pojo.
[00:16] So what is the full form of Pojo?
[00:18] Pojo
[00:19] Full form is Plain Old Java Object, and whenever you hear the jargon inside real projects, you may
[00:26] think why Madan didn't explain about Pojo classes inside the Java course.
[00:32] Are these some special kind of Java classes and what is the syntax to create the Pojo Java classes?
[00:37] You may have all these kind of questions, but I want to clarify all those questions to you inside this
[00:43] lecture so that when you start hearing about these jargon, a lot of times inside your real projects,
[00:49] you will feel comfortable and confident to create the Pojo classes.
[00:53] To explain you about Pojo classes, I'm going to create a class inside the model package.
[00:59] The class name
[01:00] I'll keep it as person.
[01:02] Inside this class I'm going to create the fields.
[01:06] The fields are going to be like String firstName.
[01:10] Similarly, I'm going to mention String lastName.
[01:14] So here for now I'm not mentioning any access modifiers.
[01:17] I'll share more details about which access modifier that you need to mention in few minutes.
[01:22] And after that I'm going to mention int age followed by double salary.
[01:29] So these are the details that I want to store with the help of the objects that I'm going to create
[01:35] with this Person class.
[01:37] Whenever we use a Java class, just to transfer the data from one place to other place, we can call
[01:44] such classes as Pojo classes.
[01:46] I'm not going to write any business logic inside this Java class.
[01:51] I'm going to simply use this class to transfer the data from one place to other place.
[01:57] Think like you have an UI application.
[01:59] There is a HTML page which you are going to show you to your end user inside the browser.
[02:05] So there will be some scenarios where you may ask your end user to enter his details, like what is
[02:10] your first name, last name, age, salary?
[02:13] Once the end user entered his details inside the UI application, the same need to be transferred to
[02:20] the back end server where you have written the business logic with the help of Java programming language.
[02:26] So how the transfer is going to happen.
[02:28] So there are multiple approaches.
[02:30] The very first basic approach is, each of these fields you can send individually.
[02:35] If you're asking ten different types of information on the UI page, then you can send all those ten
[02:41] different types of information with the respect to Java fields on the backend, but that's not a recommended
[02:49] approach.
[02:49] Instead, you need to define all the fields related to your person inside a class like this.
[02:55] And whenever the UI is trying to send that information from UI to backend behind the scenes, all the
[03:02] data that the end user entered inside the UI page is going to be mapped to these fields.
[03:08] Very similarly, whenever you want to send the information from backend to the UI to display the Person
[03:14] details in such scenarios
[03:16] also, you can retrieve the data from the database.
[03:19] Once the data is retrieved from the database, you can store all such information using the object of
[03:25] the Person class and this object of the person class you can send to the UI page.
[03:31] So if you see here, it should be pretty clear for you.
[03:33] The purpose of these class is going to be only to carry the data from one place to other place.
[03:40] So these kind of data carrier classes, we can call them as Pojo classes.
[03:46] They are simple, Plain Old Java Objects.
[03:49] They're not going to have any business logic other than related to the data that we are trying to share.
[03:55] With this, we should be able to create the object of the Person and using the object of the Person,
[04:01] we can store the information like firstName, lastName, age and salary.
[04:05] So let me show you how to do that.
[04:07] I'll go to the Main class.
[04:09] Inside the Main class, I'm going to create the object of Person with the help of new operator and the
[04:16] default constructor if needed
[04:18] you can also create a constructor that accepts multiple arguments.
[04:23] For now, let me go with the default constructor.
[04:26] So with this line of code right now I have an object of Person, and inside this Person object I don't
[04:32] have any details, it's just an empty Person object.
[04:35] So to populate information inside this Person object I can use multiple options.
[04:41] Like I can try to invoke the fields using the Person object like
[04:46] first I'll try to invoke the firstName field, but you can see I'm not able to access any of the fields.
[04:52] The reason is the Person class is present inside a different package with the default access modifier.
[04:59] So
[05:00] to make these fields accessible from Main class, we can mention the public keyword just before all
[05:07] the Java fields that we have created.
[05:09] So let me do that.
[05:10] So once I have defined this public access modifier, this time I should be able to access the firstName
[05:17] .
[05:18] And I can mention the firstName as John, followed by what is the lastName.
[05:23] So similarly I can also try to populate the lastName and the lastName I'm going to mention as Doe.
[05:29] And next I'm trying to assign the age to this Person
[05:34] I'll just keep it as 25 followed by salary,
[05:37] so the salary I'll try to assign a value which is 10,000 .00.
[05:44] So this is how you can populate the data inside this object.
[05:49] Now this object I can send to the UI application or I can send to the database layer.
[05:56] If I'm sending this object to the database layer, all this information that I have inside this object
[06:01] is going to be stored inside that database table.
[06:03] Whereas if I'm sending to an UI application, this information is going to be displayed to an end user
[06:10] inside the web pages or inside the mobile application.
[06:14] I hope you are clear
[06:15] till now we can also follow other approaches like we discussed.
[06:18] We can create an constructor that accept all these fields as an input using the multiple arguments constructor
[06:26] also, we can create the object and we can assign the data.
[06:29] That's a different approach.
[06:30] Regardless of which approach that you try to use, you need to make sure to populate the data inside
[06:36] the Person object, to share the information to an UI application or to an database layer.
[06:42] So you may think like this is Pojo and we should be good with the Pojo concept, but this is not
[06:48] an actual Pojo.
[06:49] So there are certain standards that you need to follow whenever you are trying to build a Pojo
[06:55] java classes.
[06:56] So let's try to understand what are those standards in the next lecture.
[07:00] Thank you,
[07:01] bye.

----------------------------------------
