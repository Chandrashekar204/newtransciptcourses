# 12.13 — Searching an Array

> Section 12: Arrays in Java

[00:00] Searching is another most commonly used operation on top of arrays. Using these searching operations
[00:08] we can search if a given element is present inside an array.
[00:13] If it is present at what position the element is present.
[00:17] If it is not present, we want to know the same as well.
[00:20] So how to perform the search operation?
[00:22] You don't have to write any complex logic.
[00:25] You can simply leverage the binary search static method available inside the Arrays class.
[00:32] But there is a precondition that you need to follow whenever you want to use this binarySearch() method.
[00:38] The precondition is
[00:39] first, you need to make sure you have sorted your array with the help of sort() method or parallelSort()
[00:46] method.
[00:47] Once the sorting is completed, you can invoke the binarySearch() method by providing two input arguments.
[00:55] The very first argument to this method is your array itself, and the second input parameter is which
[01:01] element you are trying to search.
[01:03] You can see here I have an array with the name num.
[01:06] First I'm trying to perform the sorting operation.
[01:09] After that I'm trying to invoke the binarySearch() method.
[01:12] And to this method I'm trying to pass my array name which is num, and what is the element that I'm
[01:18] trying to search?
[01:19] Since this nine element is going to present at the index zero, after sorting, I'm going to get the
[01:26] output as zero only.
[01:27] So this is the unsorted array.
[01:29] If I do the sorting where the nine is going to present, it is going to present at the very first index.
[01:35] That's why I'm going to get the output as zero in this scenario.
[01:39] Otherwise, if I try to pass an element to this binarySearch() method which is not available inside my
[01:45] sorted array, then I'm going to get a negative value as an output.
[01:50] There is a formula that is going to be followed by this binarySearch() method
[01:55] to derive these negative number, the formula is minus of insert to point and to this negative insert
[02:03] to point to value
[02:04] we're going to add one more minus one value.
[02:07] So how this insert point value is going to be derived.
[02:10] This insert point refers to the index where the element would be inserted to maintain the sorted order.
[02:18] Since this 999 is not present inside my sorted array, where is this going to be inserted?
[02:24] To maintain the same sorting, it is going to be inserted at the end because all the other numbers inside
[02:31] my array, they are less than 999.
[02:34] Since this is going to be inserted at the last two position with the index five, so - (5) will
[02:41] be -5 and -5, -1, it is going to be -6.
[02:45] That is our output that we are going to get.
[02:47] So let's see the demo of these searching operation as well
[02:51] inside IntelliJ.
[02:52] Inside my IntelliJ I'm going to create a new Java class
[02:56] the class name is SearchDemo.
[02:59] Inside the SearchDemo, first we need to create the main() method and post that
[03:04] I'm going to create an array of int and the variable name I'm going to mention as num.
[03:10] And inside this I'm going to mention some integer values like 36 , 9, 42, 18,
[03:19] 73.
[03:20] So the first operation that I need to perform is sorting operation.
[03:24] So that's why I'm trying to invoke the sort() method.
[03:27] And to the sort() method I'm going to pass num which is my array variable name.
[03:33] After this I'm going to invoke the binarySearch static method which is available inside my Arrays class.
[03:42] You can see for BinarySearch
[03:44] also we have multiple overloaded methods that accepts various kinds of arrays.
[03:49] Since we are working on a int array, let me try to invoke the very first method and to this binarySearch()
[03:55] method
[03:56] first I need to mention what is my array name, followed by which element I'm trying to search.
[04:02] So first I'll try to search 9.
[04:04] So the output from this method I'm going to catch inside a variable called index.
[04:10] The same I'll try to print out with the help of System.out.println().
[04:15] So if I execute this program, you can see I'm getting the output as zero, because after the sorting,
[04:20] the element nine is going to be present at the index zero.
[04:24] If I try to search for the 73, which is the maximum number inside my array, I'm going to get a different
[04:32] index.
[04:33] You can see I'm getting the index as four, because 73 element is going to be stored at the last index
[04:39] after the sorting operation.
[04:41] This time I'll try to perform the search operation by taking a number which is not present inside my
[04:47] array.
[04:47] So let me mention that 999 as an input here, and the same index value I'll try to print out one more
[04:54] time.
[04:55] We should get -6 as an output, because after the sorting
[05:00] this 999 is going to be stored at a index value five to maintain the same sorting order and the formula
[05:08] that my binary search is going to follow to derive this negative number index is what is the negative
[05:15] representation of the insert point followed by -1.
[05:20] That's why we are getting the output as -6.
[05:23] I hope you are clear on how to use this binarySearch() method.
[05:26] Always
[05:27] please make sure you are performing the sort operation before you are trying to invoke this binarySearch()
[05:33] method.
[05:33] Thank you and I'll catch you in the next lecture bye.

----------------------------------------
