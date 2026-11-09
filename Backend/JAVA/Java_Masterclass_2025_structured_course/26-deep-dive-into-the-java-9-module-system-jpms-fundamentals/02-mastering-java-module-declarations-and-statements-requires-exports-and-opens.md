# 26.2 — Mastering Java Module Declarations and Statements: Requires, Exports, and Opens

> Section 26: Deep Dive into the Java 9 Module System: JPMS Fundamentals

All right. So module declaration and statements. So let's discuss now on modules declaration and statements that are used. So as I discussed in the previous video, each module is defined using a module declaration using the newly introduced module keyword. So the syntax is the following. So you can see we've got module, module name. We've got curly braces and then some module statements and closing curly brace. And optionally, we've got this open modifier.

Now the open modifier declares an open module or in other words a module that exports all its packages to be used by reflective access, but more on this later when we start creating modules. All right. So the module name is the name of the defined module. And the module name is mandatory. We can't have two modules inside the same code base with the same name. And it's good practice to name modules with the same name as packages. And inside the curly braces, we can have zero or more module statements.

And those statements can be the export statement the open statement, the requires statement, user statement or the provides statement. So the require statement is used to specify the module that's required by the current module. In other words, if our module depends on some other modules, we have to specify it using the requires statement. Now we can use multiple required statements depending on how many modules are needed for our module. Now the export statement is used to specify the packages that are exported by the current module. Now the provide statement is used to specify the service implementations that the current modules provide. Now the user statement is used to specify the service that the current module consumes.

And a final point here is keep in mind that the open statement can't be used in open modules because all packages are open in an open module. All right. So let's move on to the next video now we're going to discuss module types and the module path. So I'll see you in the next video.

----------------------------------------
