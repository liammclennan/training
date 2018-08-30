Functions
========

A function maps a set of input values to a set of output values.

```javascript
function double(i) {
    return i * 2;
}
```

A function without a name is called an anonymous function. Functions can assigned to an identifier.

```javascript
// an anonymous function, assigned to an identifier
const double = function (i) { 
    return i * 2;
};
```

Arrow Function Syntax
-------------

A concise function syntax.

```javascript
const isPositive = (i) => i > 0;
```

Read the [MDN documentation for arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions).

### Arrow Function with statements

Enclose in `{ }` and add a return statement.

```javascript
const isPositive = (i) => {
    const zeroOrMore = i > 0;
    return zeroOrMore;
};
```

To return an object, wrap it in `( )`.

```javascript
const arrayToObject = (a) => ({
    first: a[0];
    second: a[1];
});
```