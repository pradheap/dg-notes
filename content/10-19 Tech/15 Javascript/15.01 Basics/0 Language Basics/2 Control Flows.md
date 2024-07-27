# Control Flows

## Block Statement
A block statement is enclosed within a curly brackets.
```js
{
	statement 1;
	statement 2;
	.
	.
	.
	statement n;
}

```

## if else
Js supports two conditional statements. `if ... else` and `switch`
```js
if (condition) {
  statement_1;
} else if {
  statement_2;
} else {
  statement_3;
}
```
The `condition` can be any expression that evaluates to `true` or `false`

#### Falsy values

The following values evaluate to `false` (also known as [Falsy](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) values):

-   `false`
-   `undefined`
-   `null`
-   `0`
-   `NaN`
-   the empty string (`""`)

## Switch statement
A `switch` statement allows a program to evaluate an expression and attempt to match the expression's value to a `case` label. If a match is found, the program executes the associated statement.

A `switch` statement looks like this:

```
switch (expression) {
  case label_1:
    statements_1;
    break;
  case label_2:
    statements_2;
    break;
    …
  default:
    statements_default;
}
```

#### break statements

The optional `break` statement associated with each `case` clause ensures that the program breaks out of `switch` once the matched statement is executed, and then continues execution at the statement following `switch`. If `break` is omitted, the program continues execution inside the `switch` statement (and will evaluate the next `case`, and so on).