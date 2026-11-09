# 17.2 — Understanding Synchronous Code Execution ("Sync Code")

> Section 17: Async JavaScript: Promises & Callbacks

Let's start by understanding synchronous code and how Javascript works. You might remember that at the very beginning of the course, I mentioned that Javascript is single-threaded. Until now, that didn't really matter to us that much but what single threading in the end means is that Javascript can only execute one task at a time, so let's say we have a bunch of code where we log something to the console, call a function, then maybe in that function or somewhere else after this function ran, we disable some button and then we maybe run another function.

The important thing to realize here is that all these steps run in sequence after each other, they're not running simultaneously next to each other, instead Javascript will log something to the console, then call the function and do whatever needs to be done inside of that function, then go ahead and disable that button and then call that other function, so these things happen after each other, not at the same time. We could give them a label or some ID, let's simply use a, b, c and d and then we could say that for example, this second block, the B block here runs after A but it blocks C from running until it's finished.

So the code in C won't be executed until some function execute it. Now we saw it in our course projects already, take this code here which is actually the starting code of this module, you'll find it attached to this lecture here. Here we don't have that much code but since Javascript parses and executes our code from top to bottom, what happens here is that first of all, this code runs and Javascript selects this button and stores it in a constant, then only once this first line finished, the second line is executed and this task is performed and then this function declaration as you learned works a bit differently, that happens right at the start when Javascript reads the file at the beginning but then in the execution process so to say, this line executes after these two lines executed.

So that's also important for us here because we need the button to be available in order to add an event listener, so we rely on this order which is enforced by Javascript. If it would be multi-threaded, it could maybe execute all tasks at the same time and here this would actually be bad because then we could not rely on the button to be available when we need it because if this line is executed at the same time as this line, well then the button might not have been selected yet and therefore adding an event listener to it would maybe fail.

It's not something we have to worry about though because as I just explained, Javascript is single-threaded and therefore this order is guaranteed.

----------------------------------------
