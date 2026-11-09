# 21.13 — Generating Sourcemaps

> Section 21: JavaScript Tooling & Workflows

Now what about debugging? What if I want to debug my code? Well if we go to the sources tab and you check out assets scripts, you will find a file which is pretty hard to debug, all the webpack code is in there and is pretty impossible to debug your code there but you should also have a webpack folder here so to say. There you should find a .folder and there in source, you find your original code files, at least mostly original but these are also tweaked by webpack and the app.js file is empty.

So this is better for debugging but still not ideal. To get a good debugging experience, we need to go back to the webpack.config file and there, add a so-called dev tool. Add the dev tool entry here and now you need to parse in a string here or provide a string where you use one of the provided development tools which in the end just means how webpack links your file to the original code you could say, so how well this is from a debugging experience.

There you got different levels of detail and the better the linking, the slower the build process and so on, the bigger the output. So for development, you want to have good linking for good debugging, for production you of course want to minimize this to have as small of an output as possible and to also speed up the build process. So which options do we have here? We can find that in the official docs, there under guides, if you click on development, you can click on using source maps where you can learn more about that and then here, click on different options.

There, you see all the built-in dev tools and you can check out this table to find out which one works best for you, here I'll go for cheap-module-eval-source-map, copy that and enter it here in this string and now if we save that, we have to restart our build dev process to take the new configuration file into account and with that done, if you go back to our project and reload there, you should find that in the webpack folder in the .folder now in the source folder, you really find your original code here if you inspect these files and you can also place breakpoints there, for example if I go to project list here and there to the drop event listener and we add a breakpoint, then as soon as I do drop, we indeed pause here and we can do what we can always do here, we can do everything you learned in the debugging section.

So now we have a great setup for development and we can now also debug our code and with that, we bundle our code, we have the development server and we can also debug our code and we have a good development experience. We also added linting which you can of course also fine tune to your requirements regarding the rules you used there, now what's missing is that we also have a finished production workflow, where we optimize our code and spit out as small of a codebase as possible.

Let's do that next.

----------------------------------------
