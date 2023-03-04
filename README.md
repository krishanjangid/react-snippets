
![Logo](https://d258lu9myqkejp.cloudfront.net/projects/5302/knowledge_base/original/code-snippets-pro-logo1280w-invert.png)



This Repository is made for Share React Snippets. i hope this Repo will help you. Contributions are always welcome!



## Snippets

- [Dynamic Styling using inline css in React](#1-dynamic-styling-using-inline-css-in-react)
- [Dynamic Styling using external css in React](#2-dynamic-styling-using-external-css-in-react)

## Tech Stack

**Client:** React

**Server:** Node


## Feedback

If you have any feedback, please reach out to us at krishanjangid516@gmail.com.


# Examples / Snippets

### 1. Dynamic Styling using inline css in React
```javascript
import React,{useState} from 'react';
// don't change the Component name "App"
export default function App() {
    const [isClicked, setIsClicked] = React.useState(false);
    
    function formSubmitHandler() {
        setIsClicked(isClicked => !isClicked);
    }
        
    return (
        <div>
            <p style = {{color: isClicked ? 'red' : 'white'}}>Style me!</p>
            <button onClick ={formSubmitHandler}>Toggle style</button>
        </div>
    );
}
```
### 2. Dynamic Styling using external css in React

```javascript
import React from 'react';
import './styles.css';

export default function App() {
    const [isActive, setIsActive] = React.useState(false);
    
    function togglebtn(){
        setIsActive(isActive => !isActive);
    }
    return (
        <div>
            <p className = {isActive ? 'active' : ''}>Style me!</p>
            <button onClick= {togglebtn}>Toggle style</button>
        </div>
    );
}
```

## Author

- [Krishan Kumar Jangid](https://www.github.com/krishanjangid)

