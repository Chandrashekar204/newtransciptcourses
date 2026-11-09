# 13.8 — Set: Has Unique Chars

> Section 13: <> HT: Interview / LeetCode Exercises

In this video, we're going to write code to check to see if a string contains only unique characters. So let's consider the string success, and this one does not contain all unique characters. We have multiple S's and multiple C's. And we're going to iterate over this and put each of these letters in a set. We'll check to see if the set contains an S and it does not at this point. So we'll add that. And then we iterate over to the you check to see if a u is in the set.

There is not. So we'll add that and then we'll move to the C. And because the set does not contain a C we'll add this. And now we're going to move to this c. And the reason why a set is better than an array list in this situation is that all of these lookups are O of one. If you use an array list instead of a set to look for the letter C, you would have to iterate over all of these to find that C, but with a set, that's not the case. We can go directly to that character as an O of one operation.

And when we do, and we see that C there, that means that this string does not contain unique characters. So in this case you want the method to return false. If you got to the end of this and you didn't have any matches in the set, that means all of the characters are unique. And in that case you would return true. And that's how you most efficiently check to see if a string has unique characters.

----------------------------------------
