## Complex [**Back**](./../types.md)

- When accessing a complex type, you should work on a reference to its value.
    - `object`
    - `array`
    - `function`

```js
const foo = [1, 2];
const bar = foo;  /** number type */

bar = 9;

console.log(foo, bar);  /** => 1, 9 */
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../../pic/tail.gif"></a>