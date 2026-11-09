# 32.2 — What are Programming Paradigms?

> Section 32: Bonus: Programming Paradigms (Procedural vs Object Oriented vs Functional)

So what are programming paradigms? That's of course important to understand. In the end you could say it's just a way of writing code, it's about how you write and organize your code. It's not a syntax feature, it's not a special feature exposed by the browser or anything like this, it's really just how you structure your code and how you reason about your program you're writing, so how your code is organized and in the end there are three paradigms you could follow.

You have object oriented programming, you have procedural programming and you have functional programming. Now what does this mean? If you're writing your code in an object oriented style, it means that you organize your data and logic in objects or in classes and then in objects based on those classes, which means you store your data in properties of objects, you store your logic in methods of objects, that's how you typically think about your code here, everything in your application, in your project gets represented as a class and then in the end, as an object.

So you organize who code in logical entities you could say, you kind of try to translate the application you're writing into the real world and you think about your application and the things that make up your application in real world terms. If you're building a shop application, you think about products and a shopping cart and so on, that's how you think about your code and how you organize it. Now when you're following a procedural style and that's probably the style with which you got started when work with Javascript, you simply write a sequential series of execution steps and tasks, so you have a top to bottom code execution you could say. Now you always have that in every style but here you simply list these different steps the engine in the end should execute and should perform, you don't organize your code in logical groups or in logical pieces of data, you don't use objects and entities to structure your code, in the end you just execute step after step.

And then we have functional programming and there, we organize our code in, if possible, pure functions with clearly defined tasks. You get all the data a function needs as parameters and then this function often also return something new, so you pass data around with parameters and your functions are your way of organizing your code. You have many functions, probably more than you have in the other styles and your functions hold your logic, every function if possible works on its own and this is how you structure your code.

Now that's the theory, it of course becomes way clearer if we see that on a real example.

----------------------------------------
