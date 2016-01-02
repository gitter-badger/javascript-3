## Modules [**Back**](./../README.md)

#### 1. Use modules

- Always use modules(`import`/`export`) over a non-standard module system. You can always transpile(轉譯) to your preferred module system.

```js
/**
 * bad
 */
const StyleGuide = require('./StyleGuide');
module.exports = StyleGuide.es6;

/**
 * ok
 */
import StyleGuide from './StyleGuide';
export default StyleGuide.es6;

/**
 * best
 */
import { es6 } from './StyleGuide';
export default es6;
```

#### 2. Do not use wildcart imports

> the reason is that this can make sure you have a single default export.

```js
/**
 * bad
 */
import * as StyleGuide from './StyleGuide'
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>