## String [**Back**](./../README.md)

#### 1. Use single qutoes for string

- To use single quotes `''` for strings.
- Eslint rules tags: [`quotes`](http://eslint.org/docs/rules/quotes.html)

```js
/**
 * bad
 */
const name = "PuiMan Cheui";

/**
 * good
 */
const name = 'PuiMan Cheui';
```

#### 2. Multiple lines when too many characters

- Strings that cause the line to go over **100** characters should be written across multiple lines using string concatenation.
- *Note that: if overused, long strings with concatenation could impact performance. [jsPerf](http://jsperf.com/ya-string-concat) & [Discussion](https://github.com/airbnb/javascript/issues/40).*

```js
/**
 * bad
 */
const errorMessage = 'This is a super long error that was thrown because of Batman. When you stop to think about how Batman had anything to do with this, you would get nowhere fast.';

/**
 * bad
 */
const errorMessage = 'This is a super long error that was thrown because \
of Batman. When you stop to think about how Batman had anything to do \
with this, you would get nowhere \
fast.';

/**
 * good
 */
const errorMessage = 'This is a super long error that was thrown because ' +
  'of Batman. When you stop to think about how Batman had anything to do ' +
  'with this, you would get nowhere fast.';
  
/**
 * you can also use template string
 */
const errorMessage = `This is a super long error that was thrown because `
  `of Batman. When you stop to think about how Batman had anything to do `
  `with this, you would get nowhere fast.`;
```

#### 3. Use template strings


<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>