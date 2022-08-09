<h1 align="center">React, Pause Day & Node - Week 4</h1>

### _Week challenges (Monday)_ 💻

<br>

1. [Two To One](https://www.codewars.com/kata/5656b6906de340bd1b0000ac/train/javascript) exercise

<br>

>### Solution

<br>

```js
function longest(s1, s2) {  
  return [...(new Set(s1 + s2))].sort().join('');
}
```
