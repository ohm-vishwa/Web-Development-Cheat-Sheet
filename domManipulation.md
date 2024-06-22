# DOM Manipulation

|DOM mainpulation| DOM Events |
|----------------| ---------- |
|[properties](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#properties)                        |[onclick](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#onclick)|
|[Element Manipulation](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#element-mainpulation)    |[addEventListener](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#addeventlistener)|
|[Attribute Manipulation](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#attribute-manipulation)|[]()|
|[style Manipulation](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#style-manipulation)        |[]()|
|[Navigation](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#navigation)                        |[]()|
|[Adding Element](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#adding-elements)               |[]()|
|[Remove Element](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/domManipulation.md#remove-element)                |[]()|


<!-- > ## DOM manipulation in ` Browser Console ` -->
> [!IMPORTANT]
> 
> The DOM ` Document Object Model ` represents a document with a logical tree\
> It allow us to maniplute/change webpage content ` HTML Elements `


## Properties
> [!NOTE]
> **innerText** --> visible text contained in a node\
> **innerHTML** --> full markup\
> **textContent** --> full text ` hidden also `

> ### innerText & innerHTML
```js
let home = document.querySelector('div');
home.innerHTML = ('<h1> Heading </h1>'); // insert HTML

let heading = document.querySelector('h1');
heading.innerText = "Ohm vishwa"; // Change Text
```

## Element Mainpulation

> [!WARNING]
> Use Browser Console

> ### View Global Object
```js
console.log(this) // Window
```
> ### View Document Object
```js
console.log(document)
console.dir(document) // array format
```

> ### Get Element by Tag
```js
document.getElementById("id") 
```

> ### Get Element by Class
```js
document.getElementsByClass("class")
```

> ### Get Element by TagName
```js
document.getElementsByTagName("img")
```

### Query Selector

```js
document.querySelector('p') // select first p element
document.querySelector('#myId') // select first element with id = "myId"
document.querySelector('.myClass') // select first element with class = "myClass"

document.querySelectorAll('p') // select all p elements
```

## Attribute Manipulation

> ### getAttribute()
```js
// <h1 id = "myId" >Ohm Vishwa</h1>

let heading = document.querySelector('h1');
    console.log(heading.getAttribute('id'));
// Output => myId
```

> ### setAttribute()
```js
// <h1 id = "myId" >Ohm Vishwa</h1>

heading.setAttribute('class', 'myClass');

// now =>  <h1 class="myClass" id="myId" >Ohm Vishwa</h1>
```

## style Manipulation
```js
// <h1 id = "myId" >Ohm Vishwa</h1>
let heading = document.querySelector('h1');
heading.style.color = "red"; // now h1 tag text are red
```
> [!CAUTION]
> it can mainpulate ` inline CSS ` only.

> ### classList 
```js
/* .green {
    color: green;
}
.background {
    background-color: purple;
}
.blue {
    color: blue;
} */

/* <h1 id="myId">Ohm Vishwa</h1> */

let heading = document.getElementById('myId');
    heading.classList.add("green");
    heading.classList.replace("green","blue")
    heading.classList.add("background");
    heading.classList.remove("blue",);
    heading.classList.contains("background") // true

    // toggle => if arg is present then, remove (vise vesa)
    heading.classList.toggle("background") // flase
    heading.classList.toggle("background") // true
```
> ### Navigation
```js
/* <div>
        <h1 id="myId">Heading</h1>
    </div>
    <ul>
        <li>Item-1</li>
        <li>Item-2</li>
        <li>Item-3</li>
    </ul> */
let h1 = document.querySelector('h1');
h1.parentElement // <div>...</div>

let div = document.querySelector('div');
div.children // <h1>Heading</h1>
div.childElementCount // 1

let ul = document.querySelector(ul);
ul.children[0]; // Item-1
```

> ### Adding Elements
```js
let div = document.querySelector('div');

let u = document.createElement('u');
u.innerText = "underline";
div.appendChild(u); // insert as child element at bottom

let p1 = document.createElement('p');
p1.innerText = "bottom"
div.append(p1); // insert at bottom

let p2 = document.createElement('p');
p2.innerText = "top";
div.prepend(p2); // insert at top

let btn = document.createElement('button');
btn.innerText = "Button"
div.insertAdjacentElement('beforebegin',btn); // (where,element)
// div.insertAdjacentElement('beforeend',btn);
// div.insertAdjacentElement('afterbegin',btn);
// div.insertAdjacentElement('afterend',btn);
```

> ### Remove Element
```js
/* <div>
<h1 id="myId">Heading</h1>
</div> */

let div = document.querySelector('div');
// let h1 = document.querySelector(h1);
let h1 = document.querySelector('h1');

// div.removeChild(h1);
div.remove();
```

---

# DOM Events
> [!NOTE]
> Events are signal that something has occurred. (user input / action)

> ### onclick ` Mouse Event `

```js
let button = document.querySelector('button');

let sayHello = () => {
    alert('Hello');
}

button.onclick = () => {
    alert("hello world");
};

let btns = document.querySelectorAll('button');

for (btn of btns){
    btn.onclick = sayHello; // () not bacause we don't to execute currently.
}
```
> [!NOTE]
> ` onclick ` event multiple function execution is not possible

> ### addEventListener
```js
let sayHello = () => {
    alert('Hello');
}
let sayName = () => {
    alert('ohm');
}
let button = document.querySelectorAll('button'); 

// let btns = document.querySelectorAll('button');
for (btn of button){
    btn.addEventListener('click',sayHello);
    btn.addEventListener('dblclick' ,sayName);
    // btn.onclick = sayHello; // () not bacause we don't to execute currently.
}
```

> ` this ` with Event Listenser / Handler
```js
let btn = document.querySelector('button');

btn.addEventListener('click', function(){
    this.style.backgroundColor = 'red';
})
```

> ### Keyboard Events
```js
let input = document.querySelector('input');

input.addEventListener('keydown', function(e){
    console.log(e.key) // if a pressed then,
    console.log(e.code) // code --> KeyA
})
```

> ### Form Event
```js
let form = document.querySelector('form');

form.addEventListener('submit',(event) => {
    event.preventDefault(); // redirect is prevented now
    let user = this.element[0];
    let pass = this.element[1];
});
```

> [!NOTE]
> **change** event\
> the change event occurs when the value of an element has been changed, works on ` <input> ` , ` <textarea> ` , ` <select> `
>
> **input** event\
> the input event fires when the value of an ` <input> ` , ` <textarea> ` , ` <select> ` element has been changed.

> [!IMPORTANT]
> when we handle events for nested elements, parent's event can occurs.
> to stop event bubbling ` stopPropagation() ` is used.