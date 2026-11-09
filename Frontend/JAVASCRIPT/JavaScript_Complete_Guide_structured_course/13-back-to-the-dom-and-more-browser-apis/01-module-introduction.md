# 13.1 — Module Introduction

> Section 13: Back to the DOM & More Browser APIs

We already worked with the the DOM, we created elements, inserted them, we queried for elements, you learned how to work with elements. Now in this module we'll take it one step further, we'll have a more detailed look at what we can do with DOM elements, we'll work with their coordinates, their sizes, we'll learn how to attach data to them and we'll have a look at what else the browser offers us when it comes to working with what the user sees and experiences in the browser window. In detail in this module, we will have a look at how we can attach data to DOM elements and why we might want to do that.

We will work with element coordinates and sizes so that you learn how you can use Javascript to find out where an element sits and which size it has and how you can also modify these values. We'll also have a look at a concept called templates and I will also show you how you can add scripts dynamically, so how you can load scripts and create scripts with Javascript, which is pretty meta I guess and as I mentioned we'll have a look at what else the browser offers to us and there, we'll have a look at the navigator object, the location object and window.history and you will learn what these things are, what we can do with them and why they exist. For most things in this module, we'll use this little application we worked on in the last course module which was optional, so if you skipped that last module you'll find a finished snapshot attached and you can use that.

I would recommend that you go through the code and get acquainted to it, one thing which I want to highlight which you learned about earlier but which we haven't used in a real project before is that in this project I actually pass functions around as callback functions, for example here to make sure that in this project where we got two boxes with projects, we can move projects between these two boxes and for that, we pass functions around into our two project list objects which are two instances based on the same class to trigger different actions in different instances of these classes.

So just have a thorough look through this code and if you want to learn how we wrote this and why we wrote it like this, check out this last course section. With that, let's dive right in and let's have a closer look at what we can do in the DOM and with all these cool DOM elements.

----------------------------------------
