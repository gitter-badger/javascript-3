## Arrays [**Back**](./../README.md)

#### 1. Use `[]`

- To use literal syntax for array creation.
- Eslint rules tags: [`no-array-constructor`](http://eslint.org/docs/rules/no-array-constructor.html)

```js
/**
 * bad
 */
const items = new Array();

/**
 * good
 */
const items = [];
```

#### 2. Use `push()`

- To use Array#push instead of direct assignment to add items to an array.

```js
const arr = [];

/**
 * bad
 */
arr[arr.length] = 'aleen';

/**
 * good
 */
arr.push('aleen');
```

#### 3. Use spreads

- *Notice that: computed properties are only supported by ECMAScript 6 (ES6). [**Browser Compatibility**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#Browser_compatibility)*

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>