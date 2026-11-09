# 13.4 — HT: Two Sum

> Section 13: <> HT: Interview / LeetCode Exercises

Our next coding challenge is called twosome. And you're going to pass the method an array and then also a target number. We'll use a target of nine for this example. And then at the end of the method you'll return an array with the indexes, where you can find the two numbers that add up to the target. So in this case that is going to be the index of zero and one. If you have a target where you don't have two numbers that add up to that number, let's say we had a target of 100.

We don't have any two numbers that add up to that. In that case you would return an empty array. So I'll go ahead and remove that. And in order to do that we'll need a hash map. And then we're going to iterate over the array. And I'm going to include that letter I that is the I from the for loop. So what we're going to do on each one of these iterations is calculate the corresponding number. And what I mean by that is if our target is nine, what number would go with two to add up to nine?

So the corresponding number for two would be seven. And we're going to look in the hash map to see if there's already a seven in the hash map. And there is not. So we're going to add two and show that you can find that two at the index of zero. And then we iterate to the next number. And we're going to do the same thing we did last time where we calculate the corresponding number. We'll take that target of nine subtract seven and the corresponding number is two.

We'll check the hash map to see if it contains a two. And it does. And remember we're returning the indexes. So now we know that the index of zero is going to be the first index that we return. And then the other index is going to be the index of I from the for loop. And that's why I showed that on the arrow. And then you'll return an array that contains zero and one. So now let's put everything back the way it was. And I want to show another example where we have more than one two.

So we'll do that process where we calculate the corresponding number which of course is going to be seven. And check the hash map to see if there's a seven there and there's not. So we'll add this to the hash map and move to here. Now the question is are we going to add two with an index of one to the hash map or leave it as zero. And the answer is we're going to overwrite this. It is going to be the index of the second two that we return. So when we move to here calculate the corresponding number which of course is two.

And it is in the hash map. We're going to return the one as the first index that we return. And the other one is the index of I. And we're going to return one and two. And that is how you do two some.

----------------------------------------
