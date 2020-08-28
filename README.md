# React interview questions
### Give a Star If you liked it
### Questions are collected from various sources !!

## Questions Only (for answers swipe up)
<ol>
  <li> What is React ? </li>
  <li> What are the features of React ? </li>
  <li> How React works? </li>
  <li> What are the advantages of React? </li>
  <li> What is JSX ? </li>
  <li> What is `React.createClass` ? </li>
  <li> What is the difference between element and component? </li>
  <li> What are the types of Components in React? </li>
  <li> What is `ReactDOM` and what is the difference between `ReactDOM` and `React` ? </li>
</ol>

## Questions with Answers 

1. What is React ?  <br />
A) React is an open-sourced Javascript Library (frontend) created by J. Walke, React was first deployed on FB in 2011 and on Instagram in 2012. ReactJS is used for building user interfaces especially for single page applications.It follows the component-based approach in building reusable UI Components. It is used to handle view layer for web apps.
<hr/>

2. What are the features of React ?  <br />
A) ReactJS uses re-useable UI Components to develop the view, It supports Server Side rendering. It uses virtualDOM. It uses JSX and One-way Data binding.
<hr/>

3. How React works?  <br />
A) React creates a virtual DOM and when a state changes in a react component it runs a "diffig" algorithm to know what has changed in the virtual DOM. And then it updates the DOM with the resulted difference (which is known as reconciliation)
<hr/>

4. What are the advantages of React?  <br />
A) Scope for testing the codes. Known to be SEO friendly. Reusable components and Performance enhancement
<hr/>

5. What is JSX ?  
A) JSX is a syntax extension to JavaScript and comes with the full power of JavaScript. JSX produces React “elements”. You can embed any JavaScript expression in JSX by wrapping it in curly braces  

    In the example below text inside `<h1>` tag is returned as JavaScript function to the render function.

    ```jsx harmony
    class App extends React.Component {
      render() {
        return(
          <div>
            <h1>{'Welcome to React world!'}</h1>
          </div>
        )
      }
    }
    ```
<hr/>
6. What is <b>React.createClass</b> ? <br>
A) <b>React.createClass</b> allows us to generate component classes. It is like using custom JavaScript class system. We can also implement component classes with ES6 (it is native approach) <br>
<b> React.createClass approach: </b>

  ```javascript
  import React from 'react';
  const Contacts = React.createClass({
    render(){
      return(
        <div> Hello </div>
      );
    }
  });
export default Contacts;
  ```  

<b> using ES6 approach: </b>  
  ```javascript
  import React from 'react';
  class Contacts extends React.Component{
    constructor(props){
      super(props)
    }
    render(){
      return(
        <div> Hello </div>
      );
    }
  }
  export default Contacts;
  ```  
<hr/>
7. What is the difference between element and component?  
<br>
A) Element is the plain object describing what you want to appear on the screen. Element can contain other elements in their props. <br>
<b> Creating a react element </b>
  
    
      
```javascript  
  const element = React.createElement(  
    'h1',  
    {'className':'greeting'},  
    'Hello world !'  
  );  
``` 
 

<i> When it renders it will be like in `ReactDOM.render()` </i> 
  ```html
  <h1 class='greeting'> Hello world </h1>
  ```  

Whereas component can be declared in several ways. A component can be a class with `render()` method. It takes props as input and produces JSX tree as an output
<b> Example </b>
  ```javascript
  const Button = ({ onLoggedIn }) =>
    <div id={'btn'} onClick={onLoggedIn}> Login </div>
  ```

<hr />

8. What are the types of Components in React? 
A) There are two types of components <u> Class based Component </u> and <u> Function based components </u> 
<b> Function based Components: </b> This is the simplest way to create a component Those are pure JavaScript functions that accept props object as first parameter and return React elements: 
```javascript
function Navbar(props) {
  return <nav> { props.title }</nav>
}
``` 
<b> Class based components: </b> You can also use ES6 class to define a component. The above function component can be written as: 
```javascript
class Navbar extends React.Component {
  constructor(props){
    super(props);
    this.state = {
      title: props.title;
    }
  }
  render() {
    return <h1>{`Hello, ${this.state.title}`}</h1>
  }
}
```
<hr />
