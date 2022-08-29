<h1 align="center">Node & Oracle - Week 6</h>
  
### _Week challenges (Monday)_ 💻

_1. [Expressions Matter]() exercise_

> ### Solution

```js
SELECT
(
  SELECT MAX(mx)
  FROM 
  ( VALUES (a+b+c),
           (a+b*c),
           (a*b+c),
           (a*b*c),
           (a*(b+c)),
           ((a+b)*c) )
  AS _(mx)
) AS res
FROM expression_matter;
```

<br>

[⬆ Back to homepage](https://github.com/21atalia/core-code-upskilling-readme/blob/main/README.md)
