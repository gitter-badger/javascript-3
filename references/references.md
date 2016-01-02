## References [**Back**](./../README.md)

#### Use Const
- To use `const` for all of your references, and avoid using `var`.
- Eslint rules tags: [`prefer-const`](http://eslint.org/docs/rules/prefer-const.html), [`no-const-assign`](http://eslint.org/docs/rules/no-const-assign.html)

> the reason is to ensure that you cannot reassign(重新訪問) references, which can lead to bugs and difficult to comprehend(理解) code.

```js
/**
 * bad 
 */

/**
 * good
 */

```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>