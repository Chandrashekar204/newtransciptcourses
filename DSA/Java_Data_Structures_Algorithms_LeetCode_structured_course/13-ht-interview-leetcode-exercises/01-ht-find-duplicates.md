# 13.1 — HT: Find Duplicates

> Section 13: <> HT: Interview / LeetCode Exercises

So now we're going to use a hash table to find duplicates in an array. And remember a hash table has key value pairs. So for this coding exercise and all of the LeetCode hash table problems, we're going to use the Java built in hash table which is a hash map. And like I said we're going to use this hash map to find duplicates in an array. In order to do this we're going to iterate over the array. And of course that value in the array is two. But at this point, because we are just starting to iterate, we have seen one number two.

So we're going to have two as the key and one as the value. Because we've seen one of those we're just keeping track of the count. Now one of the things I do want to point out here is I have a space after that equal sign in that hash map. Normally there is not a space there, but I think it makes it easier to read to spread this out a little bit. And then I'm also going to move that key value pair onto its own line like this. And then each key value pair will be on its own line.

So then we move to the one. And we've seen one one time. And then we go to the two. Two already exists in that hash map. It has a quantity of one. We'll update that to two and we'll move on to three. We've seen three one time four. Now we have seen that one time and then three. Previously we had seen one and now this makes two. So now we know that there are two different numbers in that array that we have seen more than once, the two and the three, these are the duplicate numbers that you can see are in the array each more than once.

And that is how we find duplicates.

----------------------------------------
