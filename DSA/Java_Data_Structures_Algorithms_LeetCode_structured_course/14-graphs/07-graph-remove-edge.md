# 14.7 — Graph: Remove Edge

> Section 14: Graphs

So now we're going to write our method to remove an edge that's going to look like this. If we remove an edge between A and B and the diagram at the bottom, it's going to look like that. And in the adjacency list on top removing the edge is going to look like this. So let's move this down to the bottom and we'll bring these back. And then we'll write the code to remove those. So we'll start our code out like this. Remove edge. We'll pass it the two vertices that we're removing an edge between.

So with this next line of code, I'm going to do the same thing we did in the last video where we break the line of code into two parts. So first we're going to say adjacency list dot get vertex one. So vertex one is a. And when we do the get it returns the array list. And because of that we can now run methods on that array list. So we can say dot remove vertex two. And that removes that. Now we'll do the same thing going the other way. And in this case we'll remove vertex one.

Like that, and that removes the edge. And just like we had in the Add Edge method, we couldn't add an edge unless both vertices existed. Similarly, with this method, remove edge, both of the vertices have to exist, so we'll have to wrap these two lines of code. In this if statement that checks to make sure both of those vertices exist. It is only then that we can run the next two lines, and after we run those, we'll return true. If the conditional in the if statement equates to false, we'll skip the if statement.

And we will return false. So that is our entire method for remove edge. We'll look at this in a moment in IntelliJ. And when we do we'll create this graph. And then we'll run remove edge between A and B. And then the graph will look like this. So now let's flip over to IntelliJ and take a look at this. So there is our remove edge method that we just created there, added to our graph class. And I'll come up here to our main class that has our main method.

And with this line here, we'll create a new graph called my graph. And then with these three lines here we'll create the three vertices a, b and c. And then with these three lines we'll connect all three of the vertices to each other. And then with this line we will print that out. So I'll run this. So you can see up here that we have three vertices A, B and C, and they all have edges with each other. So I'm going to come over here and add a line.

So this line here will remove the edge between the A and the B vertices. And then with this line here we will print that out. So I'll run this. And you can see that our A and B vertices no longer have edges with each other. And that is our method for remove edge.

----------------------------------------
