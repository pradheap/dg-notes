An array is used to store a collection of elements indexed by non negative numbers. They can store elements of different data types and are also dynamic in size. 
## Constructor
```
let arr = new Array(2);
arr.length // 2
arr[0] // undefined

let arr1 = new Array("2", "1");
arr1.length // 2
arr1[0] // "2"
```

More common way - `let arr = [0, 1, 4, 6];

## Insertion
To insert an element into an array, assign the element to the particular index. This will overwrite any previous element in that index.
```
let arr = [0,1,2,3];
arr[0] = -1; // (4) [-1, 1, 2, 3]
arr[32] = 12; // (33) [-1, 1, 2, 3, empty × 28, 12]
```
#### In the end
```
let arr = [0,1,2,3];
arr.push(50);
arr // [0, 1, 2, 3, 50]
```
## Iteration
To iterate over an array, we can use a typical for loop.
```
let arr = ['a', 'v', 'r'];
for (let i = 0; i < arr.length; i++) {
    console.log('Hi: ', arr[i]);
}

Hi:  a
Hi:  v
Hi:  r
```

To iterate over an array, we can also use a `for ... of` loop.
```
let arr = ['a', 'v', 'r'];
for (const a of arr) {
    a = 'Hi: ' + a;
    console.log(a);
}
Hi:  a
Hi:  v
Hi:  r

arr // (3) ['a', 'v', 'r']
// Eventhough a is reassigned with a prefix 'Hi: ', it doesn't affect the arr elements as the a in each iteration is a different variable. 
```
Both these for loop iterations will go through the empty slots if any in the array.
**TBD**
## Deletion
```
let arr = [0, 1, 2, 3, 4]
delete arr[3]
true
arr // (5) [0, 1, 2, empty, 4]
```
#### In the end
`.pop()` removes the last element in an array.
```
let arr = [0, 1, 2, 3, 4]
arr.pop() // 4
arr // [0, 1, 2, 3];
```
## Search

#### Find the index of an element.
```
const arr1 = [5, 6, 9, 90, 900];
arr1.indexOf(9); // 2
arr1.indexOf(50); // -1 (if no element is found)
```
#### Find if the value is present or not.
```
const arr1 = [5, 6, 9, 90, 900];
arr1.includes(9); // true
arr1.includes(50); // false (if no element is found)
```
#### Find the first element that matches the given function criteria
```
const arr1 = [5, 6, 9, 90, 900];
const found = arr1.find((element) => element > 50);
found // 90
```