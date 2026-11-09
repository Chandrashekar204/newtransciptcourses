# 21.12 — Using webpack-dev-server

> Section 21: JavaScript Tooling & Workflows

So now we got the webpack basics set up, we're able to create our output here. Now what we don't have is that development server that would automatically reload whenever we change something and that would be nice to have. For that, we have to install an extra package with npm install --save-dev and that's webpack-dev-server. Hit enter and install this package, again locally into this project as a development dependency and we can then use this dev server to serve our application. For that let's go to webpack.config.js file and there, maybe after output, you can add a dev server entry, the exact order of configuration options here doesn't matter by the way and dev server can be an object where you set a content base key.

This tells dev server where your root HTML file can be found and here, that's just ./, it's the same folder as the config file, therefore you actually also can omit this setting here altogether, it will just work because that will be the default anyways. So now to use that dev server, we can go to package.json and tweak our script, we got the build script here, now let's also add a build: dev script maybe, you can again name this however you want and there, we run webpack-dev-server, like this and this again will take our webpack config into account and will do all the webpack things but it also launches that development server that's tied to the output.

So if we now run npm run build: dev here, it should spin up that development server and still do our build but now this is a process which keeps on running and you should keep this running until you are done for the day, at which point you can always quit it with control c and then you can always restart it by executing that command again. As long as it is running, it watches for changes in your entry file or in any file associated with that and it will rebuild whenever you do change something there.

You can visit your page on this address which it outputs up there, in my case localhost:8080 and therefore now if I enter this here, I got the same running project. Now let me show you that live reload which I meant, if I go into let's say the project list file here and I comment out this console log and save, you see it recompiles, it did find out that project list changed and it also reloaded the page here. Now how do I know that it reloaded the page? Because the console here has a new output different from before, it's not printing the output from my project list from line 25 anymore, that's not happening as you see here.

Now of course we don't need serve anymore but instead we can just use this webpack dev server which automatically rebuilds whenever we change something and which therefore of course gives us a very convenient development experience.

----------------------------------------
