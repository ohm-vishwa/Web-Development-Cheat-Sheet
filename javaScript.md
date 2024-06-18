## Javascript Important Terms & Methods

> Template Literal `${ }`
```js
let amount = 100;
console.log(`I have ${amount} rupees.`);
// Output => I have 100 rupees.
```

> .length
```js
let str = "Hello";
let arr = [str, "i", "am", "ohm"];
console.log(str.length);
//Output => 5
console.log(arr.length);
//Output => 4
```

## String Methods
> <details>
>   <summary> 
> .trim()
>   </summary>
> it removes front & back spaces from string (it can`t change original string).
> 
> it can`t remove middle spaces.
> </details>

```js
let str = "   ohm vishwa    ";
let newStr = str.trim();
console.log(newStr);
// Output => ohm vishwa
```

> [!NOTE]
> Strings are immutable in JavaScript.

> .toLowerCase()
```js
let str = "OHM";
let newStr = str.toLowerCase();
console.log(newStr);
// Output => ohm
```

>.toUpperCase()
```js
let str = "ohm";
let newStr = str.toUpperCase();
console.log(newStr);
// Output => OHM
```

> .indexOf()
```js
//   index 012345678..
let str = "ILoveCoding";
console.log(str.indexOf("Love"));
// Output => 1
console.log(str.indexOf("b"));
// Output => -1
```

> [!NOTE]
> starting index is ` inclusive ` but, ending index is ` exclusive `.

> .slice()
```js
//   index 012345678..
let str = "ILoveCoding";
console.log(str.slice(5));
// Output => Coding
console.log(str.slice(1,5)); 
// Output => Love
console.log(str.slice(-3));
// Output => ing
```

> .replace()
```js
let str = "ILoveCoding";
let newStr = str.replace("Love", "Do");
console.log(newStr);
// Output => IDoCoding
```

> .repeat()
```js
let str = "Hello";
let newStr = str.repeat(3);
console.log(newStr);
// Output => HelloHelloHello
```
---

## Array Methods

> .push() ` add to end `
```js
let arr = ['a', 'b', 'c'];
arr.push('d');
console.log(arr);
// Output => [ 'a', 'b', 'c', 'd' ]
```

> .pop(); ` delete from end `
```js
let arr = ['a', 'b', 'c'];
arr.pop();
console.log(arr);
// Output => [ 'a', 'b' ]
```

> .unshift() ` add to front `
```js
let arr = ['w', 'y', 'z'];
arr.unshift('a');
console.log(arr);
// Output => [ 'a', 'w', 'y', 'z' ]
```

> .shift() ` delete from front `
```js 
let arr = ['w', 'y', 'z'];
arr.shift();
console.log(arr);
// Output => [ 'y', 'z' ]
```

> .indexOf()
```js
let arr = ['red', 'blue', 'green'];
console.log(arr.indexOf("blue"));
// Output => 1
```

> .includes()
```js
let arr = ['red', 'blue', 'green'];
console.log(arr.includes('red'));
// Output => true
console.log(arr.includes('yellow'));
// Output => false
```

> .concat()
```js
let primary = ['red', 'blue'];
let secondary = ['yellow', 'orange', 'green'];
let newArr = primary.concat(secondary);
console.log(newArr);
// Output => [ 'red', 'blue', 'yellow', 'orange', 'green' ]
```

> .reverse()
```js
let arr = ['yellow', 'orange', 'green'];
arr.reverse();
console.log(arr);
// Output => [ 'green', 'orange', 'yellow' ]
```

> .slice()
```js
let arr = [ 'red', 'blue', 'yellow', 'orange', 'green' ];
newArr = arr.slice( 1 , 3);
console.log(newArr);
// Output => [ 'blue', 'yellow' ]

newArr = arr.slice( 1 );
console.log(newArr);
// Output => [ 'blue', 'yellow', 'orange', 'green' ]

newArr = arr.slice( -1 );
console.log(newArr);
// Output => [ 'green' ]
```

> [!NOTE]
> starting index is ` inclusive ` but, ending index is ` exclusive `.

> .sort()
```js
let fruits = ['pineApple', 'banana', 'apple', 'coconut'];
fruits.sort();
console.log(fruits);
// Output => [ 'apple', 'banana', 'coconut', 'pineApple' ]
```