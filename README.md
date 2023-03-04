
![Logo](https://d258lu9myqkejp.cloudfront.net/projects/5302/knowledge_base/original/code-snippets-pro-logo1280w-invert.png)



This Repository is made for Share React Snippets. i hope this Repo will help you. Contributions are always welcome!



## Snippets

- [Dynamic Styling using inline css in React](#1-dynamic-styling-using-inline-css-in-react)
- [Dynamic Styling using external css in React](#2-dynamic-styling-using-external-css-in-react)
- [Create Button by Styled Component](#3-create-button-by-styled-component)


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
**App.js**
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
**Style.css**
```css
body {
    font-family: sans-serif;
    margin: 0;
    padding: 3rem;
    background-color: #2d2c2c;
    color: #959090;
    text-align: center;
}

.active {
    background-color: orange;
    padding: 0.5rem;
    border-radius: 4px;
    color: black;
}
```
### 3. Create Button by Styled Component
```javascript
import styled from 'styled-components';

const Button = styled.button`

  font: inherit;
  padding: 0.5rem 1.5rem;
  border: 1px solid #8b005d;
  color: white;
  background: #8b005d;
  box-shadow: 0 0 4px rgba(0, 0, 0, 0.26);
  cursor: pointer;


&:focus {
  outline: none;
}

&:hover,
&:active {
  background: #ac0e77;
  border-color: #ac0e77;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.26);
}
`;

//insted this you can use above code
// const Button = props => {
//   return (
//     <button type={props.type} className="button" onClick={props.onClick}>
//       {props.children}
//     </button>
//   );
// };

```
## Author

- [Krishan Kumar Jangid](https://www.github.com/krishanjangid)

