# 22.1 — Overlapping Subproblems

> Section 22: Dynamic Programming

Welcome to Dynamic programming. Now there are two things that are required for something to be able to use dynamic programming. We'll talk about one of those things in this video and one of those things in the next video. So the first requirement is going to be overlapping subproblems. And that might sound like a complicated turn, but this is not a complicated concept. We have already seen in this course where sometimes you can take a problem, break it down into multiple subproblems, solve each of the subproblems, put them all back together, and solve an overall problem.

With overlapping subproblems. It looks a little bit different with overlapping subproblems. You're going to have some problems that repeat. So for example subproblem number one all of these subproblems are identical. Same is true of subproblem number two and subproblem number three. So when we say overlapping subproblems we are really saying repeating subproblems. So let's say for example, we have that first subproblem subproblem number one. And let's just say it's incredibly processor intensive and it's a trillion operations.

And when we get all done running this it returns the number ten. Well when we move to the next subproblem that is identical, we already know it should return the number ten. So it would be really inefficient to do those trillion operations again. So one of the things that we could do is take that number ten and store it in an array list. And since that was subproblem number one, we'll take that ten and put it at the index of one. So when we move to this next subproblem, we could check to see if we have a value at the index of one.

And because we do this becomes an O of one operation. So now we'll move to that next subproblem. Let's say that one's a trillion operations as well. And it's going to return the number 20. Of course we're going to store that at the index of two. And the same thing for subproblem number three. And we'll store that at the index of three. Now when we move to these four subproblems we can pull up each one of these answers like this as an O of one operation, which of course is much more efficient.

And now that we have the answers to all of these subproblems, we can put them all back together and solve the overall problem. So this process of storing the answers to these subproblems is called memoization. Now it's not memorization. It is memoization. So now that we've looked at this concept of overlapping subproblems, I'm going to bring something back up that we looked at earlier in the course that uses subproblems. But they're not overlapping subproblems.

And that is merge sort. So when merge sort, the subproblem of breaking this in half is different than breaking either of these two in half. And all of these are different than breaking these in half. These are all unique problems. None of these overlap. And that is to say, none of these subproblems are repeating subproblems. They're all different and unique. Likewise putting these first two items together, this five and this four, and putting them together where they're sorted.

Is a particular subproblem that is different than putting together a seven and a one. And both of these are different than putting together a three and a two, etc.. And putting these together our unique subproblems and so on. So I want to emphasize that merge sort is not a candidate for dynamic programming. It has subproblems, but it does not have overlapping subproblems. And that is the first thing that is required to be able to use dynamic programming.

In the next video, we're going to talk about how you also need to have an optimized substructure. But for now, that is our overview of overlapping subproblems.

----------------------------------------
