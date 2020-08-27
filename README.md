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
4) What are the advantages of React?  <br />
A) Scope for testing the codes. Known to be SEO friendly. Reusable components and Performance enhancement
<hr/>
5) What is JSX ?  <br />
A) JSX is a syntax extension of JavaScript. It produces React Elements. You can also embed javascript expressions in JSX. 
Example: <br />
  ```jsx harmony
  class App extends React.Component{
    const title = 'Hello world!';
    render() {
      return(
        <div>
          <h1>{title}</h1>
        </div>
      )
    }
  }
  ```
<br />
<hr/>
<br />
