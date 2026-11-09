# 20.10 — When Does Module Code Execute?

> Section 20: Modular JavaScript (Working with Modules)

And with that, we're almost done. Now one important question might remain though, when you're working with modules and you have some code that runs inside of the module file, so which is not a class which you find on export but let's say here in project item, if we have a console log statement saying project item created, is this code executed or is only exported code executed? Well let's find out. This is my console log statement, here is my console, if I now reload, we see that output.

So code in your modules runs when the module is imported and loaded for the first time and that's important, for the first time. If you have a module which is imported multiple times, like DOM helper which I imported in project item but also in project list, then it still only runs once. So if I go here into my DOM helper class and I add console log here, DOM helper executing, we'll see that this only gets printed once even though we import from this file twice but it only runs on the first import so to say. So if I reload here, we see DOM helper executing but it never runs thereafter.

What if we have some code in a dynamically loaded file, like tooltip which we just dynamically loaded Well let's output something here, tooltip loading or running, whatever you want. Let's output this here, let's reload, of course we see no output initially because the file hasn't been loaded. If I click on more info, we see this but only for the first time, if I click on more info thereafter, it does not run again. So code in modules does execute and of course sometimes you want that, you need that behavior but it only executes once when a module is imported and used for the first time.

----------------------------------------
