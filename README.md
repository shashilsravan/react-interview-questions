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
</ol>

## Questions with Answers 

1. What is React ?
A) React is an open-sourced Javascript Library (frontend) created by J. Walke, React was first deployed on FB in 2011 and on Instagram in 2012. ReactJS is used for building user interfaces especially for single page applications.It follows the component-based approach in building reusable UI Components. It is used to handle view layer for web apps.

2. What are the features of React ?
A) ReactJS uses re-useable UI Components to develop the view, It supports Server Side rendering. It uses virtualDOM. It uses JSX and One-way Data binding.

3. How React works?
A) React creates a virtual DOM and when a state changes in a react component it runs a "diffig" algorithm to know what has changed in the virtual DOM. And then it updates the DOM with the resulted difference (which is known as reconciliation)

4) What are the advantages of React?
A) Scope for testing the codes. Known to be SEO friendly. Reusable components and Performance enhancement

5) What is JSX ?
A) JSX is a syntax extension of JavaScript. It produces React Elements. You can also embed javascript expressions in JSX. 
Example:
```javascript
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
