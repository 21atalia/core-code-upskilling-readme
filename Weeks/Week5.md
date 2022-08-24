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

### _Week challenges (Tuesday)_ 💻

<br>

_1. [Separating Strings]() exercise_

<br>

```js
```

<br>

### _Week challenges (Wednesday)_ 💻

<br>

_1. [Highest Scoring Word](https://www.codewars.com/kata/57eb8fcdf670e99d9b000272/train/javascript) exercise_

<br>

```js
function high(x){
  let as = x.split(' ').map(x => [...x].reduce((a, b) => a+b.charCodeAt(0) - 96, 0));
  return x.split(' ')[as.indexOf(Math.max(...as))];
}
```

<br>

### _Week challenges (Thursday)_ 💻

<br>

_1. [Where Is My Parent?] exercise_

<br>

```js
```


[⬆ Back to homepage](https://github.com/21atalia/core-code-upskilling-readme/blob/main/README.md)


