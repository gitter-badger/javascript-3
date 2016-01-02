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

```js
/**
 * bad
 */
const inherits = require('inherits');
function PeekableQueue(contents) {
    Queue.apply(this, contents);
}
inherits(PeekableQueue, Queue);
PeekableQueue.prototype.peek = function () {
    return this._queue[0];
}

/**
 * good
 */
class PeekableQueue extends Queue {
    peek() {
        return this._queue[0];
    }
}
```

#### 3. Use return `this`

- Methods can return `this` to help with method chaining.

```js
/**
 * bad
 */
Aleen.prototype.jump = function () {
    this.jumping = true;
    return true;
}

```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>