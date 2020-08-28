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
  <li> What is React.createClass ? </li>
  <li> What is the difference between element and component? </li>
  <li> What are the types of Components in React? </li>
  <li> What is ReactDOM and what is the difference between ReactDOM and React ? </li>
  <li> What are the differences between a class component and a functional component ? </li>
  <li> What are Pure Components? </li>
  <li> What is VirtualDOM and how does it work?  </li>
  <li> What is state in React? </li>
  <li> What are props in React? </li>
  <li>What happen if we update state directly?  </li>
  <li> Explain the purpose of render() in React </li>
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

9. What is `ReactDOM` and what is the difference between `ReactDOM` and `React` ?  
A) As the name implies, `ReactDOM` is the glue between React and DOM. Often, we will only use it for one thing: mounting with `ReactDOM` . We can also use it to gain direct access to a DOM element by using `ReactDOM.findDOMNode()`. We use `React` to define and create our elements, for lifecycle hooks, etc

<hr />

10. What are the differences between a class component and a functional component ?  
A) Class components allows us to use additional features such as local state and lifecycle hooks. Also, to enable our component to have direct access to our store and thus holds state.
When our component just receives props and renders them to the page, this is a ‘stateless component’, for which a pure function can be used. These are also called dumb components or presentational components. So, If the component needs state or lifecycle methods then use class component otherwise use function component.
However with the addition of React Hooks, you could also use state and lifecycle methods in your functional component too

<hr />

11. What are Pure Components?  
A) `React.PureComponent` is exactly same as `React.Component` except that it handles the `shouldComponentUpdate()` method for you. When props or state changes, PureComponent will do a shallow comparison on both props and state. Components on the other hand won't compare current props and state to next out of the box. Thus, the component will re-render by default whenever `shouldComponentUpdate` is called.

<hr />

12. What is VirtualDOM and how does it work?  
A) It is like an intermediary step between the render function being called and displaying elements on the screen. The render function creates a node tree of the React components and then updates this node tree in response to the mutations in the data model caused by various actions done by the user or by the system.
Whenever any data changes in the React App, the entire UI is re-rendered in Virtual DOM representation. Now, the difference between the previous DOM representation and the new DOM is calculated. Once the calculations are completed, the real DOM updated with only those things which are changed.

<hr />

13. What is state in React?  
A) State of a component is an object that holds some information that may change over the lifetime of the component. We should always try to make our state as simple as possible and minimize the number of stateful components.  
<b>Example: </b>
```javascript
class Navbar extends React.Component {
  constructor(props) {
    super(props)
    this.state = {
      title: 'SS'
    }
  }

  render() {
    return (
      <nav>
        <h1>{this.state.title}</h1>
      </nav>
    )
  }
}
```

And state is similar to props, but it is private and fully controlled by the component i.e., it is not accessible to any component other than one that owns and sets it. 
<hr />

14. What are props in React?  
A) props are inputs to component. They are data passed down from a parent component to a child component. They are single values or objects containing a set of values that are passed to components on creation using a naming convention similar to html tag attributes. 

```html
<Greet content = 'Hello world!'>
```

```javascript
function Greet(props){
    return(
        <div>
            <h1> {props.content} </h1>
        </div>
    )
}
export default Greet;
```
<hr />

15. What happen if we update state directly?  
A) If we update the state directly it won't re-render the component

So we use `setState()` method.   
Syntax is:
```javascript
this.setState({
    title: 'New title'
})
```
<hr />

16. Explain the purpose of `render()` in React?  
A) It is mandatory for each React component to have a render() function. Render function is used to return the HTML which you want to display in a component. If you need to rendered more than one HTML element, you need to grouped together inside single enclosing tag (parent tag) such as ```<div> or <form> or <group> ```etc.

<hr />
