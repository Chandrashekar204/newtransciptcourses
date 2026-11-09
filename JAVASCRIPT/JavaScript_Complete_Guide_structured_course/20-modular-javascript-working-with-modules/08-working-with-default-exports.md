# 20.8 — Working With Default Exports

> Section 20: Modular JavaScript (Working with Modules)

Now one last important feature regarding the export import syntax we saw here, if you have one core element which is exported in a file or maybe the only element which is exported, like here component is the only exported thing in component.js, then you can absolutely export it like this but you can also name it the default export of this file by adding default here, this keyword. You can then even omit the name here because you'll now not import it by name but by just pointing at that file and then automatically the default export will be picked and I'll show you how that pointing works in a second.

Now you can still have named exports along that, so here if I had the doSomething function here, so export function doSomething which actually does nothing here, then I could do that, we could import this by name and this as a default which now just leaves the question, how do we import something as a default? We'll, we're using component in tooltip after all and this import would now fail. If I save everything and I reload, we would get an error because as the error message says, component.js does not have an export named component because I removed that name and even if I would add it by the way and I reload, it would still fail because we export this as a default in which case Javascript will ignore the name.

So how do we now tell tooltip that we're interested in the default export of components.js? Very simple, you just use a syntax you already saw before, you just say import anything, any name of your choice like cmp for of course also component but doesn't have to be the exported name or the file name, can be any name from file and then here we could use cmp instead of component. This tells Javascript that since you don't wrap this in curly braces, this should be the default export of that file and of course therefore this syntax only works if a file has a default export, otherwise it will fail.

So now with this line, we import the default export of this file, which in this case is this class, under that name which is totally up to you. You can use this feature, it has the tiny disadvantage that since you have to rename it when you import it, if you're working in a team, every team member might have his or her own naming convention and you might end up with code which uses different naming conventions and therefore, using named exports where you're all forced to settle on some name might be better.

Nonetheless it is a feature which you can use and if you now would want to import that named doSomething export, you would do that by simply combining this with a comma, with a curly brace list of named imports, so here I could import doSomething. So you can have a default and non-default, also called named export side-by-side and therefore of course you can also have them imported at the same time. This is the default export and here you list all named exports, so all the things where you just added export in front of them without the default keyword.

Also of course important, should be self-explanatory though, you can only have one default export per file, you can't have more than one.

----------------------------------------
