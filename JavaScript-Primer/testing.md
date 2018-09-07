Testing
=======

Some general guidelines for JavaScript testing:

* favour testing functions. Call the function and make assertions about the result.
* Use node. Avoid testing in browsers.

Jest
----

Jest is a test runner and assertion framework published by Facebook. Here is an example jest test:

```javascript
const sum = require('./sum');

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```

Here, `toBe` is a jest matcher - a function that verifies that the left and right operands compare in a particular way. `toBe` verifies that they are the same. `toBeLessThan` verifies that the actual value is less than the expected value. 

Try [a demo](https://repl.it/repls/AnnualOilyDrawings)

Read the [Using Matchers documentation](https://jestjs.io/docs/en/using-matchers)

Setup and Teardown
---------------

Jest has `beforeEach`, `afterEach`, `beforeAll` and `afterAll` functions for setting up and tearing down. 

Read [setup and teardown](https://jestjs.io/docs/en/setup-teardown)

Testing async code
------------------

When testing async code, add a `done` argument to your test function and call it when the test is finished. 

```javascript
test('something', (done) => {
    setTimeout(()=> {
        expect(1+1).toBe(2);
        done();
    }, 100);
});
```

Read [Testing Asynchronous Code](https://jestjs.io/docs/en/asynchronous)

Exercise
--------

[Install Jest](https://jestjs.io/docs/en/getting-started)

You will implement a function that converts an angle in degrees to a compass direction (see [Points of the compass](https://en.wikipedia.org/wiki/Points_of_the_compass)). N, NNE, NE, ENE, E, ESE, SE, SSE, S, SSW, SW, WSW, W, WNW, NW, NNW 

E.g.

```javascsript
toCompassDirection(45);
// => NE
```

First implement the tests for your function, then implement the function itself and make the tests pass. 


