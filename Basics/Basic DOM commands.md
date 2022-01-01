1. Find the attributes of a HTML element -> You first have to assign the element into a variable and then use console.dir() using the variable.
```js
const HTMLElement = document.querySelector('img') //using img as an element example
// after the variable has been created, run command below...
console.dir(HTMLElement)
// this will produce an expandable object of the HTML element showing all its Attributes
```

2. Applying an array of styles to multiple elements - looping them over using for loop:
```js
const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet']; //PLEASE DON'T CHANGE THIS LINE!

//YOU CODE GOES HERE:
let rainbow = document.querySelectorAll('span');
for (let i = 0; i < rainbow.length; i++){
    rainbow[i].style.color = colors[i]
}
```
