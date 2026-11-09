# 12.7 — HT: Keys

> Section 12: Hash Tables

So now we're going to write our keys method. So in this method we're going to take all of the keys out of the hash table. We're going to put them in an array list. And then we'll return that array list. So let's bring up our hash table like this. And then we'll go right into writing the code. So the method is called keys. And we'll return an array list. So the first thing we need to do is actually create that array list that will return. We'll call it all keys.

And to get to all of these keys, the first thing we have to do is loop through the array and look at all of these indexes top to bottom. So we'll do that with a for loop that goes the length of our data map array. And then when there's an index where we have nodes we'll need to loop through those nodes in order to loop through those we will need a variable. We'll call that temp and we'll create that like this. So node temp equals data map at a particular index as we're going through the for loop.

Then to go through the linked list we'll need a while loop because we don't know how many items are in the linked list. So we can't use a for loop for that. And then inside the while loop we'll add items to that all keys array list. So in this case we're going to add nails to that array list. Then we'll move temp forward with this line temp. Temp dot next. And then we'll add tile. And then we'll add lumber. Then once we have all of the items in our all keys array list, we will return all keys like that.

And that is all of the code for the keys method. So we'll look at this code in a moment in IntelliJ. And when we do we'll create this hash table. Except I'll add a couple of items here. And then when we run the keys method, we'll expect to get an array list that looks like this. So now let's flip over to IntelliJ and take a look at this. So with this line of code here, we'll create our new hash table called my hash table. And then with these lines of code, we'll add our five key value pairs to our hash table.

And then with this line here we'll just print the table out to make sure it looks the way we're expecting. And I'll run this. And you can see here that we have paint at the index of two and bolts at the index of four. And then we have nails tile and lumber at the index of six. So now what I'm going to do is come up and replace this print table line with this line of code. Where we run our keys method and we print out that array list that that method returns.

So I'll run this. And that has returned the array list that we expected. So that is our method for keys.

----------------------------------------
