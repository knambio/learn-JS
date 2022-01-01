1. Find the attributes of a HTML element -> You first have to assign the element into a variable and then use console.dir() using the variable.
E.g:
```js
const HTMLElement = document.querySelector('img') //using img as an element example
// after the variable has been created, run command below...
console.dir(HTMLElement)
// this will produce an expandable object of the HTML element showing all its Attributes
```
