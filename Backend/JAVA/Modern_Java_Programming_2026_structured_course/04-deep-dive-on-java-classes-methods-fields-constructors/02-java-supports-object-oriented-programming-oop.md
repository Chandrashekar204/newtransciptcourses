# 4.2 — Java supports Object-oriented programming (OOP)

> Section 4: Deep dive on Java classes, methods, fields, constructors

[00:00] Welcome to the new section.
[00:02] Since we are into the new section, I'm trying to use new color for my slides.
[00:07] I'm trying to do this just to keep you engaged so that you are not get bored by seeing at the same color
[00:14] inside all the lectures of the course.
[00:16] I hope you are fine with this approach.
[00:18] Inside this section we are going to talk in detail about how to create Java classes,
[00:24] why should we create Java classes and how to create Java objects from the Java classes,
[00:29] what are the roles of methods and fields inside Java classes,
[00:34] what are constructors ?
[00:35] So all these concepts we are going to discuss inside this section in detail.
[00:40] But before we try to start the discussion around these concepts, I want to start this section with
[00:46] a funny story.
[00:47] This story is about a cowboy you will get to know in few seconds why we are calling this boy as cowboy.
[00:54] This cowboy likes the cows a lot,
[00:57] whatever
[00:58] you are trying to talk with him, he'll always bring cow into the picture and he will try to talk about
[01:04] the cow.
[01:04] Let's imagine one day the father of this boy asked him recently.
[01:09] We fly to other city and you onboarded onto the flight very first time,
[01:13] how was your experience .
[01:15] The father is trying to ask the experience of the boy since he traveled in the flight very first time.
[01:21] The boy is super excited
[01:23] in sharing the answer, he said, I'm super excited, daddy.
[01:26] I got a window seat
[01:28] I'm able to see everything in the sky.
[01:31] First I saw the clouds,
[01:32] sometimes I'm able to see what is there on the earth.
[01:36] The earth is so green,
[01:37] we have so much of forests, mountains, grass and these grass is going to be a good food for the cows.
[01:44] The father immediately got surprised why these fellow is bringing the cow into picture, when he's trying
[01:51] to explain his experience about the air travel for the very first time.
[01:55] Then the father asked him the second scenario about the ice cream shop.
[01:58] Recently we went to the ice cream.
[02:00] Did you like the ice cream?
[02:02] So this was the question by the father to the son.
[02:05] Let's see what the cowboy is going to answer in this scenario, how he's going to bring the cow into
[02:09] the picture.
[02:10] He started answering, yes, dad,
[02:12] we went to an ice cream shop.
[02:14] I like the ice cream flavors that we have in the shop.
[02:17] I ordered one of my favorite ice cream.
[02:20] And do you know that how these ice creams are being made?
[02:23] These ice creams are made with the help of milk.
[02:26] And this milk we are going to get from the cow, which is going to eat grass daily.
[02:32] So the father is scratching his head like his son bringing cow into picture every time.
[02:38] This poor fellow does not know that his son likes cows so much.
[02:42] This time the father tried to ask a different question related to the school.
[02:46] The father asked, how is your studies going on?
[02:49] How is your school?
[02:50] Are you liking your school?
[02:51] Then the son replied, yes dad.
[02:54] I like my school a lot.
[02:55] I love my friends, my teacher, my teacher is so kind.
[02:59] She explains all the topics very well.
[03:02] Do you know dad?
[03:03] Yesterday my teacher taught a lesson and this lesson is about cows.
[03:08] Inside this lesson, my teacher explained everything about cow.
[03:12] The advantage with cow, how they give milk to us.
[03:15] What are the benefits of milk?
[03:16] Now the father understands clearly that his son likes cow a lot, regardless of whatever question he
[03:23] asks, he always going to bring the cow into picture.
[03:26] I hope you like this funny story, but here you might be scratching your head why this fellow is trying
[03:32] to tell me this funny story right now.
[03:34] Just like how this boy liked cows a lot,
[03:37] very similarly, Java programming language likes objects because Java supports object oriented programming.
[03:46] So what is an object oriented programming?
[03:49] In short form, we call it as OOPS.
[03:51] Object oriented programming is a programming paradigm that is based upon the concepts of objects, which
[03:57] means all the business logic are all the logic that you are going to write inside the Java.
[04:03] You're going to build it by imagining everything as objects.
[04:07] Just for a second look around you.
[04:09] There are so many objects around you.
[04:11] You may see trees, you may see humans, you may see vehicles, you may see animals, you may see books.
[04:18] So there are so many objects around you and you think all these objects, they are going to have same
[04:25] properties and same behavior.
[04:27] Off course not
[04:28] each object that you see will have different properties and different behaviors.
[04:33] For example, take a Human example.
[04:35] The humans may have properties like name, gender, age, height, weight, and behaviors like walk,
[04:43] talk, run, study, work, sleep.
[04:46] So these are all the properties and behaviors for all the humans.
[04:51] But do you think all these properties are going to be same for all humans?
[04:55] Off course, not every human will have their own properties like their
[05:00] own name, own gender.
[05:01] But for all the humans we have a common definition
[05:05] like this is how the humans are going to look like, and this is how the properties of humans are going
[05:11] to look like
[05:11] and these are the most common behaviours of the humans.
[05:14] So all that common definition of humans we are going to define with the help of classes inside the Java
[05:22] programming.
[05:22] We know Java follows object oriented programming and Java likes objects a lot.
[05:28] But in order to create the objects, we need a common skeleton or a blueprint or a definition.
[05:33] So that definition is a class inside Java.
[05:37] So classes are the basic unit of programming in the object oriented paradigm.
[05:42] Apart from Java, there are many other languages that follows the same object oriented programming paradigm.
[05:48] For example, Java script also creates a lot of objects, and it also encourages developers to build
[05:55] the logic based upon the objects.
[05:57] Once we have defined a single definition with the help of a class, we can define any number of objects,
[06:04] and in the process of defining the objects from a class, we can provide the unique properties related
[06:10] to a particular object.
[06:12] For example, take the same Human class.
[06:14] If I'm trying to create an object related to me, then this object which I have created is going to
[06:21] have the name as modern along with other properties that are unique to me.
[06:26] So the same applies for any kind of objects that you're going to create inside the Java.
[06:31] So whenever you want to create objects inside Java, the first condition that you need to take care
[06:37] is you need to create a Java class, defining the basic skeleton at the blueprint of the objects that
[06:44] you are trying to create.
[06:45] Let me show you some business scenario to make it more clear for you.
[06:49] Think like you're working for an bank application and you as a Java developer asked to develop the business
[06:55] logic with the help of Java programming language for these bank application.
[07:00] So in this scenario, you are going to build the Java logic based upon the classes and objects like
[07:07] Customer, Account, Loan, Card, Transactions.
[07:11] So based upon your business scenario, first you're going to imagine what are the possible use cases
[07:17] inside banks,
[07:18] we know we have customers and the customers
[07:21] they'll have their own Account, Loans, Cards.
[07:24] And these customers they'll also perform transactions.
[07:27] So each of these class or object, they're going to have their own behavior and properties.
[07:33] For example, for the customer we may have properties like name, date of birth, address.
[07:38] So all those details we're going to store inside the customer. Coming to the Account, Account is going
[07:44] to have different properties like what is our account number,
[07:47] what is the account type,
[07:48] what is the total balance it has,
[07:50] So it is pretty clear when we try to build business logic with the help of Java programming language.
[07:55] First we need to create the classes by imagining all the possible use cases.
[08:00] Now let's see the other scenario where you are trying to build an application related to the health
[08:05] care domain.
[08:06] Inside this project, the use cases will be evolve around the Patient, Doctor, Treatment, Medicines and
[08:14] reports.
[08:15] This way, since Java is going to support and encourage us to build a programming language based upon
[08:21] object oriented programming, first we need to create the Java classes.
[08:25] Inside these Java classes, we need to define the variables and fields and methods.
[08:30] Once the Java class is populated with all the required details, we are going to create the Java objects.
[08:36] And using these Java objects only, we are going to build all the business logic. Apart from object oriented
[08:41] programming paradigm.
[08:43] There are many other programming styles like imperative style, declarative style, functional programming,
[08:49] procedural programming.
[08:51] Java also supports functional style programming.
[08:54] When we are going to discuss that in the coming sections, when we're trying to explore the concepts of Lambdas
[08:59] and Streams inside Java.
[09:00] For now, let's focus on these object oriented programming.
[09:04] So inside Java, oops, there are some important concepts available.
[09:08] These concepts are class.
[09:11] So using class we are going to create the skeleton.
[09:13] Once the class is defined we are going to create objects from the class.
[09:17] And very similarly we are also going to have concepts like interface, inheritance, encapsulation, polymorphism,
[09:24] abstraction.
[09:25] So these are all the principles of oops programming any language who is trying to follow the object
[09:32] oriented programming.
[09:33] It has to follow all these principles and concepts.
[09:36] We are going to discuss in detail about all these concepts throughout this course.
[09:40] For now, please don't try to understand what are these new jargons that I'm trying to introduce here.
[09:46] At last, I want to give information on why Java is following these object oriented programming.
[09:53] What are the advantages that we get. Inside the object oriented programming paradigm
[09:57] it is always going to prioritize
[10:00] data over imperative commands.
[10:02] So what is an imperative
[10:04] commands.
[10:04] Like I said before, one of the programming style that we have is imperative style.
[10:09] Inside the imperative style, we are going to give clear instructions using the language for each and
[10:15] every step.
[10:16] At this step, what my computer has to do.
[10:18] So when we try to give this clear steps inside a program, we call that style as imperative style.
[10:24] So Java also follows imperative style.
[10:27] That's why whenever we are trying to build logic with the help of Java, we are going to give clear
[10:32] instructions to the JVM.
[10:33] But the advantage with Java is it is not going to blindly follow the imperative approach.
[10:39] Apart from imperative approach, it is going to first prioritize everything as an objects.
[10:45] So instead of telling like do this, do that to the JVM, my Java language first encourages developers
[10:51] to create the classes, methods, and from these classes we can create objects,
[10:57] and using these objects, we can build the imperative commands.
[11:01] So that's why inside the Java, any logic that you want to write, first you need to define a Java class,
[11:07] java object, java methods.
[11:09] Without defining these components, you cannot issue any commands to the JVM.
[11:15] So this hybrid approach of object oriented along with the imperative commands, brings a lot of advantages
[11:22] to the Java programming language.
[11:24] These advantages are like reusability, modularity, easy maintenance, encapsulation, inheritance,
[11:31] and polymorphism.
[11:32] I'm going to talk about encapsulation, inheritance, and polymorphism in the coming sections, but
[11:39] let me provide more details about what is reusability.
[11:42] When I say reusability, if you write your business logic inside a method which is present inside a
[11:48] Java class, the same business logic you can use in many other scenarios or in many other Java classes.
[11:55] So the advantage that we get here is, we write the code in one place, but the same code can be used
[12:01] in many other places.
[12:02] With that, the number of lines of Java code that we write will be reduced drastically.
[12:07] Now coming to the modularity, modularity means we're going to separate the business logic that we are
[12:13] going to write based upon our business requirements.
[12:15] Think of the same bank application scenario,
[12:18] I can write all the customer related logic inside a customer class, very similarly
[12:23] all the Accounts, Loans and Cards related logic I can write inside their respective Java classes.
[12:29] So this brings modularity and the separation of business logic into the respective components
[12:36] and with all this reusability and modularity, we can maintain the Java language very easily
[12:42] in future,
[12:43] if there is a defect identified, it will be very easy for the developer to identify that because we
[12:49] have not dumped all the logic inside a single class, we have separated it.
[12:53] If I face any defect inside the loans related functionality, then I know where to go and debug that
[12:59] defect.
[12:59] So these are the advantages that we get inside the Java programming language.
[13:04] I hope you are clear with this object oriented programming why Java follows this object oriented programming.
[13:10] If something is not clear, don't worry,
[13:12] when we try to start building the business logic with the help of Java classes, methods and objects,
[13:18] it is going to make more sense to you.
[13:21] But for now, please note that Java supports and follows object oriented programming language.
[13:26] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
