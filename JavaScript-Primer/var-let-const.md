var, let, const
===============

The assignment operator (`=`) assigns a value to its left operand based on the value of its right operand.

Often, the left operand is an __identifier__ and the right operand is an __expression__ (something that evaluates to a value).

```javascript
const a = 1 + 2;
```

var
---

Var is the old way to assign a value to an expression. Consider it deprecated and use `let` or `const` instead. 

let
---

The let statement declares a block scope local variable, optionally initializing it to a value.

Read the [MDN documentation for let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)

const
----

The const statement declares a block-scoped local value. The value of a constant cannot change through re-assignment, and it can't be redeclared.

Read the [MDN documentation for const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)

__Use `const` to assign values to identifiers unless there is a particular reason to use `let`__