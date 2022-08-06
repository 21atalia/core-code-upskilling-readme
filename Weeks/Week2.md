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

> Solution

```js
const React = require("react");

class WishlistForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = { name: '', wish: '', priority: 1 };
    this.handleNameChange = this.handleNameChange.bind(this);
    this.handleWishChange = this.handleWishChange.bind(this);
    this.handlePriorityChange = this.handlePriorityChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
  
  handleNameChange(e) {
    this.setState({name: e.target.value});
  }
  
  handleWishChange(e) {
    this.setState({wish: e.target.value});
  }
  
  
  handlePriorityChange(e) {
    this.setState({priority: e.target.value});
  }
  
  handleSubmit(e){
    e.preventDefault();
    this.props.send(this.state);
  }
  render() {
    return (
      <form onSubmit={this.handleSubmit}>
       Name: <input type="text" id="name" value={this.state.name} onChange={this.handleNameChange}/>
       Wish: <textarea rows="10" cols="10" id="wish" value={this.state.wish} onChange={this.handleWishChange} />
       <br />
       Wish Priority:
       <select value={this.state.priority} id="priority" onChange={this.handlePriorityChange}>
         <option value={1}>1</option>
         <option value={2}>2</option>
         <option value={3}>3</option>
         <option value={4}>4</option>
         <option value={5}>5</option>
      </select>
      </form>
    );
  }
};
```

<br>

### _Extra challenges_ 💻

_1. [Easter egg list in ReactJS](https://www.codewars.com/kata/5a95947f4a6b342636000173/train/javascript)_

<br>

> Solution

```js
import React from 'react';

export const EggList = ({eggs}) => { 
  return <ul>{eggs.map((value, id) => <EasterEgg name={value} key={id}/>)}</ul>;
};

export const EasterEgg = ({name, key}) => {
  return <li key={key}>{name}</li>;
};
```

<br>

_2. [PC upgrade specs using HOC in ReactJS](https://www.codewars.com/kata/5a9c0fa45084d79b1f000138)_

<br>

> Solution

```js
const React = require('react');

// Don't change PcDisplay
const PcDisplay = (props) => {
  return (<div>
  <h1>{props.title}</h1>
  <p id="price">£{props.price}</p>
  <ul>
    <li><label>CPU</label> <span>{props.cpu}</span></li>
    <li><label>RAM</label> <span>{props.ram}</span></li>
    <li><label>SSD</label> <span>{props.ssd}</span></li>
  </ul>
  </div>);
};

// Implement HOC -> returns a functions that wraps the passed in `PcDisplay` component
let withPriceModel = (WrappedComponent, increase = 0) => {
  return (props) => {
    return <WrappedComponent
            title = { props.title }
            price = { 50 + increase }
            cpu = { props.cpu }
            ram = { props.ram }
            ssd = { props.ssd }
            />
  }
};

// Build basic and pro model components using `withPriceModel`
const BasicModel = withPriceModel(PcDisplay);

const ProModel = withPriceModel(PcDisplay, 60);
```

<br>


[⬆ Back to homepage](https://github.com/21atalia/core-code-upskilling-readme/blob/main/README.md)
