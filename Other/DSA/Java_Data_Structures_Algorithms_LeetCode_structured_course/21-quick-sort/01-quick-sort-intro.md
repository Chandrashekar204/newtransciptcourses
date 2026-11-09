# 21.1 — Quick Sort: Intro

> Section 21: Quick Sort

So now let's look at our overview of quicksort. We'll start out with a list like this. Except I'll put it like this. And the way quicksort works is we start with a pivot point. That's going to be that first item. Then we're going to compare each of the numbers after that to this to see if it's greater than or less than. So we start with the six. The six is greater than and I'll color that in gray. The one is less than. I'll color that in yellow.

All the less than will be yellow and the greater than will be gray. And then what we're going to do is swap that one with the first item that was greater than. Like this. Then we move to the seven wheel colour that in grey. The three is less than and we'll swap that with the first item that was greater than, which is the six like that. The two is less than. And we'll swap that with the seven, because the seven is now the first item in the list that is greater than the four.

Like this. And then the five is greater than. So we have all of the items that are less than the four together, and all of the items that are greater than the four together. And then in the next step, we'll swap the four with the last of the less than items like this. So two things to point out here. First, the four is now sorted. I colored that in green and everything less than the four is to the left of the four. Everything greater than the four is to the right of the four.

And then what we're going to do is run quicksort again on these items as well as on these items. We'll start on the left. First two will be our pivot. In this case one is less. The three is greater than we swap these two items. And now the two is sorted. Then we'll run quicksort on these two. And because there's only one item in each of these, we know those are sorted. Then we'll run quicksort. On this side the pivot is going to be six. Seven is greater five is going to be less.

We're going to swap these. And they will swap these. The six is sorted. We'll run quicksort on these. And because there's only one item in each of these we know these are sorted. And now we have a completely sorted list. And that is our quick overview of quicksort.

----------------------------------------
