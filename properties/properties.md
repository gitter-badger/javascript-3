## Properties [**Back**](./../README.md)

#### 1. Use dot notation

- To use dot notation when accessing properties.
- Eslint rules tags: [`dot-notation`](http://eslint.org/docs/rules/dot-notation.html)

```js
const Aleen = {
    name: 'PuiMan Cheui',
    age: '22'
};

/**
 * bad
 */
const name = Aleen['name'];

/**
 * good
 */
const name = Aleen.name;
```

#### 2. Use subscript notation `[]`

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>