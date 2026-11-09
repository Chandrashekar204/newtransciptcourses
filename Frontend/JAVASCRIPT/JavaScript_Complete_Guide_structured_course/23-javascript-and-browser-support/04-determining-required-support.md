# 23.4 — Determining Required Support

> Section 23: JavaScript & Browser Support

So now we know how we can check browser support, now with that, the naive thought might be that you simply check all these resources and then you need to find a way to make the feature you want to use work in all possible browsers across all browser versions and here, the clear answer is don't do this. For one, this will never be entirely possible, there are super older versions of Internet Explorer that don't support anything, you will never be able to make your application with all its features work there.

You would just cut so many features that just to support a small fraction of the user base, you pass on some awesome features and awesome improvements you could offer to the vast majority of the user base. So you definitely have a tradeoff there and you want to be careful regarding your decision. Don't build an application for the smallest possible denominator, instead analyze your market, get an idea of who your users will be and then build your application for those users and use the features or make the features you plan on using work for these users and their browsers, not for the global user base.

Here are some ideas, let's say you're building some internal tool or application, so something that runs in the internal company network and only employees of the company will be able to use that. It's a common use case, all companies have their own internal systems which often also are just web applications. Now there, the company browser might be clearly defined, maybe as a policy in your company, everyone has to use Chrome or Chrome or Firefox or everyone has to use Internet Explorer 11, then you know exactly what your user base is, you know exactly for which browser you need to build and you certainly don't need to support any other browser or let's say you are building some web page that targets tech savvy users, some blog about technology, some online learning site, anything like that.

Well there, it's very likely that you have users who are using cutting edge or modern browsers and versions of these browsers by default because they're interested in technology, they keep their system up-to-date and of course they're using the latest browsers because they want to use all these rich web applications, then you might not need to support very old legacy browsers because only a very small fraction of your users visits your site with these browsers and it might be fine to pass up on these users, you can't satisfy everyone, maybe you want to show some message to these users who won't be able to use your site but that's all.

Or you're building a site that targets older people or is simply a non-tech savvy audience, so then of course these people might be more likely to use slightly older browsers and therefore you want to make sure that you support these people and their browsers. You might not be able to rely on your audience to use cutting edge browsers and maybe therefore you need to be more cautious regarding which features you use and how you test your code on older browsers and that's one other thing by the way.

You of course also want to test your application in a broad variety of browsers, reflecting the browsers you would expect your users to have.

----------------------------------------
