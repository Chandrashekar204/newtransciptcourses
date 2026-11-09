# 30.10 — Primitive Types Challenge

> Section 30: First Steps - Old content for Java 11

All right, so it's time for a challenge. So your challenge is to create some variables. First one is a variable of type byte, where you can set it to any valid byte number, doesn't matter. Also then do the same for a short variable, setting it to any valid short number, and then create an int variable, setting it to any valid int number. Lastly, then create a variable of type long, and make that equal to 50,000 plus 10 times the sum of the byte plus the short plus the integer values.

So that's your challenge. See how you go, pause the video, go away and do that. And when you get back, I'll go through it and show you how to do that. Pause now, see you when you get back. Right, so how did it go? Did you manage to figure it out? Well, let's make a start on that. So what we're gonna do, firstly, is I'm gonna create a new project. So we're not going to use the existing one. The code's available if you need to get access to that one.

I create a new project. I'm just gonna call this one... I'm clicking a create project. We're gonna call this one Primitive Type or Primitive Types Challenge. We are gonna put the code in there. Just so it's separate from the code they've been working on, right. All right, so we're gonna start off by creating our variables. If you remember, there was three that we needed to create. We've got a byte, we'll call that one byte value, we'll set that equal to 10.

And again it could be any value. Short value equals 20. An int, int value, set that equal to 50. Then our long variable, long, long total is equal to 50,000. I'm gonna put an l there to signify that it's a long, but bearing in mind that we don't have to do that because Java will assume, an integer type and it'll automatically convert that to a long. But I'm gonna put it in anyway. Plus 10 l multiplied by, then we need to multiply the sum of byte value plus short value plus int value.

So byte value in parenthesis plus short value plus int value. Closing parenthesis, and a semicolon to make the line valid. So that's actually the solution. And just to confirm this, let's actually just print out the value long total. Okay, we'll run the programme. Can you see, we got the result 50,800? There we didn't need to do any casting, and again we've talked about the reasoning for that is an integer value which these results are assumed, to the right-hand side, this is assumed to be an int value, but we've established that longs work quite nicely with ints so we don't need to do any casting, but we wanted to do something similar with, say, a short.

And I know this isn't part of the challenge, but we just are going through it anyway. And would be something like short, short total is equal to parenthesis 1,000 plus 10 multiplied by then parenthesis byte value plus short value plus int value. Now clearly we've got an error doing that, and the reason we've got an error is, now we do have to cast. And if we hover over it, "Required a short and found an int." So we need to be specific here, and put a short at the front of the expression there, put it specifically.

And I'll just press enter there. This is something else you can do with Java, by the way, you can actually go over multiple lines, and Java is smart enough to determine that this statement is over two lines. We've got a semicolon on the end of the second line, and it quite happily accepts that. So the point of all this, after solving the challenge, was just to suggest that integer is the best primitive data type for whole numbers to use generally, but even if you're using type long, you saw that Java handles a lot of the complexity for you, and you don't have to do this casting with a long, and the reason for that was because the long will happily accept an integer because, of course, a maximum integer value will always fit within a long value.

So that's bytes, shorts, integers, and longs. Four primitive types. So we still got four to go. Into the next video, we are going to start talking about decimal numbers. Because, of course, to date we've only been dealing with whole numbers. But can be very common requirement for you to wanna use decimal points. For example, you might wanna convert pounds to kilogrammes, or something of that nature, and in that scenario, having the ability to use decimal points in the number, would be really useful.

So let's start working on that in the next video.

----------------------------------------
