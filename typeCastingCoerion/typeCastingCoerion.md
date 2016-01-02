## Type Casting & Coercion [**Back**](./../README.md)

#### 1. Strings

```js
const reviewScrore = 9;

/**
 * bad
 */
const totalScore = reviewScore + '';

/**
 * good
 */
const totalScore = String(reviewScore);
```

#### 2. Numbers

- To use `Number` for type casting and `parseInt` always with a radix for parsing strings.

```js
const inputValue = '4';

/**
 * bad
 */
const val = new Number(inputValue);
const val = +inputValue;
const val = parseInt(inputValue);

/**
 * good
 */
const val = Number(inputValue);
const val = parseInt(inputValue, 10);
```

- If for whatever reason you are doing something wild and parseInt is your bottleneck(瓶頸) and need to use Bitshift(位移操作) for [performance reasons](http://jsperf.com/coercion-vs-casting/3), leave a comment explaining why and what you're doing.

```js
/**
 * parseInt was the reason my code was slow.
 * Bitshifting the String to coerce it to a
 * Number made it a lot faster.
 */
const val = inputValue >> 0;
```
- *Notice that: when using Bitshift, you should care more about the problem of overflow*

```js
/**
 * Largest signed 32-bit Int is 2,147,483,647
 */
```

#### 3. Booleans


<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>