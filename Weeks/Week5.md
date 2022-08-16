<h1 align="center">Node - Week 5</h1>

<br>

### _Week challenges (Monday)_ 💻

<br>

_1. [Fun With Lists](https://www.codewars.com/kata/58259d9062cfb45e1a00006b/train/javascript) exercise_

<br>

> ### Solution 

<br>

```js
function map(head, f) {
  if (head) {
    return new Node(f(head.data), map(head.next, f));
  }
  return null;
}
```

<br>


