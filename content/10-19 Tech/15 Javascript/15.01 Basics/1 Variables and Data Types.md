# Basics

## Statement


## Expression
From MDN,
> An _expression_ is any valid unit of code that resolves to a value.

```js
// An expression without side effect.
10 + 9;
// 
```


## Variables
A variable is like a box to store some values. A variable has to be declared and then initialized.
```javascript
// Declare j
let j;
// j is undefined.

// initialize j with 1
let j = 1;
// j is 1.
let y = j - 9;
// y is -8
let a = b = 2;
// a and b are 2.

// ERROR as you can't redeclare a variable.
let j = -2;

```
JS can use unicodes in identifiers - https://mathiasbynens.be/notes/javascript-identifiers-es6
A JavaScript identifier must start with a letter, underscore (`_`), or dollar sign (`$`). Subsequent characters can also be digits (`0`–`9`).

Because JavaScript is case sensitive, letters include the characters "`A`" through "`Z`" (uppercase) as well as "`a`" through "`z`" (lowercase).

## Constants
A constant is like a read-only variable where once it is initialized, you can't change its assignment.
```js
const i = 0;

// ERROR
i = 2;
```

## Data Types
-   Seven data types that are [primitives](https://developer.mozilla.org/en-US/docs/Glossary/Primitive):
    1.  [Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean). `true` and `false`.
    2.  [null](https://developer.mozilla.org/en-US/docs/Glossary/Null). A special keyword denoting a null value. (Because JavaScript is case-sensitive, `null` is not the same as `Null`, `NULL`, or any other variant.)
    3.  [undefined](https://developer.mozilla.org/en-US/docs/Glossary/undefined). A top-level property whose value is not defined.
    4.  [Number](https://developer.mozilla.org/en-US/docs/Glossary/Number). An integer or floating point number. For example: `42` or `3.14159`.
    5.  [BigInt](https://developer.mozilla.org/en-US/docs/Glossary/BigInt). An integer with arbitrary precision. For example: `9007199254740992n`.
    6.  [String](https://developer.mozilla.org/en-US/docs/Glossary/String). A sequence of characters that represent a text value. For example: "Howdy"
    7.  [Symbol](https://developer.mozilla.org/en-US/docs/Glossary/Symbol) (new in ECMAScript 2015). A data type whose instances are unique and immutable.
-   and [Object](https://developer.mozilla.org/en-US/docs/Glossary/Object)

### Integer literals
Integer and [`BigInt`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt) literals can be written in decimal (base 10), hexadecimal (base 16), octal (base 8) and binary (base 2).
-   A _decimal_ integer literal is a sequence of digits without a leading `0` (zero).
-   A leading `0` (zero) on an integer literal, or a leading `0o` (or `0O`) indicates it is in _octal_. Octal integer literals can include only the digits `0`–`7`.
-   A leading `0x` (or `0X`) indicates a _hexadecimal_ integer literal. Hexadecimal integers can include digits (`0`–`9`) and the letters `a`–`f` and `A`–`F`. (The case of a character does not change its value. Therefore: `0xa` = `0xA` = `10` and `0xf` = `0xF` = `15`.)
-   A leading `0b` (or `0B`) indicates a _binary_ integer literal. Binary integer literals can only include the digits `0` and `1`.
-   A trailing `n` suffix on an integer literal indicates a [`BigInt`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt) literal. The integer literal can use any of the above bases. Note that leading-zero octal syntax like `0123n` is not allowed, but `0o123n` is fine

> 0, 117, 123456789123456789n             (decimal, base 10)
015, 0001, 0o777777777777n              (octal, base 8)
0x1123, 0x00111, 0x123456789ABCDEFn     (hexadecimal, "hex" or base 16)
0b11, 0b0011, 0b11101001010101010101n   (binary, base 2)

### Floating-point literals
A floating-point literal can have the following parts:

-   An unsigned decimal integer,
-   A decimal point ("`.`"),
-   A fraction (another decimal number),
-   An exponent.

The exponent part is an "`e`" or "`E`" followed by an integer, which can be signed (preceded by "`+`" or "`-`"). A floating-point literal must have at least one digit, and either a decimal point or "`e`" (or "`E`").

**The syntax is**
> \[digits].\[digits] \[ (E|e) \[(+|-)] digits ]

**Examples**
>3.1415926
 .123456789
 3.1E+12
 .1e-23

### String Literals

`\0` - Null Byte, `\b` - Backspace,  `\f` - Form feed,  `\n` - New line,  `\r` - Carriage return
`\t` - Tab,  `\v` - Vertical tab,  `\'` -Single quote, `\"` - double quote , `\\` - Backlash character,
We will see about encodings and unicodes later.



