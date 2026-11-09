# 14.1 — Graph: Intro

> Section 14: Graphs

Okay. Now let's look at graphs. We're going to start out by bringing this up. This is called a vertex or a node. The proper way to say it is vertex but you'll hear the word node. And we'll bring up another vertex. The plural would be vertices. Then between the vertices we have what is called an edge or a connection. The proper way to say it is edge. So we have vertices and edges. Let's bring in another vertex like this. So this vertex can have an edge with this vertex, or it can have one.

With this one we're going to have one with both. There is no limit to how many other vertices that a vertex can connect to. So now that we have a small graph, let's look at a couple of concepts. Let's say you want to go from this vertex to this vertex. Well, when you look at this, you would say that you don't want to go this way because that is two hops. And this one is one you'd want to go the more direct route. But with graphs, one of the things you can have, you're not always going to have, but you can have are weighted edges.

So where you would use something like this would be in a maps app. You're using Google Maps. And the road between 76 and 82 has a lot of traffic. So you go this way instead, because this has a cost of five, and going this way has a cost of 15. Another place you'll see something like this is with network routing protocols. It would be better to have an extra router hop and have two very fast links, then to go the way with the very slow link. And like I said, the edges can be weighted or not weighted.

So another concept with graphs. We'll explain this with a Facebook connection between you and a friend. So with a typical Facebook account, your friend is friends with you and you are friends with your friend. It is a bidirectional relationship. So in a graph where all of the edges are bidirectional, you'll often see it like this without arrows. And when you see it like this, it is assumed that it goes both ways. So let's compare this to something like Instagram or Twitter when you follow a celebrity.

You are following the celebrity, they don't follow you back. That is directional. So the edges can be weighted or non weighted. They can be directional or bi directional. Also we have seen a graph in this course. It was a tree. Trees are a form of graphs, but they have the limitation that each node can only point to two other nodes. And when we looked at trees, we had mentioned that we had seen a tree before, which was a linked list. So linked lists are a form of a tree, and a tree is a form of a graph.

Therefore, a linked list is a form of a graph with the limitation that they can only point to one other node. But we typically think of something that looks like this when we think of graphs.

----------------------------------------
