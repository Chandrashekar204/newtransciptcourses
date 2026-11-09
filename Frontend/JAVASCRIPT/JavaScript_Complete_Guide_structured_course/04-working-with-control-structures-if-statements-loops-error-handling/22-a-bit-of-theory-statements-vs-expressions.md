# 4.22 — A Bit of Theory: Statements vs Expressions

> Section 4: Working with Control Structures (if Statements, Loops, Error Handling)

It's time for a little bit of behind the scenes theory about Javascript code and how we call things there. You might have heard me say things like statement or expression, well there actually is a difference, this here is an expression. Basically in Javascript, an expression is something that yields a value you could store in a constant or a variable or return in a function, something like this, that's an expression. Now every expression also is a statement, this here for example is also a statement but an if statement on the other hand is just a statement, not an expression because you can't use it in the places where you for example just need a value as you just learned, you can't do that, instead an if statement here can only be used in code like this, you can't use it on the right side of the equals sign basically and therefore this is a statement but not an expression.

So you could kind of memorize that an expression is basically something which would work if you use it on the right side of an equal sign. It's not super important for you to learn it by heart, I just want to clarify what I mean when I say expression or statement and as you see, most things in Javascript are expressions but something like the if statement would be a statement. We will also see other statements later when we dive into loops because these also are statements then but for now, the if statement is the important statement which is not an expression which we learned about thus far.

----------------------------------------
