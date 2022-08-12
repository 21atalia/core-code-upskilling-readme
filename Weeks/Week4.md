<h1 align="center">React, Pause Day & Node - Week 4</h1>

### _Week challenges (Monday)_ 💻

<br>

_1. [Two To One](https://www.codewars.com/kata/5656b6906de340bd1b0000ac/train/javascript) exercise_

<br>

>### Solution

<br>

```js
function longest(s1, s2) {  
  return [...(new Set(s1 + s2))].sort().join('');
}
```

<br>

### _Week challenges (Tuesday)_ 💻

_1. [Leap Years](https://www.codewars.com/kata/526c7363236867513f0005ca/train/javascript) exercise_

<br>

>### Solution

<br>

```js
function isLeapYear(year) {
   return (year % 100 !== 0 && year % 4 === 0) || year % 400 === 0;
}
```

<br>

### _Week challenges (Wednesday)_ 💻

<br>

_1. [Maximum Length Difference](https://www.codewars.com/kata/5663f5305102699bad000056/train/javascript) exercise_

<br>

> ### Solution

```js
function mxdiflg(a1, a2) {
  if (a1.length === 0 || a2.length === 0) return -1
  let l1 = a1.map(str => str.length)
  let l2 = a2.map(str => str.length)
  return Math.max(Math.max(...l1) - Math.min(...l2), Math.max(...l2) - Math.min(...l1))
}
```

[⬆ Back to homepage](https://github.com/21atalia/core-code-upskilling-readme/blob/main/README.md)


