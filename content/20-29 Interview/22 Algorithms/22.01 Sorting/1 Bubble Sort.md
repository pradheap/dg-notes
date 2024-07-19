Bubble Sort is where the largest numbers in the array bubbles towards the end on each pass.
**First pass**
5 3 1 7 4 6 -> 3 5 1 7 4 6 ( 5 > 3 yes swap)
3 5 1 7 4 6 -> 3 1 5 7 4 6 ( 5 > 1 yes swap)
3 1 5 7 4 6 -> 3 1 5 7 4 6 ( 5 > 7 no swap)
3 1 5 7 4 6 -> 3 1 5 4 7 6 ( 7 > 4 yes swap)
3 1 5 4 7 6 -> 3 1 5 4 6 **7** ( 7 > 6 yes swap)
**Second Pass**
3 1 5 4 6 **7** -> 1 3 5 4 6 **7** ( 3 > 1 yes swap)
1 3 5 4 6 **7** -> 1 3 5 4 6 **7** ( 3 > 5 no swap)
1 3 5 4 6 **7** -> 1 3 4 5 6 **7** ( 5 > 4 yes swap)
1 3 4 5 6 **7** -> 1 3 4 5 6 **7** ( 5 > 6 no swap)
1 3 4 5 6 **7** -> 1 3 4 5 **6** **7** ( 6 > 7 no swap)
Third Pass
1 3 4 5 **6** **7** -> 1 3 4 5 **6** **7** ( 1 > 3 no swap )
1 3 4 5 **6** **7** -> 1 3 4 5 **6** **7** ( 3 > 4 no swap)
1 3 4 5 **6** **7** -> 1 3 4 5 **6** **7** ( 4 > 5 no swap)
1 3 4 5 6 **7** -> 1 3 4 5 6 **7** ( 5 > 6 no swap)
1 3 4 5 6 **7** -> 1 3 4 5 **6** **7** ( 6 > 7 no swap)
Fourth Pass same as Third Pass
Fifth Pass same as Third Pass
