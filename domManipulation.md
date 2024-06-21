# DOM Manipulation

|DOM mainpulation|
|----------------|
|[properties]()|
|[Element Manipulation]()|
|[Attribute Manipulation]()|
|[style Manipulation]()|
|[classList Property]()|
|[]()|


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
