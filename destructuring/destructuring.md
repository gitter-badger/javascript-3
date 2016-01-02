## Destructuring [**Back**](./../README.md)

- *Notice that: destructuring is only supported by ECMAScript 6 (ES6). [**Browser Compatibility**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Browser_compatibility)*

#### 1. Use object destructuring

- To use object destructuring when accessing and using multiple properties of an object.

> the reason is that destructuring can save from creating temporary references for those properties.

```js
/**
 * bad
 */
function getFullName(user) {
    const firstName = user.firstName;
    const lastName = user.lastName;
    
    return firstName + ' ' + lastName;
}

/**
 * good
 */
function getFullName(user) {
    const {firstName, lastName} = user;
    
    return firstName + ' ' + lastName;
}
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>