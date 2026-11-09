# 14.8 — Graph: Remove Vertex

> Section 14: Graphs

So now we're going to create our remove vertex method. I'm going to bring up a graph like this. And let's say we're going to remove the d vertex. If we're going to remove that we also need to remove all of the edges with D like this. And then we can remove the vertex. So I'm going to bring D back like this and put everything back the way it was. So this graph would be represented by this adjacency list. And I'll just keep that on the screen since that's what we're actually working with.

In the big O video, I talked about an efficiency that we could use when removing a vertex when all of our edges are bidirectional. And we're able to use that efficiency because of what is stored in this adjacency list. If D has edges with A, B, and C, we know if there are bidirectional edges that A, b, and C also have edges with d. So even if we had a graph that had a thousand vertices in it, we know that only these three have edges that connect back to D.

So what we can do is loop through this array list, and we know that a in its array list must have an edge back to D. And then we can remove that. And we can keep looping through that array list at the bottom. And we know that B must have an edge back to D. And we know that C must have an edge back to D. And like I said, if we had a thousand vertices, we don't have to visit any of those other vertices to remove the edge back to D, we only have to visit these three.

Now that we've removed all of the edges going back to D, we can come down here and remove the vertex. And that leaves us with a graph that looks like this. So now that we've walked through that, let's start writing the code. We'll call this remove vertex. And then we're just going to pass this the vertex that we want to remove. So the first thing we'll do is this. We'll say if adjacency list dot get and we'll pass this the vertex. If it's null, that means that the vertex is not in the graph.

If that's the case we're just going to return false. Otherwise we know the vertex is on the graph. And the first thing we want to do is create a for loop to loop through that array list. So we'll do that like this. And we'll walk through all of this here in a second. But we're going to pass this the vertex adjacency list dot get. We're going to pass that the vertex. So now I'm going to focus in just on this line of code and bring this up. So remember when we do adjacency list dot get pass it the vertex that vertex is d.

And what it returns is this array list. So this is what we're looping through in this for loop. So I'm going to call this variable here other vertex. Because this is the other vertex that we need to go to to remove the edge that goes back to d. So I'm going to bring back the rest of our code like this. So I'm going to break this next line down into two steps. We're going to say adjacency list dot get. Other vertex. And remember that's going to return an array list.

So we can use the methods associated with array list. And we can say dot remove. The vertex that we want to remove from that array list. So now let's look at just this line of code. Remember that this line is inside of the for loop. So I'm going to do this and walk through what this does. So the first time through the for loop other vertex is going to be that a variable that I have highlighted in the d vertex at the bottom there. So the adjacency list dot get is going to give us this vertex.

The dot remove vertex is going to remove d. And then we move through the for loop and do that here. Now other vertex is going to be b and then we remove d. And then we do it again here other vertex will be c here. And then we remove that. So let's bring back the rest of our code. Like this. Now we've removed all of those edges that go back to D. Now we can actually remove the vertex d like this. So adjacency list dot remove. We pass it this vertex.

And that is going to do this which gives us a graph that looks like this. Now there's one thing left to add to our code. And that is to return true because we are returning a boolean. So that's the entire method there. We'll look at this method in a moment in IntelliJ. And when we do we'll create this graph. And then we'll run the remove vertex method to remove the d vertex like that. And that will leave us with an adjacency list that looks like this.

So now let's flip over to IntelliJ and take a look at this. So there is our remove vertex method there that we just created. Then I'll come up here to our main class that contains our main method. And then with this line here we create a new graph called my graph. With these four lines. Here we create the four vertices a, b, c and d. And then with these lines here we'll add all of the edges that we had in the diagram. And with this line here we'll print this out.

So I'll run this. And this prints out our graph up here. So now I'm going to come over here and I'm going to add this line of code. And this will remove that vertex D. And then with this line here we will print this out. So I'll run this. So you can see that the vertex d and all of the edges to d have been removed. So it looks like we have a working method for remove vertex.


########################################
