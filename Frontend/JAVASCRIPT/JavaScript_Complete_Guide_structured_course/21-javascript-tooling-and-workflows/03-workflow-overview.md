# 21.3 — Workflow Overview

> Section 21: JavaScript Tooling & Workflows

Before we get started, let's see how we would combine these tools though. Well the idea would be that when we write our code, we want to have two different workflows which we can start. We either have our development workflow which should start whenever we save changes to our code or our production workflow which you typically want to start with a certain command because that should not run whenever you change your code but only once you're ready for it and you explicitly want to start it.

Now no matter which workflow we're in, we'll always need npm and Node.js. You might remember we installed that earlier already because we needed it to install that development server globally and the development server in turn also requires Node.js to run. So this should already be installed globally, if not make sure you do it, we do it together in this module because Node.js will be used by many of these tools behind the scenes to execute code on your machine and do these various optimizations and npm is the Node Package Manager which typically is used to install these different tools and also to orchestrate them, to start the different workflows and so on.

Now with that let's see what we have inside of these workflows. Well when we build for development, we want to have linting set up so that we basically can check our code and we always see if we have code quality issues in our code. We then of course also want to bundle our code so that we combine our different files into a couple of bigger files, so that we don't send all these unnecessary HttpRequests and we then want to have a development server which automatically reloads whenever our code did change and that in a nutshell would be what we want to do when we develop and when we changed our code.

Now during production, we still might want to lint but we're doing this all the time during development so this kind of already should have been done by this point but of course we also want to bundle our code with the help of webpack, we still want to ship a couple of files instead of dozens of files. Now however, we also want to compile our code, to translate it from modern Javascript to Javascript that runs in older browsers as well but again we'll cover this in a separate module and once this is done, we want to optimize the code, something we don't do during development because it can make debugging harder but we definitely want to do it in production. Well and then we have our production ready code which we get as an output and which we can now upload to the server where we need it.

These are the two workflows and we'll implement both in this module.

----------------------------------------
