# 7.20 — Using this and super for Constructors

> Section 7: Mastering Java OOP: Classes & Inheritance

Kind: captions Language: en Let's discuss the difference between the this and super keywords. We'll also find out about the differences between the this() and super() method calls, as you can see by adding parentheses on the end. Let's start with the super and this keywords first. The keyword super is used to access or call the parent class members (both variables and methods). The keyword this, on the other hand, is used to call the current class members (both variables and methods).

this is required when we have a parameter with the same name as an instance variable or field. for static elements such as a static method. Any attempt to do so will lead to compile time errors. The keyword this is commonly used within constructors and setters and is optionally used within getters. In this example, I'm using the this keyword in a constructor and setter since there's a parameter with the same name as the instance or field. In the getter, I don't have any parameters so there's no conflict. Therefore, the use of this is optional there.

The keyword super is commonly used with method overriding when we call a method with the same name from the parent class. In this example, I have a method called printMethod that calls super.printMethod. It's calling the method with the same name from the parent class. Without adding the keyword super in this case, it would end up being a recursive call. What that means is that the method would call itself forever, or actually until memory is fully used on your computer.

That's why we need the super keyword, so that we can call a method with the same name from a parent class. In Java, we've got the this() and super() parentheses calls. Notice the parentheses. These are known as calls since they look like regular method calls although we're calling certain constructors. You'll Use this() parentheses to call a constructor from another overloaded constructor in the same class. The call to this() parentheses can only be used in a constructor, and it must be the first statement in a constructor.

It's used with constructor chaining, in other words, when one constructor calls another constructor, and it helps to reduce duplicated code. The only way to call a parent constructor is by calling super() parentheses, which calls the parent constructor. The Java compiler puts a default call to super() parentheses if we don't add it, and it's always a call to the no argument constructor, which is inserted by the compiler. In other words, a call to the constructor that hasn't got any arguments.

Keep in mind that The call to super() parentheses must be the first statement in each constructor. And importantly, A constructor can have a call to super() parentheses or this() parentheses, but never both. Alright, so let's look at some code, which I would call a bad constructor example. Here, I have three constructors. All three constructors initialize variables. But There's repeated code in each constructor, as you can see there. I'm initializing variables in each constructor with some default values.

You should never write constructors like this. Let's look at the right way to do this by using a this() parentheses call. In this example, I still have three constructors. This example is very similar to the previous example, but the difference is that The 1st constructor calls the 2nd constructor, the 2nd constructor calls the 3rd constructor, and then the 3rd constructor actually initializes the instance variables. In other words, The 3rd constructor does all the work.

Now that I've done this, No matter what constructor I call, the variables will always be initialized in the 3rd constructor, and only there. This is known as constructor chaining, and what we're doing is making sure the last constructor has the responsibility to initialize the variables. Alright, so looking at both examples on screen now. On the left-hand side again, this is a bad example of constructors. On the right-hand side, I've got a good example.

Again, The problem with the left-hand side is the duplicated code. So, as you can see, all three constructors on the left-hand side are initializing the variables. Now, contrast that with the solution on the right-hand side. I've got one constructor that initializes variables, and the other constructors are just calling each other. Ultimately, we end up in the third constructor. And That's again called constructor chaining. With constructor chaining, we can and do avoid code duplication.

By the way, duplicated code can lead to many bugs and a lot more work on your behalf. It's also bad practice, as a rule, to write duplicate code, which of course, I did in the bad example. Alright, let's have a quick look at the super call example. In this example, I have a class Shape, with x and y instance variables, and class Rectangle that extends Shape with variables width and height. In the Rectangle class, the 1st constructor is calling the 2nd constructor.

The 2nd constructor calls the parent constructor with parameters x and y. The parent constructor will initialize the x and y variables, while the 2nd Rectangle constructor will initialize the width and height variables. Here, as you can see in this code, I have both the super() and this() calls, but in different constructors. You may want to watch this video a few times, or come back to this one later, after progressing to other videos in this section, if you have any confusion.

It's very important, as a Java developer, to understand the differences between these calls to be able to use them properly. Alright, so let's move on now to the next video.

----------------------------------------
