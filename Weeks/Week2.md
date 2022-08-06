<h1 align="center">React - Week 2</h1>

### _Week challenges (Monday)_ 💻
<br>

_1. [Is Palindrome?](https://www.codewars.com/kata/57a5015d72292ddeb8000b31/train/javascript) exercise_

<br>

```js
function isPalindrome(line) {
  return (String(line) == String(line).split('').reverse().join('') )
}
```
<br>

### _Week challenges (Tuesday)_ 💻

_1. [Well Of Ideas](https://www.codewars.com/kata/57f222ce69e09c3630000212/train/javascript) exercise_

> Solution 1

<br>

```js
function well(x) {
  const count = x.reduce((s, v) => s + (v == 'good'), 0);
  return count ? count > 2 ? 'I smell a series!' : 'Publish!' : 'Fail!';
}
```

<br>

> Solution 2

<br>

```js
const well = x => {
  const good_count = x.filter(x => x == 'good').length;
  return good_count < 1 ? 'Fail!' : 
         good_count < 3 ? 'Publish!' : 'I smell a series!';
}
```

<br>

### _Week challenges (Wednesday)_ 💻

_1. [React Manage Events](https://www.codewars.com/kata/5a8319f257c562ede8000037/train/javascript) exercise_

> Solution 

```js
import React from 'react';

export class Counter extends React.Component{
    constructor(props){
        super(props);
        this.state = {
            counter: 0
        };
        this.increment = this.increment.bind(this);
        this.decrement = this.decrement.bind(this);
    }

    increment(){
        this.setState({counter: this.state.counter + 1});
    };

    decrement(){
        this.setState({counter: this.state.counter - 1});
    };

    render(){
        return (
            <div className='counter'>
                <p id='counter'>{this.state.counter}</p>
                <button id='increment' onClick={this.increment}>+</button>
                <button id='decrement' onClick={this.decrement}>-</button>
            </div>
        );
    }
}
```

<br>

### _Week challenges (Thursday)_ 💻

_1. [React Santa Wish List]() exercise_


### _Extra challenges_ 💻

_1. [Easter egg list in ReactJS](https://www.codewars.com/kata/5a95947f4a6b342636000173/train/javascript)_
_2. [PC upgrade specs using HOC in ReactJS](https://www.codewars.com/kata/5a9c0fa45084d79b1f000138)_

<br>


[⬆ Back to homepage](https://github.com/21atalia/core-code-upskilling-readme/blob/main/README.md)
