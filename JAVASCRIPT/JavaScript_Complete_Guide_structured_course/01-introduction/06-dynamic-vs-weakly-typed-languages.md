# 1.6 — Dynamic vs Weakly Typed Languages

> Section 1: Introduction

Javascript is a dynamic, interpreted programming language but it's also a weakly typed programming language. Now what does this mean? For one, the dynamic interpreted part as you learned means that it's not pre-compiled, other languages like C++ are compiled during or after development, so before you share them with the end users, Javascript is on-the-fly compiled and that means that the code is evaluated and executed at runtime, it also means that the code can change at runtime.

Now of course not the code you wrote and it won't magically change, of course the code you wrote gets executed but in that code, you can do some things which you are not allowed to do in other programming languages, for example if you're working with a variable, something we will only learn in the second module, for now you can just keep in mind that a variable is a data container, you might store let's say some text in there, text you need in your script to for example output it to the user. In Javascript you are allowed to dynamically switch the type of data there. In a variable, you might start by storing some text and suddenly at a later point of time, you store a number in there instead, in the same variable.

Now again, we haven't really learned about variables yet, we will of course do that but the one thing you can simply keep in mind is that the dynamic thing in Javascript means that it is parsed and interpreted and compiled at runtime and that therefore it is able to do certain things, for example switching the data of a variable other programming languages are not allowed to do. Now it's not necessarily good to switch the type of data dynamically or unexpectedly but you can do that, the main takeaway however is the on-the-fly compilation and interpretation. Now what about the weakly typed part here?

This means that when we work with data in Javascript, for example text data or numbers, you don't have to tell Javascript that you're going to work with a text now or you're going to work with a number now, instead data types are assumed, are inferred automatically so to say, that's also related to this dynamic nature where data types can also change from one line to another. Now this might sound strange but in other programming languages, you have to define the type of data a variable will hold in advance. In Javascript, that's not the case, you don't have to tell Javascript that this variable, this data container will hold a number, instead you store a data in there and if that happens to be a number, so it is. In other programming languages, you have to tell the language that you're going to store a number in there and if you store something else, you would get an error.

That's not the case in Javascript, it's forgiving there because it's dynamic and it also doesn't care about strong type definitions in advance, instead you just store data in there and go with every type of data that holds. So data types are not set in stone but can change. Now this is arguably a bit more advanced, I just want you to be aware of these terms, dynamic and weakly typed right now and they will make more and more sense as we progress throughout this course and work with data and variables.

For now, just be aware of these terms.

----------------------------------------
