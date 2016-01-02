## Functions [**Back**](./../README.md)

#### 1. Use function declarations

- To use function declarations instead of function expressions.

> the reason is that function declarations are named, so they are easier to identify in call stacks. Also, the whole body of a function declarations is hoisted(提升), whereas(然而) only the reference of a function expression is hoisted. This rule makes it possible to always use [*Arrow Functions*](./../arrowFunctions/arrowFunctions.md) in place of function expressions.

```js
/**
 * bad
 */
const foo = function() {
};

/**
 * good
 */
const foo() {
}
```

- Use arrow functions in place of function expressions as follow:

```js
/**
 * immediately-invoked function expression (IIFE)
 */
(() => {
    console.log('Welcome to the Internet. Please follow me.');
})();
```

- *Notice that: arrow functions are only supported by ECMAScript 6 (ES6). [**Browser Compatibility**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#Browser_compatibility)*

#### 2. Do not declare functions in a non-function block

- Never declare a function in a non-function block (if, while, etc). Assign the function to a variable instead. Browsers will allow you to do it, but they all interpret it differently, which is bad news bears.

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>