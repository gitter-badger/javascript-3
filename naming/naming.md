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

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>