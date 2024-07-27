# Functions

### Function declarations

A **function definition** (also called a **function declaration**, or **function statement**) consists of the [`function`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function) keyword, followed by:

-   The name of the function.
-   A list of parameters to the function, enclosed in parentheses and separated by commas.
-   The JavaScript statements that define the function, enclosed in curly brackets, `{...}`.

Parameters are essentially passed to functions **by value** — so if the code within the body of a function assigns a completely new value to a parameter that was passed to the function, **the change is not reflected globally or in the code which called that function**.

When you pass an object as a parameter, if the function changes the object's properties, that change is visible outside the function, as shown in the following example:

```
function myFunc(theObject) {
  theObject.make = 'Toyota';
}

var mycar = {make: 'Honda', model: 'Accord', year: 1998};
var x, y;

x = mycar.make; // x gets the value "Honda"

myFunc(mycar);
y = mycar.make; // y gets the value "Toyota"
                // (the make property was changed by the function)
```

### Function expressions

While the function declaration above is syntactically a statement, functions can also be created by a [function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function).

Such a function can be **anonymous**; it does not have to have a name. For example, the function `square` could have been defined as:

```
const square = function(number) { return number * number }
var x = square(4) // x gets the value 16
```

However, a name _can_ be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces:

```
const factorial = function fac(n) { return n < 2 ? 1 : n * fac(n - 1) }

console.log(factorial(3))
```


Function expressions are convenient when passing a function as an argument to another function.

In JavaScript, a function can be defined based on a condition. For example, the following function definition defines `myFunc` only if `num` equals `0`:

```
var myFunc;
if (num === 0) {
  myFunc = function(theObject) {
    theObject.make = 'Toyota';
  }
}
```


In addition to defining functions as described here, you can also use the [`Function`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function) constructor to create functions from a string at runtime, much like [`eval()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval).

A **method** is a function that is a property of an object.