# 22.2 — Optimized Substructure

> Section 22: Dynamic Programming

So in this video we're going to talk about the second requirement for dynamic programming. And that is an optimized substructure. Now optimized substructure sounds really complicated but it is a pretty simple concept. It's an extension of what we saw in the last video. In the last video, we took a problem and we broke it down into subproblems. And they needed to be overlapping subproblems. But there's something else about these subproblems that has to be true.

They have to have an optimized substructure. So to explain what that is I'm going to bring up a weighted graph. Let's say we want to go from A to D and we want to have the lowest cost path. Well there are two ways to get there. We can go a C, D and the total cost would be 50. The 30 plus the 20. Or we can go this way and the cost is 25. The ten plus the 15. Obviously this would be the better path. But in order to get from A to D we have a couple of subproblems.

We have the sub problem of how do we go from A to B, and the sub problem of how do we go from B to D. And what makes this an optimized substructure is if you get the optimal way of going from A to B, and the optimal way of going from B to D, it gives you the optimal way of going from A to D. So going back and looking at the subproblems like this, you have to have an optimized substructure, which means if you have the optimal solution for subproblem one and subproblem two and subproblem three, that's going to give you the optimal solution to the overall problem.

Now, to show something that does not have an optimal substructure, I'm going to bring back that same weighted graph. But now instead of doing the lowest cost path, we're going to do the highest cost path, which is going to be this. Now I want to point out this is the highest cost path that doesn't have any overlap or retracing, because you could just go from A to C, back to A, back to C infinitely and have an infinite cost path. So this is doing it with no overlapping.

So now let's look at what is the highest cost path from A to C. It is not to go directly from A to C, it is to go all the way around like this. And the highest cost path to go from C to D is to go all the way around like this. So in this situation, you can't take the optimal solution to each subproblem and solve the overall problem. So this is our second requirement for dynamic programming. Remember, the first one is that you have to have overlapping subproblems.

And the second one is that you need to have an optimized substructure.

----------------------------------------
