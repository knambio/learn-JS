1. Find the attributes of a HTML element -> You first have to assign the element into a variable and then use console.dir() using the variable.
```js
const HTMLElement = document.querySelector('img') //using img as an element example
// after the variable has been created, run command below...
console.dir(HTMLElement)
// this will produce an expandable object of the HTML element showing all its Attributes
```

2. Applying an array of styles to multiple elements - looping them over using for loop:
```html
<h1>
        <span>R</span>
        <span>A</span>
        <span>I</span>
        <span>N</span>
        <span>B</span>
        <span>O</span>
        <span>W</span>
    </h1>
```
```js
const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet']; //an array of styles that you'll put

//using for loop to assign
let rainbow = document.querySelectorAll('span');
for (let i = 0; i < rainbow.length; i++){
    rainbow[i].style.color = colors[i]
}
```
3. Same ideas above but changing DOM using Objects key-value in an Array using For loop:
```html
<ul>
  <li><figure><img src=""><figcaption>no image</figcaption></figure></li>
  <li><figure><img src=""><figcaption>no image</figcaption></figure></li>
  <li><figure><img src=""><figcaption>no image</figcaption></figure></li>
  <li><figure><img src=""><figcaption>no image</figcaption></figure></li>
  <li><figure><img src=""><figcaption>no image</figcaption></figure></li>
</ul>
```js
const pandaPics = [
  {
    url: 'https://files.worldwildlife.org/wwfcmsprod/images/HERO_Red_Panda_279141/hero_small/4ocbtgyvq7_XL_279141.jpg',
    caption: '<span>first red panda</span>'
  },
  {
    url: 'https://www.lpzoo.org/wp-content/uploads/2021/07/p_rp.jpg',
    caption: 'second red panda'
  },
  {
    url: 'https://media.hswstatic.com/eyJidWNrZXQiOiJjb250ZW50Lmhzd3N0YXRpYy5jb20iLCJrZXkiOiJnaWZcL3JlZC1wYW5kYS5qcGciLCJlZGl0cyI6eyJyZXNpemUiOnsid2lkdGgiOjgyOH19fQ==',
    caption: 'third red panda'
  },
  {
    url: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQYtJbnHPG3ozVoGzwk94OCRysnM7iNgu9nPg&usqp=CAU',
    caption: 'fourth red panda'
  },
  {
    url: 'https://s1.reutersmedia.net/resources/r/?m=02&d=20200226&t=2&i=1495671525&w=&fh=545px&fw=&ll=&pl=&sq=&r=LYNXNPEG1P2B0',
    caption: 'fifth red panda'
  }
]
let pandaImg = document.querySelectorAll('img');
for (let i = 0; i < pandaImg.length; i++){
pandaImg[i].src = pandaPics[i].url;
}
let pandaCap = document.querySelectorAll('figcaption');
for (let i = 0; i < pandaCap.length; i++){
pandaCap[i].innerText = pandaPics[i].caption;
}
```
