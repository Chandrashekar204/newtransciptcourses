# 2.1 — Big O: Intro

> Section 2: Big O

In this course, we're going to spend a lot of time on big O. It is a huge topic when it comes to data structures and algorithms. So what is big O? Big O is a way of comparing two sets of code. And let's say code one and code two accomplish exactly the same thing. How would you compare one against the other? Code one might be more readable. That might be better. Koto might be more concise, the code might take up fewer lines, and if that's what you're measuring, then you would say that code two is better.

Big O is a way of comparing code one and code two mathematically about how efficient they run. In a coding interview, you will absolutely be asked questions about big O. So let's look at what big O is. Let's say we have a stopwatch and we run code one, and we start the stopwatch, and it runs for 15 seconds, and we reset the stopwatch, and we run code two, and code two runs a lot longer than 15 seconds. It runs for a full minute. Based on this, you would say that code one is better than code two.

You can measure it. This is called time complexity. The thing about time complexity that is interesting is that it is not measured in time. Because if you took the same code and ran it on a computer that runs twice as fast, it would complete twice as fast. It doesn't make the code any better. It just means the computer is better. So it is measured in the number of operations that it takes to complete something. And we'll look at examples of that as we go along here.

In addition to time complexity, we measure space complexity. So let's say that code one. While it runs very fast comparatively, let's say it takes up a lot of memory when it runs. And maybe code two, even though that takes much longer to finish. Maybe it takes up less memory. If preserving memory space is your most important priority and you don't mind having some extra time complexity, maybe code two is better. So when you get into an interview, there's a good chance that you'll be asked questions about time complexity.

And then they'll say, hey, well, what if space complexity is our main priority? How would you approach it then? You have to understand both concepts and be able to address that in the job interview. But for the most part in this class we will be dealing. With time complexity. And that is our quick intro to big O.

----------------------------------------
