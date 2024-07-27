In Python a list is an ordered sequence of elements of any data types and is dynamic in size. The list is is used in place of array for most of the problem solving and in coding. 
**Note**: Python has got Arrays too which is just a wrapper to C arrays.

```python
def foo():
    pass
a = [1, 2, 'foo', foo]
a # [1, 2, 'foo', <function foo at 0x01DB829>]

```
> A list can contain any number of objects, from zero to as many as your computer’s memory will allow.

## Operations
### Add
`list.append(x)` - add `x` to the end of the list.
`list.insert(idx, x)` - insert `x` at index `idx`
`list.extend(iterable)` - Extend the list by adding all of the elements from the `iterable`
### Remove
`list.pop([idx])` - Remove the element at index `idx`, and index is optional, if `idx` is not specified, it removes the last element from the list.
`list.clear()` - Remove all items from the list. Also can do `del list[:]`
### Find
`list.index(x, [,start[, end]])` - Return index of the item `x`otherwise `ValueError`, if not found.
`list.count(x)` - Return the number of times x appears in the list.
### Comprehension
In JS, you often transform an array into a new array using higher order functions such as map, reduce etc., In python you can do it too, for example.
```python
>>> def square(x):
...     return x * x
>>> a = [1, 4, 5]
>>> b = map(square, a)
>>> list(b)
[1, 16, 25]
```
But doing this via list comprehension is also possible
```python
>>> def square(x):
...     return x * x
>>> a = [1, 4, 5]
>>> b = [square(x) for x in a] # new_list = [expression for elem in iterable]
>>> b
[1, 16, 25]
```
You can even filter or modify the output of a list using list comprehension. The syntax for a single if and an if-else is given below.
```
new_list = [expression for member in iterable if conditional]
new_list = [true_expr if conditional else false_expr for member in iterable]
```
Code example
```python
>>> b = [square(x) for x in a if x > 4] # Filter
>>> b
[25]

# Multiple output for single element.
>>> a = [-1, -2, 1, 4, 5]
>>> b = [square(x) if x > 0 else x for x in a]
>>> b
[-1, -2, 1, 16, 25]
```
### Traverse/Iterate
```python
>>> a = [0, 1, 2, 3]
>>> for i in a:
        print(i) 
0
1
2
3

# Get the index too
    for i, v in enumerate(['tic', 'tac', 'toe']):
...     print(i, v)
...
0 tic
1 tac
2 toe
```
### Slicing
