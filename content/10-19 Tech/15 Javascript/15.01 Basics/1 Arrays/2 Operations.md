## Insertion
To insert an element into an array, assign the element to the particular index. This will overwrite any previous element in that index. O(1)
```js
let arr = [0,1,2,3];
arr[0] = -1; // (4) [-1, 1, 2, 3]
arr[32] = 12; // (33) [-1, 1, 2, 3, empty × 28, 12]
```
#### In the end 
```js
let arr = [0,1,2,3];
arr.push(50);
arr // [0, 1, 2, 3, 50]
```
### In the start
O(N) - because at least all of the elements have to be shifted to the right.
```js
const arr1 = [1, 2, 3];

arr1.unshift(-1, 0)

console.log(arr1);
// Expected output: Array [-1, 0, 1, 2, 3]
```
### Splice
You can use splice to remove or insert element(s) at an index.
```js
let arr = [0, 1, 2, 3, 4]
// delete element at index 3. O(1)
delete arr[3] // true
arr // (5) [0, 1, 2, empty, 4]
// If you don't want an empty (hole) in the array, you use splice.
let arr = [0, 1, 2, 3, 4]
// From idx 3, remove 1 element - O(N)
arr.splice(3, 1) // [3]
arr // [0, 1, 2, 4]
let arr = [0, 1, 2, 3, 4]
// From idx 3, insert 2 elements - O(N)
arr.splice(3, 0, 'foo', 'bar') // []
arr // [0, 1, 2, 'foo', 'bar', 3, 4]
```
## Iteration
To iterate over an array, we can use a typical for loop. O(N)
```js
let arr = ['a', 'v', 'r'];
for (let i = 0; i < arr.length; i++) {
    console.log('Hi: ', arr[i]);
}

Hi:  a
Hi:  v
Hi:  r
```

To iterate over an array, we can also use a `for ... of` loop.
```js
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
## Deletion
### Delete & Splice
```js
let arr = [0, 1, 2, 3, 4]
delete arr[3] // O(1)
true
arr // (5) [0, 1, 2, empty, 4]
```
#### In the end .pop()
`.pop()` removes the last element in an array. O(1)
```js
let arr = [0, 1, 2, 3, 4]
arr.pop() // 4
arr // [0, 1, 2, 3];
```
### Reassign .length
Also shortening the `.length`  of the array can remove elements in the end.
```js
let arr = [0, 1, 2, 3, 4]
arr.length = 3
arr // [0, 1, 2]
arr.length = 0 // Also clears the array
arr // []
```
### In the start
.shift() removes the element from the beginning of the array and shifts remaining elements to the left.
```js
let arr = [0, 1, 2, 3, 4]
arr.shift() // 0
arr // [1, 2, 3, 4];
```
## Search
O(N)

#### Find the index of an element.
```js
const arr1 = [5, 6, 9, 90, 900];
arr1.indexOf(9); // 2
arr1.indexOf(50); // -1 (if no element is found)
```
#### Find if the value is present or not.
```js
const arr1 = [5, 6, 9, 90, 900];
arr1.includes(9); // true
arr1.includes(50); // false (if no element is found)
```
#### Find the first element that matches the given function criteria
```js
const arr1 = [5, 6, 9, 90, 900];
const found = arr1.find((element) => element > 50);
found // 90
```
## To String
```js
let arr = [0, 1, 2, "abc"]
arr.toString() // '0,1,2,abc'
```

## Transforms
### Map
### Reduce
### Sort