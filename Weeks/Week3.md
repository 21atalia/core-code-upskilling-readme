<h1 align="center">React - Week 3</h1>

### _Week challenges (Monday)_ 💻
<br>

_1. Build Search Filter In React exercise_

<br>

>### Solution

<br>

```js
import "./styles.css";
import React, { useState } from "react";

export default function App() {
const itemList = [
    "Apple",
    "Orange",
    "Pineapple",
    "Banana",
    "Cherry",
    "Milk",
    "Peanuts",
    "Butter",
    "Tomato"
];

const [filteredList, setFilteredList] = new useState(itemList);

const filterBySearch = (event) => {
    // Access input value
    const query = event.target.value;
    // Create copy of item list
    var updatedList = [...itemList];
    // Include all elements which includes the search query
    updatedList = updatedList.filter((item) => {
    return item.toLowerCase().indexOf(query.toLowerCase()) !== -1;
    });
    // Trigger render with updated values
    setFilteredList(updatedList);
};

return (
    <div className="App">
    <div className="search-header">
        <div className="search-text">Search:</div>
        <input id="search-box" onChange={filterBySearch} />
    </div>
    <div id="item-list">
        <ol>
        {filteredList.map((item, index) => (
            <li key={index}>{item}</li>
        ))}
        </ol>
    </div>
    </div>
);
};
```
<br>

>### Example




### _Week challenges (Tuesday)_ 💻
<br>

_1. Fetch Random User Data_


### _Week challenges (Wednesday)_ 💻
<br>

_1. React Router Blog exercise_

