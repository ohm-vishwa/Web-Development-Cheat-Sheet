## Javascript Important Terms & Methods
> Template Literal `${ }`
```js
let amount = 100;
console.log(`I have ${amount} rupees.`);
// Output => I have 100 rupees.
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
let str = "ILoveCoding";
console.log(str.indexOf("Love"));
// Output => 1
console.log(str.indexOf("C"));
// Output => 5
console.log(str.indexOf("b"));
// Output => -1
```
> .slice()
```js
        // 012345678..
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
## Array Methods