# 19.1 — Bubble Sort: Intro

> Section 19: Basic Sorts

All right. Now we're going to look at our first sorting algorithm bubble sort. And in this video we'll walk through the logic of how bubble sort works. And in the next video we'll write the code. So we're going to sort. This list, except I'm going to change it to look like this so we can visually see the size of the numbers. And previously I had shown lists to be in green. And what I'm going to do here is I'm only going to show these to be in green once they're sorted.

So I'm going to move this back. And with bubble sort, what we're going to do is we're going to start with the first item in the list, and we're going to compare it to the second item. And if the first item is larger than the second item. We're going to switch these. Then we'll take the second item and compare it to the third item. And in this case these don't need to be switched. So we'll go to the third item and compare it to the fourth item. These do need to be switched, and the fourth item with the fifth item, and the fifth item with the sixth item.

And now that six is sorted, what we've done is we've bubbled up the largest item. So in order to do this, we had to do five comparisons. We had six items and we did five comparisons. Now we only have five items left to sort. So in this round we'll only have four comparisons. So we'll start back at the beginning and compare the first item to the second item that doesn't need to be switched, the second item to the third item, the third to the fourth, the fourth to the fifth.

That's four comparisons. And now the second largest item out of the list has been sorted. It has been bubbled up. So let's just finish sorting these. We'll compare first to the second, second to the third, third to the fourth. Now that item is sorted. And they will compare first to second, second to third, and now the third item is sorted. And then we'll just compare these two. And if they need to be switched, they'll be switched. Otherwise we know they are both sorted.

And now we have a completely sorted list. So now I'm going to put this back the way it was. And this is where we're going to start in our next video when we code. Bubblesort.

----------------------------------------
