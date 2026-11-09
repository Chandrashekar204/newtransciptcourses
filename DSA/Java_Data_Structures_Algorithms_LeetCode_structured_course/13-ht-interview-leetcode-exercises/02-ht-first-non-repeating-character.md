# 13.2 — HT: First Non-Repeating Character

> Section 13: <> HT: Interview / LeetCode Exercises

In this coding exercise, we're going to use a hash map to help us determine what is the first non-repeating character in a string. So our hash map we're going to have a key value pair. And the string in this case is going to be success. And then we're going to iterate over the string. So the first character we're going to see is going to be the character S. And we have now seen that one time. Now if you print out a hash map it's not going to print out those single quotes.

But I'm going to leave those there to emphasize that this is a character. And just like we did last time, I'm going to put each of the key value pairs on its own line. So now you. We have seen that one time. See, we have seen one time and now we're seeing C again. So we'll change that to a two. E we have seen one time. So we will do that. And then s we will update that number and another S and we will update the number again. So now we're done looping through this string and adding these items, these key value pairs to the hash map.

And now we're going to have another loop that loops over the string again. So now we're going to look at this s and see is s something that only appears once in the string. And we come up to the hash map. And s is equal to three. So that is not a unique character. And then we get to the U. Well now the U only has a quantity of one. So we know that that is the first unique character in this string. And then we will return that character. If you have a situation like this where you don't have any unique characters, you would just return null.

And that is how you can use a hash map to determine the first non-repeating character.

----------------------------------------
