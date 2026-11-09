# 13.3 — HT: Group Anagrams

> Section 13: <> HT: Interview / LeetCode Exercises

Our next coding challenge is group anagrams, and you might be wondering what is an anagram? Eat T and H are all anagrams of each other. They all have the same letters, and they have the same quantity of each letter. And an easy way to tell that these are all anagrams of each other is if you sort the letters, you're going to get the same result. I'll go ahead and put that back and eat. T and eight are just going to be three of the words that we have in this array.

And we're going to group all of the anagrams together. So in order to do that of course we'll need to iterate over this array. And then you have the word eat as the first one. If you sort the letters it is a T. And what we're going to do is have a E be the key and a key value pair, and then the value is going to be an array list and we'll add each to that array list. Now if you were to print out this hash map, Java is not going to print out those quotes.

But once again I'm going to leave those in just to emphasize that these are strings. So now we'll move to the next item in the array T. So I'm going to show the word t. And then I'm also going to show it sorted as already exists as a key in our hash map. So we'll add this to the array list here. Then we move to the next one. And then here is the word and the letters sorted. And T is not in the hash map yet. It's not a key. So we're going to add that as a key.

And then add tan to the array list associated with that key. And then we'll move on to h. Here's the word. And with it sorted A already exists. So we'll add this to this array list. And then Nat. Ant is already a key here. So we'll add this to this array list. And then finally we'll look at bat sorted. It is abt. And we'll have to create a new key and a new array list. So I'm going to remove this array from the bottom and show you what we're going to return.

We're going to return an array list of array list. Starting with that first array list. We're going to add this to the array list that we're going to return. And then we'll add the next array list to that and the next one. So you see the first three anagrams are all together. And this array list. And then these two anagrams. And then bat doesn't have any others that match it. And that is how we group anagrams.

----------------------------------------
