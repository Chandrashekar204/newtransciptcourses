# 26.1 — Module Introduction

> Section 26: Meta-Programming: Symbols, Iterators, Generators, Reflect API & Proxy API

This will be an interesting module, it's about meta programming or to be precise, it's about symbols, iterator and generators, the reflect API and the proxy API and these are all very niche and advanced Javascript features which you will, to be honest, not use that often. I would say they are most interesting to library authors, so if you're building a Javascript package what you plan on sharing with other people, either by sharing it on npm or even if it's just an internal, a company internal package, then some of these features might come in handy because all these features basically have in common that you can make life easier for other developers.

So these are Javascript features but they're not like adding a click listener to a button which does something which your end users will in the end have something from, right, because they can click on a button and something happens, no these are features which the end allow you to change the way certain parts of the code behave or work and they allow you to improve code safety, not from a security standpoint but from an API standpoint where you can for example make sure that the objects or the functions you expose to other developers are used properly.

These are basically the things these features help you with, so we'll have a look at them in this module so that you heard about them, that you get the general idea but you will probably not use them every day in all your projects. Still, if you encounter them or if you are building some third-party library or you're working in a very advanced projects, then these features might come in handy.

----------------------------------------
