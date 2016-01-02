## Iterators and Generators [**Back**](./../README.md)

#### 1. Do not use iterators

- Do not use iterators. Prefer JavaScript's higher-order functions like `map()` and `reduce()` instead of loops like `for-of`.

> the reason is that this enforces(強制執行) our immutable(永恆不變的) rules. Dealing with pure functions that return values is easier to reason about than side-effects.

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>