# 15.7 — Closures & Memory Management

> Section 15: Advanced Function Concepts

Now one word about memory consumption and memory usage. If every function logs in all surrounding variables, doesn't that lead to a pretty bad effect in our memory because in big applications where we have many variables, a function might log in a lot of variables which it never uses. So Javascript doesn't get rid of these variables because a function closed over them but the function might never get called or even if it gets called, it might not be interested in all variables, so isn't that a memory issue?

In theory, it would be but of course Javascript engines are pretty smart or the people who are working on them are pretty smart and therefore, modern Javascript engines optimize this. They basically track variable usage you could say and if a variable obviously isn't getting used by anything, not by any functions and nowhere else, then they will get rid of it and they will do so of course in a safe way so that they don't accidentally crash your program because you need to use that function at some point of time, they're really smart about that and they optimize this whole behavior so that you don't manually have to reset all variables that you don't need, Javascript engines will do that for you in a smart way.

----------------------------------------
