Spread Syntax
============

Expand an object or array in place to:

* Expand an array into arguments for a function
    ```javascript
        Math.min(...[5,2,-9])
        // => -9
    ```
* copy one object into another
    ```javascript
    const identity = {
        firstName: 'Peter',  
        lastName: 'Smith'
    };
    { ...identity, age: 35 }
    // {
    //    firstName: 'Peter',  
    //    lastName: 'Smith',
    //    age: 35
    // }


Read the [MDN documentation for Spread Syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)