## Variables [**Back**](./../README.md)

#### 1. Always use `const`

- Always use `const` to declare variables. Not doing so will result in global variables. We want to avoid polluting the global namespace.

```js
/**
 * bad
 */
hero = new Hero();

/**
 * good
 */
const hero = new Hero();
```

#### 2. Use one `const` declaration per variable

- Eslint rules tags: [`one-var`](http://eslint.org/docs/rules/one-var.html)

> the reason is that it's easier to add new variable declaration, and you don't have to worry about swapping out a `;` or `,`.

```js
/**
 * bad
 */
const items = getItems(),
    goSportsTeam = true,
    dragonball = 'z';

/**
 * bad
 */
 const items = getItems(),
    goSportsTeam = true;
    dragonball = 'z';
    
/**
 * good
 */
const items = getItems();
const goSportsTeam = true;
const dragonball = 'z';
```

#### 3. Group all the `const` and `let`

- To group all your `const` and `let` together.

> the reason is that it's helpful to find when later on you need to assign a variable depending on one of the previous assigned variables.

```js
/**
 * bad
 */
let i;
const items = getItems();
let dragonball;
const goSportsTeam = true;
let len;

/**
 * good
 */
const items = getItems();
const goSportsTeam = true;
let i;
let dragonball;
let len;
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>