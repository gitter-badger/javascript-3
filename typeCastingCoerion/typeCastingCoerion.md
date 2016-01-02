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

#### 3. Booleans


<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>