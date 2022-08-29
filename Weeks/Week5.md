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

> ### Solution 

<br>

_1. [Separating Strings]() exercise_

<br>

```js
function sepStr(arr) {
  const words = arr.split(' ');
  const longest = [ ...(words.reduce((l, w) => w.length > l.length ? w : l, '')) ];
  return longest.map((_, i) => words.map(w => w[i] || ''));
}
```

<br>

### _Week challenges (Wednesday)_ 💻

<br>

_1. [Highest Scoring Word](https://www.codewars.com/kata/57eb8fcdf670e99d9b000272/train/javascript) exercise_

<br>

> ### Solution 

```js
function high(x){
  let as = x.split(' ').map(x => [...x].reduce((a, b) => a+b.charCodeAt(0) - 96, 0));
  return x.split(' ')[as.indexOf(Math.max(...as))];
}
```

<br>

### _Week challenges (Thursday)_ 💻

<br>

_1. [Where Is My Parent?](https://www.codewars.com/kata/58539230879867a8cd00011c/train/javascript) exercise_

<br>

> ### Solution 

```js
function findChildren(str) {
  str = str.toLowerCase()
//   beeeebb
  let arr = str.split('')
//   [ 'b', 'e', 'e', 'e', 'e', 'b', 'b' ]
  var r = '';
  let letters = [...new Set(arr)].sort()
//   ['b','e']

  for(let i = 0; i<letters.length; i++){
//     Will iterate ['b','e']
    for(let j = 0; j<str.length; j++){
//       Will iterate //   [ 'b', 'e', 'e', 'e', 'e', 'b', 'b' ]
      if(letters[i] == arr[j]) r += arr[j]
    }
  }
  return r.split('').map((x,i)=> x !== r[i-1] ? x = x.toUpperCase() : x ).join('')
//   in the map, if the actual letter isn't the same as the last one it'll make it upperCase becuase it is the first one of those group
}
```


[⬆ Back to homepage](https://github.com/21atalia/core-code-upskilling-readme/blob/main/README.md)


