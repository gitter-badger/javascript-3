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
    this._queue.splice(0, 1);
    return value;
}

/**
 * good
 */
class Queue {
    constructor(contents = []) {
        this._queue = [...contents];
    }
    
    pop() {
        const value = this._queue[0];
        this._queue.splice(0, 1);
        return value;
    }
}
```

#### 2. Use `extends` for inheritance

> the reason is that it's a built-in way to inherit prototype functionality without breaking `instancof`

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>