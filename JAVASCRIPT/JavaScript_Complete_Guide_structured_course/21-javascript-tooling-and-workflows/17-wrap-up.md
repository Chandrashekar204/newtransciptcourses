# 21.17 — Wrap Up

> Section 21: JavaScript Tooling & Workflows

And that's it for now. Now we're using webpack to bundle our files, to optimize them, to have a dev server. We're using ESLint to lint to our files and of course there, you can configure this to your requirements, to your needs with the help of the official docs also as I mentioned and we now therefore have a setup where we're able to write our code in a way that works well for us developers, in a way where we can split our code across multiple files and where we then still produce output which is optimized and which also is bundled together to minimize the amount of HttpRequests and still, features like this dynamic request for more here, for this tooltip.js file which is only needed eventually still works, so that all is supported by webpack, a very powerful tool therefore with which you of course can do more.

The docs are very long and there's a lot you can tweak and manipulate there, so definitely dive into this documentation if you want to learn more about webpack and what you can configure there, you can fine tune it in a lot of different ways. Also one thing which we haven't done at all right now is we haven't used loaders in webpack. Loaders allow us to transform files and that allows us for example to use next gen Javascript features when we write our code and still produce code that does not use these features and works on older browsers as well and this is a pretty exciting technology or thing we'll explore in the browser support module.

----------------------------------------
