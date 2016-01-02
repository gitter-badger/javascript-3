## Constructors [**Back**](./../README.md)

#### 1. Use class

- Always use class, and avoid manipulating `prototype` directly.

```js
/**
 * bad
 */
function Queue(contents = []) {
    this._queue = [...contents];
}
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>