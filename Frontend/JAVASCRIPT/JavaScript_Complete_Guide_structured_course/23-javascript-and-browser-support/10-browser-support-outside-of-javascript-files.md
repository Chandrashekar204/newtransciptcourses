# 23.10 — Browser Support Outside of JavaScript Files

> Section 23: JavaScript & Browser Support

Now one last word about browser support. This is a Javascript course and therefore I talked a lot about Javascript code and how you can make it work and the different features you might be using, how you can make all these things work in different browsers. Now of course it doesn't stop at our Javascript file though, if we go to index.html, we also have our script import and there here I'm just importing app.js like this because webpack bundles it all together into one big file.

If you would be using Javascript modules without webpack, then you might remember that you had to add type module, you can also leave it here when you use webpack but you technically don't need it because you don't really use modules anymore, webpack bundles it all into one file after all. Now if you do add it however because you're maybe not using webpack, you're working with multiple finds and modules, then older browsers will not support this type module script and then you can add a script where you add the no module tag just like this, which will be used by older browsers as a fallback. To be precise, older browsers will not understand this script tag and ignore it and they will not understand no module but they'll just ignore this attribute and instead execute the script.

Modern browsers on the other hand do understand type module and execute this script and they also do understand the no module attribute and therefore they ignore this script. So this script can hold any fallback code that you want to use in older browsers which don't support modules, again if you're bundling all your code together, you don't need that however. Another thing that might be interesting is users who disabled Javascript. Now most users these days have it enabled but some might have it disabled.

Now depending on your web site you're building, on the application you're building, that might mean that your entire app doesn't work properly, imagine rich web applications like Google Docs and so on, they really rely on Javascript and you can't make them work with fallbacks without Javascript. In that situations, you might want to show some message to your users though and that can be done with noscript HTML tag where you can say Please enable Javascript to use this page and now your users at least know why it's not working.

So this is not really a fallback that magically makes your application work but at least it tells your browsers who have Javascript disabled why the page is not working properly. So this is also something you might want to keep in mind.

----------------------------------------
