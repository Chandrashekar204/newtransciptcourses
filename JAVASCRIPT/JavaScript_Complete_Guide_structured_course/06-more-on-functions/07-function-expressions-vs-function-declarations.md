# 6.7 — Function Expressions vs Function Declarations

> Section 6: More on Functions

Well if you compare both, we have the function declaration, function statement which look like this and the function expression like this which I just showed you. Of course needless to say, in function expression form here, you can also still take arguments and still return values that didn't change. Now the important difference to what it really boils down here is that for this function declaration, function statement syntax, Javascript automatically hoists the function to the top and then also fully initializes it for you.

So what I mentioned, Javascript reads the file and no matter where you defined your function, it acts as if it would be defined at the top of the file, which means you can actually call functions before you declare them. That can be convenient and if your code style is to always have the functions at the end of the file, then you have to use this approach. With function expressions, this hoisting is also working but the constant gets hoisted but it gets hoisted as undefined, something I also had a look at in this behind the scenes module.

So it's basically not initialized so you can't call the function before you defined it and that's an important difference, you have to define, you have to initialize your functions before you try calling them and in my opinion this is a bit of a cleaner style, though you will find both code styles, I will say that, it's not strictly bad or worse than the other. I personally prefer this approach a little bit, I think being forced to define functions before you use them is a great thing but of course it's needless to say that you could also simply define functions with the left approach before you use them. So you don't have to use the right approach just because you want to do that, the right approach just forces you to define functions before you call them. Now ultimately it's therefore up to you which one you prefer, I am personally a fan of the right approach but as I said, both works and both can be used, there is no bad approach here.

Just to also quickly demonstrate what I meant, here we have this function defined. Now if I would call start here before that definition, if I save that and reload, I get an error that we cannot access start before initialization and we wouldn't get that error if I had my function started let's say like that, so in this declaration, in this statement syntax. If I would do that, this would work just fine as I mentioned because Javascript reads the entire file and if it finds function declarations like this, it kind of acts like they were at the top of the file.

So that is an important difference, as I mentioned this is the style I prefer but not a style you absolutely have to use necessarily.

----------------------------------------
