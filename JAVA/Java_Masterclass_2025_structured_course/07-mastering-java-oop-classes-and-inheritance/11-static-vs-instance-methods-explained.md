# 7.11 — Static vs. Instance Methods Explained

> Section 7: Mastering Java OOP: Classes & Inheritance

Kind: captions Language: en Static vs. Instance Methods In the last video, I talked about the differences between static and instance variables. Let's discuss the differences between static methods and instance methods. Firstly, static methods. Static methods are declared using a static modifier. Static methods can't access instance methods and instant variables directly. They're usually used for operations that don't require any data from an instance of the class (from THIS) in other words.

If you remember, the THIS keyword is the current instance of a class. Inside a static method, we can't use the THIS keyword. Whenever you see a method that doesn't use instance variables, that method should probably be declared as a static method. For example, main is a static method and it's called by the Java virtual machine when it starts the Java application. In this example on screen, I've got a class called calculator with a static method called print sum.

And it just prints the sum of two integer numbers. Then I've got the main class with two static methods. Main and print hello. Inside main, I'm calling the method print sum from the calculator class. As you can see, to call the print sum method, I just need to type the class name, in this case, calculator and then the method name print sum. In the second method call, I invoke print hello, without using the class name. You can call a static method without using the class name, if the method being called is in the same class.

Static methods don't require an instance to be created. I can just type the class name and use the dot notation with the method name to access them. Alternatively, you can drop the class name, and just use the method name, if the static method being called is in the same class. Let's move on now to instance methods. Instance methods belong to an instance, (a specific instance), of a class. To use an instance method, we have to instantiate the class first, usually by using the new keyword.

Instance methods can access instance methods and instance variables directly. Instance methods can also access static methods and static variables directly. What I mean by directly is that we don't usually have to use the keyword THIS with the dot notation to use them. And we don't have to use the class name with the dot notation to access static variables or methods, if the static variable or method is in the same class. Although doing so can help with clarity.

In this example, I've got a class called dog with a method bark. Notice here how the method bark is not using the static keyword this time. The method is a standard instance method. I've got the main class with a method main. Inside the main method, I first need to create an instance of the dog class, and that's done with the line dog Rex equals new dog. As you can see, I'm using the new keyword to create an instance of that class. After I've created the instance, I call the instance method, bark, in this case, by typing Rex dot bark.

The hard part here could be deciding when to create an instance or when to create a static method. Here are some basic rules that should help you decide. Instance methods are created more often than static methods, but let's see how to follow this diagram. The first question I'd ask myself is, "Should the method be static?". After that question, the next question would be, "Does it use any instance variables, that is fields, or instance methods of this object?".

Remember, we're asking these questions about the proposed method we plan to write, so if that's true, then, we'd want to make it an instance method. In the other scenario, if the method doesn't use or is not proposed to use any instance variables or instance methods, in that case, then its likely you would choose defining it as a static method. Generally speaking, if we're not using any fields or instance methods with the new proposed method, we should consider making that method static instead of a regular instance method.

So, that's the main differences between static and instance methods. In the last couple of videos, we've reviewed some very important terms. Hopefully, now, you have a clearer understanding of what an instance, object, and reference are as well as the differences between static and instance members of a class. In the next video, I'm going to talk about a class that usually only has fields to store data. This is called the plain old Java object, or poe joe, and then I'll introduce you to a fairly new type in Java, the record.

See you in the next video.

----------------------------------------
