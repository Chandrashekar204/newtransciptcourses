# 7.1 — DLL: Palindrome Checker

> Section 7: <> DLL: Interview / LeetCode Exercises

In this coding exercise, we're going to check to see if a doubly linked list is a palindrome. And usually when we're talking about palindromes we're talking about words or sentences. For example the word racecar is a palindrome. And that means it's spelled the same way forwards or backwards. But in our doubly linked list we're going to have numbers. So we're going to see if this is a palindrome. And it is. You will be given the length in this coding exercise.

And you'll need to use that to calculate how many iterations that you need to go through the doubly linked list. So we'll have variables. I'll call mine forward and backward. And we check to see if these are equal. They're both one. So that's good. And then we do it again. And because this is an odd number we don't need to check the one in the middle. So in this situation you would return true. If at any time forward and backward were not equal, you would return false that it is not a palindrome.

Of course, you can also have a doubly linked list that has an even number of nodes. And then you would check if these two are equal and these two are equal. The big thing is figuring out how to do this for an odd number of nodes, and an even number of nodes. And of course, if you only have one node that's going to be a palindrome, you would return true. And that is our introduction to the coding exercise palindrome.

----------------------------------------
