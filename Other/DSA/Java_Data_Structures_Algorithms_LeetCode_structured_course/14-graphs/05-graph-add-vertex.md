# 14.5 — Graph: Add Vertex

> Section 14: Graphs

So now we're going to write our add vertex method which is going to create one of these. In the next video we'll write our add edge method. And that will allow this vertex to connect to other vertices like this. But for now in this method, all we're creating is just this. So once we add this first vertex that we're going to give a value of a, our adjacency list is going to look like this. So let's move this down to the bottom and start writing our code.

So we're going to start this out by saying public class graph. So with previous data structures we broke the constructor out into a separate video. And we started this line of code in the constructor video. But with the class graph all we're going to do is create one class variable. So it didn't make sense to break that out into its own video. And that class variable is just going to create this, an empty HashMap that is going to be used to store our adjacency list.

Once we've created that, we can write the add vertex method which will do this part. So let's create that class variable. It's going to look like this. When we flip over to IntelliJ you'll see I have this all on one line. But Java doesn't care about line breaks or extra spaces. It's just going to go up to the semicolon. So you can break something like this into two lines if it is too long. So this is of type HashMap. And then it has a key value pair here.

So the key is a string that is the A down here. And then the value is an array list that will hold strings. That's what this is down here. So this code here just creates an empty HashMap called adjacency list. So once you run this, all you're going to have. Is this? So now let's start writing the code to add a vertex. We'll start it out like this. We're going to return a boolean. I'll show you why here in a moment. But we will pass this a string that we're going to call vertex.

And then we will add that into the adjacency list like this. We'll say adjacency list dot put and we'll use the vertex that will be the key and the key value pair. And then the value is going to be this empty array list. And because you're creating a new array list you do have to use that keyword new. And that will add this into our adjacency list. So one of the things about a hash map, though, is that we cannot have duplicates. So we'll need to have some code to make sure this value a that we're using for our vertex isn't already and our HashMap.

So I'm going to remove this. And then I'm going to wrap this last line of code that we just wrote in this if statement. So we'll say if adjacency list dot get and we'll pass it the vertex if that's equal to null. What that means is that vertex is not already in the graph. Only then do we want to run that next line where we put that new vertex into the graph. And then we'll want to add a line here where we say return true. Now, if the conditional in this if statement equates to false, we're going to skip the if statement and come down to here and return false.

And that is all of the code for our add vertex method. So now let's flip over to IntelliJ and take a look at this. So to begin with, we'll come up here. We have a new package that we call graph. The package name is lowercase and that's going to contain two classes. First will be graph with an uppercase G. That's what you see in the window to the right there. And then we'll have our main class that contains our main method. So I'm going to come up here and close this side window.

So here is our graph class that we've just created. I have added one method here and that is print graph. And this is our add vertex method down here. So now I'm going to come up here to move to our main class that contains our main method. And with this line we're creating a new graph called my graph. And then we're saying my graph dot add vertex. And we're passing that letter A. And then with this line here we will print that out. So I'll run this.

And there is our graph with our vertex A. And that is our method for add vertex.

----------------------------------------
