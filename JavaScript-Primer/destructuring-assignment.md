Destructuring Assignment
====================

Unpack objects or arrays into distinct variables.

Destructuring Arrays
------------

```javascript
const numbers = [1,2,3];

const [first, second, third] = numbers;
// first => 1
// second => 2
// third => 3
```

Destructuring Objects
-------------

```javascript
const numbers = {
    first: 1,
    second: 2,
    third: 3
};

const { first, second, third } = numbers;
// first => 1
// second => 2
// third => 3
```

This also works for function arguments

```javascript
const point = { x: 3, y: 7 };
let distance = ({ x, y }) => Math.sqrt(x * x + y * y);
distance(point);
// => 7.6157731
```

Read the [MDN documentation for destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
