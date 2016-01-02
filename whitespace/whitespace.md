## Whitespace [**Back**](./../README.md)

- Although it's recommended to set soft-warp as 2 spaces, I am still familiar with 4 spaces.
- Eslint rules tags: [`indent`](http://eslint.org/docs/rules/indent.html)
- My recommendation is to listen to your habits when setting `soft-tab`.

#### 1. One space

- Place 1 space before the leading brace.
- Eslint rules tags: [`space-before-blocks`](http://eslint.org/docs/rules/space-before-blocks.html)

```js
/**
 * bad
 */
function test(){
    console.log('test');
}

/**
 * good
 */
function test() {
    console.log('test');
}
```

- Place 1 space before the opening parenthesis in control statements (`if`, `while` etc.). Place no space before the argument list in function calls and declarations.
- Eslint rules tags: [`space-after-keywords`](http://eslint.org/docs/rules/space-after-keywords.html), [`space-before-keywords`](http://eslint.org/docs/rules/space-before-keywords.html)

```js
/**
 * bad
 */
if(isAleen) {
    console.log('Yo.');
}

/**
 * good
 */
if (isAleen) {
    console.log('Yo.');
}

/**
 * bad
 */
console.log ('Not good.');

```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>