# 15.3 — Impure vs Pure Functions

> Section 15: Advanced Function Concepts

Typically it's a good idea in programming, not just in Javascript but especially in Javascript, to aim for pure functions without side effects simply because they are predictable and if someone calls them without knowing the function definition, it's always good if you can rely on the fact that this function doesn't do anything strange behind the scenes. Now that being said, when you're building an application, when you're writing code, it will be impossible for you to avoid introducing side effects at some point of time.

A function might need to set up some event listener or might need to send some data to a server and that is absolutely fine. The goal just is to minimize the amount of functions which are impure or which have side effects, just work with your code in a logical way, try to keep your functions predictable and pure and if you then occasionally have some functions that need to perform a side effect or that needs to be impure, that's absolutely fine.

Maybe just try to be clear regarding the function naming that this might be a function that does something as a side effect, for example a function which is named send data to server would be expected to send some data to a server and it wouldn't come as a surprise that this function as a side effect produces an HTTP request. A function which is just called add on the other hand should probably not create some side effect or be impure because a function with this name, well we would expect this to be pure, right?

As always, it comes with experience and now of course it's OK to not be perfect regarding that, you should definitely be aware of this concept of pure functions though and as I said, aim for more pure functions and less impure functions that might introduce side effects.

----------------------------------------
