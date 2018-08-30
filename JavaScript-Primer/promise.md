Promise
=======

The Promise object represents the eventual completion (or failure) of an asynchronous operation, and its resulting value.

It is a value you don't (might not) have yet!

Get the value from a promise
----------------------------

To get the value from a promise, use the `then` method.

```javascript
somePromise.then((value) => 
  { console.log(value); });
```

Handle the error in a promise
-----------------------------

If the asynchronous operation represented by the promise fails then the promise will enter the 'error' state. Use the `catch` method to handle promise errors.

```javascript
somePromise
  .then((value) => { console.log(value); })
  .catch((error) => { console.error(error); });
```

Creating a promise
------------------

You will nearly always be given instantiated promises from APIs that you use, but if you do need to create a promise there are some different ways.

### Promise.resolve

```javascript
const promise = Promise.resolve(1);
```

### Promise constructor

This is one way to convert a callback API to a promise API.

```javascript
const p = new Promise((resolve, reject) => {
  setTimeout(resolve, 100);
});
```

### Sequential async operations

Chain sequential operations with then. Only do this if the result of early operations is required to commence later operations. 

```javascript
  first()
    .then(second)
    .then(third);
```

Each operation will complete before the next one starts.

### Parallel async operations

If the async operations do not depend upon each other use `Promise.all` to perform all async operations at the same time.

```javascript
Promise.all([
  Promise.resolve(1), 
  Promise.resolve(2), 
  Promise.resolve(3)
])
  .then(continue);
```

Read the [MDN documentation for Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise).

async and await
---------------

`async` and `await` provide a syntax that makes promise handling look like imperative, procedural code. 

The sequential async operation above can also be represented as

```javascript
const sequentialStuff = async () => {
  const firstResult = await first();
  const secondResult = await second(firstResult);
  return third(secondResult);
};
```

Note that `await` only works inside a function marked with the `async` keyword and that this function returns a promise. 

Logically, await works by moving all subsequent code in the function into a callback. 

Read the MDN documentation for [async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/async_function) and [await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await).
