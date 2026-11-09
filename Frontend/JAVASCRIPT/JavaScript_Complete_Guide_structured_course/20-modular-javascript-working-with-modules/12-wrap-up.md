# 20.12 — Wrap Up

> Section 20: Modular JavaScript (Working with Modules)

And this is it for modules, an extremely important feature for serious Javascript projects. Having all your code in one file quickly makes it hard to maintain and read, having manual imports in the index.html file on the other hand means a lot of micromanagement and it can easily become an error source. With modules which you unlock by adding type module and by using a web server, even if it's just a dummy one for development, with modules you get rid of that because there every Javascript file states its dependencies and has its own import so to say. Now you can only import what you export with the export keyword, either with such a named export where you're just throw export in front of your class, function, constant or variable or with a default export, something you can also do and which we did in the component.js file for example.

You can have both named and default exports in the same file and when it comes to importing, you also got a lot of flexibility. You can import named exports without or with an alias, you can bundle all exports together or of course, you can also import default exports and named exports at the same time. Last but not least, we also had a look at the dynamic import which can help you split your code and download things only when you need them instead of in advance and that's it for modules.

Modules are a core feature and in the next course section, we'll build upon this knowledge and see how we can improve them even more.

----------------------------------------
