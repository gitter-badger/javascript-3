## Naming [**Back**](./../README.md)

#### 1. Use camelcase

- To use camelCase when naming `objects`, `functions` and `instances`.
- Eslint rules tags: [`camelcase`](http://eslint.org/docs/rules/camelcase.html)

```js
const thisIsAnObject = {};
function helloAleen() {}
```

#### 2. Use pascalcase

- To use PascalCase when naming `constructors` or `classes`.

```js
class PuiManCheui {
    constructor(options) {
        this.name = options.name;
    }
}

const good = new PuiManCheui({
    name: 'Aleen',
});
```

#### 3. Use a leading underscore `_`

- To use a leading underscore `_` when naming private properties.
- Eslint rules tags: [`no-underscore-dangle`](http://eslint.org/docs/rules/no-underscore-dangle.html)

```js
this._firstName = 'PuiMan';
```

#### 4. Do not save references to `this`

- Do not save references to `this`, and use arrow functions or Function#bind instead.

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>