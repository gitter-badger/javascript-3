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
Queue.prototype.pop = function () {
    const value = this._queue[0]
    this._que.splice(0, 1);
    return value;
}

/**
 * good
 */
class Queue {

}
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>