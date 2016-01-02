## Comments [**Back**](./../README.md)

- use `/** ... */` for a single line
- use follow for multi-line:

```js
/**
 * this is a mutli-line comment
 */
```

#### 1. Function comments

- use `@param` to give comments for all the parameters of this function.
- use `@return` to give comments for what will be return of this function.

```js
/**
 * [initData: description]
 * @param  {[type]} data [description]
 * @return {[type]}      [description]
 */
function initData(data) {
    /**
     * ...
     */
}
```

#### 2. Structural comments

- Comments of structural comments such as `if`, `switch`, `for`, `while`.

```js
/** 
 * [if: description]
 * @param {[type]} test [description]
 */
if (test) {
    /**
     * ...
     */
}

/** 
 * [switch: description]
 * @param {[type]} test [description]
 */
switch (test) {
    case 'a':
        break;
}

/** 
 * [while: description]
 * @param {[type]} test [description]
 */
while (test) {
    /**
     * ..
     */
}

/** [for: description] */
for (len i = 0; i < 10; i++) {
    /**
     * ...
     */
}
```

#### 3. Helping comments

- `FIXME`: it's used to annotate(注釋) problems.
- `TODO`: it's used to annotate solutions to problems.


<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>