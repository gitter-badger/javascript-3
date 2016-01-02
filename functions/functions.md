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

- you can use function expressions as follow:

```js
/**
 * immediately-invoked function expression (IIFE)
 */
(() => {
    console.log('Welcome to the Internet. Please follow me.');
})();
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>