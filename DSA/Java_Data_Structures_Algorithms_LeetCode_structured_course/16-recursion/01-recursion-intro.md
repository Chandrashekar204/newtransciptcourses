# 16.1 — Recursion: Intro

> Section 16: Recursion

So now we're going to talk about recursion. So my favorite definition of recursion is that it's a method that calls itself until it doesn't. So to explain this I'm going to bring up a gift box. And we need to open this gift box. And the way to do that of course is with the open gift box method. And when we open this gift box there are two possibilities. Either the gift box contains a ball or it contains a new smaller gift box. So how are we going to open this gift box?

Well, we're going to do it with the open gift box method. And you can see that we're using the same method for both boxes. And once again we could get a ball or a new smaller gift box. And then we'll use the same method to open this one. And let's say this one contains the ball. Well obviously we're not going to run the open gift box method on this. Which brings us back to that definition at the beginning, that it's a method that calls itself until it doesn't.

Well, it doesn't call itself once we get to the ball. So let's put these boxes and the ball back and we're going to write some pseudo code. So I want to emphasize that this code I'll try to make it look like Java code. But this is not real code. This is for example purposes only in case we're going to do this. This is going to be our open gift box method. And the return type is ball. Which means once we open a box and it contains a ball we will return it.

So when we open a gift box, if we'll say is ball, it contains a ball, we will return the ball. Now technically we would need to have some kind of variable that is of type ball. And we're going to create a new ball. And I'm not going to put that in here. I'm just going to simplify this and take this out. But suffice it to say we are dealing with some object that we're calling ball. But if we open a box and it does not contain a ball, we want to run the open gift box method.

Again, this is where the method calls itself. So a couple of things about our recursive method or any recursive method. The process of opening each new box is the same, or the process of doing whatever you're doing with recursion. Each time you run that recursive method, it is doing the same thing. The other thing is that each time we open a box, we make the problem smaller. So each of these boxes got smaller and smaller until we got to the ball.

So any recursive method, each time you call it it is working on a smaller problem. So let's remove these and walk through this code. Since we have a gift box, we need to run the open gift box method. We'll check to see if it is a ball that it contains. In this case we're going to say it's not. It's a gift box. And that will cause this line to run, which will initiate a new instance of the open gift box method. And then we'll check to see if this box contains a ball.

It does not. It's a gift box which causes this line to run, which creates another instance of the open gift box method. This time though, this if statement is ball, this time it is a ball, so we'll just return the ball. And because it's a return statement, we stop running code and we do not move to this line. So it's essential to have some type of return statement here, to break us out of the loop of having the method call itself over and over. So let's put these boxes back like this and talk a little bit of terminology.

When you have a situation where you get to the ball or whatever it is that causes you to stop having the method call itself. This is called a base case. So if you have a situation like this where the method is going to call itself again because you have another gift box, this is called a recursive case. And this would be a recursive case and this would be a base case. And when you're using recursion you always have to have a base case. So let's say we have a situation like this.

And instead of having an if statement we remove it like this. So what happens when you don't have a base case is when you run the open gift box method. You will then run this line which initiates another instance of the open gift box method, which will cause this line to run. And then you'll have another instance of the open gift box method and so on, and you'll get what is called a stack Overflow. So you have to have a base case. But there are a couple of ways that you could have an if statement here and still not have a base case, because this if statement has to be true at some point.

So let's say you have something like this. If one is greater than two. Well one is never greater than two obviously. So this is never going to be true. This is essentially not having a base case. And you might look at that and say, well obviously one is never going to be greater than two. But sometimes the conditional you have in an if statement can be really complex. So if you get a stack overflow, this will be one of the places to go back and troubleshoot your code.

So let's put this back. So the other thing that you need to have is a return statement, because that causes the code to stop running. Let's say we remove this return statement and instead we just print hello out to the screen. So what happens in this situation where we finally get to the point where is ball is true in the if statement. It's just going to print out hello. Then we're going to go down to here and we'll add another open gift box method and continue that infinite loop of adding instances of the open gift box method to the stack, which is going to cause a stack overflow.

So the other thing that's essential here is we have to have a return statement. And that's our overview of recursion.

----------------------------------------
