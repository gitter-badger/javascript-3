## Hoisted [**Back**](./../README.md)

#### 1. Instruction

- `var` declarations get hoisted to the top of their scope, but their assignment does not.
- `const` and `let` declarations also get hoisted to the top of their scope, but their references do not.
- `const` and `let` declarations are blessed with(享有) a new concept called [*Temporal Dead Zones (TDZ)*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#Temporal_dead_zone_and_errors_with_let).
- It's important to know that `typeof` is no longer safe.

```js
/**
 * var
 */
{
    console.log(foo);   /** undefined       */
    var foo = 2;
}

/**
 * let and const
 */
{
    len foo;
    console.log(foo);   /** undefined       */
    foo = 2;
}
 
{
    /**
     * In ECMAScript 2015, let will hoist the variable
     * to the top of the block. However, referencing the 
     * variable in the block before the variable declaration 
     * results in a ReferenceError. 
     * The variable is in a "temporal dead zone"
     * from the start of the block until the
     * declaration is processed.
     */
    console.log(foo);   /** ReferenceError  */
    const foo = 2;
}
```

- Anonymous function expressions hoist their variable name, but not the function assignment.

```js
function example() {
    console.log(anonymous);     /** undefined                    */
    
    anonymous();                /** TypeError, not a function  */
    
    var anonymous = function() {
        console.log('anonymous function expression');
    };
}
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>