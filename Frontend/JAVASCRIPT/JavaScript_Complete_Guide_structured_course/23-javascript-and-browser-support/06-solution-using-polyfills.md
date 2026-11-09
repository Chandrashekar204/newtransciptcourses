# 23.6 — Solution: Using Polyfills

> Section 23: JavaScript & Browser Support

Another strategy for making code work in more browsers is to use polyfills. A polyfill is a third-party package that adds a functionality which otherwise might be missing in a browser, let's say you want to use promises. Promises might not be available in all browsers, for example Internet Explorer does not support promises and therefore to still make it work there, you can add such a polyfill which again is just a third-party package that actually teaches the browser how to use that feature.

Now obviously, this is not possible for all features, some features rely on some core mechanics which can't be worked around with Javascript, some features however can be replicated with other Javascript features and therefore an older browser which might not support let's say promises but supports other features with which you can rebuild the idea behind promises might be able to utilize such a promise polyfill. So it's a third-party Javascript feature that simply adds something to a browser which otherwise is missing there.

So for some features and functionalities, this might be very interesting to have. Now how do you find such a polyfill? For example if you search for fetch here on caniuse and you want to use fetch and you know you also need to target older versions of Edge and let's say Internet Explorer. Well then here under resources, you would find a link to a polyfill, of course you can also just try your luck and search for fetch polyfill. In both scenarios here with that link or with our first search result, you actually would end up on this GitHub page here and there, you learned about this fetch polyfill and here you learn what it does, what it is able to do and what it is not able to do and how you can add it and how you can use it.

You also learned that for this polyfill to work, you also need to add another polyfill to make promises work and there, you could for example dive into this recommendation and make this promise polyfill work, then you would also have to follow the installation instructions there, here you can simply use the CDN link for example and throw that into your index.html file and with that you would be able to use promises and with this polyfill, you would also be able to use the fetch API because what the polyfill does behind the scenes is it basically adds this fetch function, fetch method to the global window object you could say and it does so by rebuilding the fetch API with features that are available in older browsers as well.

And if you're interested in seeing what happens under the hood, you can simply dive into that open source code here and learn how they rebuild the fetch API with other tools, to be precise with XMLHttpRequest here. So polyfills can also be a very nice feature to making features work in browsers that would normally not support it. Of course not magically, you're not touching the browser source code after all but by simply working around the features with features the browser does support.

Therefore this is not available for all features you might want to use but for some, especially promises and the fetch API are prominent examples which you can make work in older browsers even though they normally would not work there.

----------------------------------------
