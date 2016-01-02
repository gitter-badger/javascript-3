## Objects [**Back**](./../README.md)

#### Use `{}`

- To use the literal syntax for object creation.
- Eslint rules tags: [`no-new-object`](http://eslint.org/docs/rules/no-new-object.html)

```js
/**
 * bad
 */
const item = new Object();

/**
 * good
 */
const item = {};
```

#### Do not use `reserved words`
- If your code will be executed in browsers in script context, remember that it's not recommended to use reserved words as keys.

> the reason is that they won't work in IE8, but it's OK to use them in ES6 modules and server-side code.

```js
/**
 * bad
 */
const heros = {
    default: { name: 'aleen' },
    private: true
};

/**
 * good
 */
const heros = {
    defaults: { name: 'aleen' },
    hidden: true
};
```

- It's recommended that using readable synonyms(同義詞) in place of reserved words.

```js
/**
 * bad
 */
const heros = { class: 'alien' };

/**
 * bad
 */
const heros = { klass: 'alien' };

/**
 * good
 */
const heros = { type: 'alien' };
```

#### Use computed property names

- To use computed property names when creating objects with dynamic property names.

> the reason is that they allow you to define all the properties of an object in one place.

```js
function geyKey(k) {
    return `${k}`;
}


/**
 * bad
 */
const obj = {
    id: 5,
    name: 'Foshan'
};
obj[geyKey('enabled')] = true;
```

- *Notice that: computed properties are only supported by ECMAScript 6 (ES6)* 

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>