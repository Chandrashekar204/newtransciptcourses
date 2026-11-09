# 14.6 — Graph: Add Edge

> Section 14: Graphs

So now let's build our Add Edge method. And Add Edge is just going to take two vertices which will look like this. And then we add an edge between them. And in the adjacency list that will look like this. So let's bring this down to the bottom and write the code for this. So we'll call this Add Edge. We'll pass it the two vertices that we're creating an edge between and for the next line of code, what I'm going to do is I'm going to break it into two pieces.

So we're going to say adjacency list dot get we're going to pass it vertex one. In this case that's going to be a down here. And when we run this get method what it's going to return is this array list. So we pass it the key and it returns the value. This is just like we did with the get method and the hash table section. That's doing the same thing here. So since we've returned an array list we can now use the methods that apply to an array list.

So we can say dot add. And this dot add applies to the array list. And we'll pass it vertex two which is b which does this. So we'll do this exact same thing again, except switching vertex two and vertex one. And then we'll add vertex one to this array list. And that adds the edge between a and b. So these two lines of code here can only be run if both of the vertices that we're adding the edge between exist. If all the vertices that we have in our graph are a and B like we have here, then obviously we cannot add an edge between A and C.

So we're going to wrap these two lines of code with an if statement like this that says if vertex one and vertex two both exist, they're not equal to null. Only then do we run these next two lines of code. And if the conditional in this if statement is true and we've added the edge, we'll also want to return true. You have the conditional in the if statement is false, we'll skip past that and we'll return false. So that is our entire add edge method.

Now let's flip over to IntelliJ and take a look at this. So there is the add edge method that we just created. And I'll come up here to this tab where we have our main method. And with this line here we'll create a new graph. And then with these two lines we'll add those vertices a and b. And then we'll print this out and I'll run this. So you can see up here that we have our two vertices A and B, but we don't have an edge between them yet. So I'm going to come up here and add a line.

And with this line we'll add an edge between A and B, and then we'll once again print out the graph with this line here. So I'll run this. And you can see now that we have an edge between A and B. And that is our method for add edge.

----------------------------------------
