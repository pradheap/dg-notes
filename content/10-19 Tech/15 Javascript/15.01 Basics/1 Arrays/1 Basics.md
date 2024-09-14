An array is used to store a collection of elements indexed by non negative numbers. They can store elements of different data types and are also dynamic in size. 
## Constructor
```js
let arr = new Array(2);
arr.length // 2
arr[0] // undefined

let arr1 = new Array("2", "1");
arr1.length // 2
arr1[0] // "2"
```

More common way - `let arr = [0, 1, 4, 6];

## Copy by reference
Arrays are copied by reference, let's look at an example to prove it.
```js
let fruits = ['apple', 'orange']
let fruitsOne = fruits;
fruitsOne.push('grape');
fruits.length // 3
fruitsOne.length // 3
fruits // ['apple', 'orange', 'grape']
fruitsOne // ['apple', 'orange', 'grape']
```
## Quirks
In JS, an array is a special type of object and can be assigned with string properties or some larger index on an array. And the length is simply largest index + 1. For example,
```js
let arr = [0, 1]
arr[454545] = 34
arr.foo = "bar"
arr.length // 454546
```
But, if we do the above, we would lose any array specific optimizations that a JS engine would do.

Also when you try to access an index outside the length of the array, it returns `undefined` instead of throwing an index out of bounds error.
``` js
let arr = [0, 1]
console.log(arr[45]) // undefined
```