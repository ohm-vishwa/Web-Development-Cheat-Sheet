# DOM Manipulation
<!-- > ## DOM manipulation in ` Browser Console ` -->
> [!IMPORTANT]
> 
> The DOM ` Document Object Model ` represents a document with a logical tree\
> It allow us to maniplute/change webpage content ` HTML Elements `


## Properties

> > **innerText**\
> > Shows the visible text contained in a node
> >
> > **innerHTM**\
> > Shows the full markup
> >
> > **textConten**\
> > Shows the full text
 

## Methods

> [!WARNING]
> These Commands works Only in ` Browser Console `

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


