# 7.10 — Static vs. Instance Variables in Java

> Section 7: Mastering Java OOP: Classes & Inheritance

Kind: captions Language: en Let's discuss the differences between static variables and instance variables. Firstly, a static variable is Declared by using the keyword static. Static variables are also known as static member variables. Every instance of the class shares the same static variable. If changes are made to that variable, all other instances of that class will see the effect of that change. It is considered best practice to use the Class name and not a reference variable to access a static variable.

This makes it clearer that the variable is associated with the class and therefore not stored with the instance. An instance isn't required to exist to access the value of a static variable. Static variables aren't used very often but can sometimes be very useful. They can be used for: Storing counters. Generating unique IDs. Storing a constant value that doesn't change, like PI, for example. Creating and controlling access to a shared resource. Some examples of shared resources include a log file, a database, or some other type of input or output stream. ; In this example, I've got a class called dog, and it's got a static variable called name.

There's a constructor that sets the static variable to the parameter value passed to the constructor. And I've got a method called print name, which isn't static. That's a pretty simple class, and inside main, I'm creating two instances of the dog class with the line: dog Rex equals new dog, Rex. I'm creating an instance of the dog class and at the same time, passing the string Rex as an argument. That will be the name of the dog. On the next line, I've got a similar situation, passing the argument, fluffy.

Then I call the print name method on both of the instances. They're just regular instance methods because they aren't defined using static. So, both method calls will print fluffy. You might be wondering, why is that the case? Why would both methods here print fluffy? Well, remember that static variables are shared between instances. Once we change the static variable, all instances will see the change we made. When I called the constructor with the argument fluffy, it modified the static variable name because both instances were sharing that variable.

That's why it prints fluffy twice. You could also say that both dogs have the same name, but that's logically incorrect. There is only one static field. Hopefully, you can see how static variables can be used inappropriately sometimes, as in this example. Probably, you were assuming that the dog's name would be associated with each instance of the dog and therefore would be different for each one. One dog would be named Fluffy and the other would be Rex.

This is a scenario where using a static variable probably wouldn't be a good idea, and using a regular instance variable would make a lot more sense. Let's move on now to instance variables. Firstly, They don't use the static keyword when you're defining them. They're also known as fields or member variables. Unlike a static variable, Instance variables belong to a specific instance of a class. Each instance has its own copy of an instance variable.

Every instance can have a different value. Instance variables represent the state of a specific instance of a class. Let's see an example using instance variables. In this example, I've again used very similar code to what we looked at earlier in the video, but this time, the variable name in the dog class isn't static. Rather, it's just a regular instance variable. Once again, the constructor is setting the value from the argument passed to that instance variable.

But now the code will print Rex and on the next line Fluffy, and that's because I'm using instance variables. Each instance of the class has its own state or its own values for any variables that have been defined. Because we are using instance variables, every dog has its own value for the name field. It's not shared like it was before, when a static variable was used. In most cases, you'd probably want to use instance variables, but there'll be scenarios when it can be useful to use a static variable.

So, that's instance and static variables. Let's move on now to the next video.

----------------------------------------
