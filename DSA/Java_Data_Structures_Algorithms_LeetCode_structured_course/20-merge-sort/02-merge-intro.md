# 20.2 — Merge: Intro

> Section 20: Merge Sort

So in this video we're going to talk about our merge function. Merge is what is called a helper function. It doesn't do all of what is required for merge sort. It just does a portion of it. So the portion that merge does is it takes two sorted lists. And they do need to be sorted lists. And it takes the values from these and puts them into a new combined list like this. So let's put this back like this and walk through how we would do that. So we're going to loop through each of these lists.

And we'll loop through the first one with a variable I and the second one with a variable j. Then what we'll do is just compare I and j. Whichever one is lowest, we will add to the new combined list. Then we'll do it again. In this case j is lower so we'll add that one. Then we just keep going through making these comparisons. And we do this until one of the lists is empty. Once we've done that, we'll have another loop that loops through whichever list still has items.

And we'll add these items to the combined list. So we will code this helper function in the next video. But for now that is our introduction. To merge.

----------------------------------------
