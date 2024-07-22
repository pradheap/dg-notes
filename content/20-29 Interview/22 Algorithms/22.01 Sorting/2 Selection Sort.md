Selection Sort is where the smallest numbers in the array are selected and moved towards the start of the array on each pass. To select the smallest number, you've to iterate over all of the elements in the array. Let's look at an example below.
**First pass**
5 3 1 7 4 6 -> **1** 3 5 7 4 6
i = 0, value = 5, min is 1, min index is 2. so swap values at index 0 and 2.
**Second Pass**
 **1** 3 5 7 4 6 ->  **1** **3** 5 7 4 6
i = 1, value = 3, min is 3, min index is 1. no swap as the indexes are the same
**Third Pass**
**1** **3** 5 7 4 6 ->  **1** **3** **4** 7 5 6
i = 2, value = 5, min is 4, min index is 4, so swap values at index 2 and 4.
**First pass**
**1** **3** **4** 7 5 6 -> **1 3 4 5** 7 6
i = 3, value = 7, min is 5, min index is 4, so swap values at index 3 and 4.
**Fifth Pass**
**1 3 4 5** 7 6 -> **1 3 4 5** **6** 7
i = 4, value = 7, min is 6, min index is 5, so swap values at index 4 and 5.

In selection sort, though there are n-1 comparisons on each pass but there is only one swap per pass. So in total, O(n<sup>2</sup>) comparisons and O(n) swaps.