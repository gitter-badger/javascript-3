## Variables [**Back**](./../README.md)

#### 1. Always use `const`

- Always use `const` to declare variables. Not doing so will result in global variables. We want to avoid polluting the global namespace.

```js
/**
 * bad
 */
hero = new Hero();

/**
 * good
 */
const hero = new Hero();
```

#### 2. Use one `const` declaration per variable

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>