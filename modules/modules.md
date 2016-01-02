## Modules [**Back**](./../README.md)

#### 1. Use modules

- Always use modules(`import`/`export`) over a non-standard module system. You can always transpile(轉譯) to your preferred module system.

```js
/**
 * bad
 */
const styleGuide = require('./styleGuide');
module.exports = styleGuide.es6;

/**
 * ok
 */
import styleGuide from './styleGuide';
export default styleGuide.es6;

/**
 * best
 */
import { es6 } from './styleGuide';
export default es6;
```

#### 2. Do not use wildcart imports

> the reason is that this can make sure you have a single default export

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>