In insertion sort, each element of the array is taken and swapped with the element in its previous index if it is smaller. This is done until the particular element reaches an index where the previous element is even smaller. Let's look at an example below.
**First pass**
We start with the second element and index 1.
5 3 1 7 4 6 -> 3 5 1 7 4 6
index 1. 1 comparison and one swap.
**Second pass**
3 5 1 7 4 6 -> 3 1 5 7 4 6
3 1 5 7 4 6 -> 1 3 5 7 4 6
index 2. comparisons and swaps = 2.
**Third pass**
1 3 5 7 4 6 -> 1 3 5 7 4 6
index 3, value 7. comparisons and swaps = 0. (7 is greater than 5 and we can stop any further comparisons with previous elements before 5 as they are going to be even smaller)
**Fourth pass**
1 3 5 7 4 6 -> 1 3 5 4 7 6
1 3 5 4 7 6 -> 1 3 4 5 7 6
index 4, value 4. comparisons and swaps = 2.
**Fifth pass**
1 3 4 5 7 6 -> 1 3 4 5 7 6
index 5, value 6, comparisons and swaps = 1.

Some advantages of insertion sort are 
1. stable - meaning it does not change the relative order of elements with equal keys.
2. online - can sort an element as it receives it. 