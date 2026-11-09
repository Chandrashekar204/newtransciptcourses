# 14.4 — Graph: Big O

> Section 14: Graphs

So now we're going to look at the big O of graphs. I'm going to bring up the graph that we've been using. And we've looked at two ways of representing this graph an adjacency matrix and an adjacency list. And we're going to look at the big O of both. So first we'll look at space complexity. So if we have a vertex like a with an adjacency list we're going to store that vertex. And then we're going to store each one of the edges in an adjacency matrix.

We store those edges. But we also have to store everything that it is not connected to all of these zeros. And that is a big advantage of the adjacency list. So for space complexity the adjacency matrix is O of the number of vertices squared in the adjacency list, it's the number of vertices plus the number of edges. So from a space complexity perspective, the adjacency list is better. So let's bring back our graph. And let's say we're going to add a vertex.

We're not adding an edge yet. We'll look at that in a moment. We're just adding a vertex. And it is not connected to anything with an edge yet. So let's bring these back up and we'll look at the adjacency list first. Adding a vertex is just a matter of doing this with the adjacency matrix. We have to do this. So the adjacency matrix is going to be stored in a two dimensional array. As soon as you make those arrays bigger you have to create new arrays that are bigger.

And recreating those arrays is very inefficient. So from a big O perspective, the adjacency matrix is the number of vertices squared every time you add a vertex, whereas with an adjacency list it's O of one to add a vertex. So the adjacency list is much more efficient at doing this. So let's bring our graph back. And we're going to add an edge between B and our new vertex f like this. And let's bring these back up and look at the adjacency list first.

In order to do this we'll add an edge that goes from B to F like this. And then one that goes from f to be like this with the adjacency matrix, we just go in and change this from a zero to a one. And then we do the same thing here. And that adds that edge between f and b. So both the adjacency matrix and the adjacency list are O of one to add an edge. So let's bring back our graph and look at what it would take to remove this edge. We'll bring these back up and start with the adjacency list.

In order to remove the edge between b and f we're going to go find B. And finding a key and a hash map is O of one. But once we find B, we have to iterate through that entire array list and find f and then remove it. Then we'll come down to f and do the same thing. Here. Go through this array list. And remove be. With an adjacency matrix. We just come here and change the one to a zero. Change this one to a zero, and that edge is removed. So this is a situation where the adjacency matrix outperforms the adjacency list.

The adjacency matrix is O of one. But the adjacency list you have to go through all of the edges. And a particular vertex might have a thousand edges. And you'd have to go through the entire array list to remove the edge. So now let's bring back our graph and we will remove a vertex like that. So let's bring this back up and we'll start with the adjacency list. So when you're looking at this this looks pretty simple that you would just remove this.

But we're also going to have to come here and go through this entire array list here and see if there are any F's. Then we're going to come down here and do the same thing with this array list and so on through the entire adjacency list. So you're going to have to touch every vertex and every edge. There is a way to do this more efficiently if you have bidirectional edges. And we'll go over that when we do our method for remove vertex, because we're going to create our graph with bidirectional edges.

So now let's look at this with an adjacency matrix. In order to remove that f vertex we have to do this and rewrite the arrays. So this is also very inefficient when we remove a vertex from an adjacency matrix. So the big O of the adjacency matrix is going to be O of the number of vertices squared. The adjacency list is O of v plus e. In other words, you have to touch every vertex and every edge. So in this course we're just going to create an adjacency list.

And I want to talk a little bit more about why an adjacency list is typically better than an adjacency matrix. So we talked about with an adjacency matrix that we're not just storing the connections the ones. We also have to store all of the zeros. All of the things that we're not connected to. This becomes incredibly inefficient when you have a very large graph. So say you have something like Facebook. And we'll say for easy figuring that Facebook has a billion active users, well, you would have a graph that has instead of five like we're showing here, that would be a billion items across the top and a billion items down the left side of this graph.

Even if each of the billion users had a thousand friends, you would have literally a million zeros in that graph for every one. So that would be incredibly inefficient. So that is why in this course we are going to use an adjacency list. And that is graph big O.

----------------------------------------
