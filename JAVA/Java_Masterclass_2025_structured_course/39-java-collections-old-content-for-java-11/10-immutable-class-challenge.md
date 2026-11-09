# 39.10 — Immutable Class Challenge

> Section 39: Java Collections - Old content for Java 11

So let's just finish up our discussion about immutable objects before we go on to the challenge. So I just want to make it clear with a question what exactly is wrong with allowing the class to be extended? So have a look at the declarations of our locations map, come back here. On line 8, as you can see there are locations map in main. Now the map is declared using generics, so that it accepts an integer key and a value of type location. But if location is extended then instances of the new class could also be used.

So this is generally not a problem. In fact, it's actually incredibly useful. But if we use the location type for the key instead of the value and we wanted to ensure that only completely immutable objects could be used as the keys, then we'd have to prevent subclasses over which we've got no control from being used. So anyone who wants to use the functionality of the locations class, once we prevent them from extending it, can still do so using composition.

They create methods that then call the locations class methods from an instance of a location. Now they can still do almost everything that subclassing would have allowed them to do except use their own class where a location object was expected. Now most of the time you will not want your classes to be immutable. A bank account account class where the balance never changes would be a little use no matter, how much we'd love to checkbook on such an account.

But even if we don't want an immutable, class you can use these techniques in various combinations to make your classes certainly more robust than if you didn't do anything at all. Now the challenge is that there's still a problem with location. It's possible to crash the program as a result. The problem is with the location class itself. So they don't waste time trying to crash it by entering invalid input. There's also no consistency checking in the main method.

So if we created exits that refer to a location, say, for example, location 6, that doesn't exist in our locations map, then the program will also crash. But this challenge is about finding a problem with the location class. So here's your challenge. And your challenge is to work out what is wrong with the location constructor that will allow the program to compile but crash at run time. So when you've identified the problem, modify the code to fix it. So I'll just say that again, your challenge here is to work out what is wrong with the location constructor that you can see on screen, line 14, that would allow the program to compile but crash at run time.

When you've identified the problem, modify the code to fix it. And so pause the video now. And when you come back, I'll show you what the problem was and how to fix it. Okay. So did you figure out what the problem was? Well, the problem is that the constructor will crash with a null pointer exception at line 17 if none is passed instead of a map. Now to see this, let's modify the method or go back to the main method and location zero I'll just close down the wrong window, disconnect that for now.

And we'll change temp exit to null. We're now passing a null map. So if we run this, we're going to crash a null pointer exception, and we're getting a crash on line 17, but the program crashes as a result. So you might look at the code there and think, well, it's probably reasonable on line 22 to have a null pass because there aren't any exits because it's a special sort of location that we're using to indicate that the programs quit. But obviously, having a crash is a bad thing.

So the solution we'll go back to our location constructor is to test the contract the constructor's argument and don't try to initialize the new map if null is passed for the exits. So consider what I mean there, we put a test here. We put if exits not equal to null. So if there is some valid a map that was passed to this method, and we're going to initialize it with that map. Else, we're going to put this.exits equals new hash map with an empty constructor, meaning it's going to just create a new hash map.

But obviously, there's no no data because no no valid data was passed to this constructor. And everything else can remain the same. The code on line 22 will still work because it's got a valid map because it has been initialized correctly. Just to confirm that, we run that again. We're now no longer getting an error, and we can still sort of navigate and do things as we would normally have done. So that's it. I hope you got a lot out of immutability and out of these adventure challenges.

And I'll see you in the next video.

----------------------------------------
