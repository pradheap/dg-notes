
Traditionally, an array data structure refers to a collection of elements stored at a particular memory location. The elements stored in an array are of same data type (int, char etc.,), so that we know the size of each element (let's assume a char holds 4 bytes) and we can use it to calculate the memory location of each element in an array.  

For example, we need to store `word` in an array, and we choose `3000` to be its memory location. `w` will be stored at `3000`, `o` will be stored at `3004` and so on. 

And the size of the array is also fixed during the time of creation. (Apparently there is also array data type which I will skip as I find it confusing.)

Python - Array
JS - TypedArray

## Dynamic Array
If we move to high level languages, we normally work with dynamic arrays which are not fixed in size and in some languages can store multiple data types. 

Java - ArrayList
Python - List
JS - Array

> *It's worth noting that there is actually an array data structure in Python.*

> *And in JS, the Array data structure is an object which is classified as a indexed collection, which means you can do the below.*
  `let gh = ['a', 'b']; gh['abc'] = 4` results in `['a', 'b', abc: 4]` but you can't use `abc`  as a valid index during an iteration, or if you use TS, you can avoid this JS quirk.

See Also [[1 Basics (Indexed or Ordered Collection)]] (JS) and [[1 List]] (Python)
