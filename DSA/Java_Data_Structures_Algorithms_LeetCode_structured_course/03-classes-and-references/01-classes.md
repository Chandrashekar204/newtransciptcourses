# 3.1 — Classes

> Section 3: Classes & References

So now we're going to talk about classes. And this is a very important topic to understand particularly when we're going to build our data structures. So I think of a class like a cookie cutter. A cookie cutter is not a cookie. But you can create cookies with it. I'm going to shrink this down here, and we're going to build the class and we're going to call it cookie. And classes can have class variables. I'm only going to have one variable for cookie, and that's going to be the color of the cookie.

A best practice is to make all of your class variables private. And then inside the class we can have methods. And the first method we create is called a constructor. This is what we'll use to create a new cookie with this cookie cutter. And the constructor method always has the name of the class. So our method is called cookie, just like our class. And when we run this constructor we're going to pass it a color. That's what this color is. And we're going to set this dot color equal to that.

And we'll talk a little bit about the keyword this as we're going through this video. But this dot color is this color up here. And it's used for a particular instance of cookie. So once we've created this class, we can create a new variable that is of the type cookie. Like this. We're going to call our variable cookie one and we'll set it equal to new cookie. And then pass it the color green. So this particular instance of cookie is called cookie one.

It is of type cookie. We use the new keyword, and the new keyword means we're going to run the constructor. We're going to pass the constructor the color green. And that is going to create a green cookie. So we would say that this cookie this particular instance of cookie here. He is green. So to emphasize the point, let's create another cookie. In other words, another instance of cookie. We'll call this one cookie two. And we'll say that's equal to new cookie.

We'll pass it the color blue. So we'll say the new instance of cookie that we're calling cookie two. We're making this one blue. This particular instance of cookie is blue. So we have two instances of the class cookie. So in addition to our constructor method, we can create other methods. So we'll do something simple like this and have a method called Getcolor. It just returns the color for a particular instance of cookie. Then we'll also have another method that we'll call Setcolor.

With this one, we're going to pass it a color and it will change the color of a particular cookie. So let's bring our cookies back here. And let's look at all of this code in IntelliJ. So here is our class here for cookie. So the code that we're going to look at is going to be in two separate files. I want to show you how I have this set up. So I'm going to come over here to project. And I'm going to click on this and it'll bring up this side window.

This is what we're working with here I have a package called classes. And I have two different classes in here, one called cookie and one called main. I have both of these open in these tabs up here. And as we're going through the course, this will be the format that I have that I have a class that we're building, but we're going to test it and actually run that class in a separate class called main. So I'm going to close this side window and I'm going to come over to this tab called main.

And look at this. This is where we actually create cookie one and cookie two with a colors green and blue. And then down here we're just going to print out cookie one dot get color and cookie two dot get color. So notice the syntax here. We're using the name of an instance of cookie dot then a method. So I'll run this. And you can see here that this prints out green and blue, which is exactly what we would expect based on what we have here. But I'm going to add a line here to see what it's like to use the set color method as well.

I'm just going to paste this in here and it's going to say cookie one dot set color yellow. Then when we run these two lines of code down here, we would expect to get yellow in blue instead of green and blue. So I'll run this. And you can see up here we have gotten yellow and blue. Okay, so now let's flip back. So we have created a class that we can use for creating cookies. And we have cookie one that was green and is now yellow, and cookie two.

Now how will we use classes in the course? Let's say we have a data structure, a linked list, and to create a linked list we'll need a constructor. But we'll want to do other things with the linked list as well, like append an item to the end of the linked list. Maybe we want to remove the last item, or prepend an item, or insert an item somewhere in the middle, or remove an item. This is the kind of structure right here that we're going to use for every single one of our data structures in the course.

So it's important to understand conceptually how these classes work. And so that is our overview. For classes.

----------------------------------------
