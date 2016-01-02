## Arrow Functions [**Back**](./../README.md)

#### 1. Use arrow functions notation

- To use arrow functions notation when you must use function expressions (as when passing an anonymous function).
- Eslint rules tags: [`prefer-arrow-callback`](http://eslint.org/docs/rules/prefer-arrow-callback.html), [`arrow-spacing`](http://eslint.org/docs/rules/arrow-spacing.html)

> Why? It creates a version of the function that executes in the context of `this`, which is usually what you want, and is a more concise syntax.
> Why not? If you have a fairly complicated function, you might move that logic out into its own function declaration.

```js
/**
 * bad
 */
[1, 2, 3].map(function (x) {
    const y = x + 1;
    return x * y;
});

/**
 * good
 */
[1, 2, 3].map((x) => {
    const y = x + 1;
    return x * y;
});
```

#### 2. Omit the braces(忽略大括號) and use the implicit(隱式) return

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>