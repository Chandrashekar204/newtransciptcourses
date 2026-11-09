# 18.19 — XMLHttpRequest vs fetch()

> Section 18: Working with Http Requests

So now we had a look at XMLHttpRequest and the fetch API, both allow us to send requests, the fetch APIs more modern and not supported in older browsers. A big plus is that it's generally easy to use and uses promises out of the box, a minus is that error handling can be clunky. Of course not the end of the world but not the most beautiful approach. Now arguably, that's also not that beautiful but if you hide it behind some custom function, it might be fine and might be a bit more straightforward to understand, in the end however you can also hide this behind a custom function and you're probably fine again.

It's up to you which approach you use, both are fine to be used and actually another alternative which you have is that you use a third-party library, something we haven't really touched on yet which might wrap this, so the XMLHttpRequest or this fetch API approach and gives you a nicer API to work with, where you don't have to care about how it's implemented internally and that's actually something we'll have a look at in the third-party libraries module which comes right after this one.

But it's important to understand how to implement this natively and often, the fetch API is great because it's easy to use, quick to get started and uses promises out of the box but also be aware that XMLHttpRequest has better support for older browsers out of the box and in some places, regarding error handling specifically, might be more straightforward.

----------------------------------------
