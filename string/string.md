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
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>