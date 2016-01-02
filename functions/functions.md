## Functions [**Back**](./../README.md)

#### 1. Use function declarations

- To use function declarations instead of function expressions.

> the reason is that function declarations are named, so they are easier to identify in call stacks. Also, the whole body of a function declarations is hoisted(提升), whereas(然而) only the reference of a function expression is hoisted. This rule makes it possible to always use [*Arrow Functions*](./../arrowFunctions/arrowFunctions.md) in place of function expressions.

```js
/**
 * bad
 */
const foo = function() {
};

/**
 * good
 */
const foo() {
}
```

- Use arrow functions in place of function expressions as follow:

```js
/**
 * immediately-invoked function expression (IIFE)
 */
(() => {
    console.log('Welcome to the Internet. Please follow me.');
})();
```

- *Notice that: arrow functions are only supported by ECMAScript 6 (ES6). [**Browser Compatibility**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#Browser_compatibility)*

#### 2. Do not declare functions in a non-function block

- Never declare a function in a non-function block (if, while, etc). Assign the function to a variable instead. Browsers will allow you to do it, but they all interpret it differently, which is bad news bears.
- *Note: ECMA-262 defines a block as a list of statements. A function declaration is not a statement. [**Read ECMA-262's note on this issue**](http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-262.pdf#page=97).*

```js
/**
 * bad
 */
if (currentUser) {
    function test() {
        console.log('Nope.');
    }
}

/**
 * good
 */
if (currentUser) {
    test = () => {
        console.log('Yup.');
    };
}
```

#### 3. Never name a parameter `arguments`

- Never name a parameter `arguments`, because this will take precedence(優先級) over the `arguments` object that is given to every function scope.

```js
/**
 * bad
 */
function nope(name, options, arguments) {
    /**
     *  ...stuff...
     */
}

/**
 * good
 */
function yup(name, options, args) {
    /**
     *  ...stuff...
     */
}
```

- Also, never use `arguments`, opt to use rest syntax `...` instead.

> the reason is that `...` is explicit about which arguments you want pulled. Plus rest arguments are a real Array and not Array-like like `arguments`.

```js
/**
 * bad
 */
function concatenateAll() {
    const args = Array.prototype.slice.all(arguments);
    return args.join(' ');
}

/**
 * good
 */
function concatenateAll(...args) {
    return args.join(' ');
}
```

#### 4. Use default parameter syntax

- To use default parameter syntax rather than mutating(使...變異) function arguments.

```js
/**
 * really bad
 */
function handleThings(opts) {
    /**
     * No! We shouldn't mutate function arguments.
     * Double bad: if opts is false it'll be set to an object which may
     * be what you want but it can introduce subtle bugs.
     */
    opts = opts || {};
    
    /**
     * ...
     */
}

/**
 * still bad
 */
function handleThings(opts) {
    if (opts === void 0) {
        opts = {};
    }
    
    /**
     * ...
     */
}

/**
 * good
 */
function handleThings(opts = {}) {

}
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>