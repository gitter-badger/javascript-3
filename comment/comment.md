## Comments [**Back**](./../README.md)

- use `/** ... */` for a single line
- use follow for multi-line:

```js
/**
 * this is a mutli-line comment
 */
```

#### 1. Function comments

- use `@param` to give comments for all the parameters of this function.
- use `@return` to give comments for what will be return of this function.

```js
/**
 * [initData: description]
 * @param  {[type]} data [description]
 * @return {[type]}      [description]
 */
function initData(data) {
    /**
     * ...
     */
}
```

#### 2. Structural comments

- Comments of structural comments such as `if`, `switch`, `for`.

```js
/** 
 * [if: description]
 * @param {[type]} test [description]
 */
if (test) {
}

/** [for: description] */
for (len i = 0; i < 10; i++) {
}
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>