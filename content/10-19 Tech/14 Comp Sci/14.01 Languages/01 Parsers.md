

Parsing can be two steps rolled into one
* lexical analysis
* syntactical analysis
* Psychoanalysis

Parsing tokens from a line. token ~ word

** Token **: A small unit of the programming language.

We need a lexer for it.
What it needs to do?

* accept an input string.
* a cursor to know the position in a string.
* create a list of tokens. 
* while loop on the input string
* get each token and see if it matches one of your types, if it matches, add it to the list of tokens.

we need some helpers

we will have something like the below to go over a string and collect tokens.

```javascript
const tokenize = (input) => {
    let cursor = 0;
    const tokens = [];
    while (cursor < input.length) {
        // logic goes here.
    }

    return tokens;
}
```

For example, (add 1 3 "hello") tokens are parenthesis, name - add, numbers 1 and 3, a string hello.

Thoughts:
1. Do we even need those parentheses?
2. What do we do about nested expressions?

So how do we go from token to expressions?
if we see an open parenthesis, start an expression, if you see a closing parenthesis, end the expression.
If you are in the middle of an expression and you see another open parenthesis, you've got another expression.
But ditch them, we don't need them anymore.

Syntactic analysis: convert the list of tokens into an intermediate representation or AST.

https://astexplorer.net
break the code into a tree data structure.
Each language has its own AST and can be unique to your language.
You can convert one language's AST into another language's AST.

So how do we build an AST?
* Iterate through the list of tokens
* For each number, string etc., add the token to the same level of the tree.

(add 1 2 (subtract 6 3))
We should convert this list of tokens to
```js
[
    { type: 'Name', value: 'add'},
    { type: 'Number', value: 1 },
    { type: 'Number', value: 2 },
    [
        { type: 'Name', value: 'subtract'},
        { type: 'Number', value: '6'},
        { type: 'Number', value: '3'},
    ]
]
```
an AST like the below. (loosely based on Babel's EST tree)

```js
const ast = {
    type: 'CallExpression',
    name: 'add',
    arguments: [
        { type: 'NumericLiteral', value: 1 },
        { type: 'NumericLiteral', value: 2 },
        {
            type: 'CallExpression',
            name: 'subtract',
            arguments: [
                { type: 'NumericLiteral', value: 4 },
                { type: 'NumericLiteral', value: 2 },
            ]
        }
    ]
}
```
