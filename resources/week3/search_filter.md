<h2>App.js<h2>
    
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
    
<h2>Styles.css</h2>
    
<br>
    
```js    
 .App {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    font-size: 22px;
}
.search-header {
    display: flex;
}
.search-text {
    margin-right: 10px;
    font-size: 22px;
    display: flex;
    align-items: center;
    justify-content: center;
}
#search-box {
    height: 25px;
}
#search-box[placeholder] {
    line-height: 25px;
    font-size: 25px;
}
#item-list {
    min-height: 260px;
}
```
