# Javascript Important Terms & Methods

| Terms  | String Methods | Array Methods | Higher Order Functions |
| -----  | -------------- | ------------- | ---------------------- |
||[trim()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#trim)               |[for( of )](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#for-of-)              ||
||[toUpperCase()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#tolowercase) |[push()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#push-add-to-end)         ||
||[indexOf()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#indexof)         |[pop()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#pop-delete-from-end)      ||
||[slice()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#slice)             |[unshift()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#unshift-add-to-front) ||
||[replace()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#replace)         |[shift](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#shift-delete-from-front)  ||
||[repeat()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#repeat)           |[indexOf()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#indexof-1)            ||
||                                                                                                    |[include()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#includes)             ||
||                                                                                                    |[concat()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#concat)                ||
||                                                                                                    |[reverse()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#reverse)              ||
||                                                                                                    |[slice()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#slice-1)                ||
||                                                                                                    |[splice()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#splice)                ||
||                                                                                                    |[sort()](https://github.com/ohm-vishwa/MERN-Cheat-Sheet/blob/main/javaScript.md#sort)                    ||

> [!IMPORTANT] 
> ` const array = newArray; `\
> we can't assign new array refrence to **array**. \
> but, we can perform all Array operations inside it.
> 
> ` let array = newArray; ` \
> it makes refrence of assigned array.\
> change in one array reflect in both
> 
> these cases are same with ` object `.

> ### Spread Operator ` ... ` 
```js
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5, 6];    // Spreading an Array
console.log(arr2); 
// Output => [1, 2, 3, 4, 5, 6]

const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 }; // Spreading an Object
console.log(obj2);
// Output => { a: 1, b: 2, c: 3 }

const numbers = [1, 2, 3];
const sum = (a, b, c) => a + b + c;
console.log(sum(...numbers)); // Function Arguments
// Output => 6 

const original = [1, 2, 3];
const copy = [...original]; // Copying Arrays
console.log(copy);
// Output => [1, 2, 3]

const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const combined = [...array1, ...array2]; // Concatenating Arrays
console.log(combined);
// Output => [1, 2, 3, 4, 5, 6]

const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const combined = { ...obj1, ...obj2 }; // Combining Objects
console.log(combined); 
// Output => { a: 1, b: 3, c: 4 }
```

> ### Template Literal `${ }`
```js
let amount = 100;
console.log(`I have ${amount} rupees.`);
// Output => I have 100 rupees.
```

> ### ` this ` keyword

> [!IMPORTANT]
> In JavaScript, the ` this ` keyword is a special identifier that refers to the context in which the current code is executing.
> 
> ` this ` with <u>Normal Function</u>  ` scope --> calling object `\
> ` this ` with <u>Arrow Function</u> ` scope --> parent's scope `

```js
console.log(this); // In a browser: Window, In Node.js: global

const obj = {
  value: 42,
  getValue: function() {
    return this.value; // scope --> obj
  },
  getValue2 : () => {
    return this.value; // parent`s scope --> Window
  }
};
console.log(obj.getValue()); // 42
console.log(obj.getValue2()); // undefined
```

> ### Destructuring Array
```js
let names = ["Ohm", "Abhishek", "Asif", "jay prakash"];
// let student1 = names[0];
// let student2 = names[1];
// let student3 = names[2];
// let student4 = names[3];
let [student1, student2, student3, student4] = names;
    console.log(student2);
// Output => Abhishek
```

> ### Destructuring Object
```js
const student = {
    name: "Priyanka",
    age : 12,
    class : 4,
    subjects: ["maths", "science", "english", "hindi"],
    username: "@priyanka1513",
    password: "abcd"
}
let {username, password} = student;
    console.log(username);
// Output => @priyanka1513

let { username: user, password: secret} = student;
console.log(user);
// Output => @priyanka1513

```

> ### length
```js
let str = "Hello";
let arr = [str, "i", "am", "ohm"];
console.log(str.length);
//Output => 5
console.log(arr.length);
//Output => 4
```

> ### try & catch
```js
try {
  // Code that may throw an exception
} catch (error) {
  // Code to handle the exception
} finally {
  // Code that will always run, regardless of an exception (optional)
}
```

> ### Arrow Function ` () => {} ` vs Regular function
```js
// Regular function
function name(params) {
// function body
};

// Arrow function
const add = (a, b) => a + b;

const func = () => {
// function body
};

// inside class
const myClass = { 
   getName2 : () => {
  // function body 
  }
};

const square = x => x * x;

const nestedFunction = x => y => x + y;
```

### String Methods

> ### trim()

> [!NOTE]
> it removes front & back spaces from string.\
> it can't changes original string.\
> it can't remove middle spaces.

```js
let str = "   ohm vishwa    ";
let newStr = str.trim();
console.log(newStr);
// Output => ohm vishwa
```

> [!NOTE]
> Strings are immutable in JavaScript.

> ### toLowerCase()
```js
let str = "OHM";
let newStr = str.toLowerCase();
console.log(newStr);
// Output => ohm
```

> ### toUpperCase()
```js
let str = "ohm";
let newStr = str.toUpperCase();
console.log(newStr);
// Output => OHM
```

> ### indexOf()
```js
//   index 012345678..
let str = "ILoveCoding";
console.log(str.indexOf("Love"));
// Output => 1
console.log(str.indexOf("b"));
// Output => -1
```

> [!NOTE]
> starting index is ` inclusive ` but,\
> ending index is ` exclusive `.

> ### slice()
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

> ### replace()
```js
let str = "ILoveCoding";
let newStr = str.replace("Love", "Do");
console.log(newStr);
// Output => IDoCoding
```

> ### repeat()
```js
let str = "Hello";
let newStr = str.repeat(3);
console.log(newStr);
// Output => HelloHelloHello
```

---

# Array Methods

> ### push() ` add to end `
```js
let arr = ['a', 'b', 'c'];
arr.push('d');
console.log(arr);
// Output => [ 'a', 'b', 'c', 'd' ]
```

> ### pop(); ` delete from end `
```js
let arr = ['a', 'b', 'c'];
arr.pop();
console.log(arr);
// Output => [ 'a', 'b' ]
```

> ### unshift() ` add to front `
```js
let arr = ['w', 'y', 'z'];
arr.unshift('a');
console.log(arr);
// Output => [ 'a', 'w', 'y', 'z' ]
```

> ### shift() ` delete from front `
```js 
let arr = ['w', 'y', 'z'];
arr.shift();
console.log(arr);
// Output => [ 'y', 'z' ]
```

> ### indexOf()
```js
let arr = ['red', 'blue', 'green'];
console.log(arr.indexOf("blue"));
// Output => 1
```

> ### includes()
```js
let arr = ['red', 'blue', 'green'];
console.log(arr.includes('red'));
// Output => true
console.log(arr.includes('yellow'));
// Output => false
```

> ### concat()
```js
let primary = ['red', 'blue'];
let secondary = ['yellow', 'orange', 'green'];
let newArr = primary.concat(secondary);
console.log(newArr);
// Output => [ 'red', 'blue', 'yellow', 'orange', 'green' ]
```

> ### reverse()
```js
let arr = ['yellow', 'orange', 'green'];
arr.reverse();
console.log(arr);
// Output => [ 'green', 'orange', 'yellow' ]
```

> ### slice()
```js
let arr = [ 'red', 'blue', 'yellow', 'orange', 'green' ];
let newArr = arr.slice( 1 , 3); // (start index, end index) end index is excluded
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
> starting index is ` inclusive ` but,\
> ending index is ` exclusive `.

 > ### splice()
```js
//       index :  0   1   2   3   4   5     
let alphabets = ['a','b','c','d','e','f'];
alphabets.splice(2,3,'x','y','z'); // (start index,delete count,insert)
console.log(alphabets);
// Output => [ 'a', 'b', 'x', 'y', 'z', 'f']

let alphabets = ['a','b','c','d','e','f'];
alphabets.splice(2,3); // (start index,delete count)
console.log(alphabets);
// Output => [ 'a', 'b','f']

alphabets = ['a','b','c','d','e','f'];
alphabets.splice(3); // (start index) delete all after index
console.log(alphabets);
// Output => [ 'a', 'b', 'c' ]


alphabets = ['a','b','c','d','e','f'];
alphabets.splice(1,3,'g','h','i'); // (start index,delete count,insert,...)
console.log(alphabets);
// Output => [ 'a', 'g', 'h', 'i', 'e', 'f' ]
```

> [!NOTE]
> .slice() ` doesn't change ` original array but,\
> .splice() ` changes ` original array

> ### sort()
```js
let fruits = ['pineApple', 'banana', 'apple', 'coconut'];
fruits.sort();
console.log(fruits);
// Output => [ 'apple', 'banana', 'coconut', 'pineApple' ]
```

# Math Object Important Properties & methods

```js
console.log(Math.random()); // generate random number between [0 , 1)

let arr = [1,2,3,34,6,56,4,3];
console.log(Math.max(...arr)); //reutrn largest number
// Output => 56

console.log(Math.min(2,1,3,2)); // return smallest number
// Output => 1

console.log(Math.abs(-5.3)); // gives +ve value
// Output => 5.3

console.log(Math.pow(2,3)); // power function
// Output => 8

console.log(Math.sqrt(9)); // square root function
// Output => 3

console.log(Math.cbrt(27)); // cube root
// Output => 3

console.log(Math.floor(2.34)); // floor function
// Output => 2

console.log(Math.ceil(3.2)); // ceiling function
// Output => 4

console.log(Math.PI); // value of PI
// Output => 3.141592653589793

console.log(Math.log2(34)); // log 2 base 2
// Output => 5.087462841250339

console.log(Math.LOG2E); // value of log 2 base e
// Output => 1.4426950408889634

console.log(Math.LOG10E); // value of log 10 base e
// Output => 0.4342944819032518
```

# Higher Order Functions & Callback Functions

> ### for (of) vs ForEach()
```js
const arr = [1, 2, 3, 4, 5, 6, 7];
// forEach function
arr.forEach(el => {
    console.log(el); // print all array elements
});

// for (of) function
for (el of arr){
    console.log(el); // print all array elements
};

const arrClass = [{
    name: 'ohm',
    roll: 1
},
{
    name: 'Abhishek',
    roll: 2
},
{
    name: 'jay Prakash',
    roll: 3
}]

// forEach function
arrClass.forEach((el) => {
    console.log(el.name); // print all obejcts name
    console.log(el.roll); // print all obejcts roll
});

// for (of) function
for (el of arrClass){
    console.log(el.name); // print all obejcts name
    console.log(el.roll); // print all obejcts roll
}
```


> ### setTimeout()
```js
setTimeout(() => {
    console.log('too kaise hai aap log.');
},2000);    // execute after 2 sec
console.log('Hello guies,');

// Hello guies,
// too kaise hai aap log.  [after 2 sec]
```

> ### setTnterval() & clearInterval()
```js
let id = setInterval(() => {    // continuously executing until we stoped using clearInterval(id)
    console.log('too kaise hai aap log.');
},1000);    // 1sec interval
console.log('Hello guies');
// Hello guies
// too kaise hai aap log.  [in 1 sec interval 4 times]

setTimeout(() => {
    clearInterval(id);  // terminate setInterval()
},4000);    // execute after 4 sec
```

> ### map() vs filter()
```js
const arr = [1,2,3,4,5,6,7];

const newArr1 = arr.map((el) => {
    return el*2;
});
console.log(newArr1);
// Output => [ 2,  4,  6, 8, 10, 12, 14 ]

const newArr2 = arr.filter((el) => (el % 2 == 0));
console.log(newArr2);
// Output => [ 2, 4, 6 ]
```

> ### every() vs some()
```js
let arr = [2, 4, 6, 8];
console.log(arr.every((el) => (el % 2 == 0)));
// OutPut => true

let arr1 = [...arr, 1];
console.log(arr1.every((el) => (el % 2 == 0)));
// Output => false


let arr2 = [2, 3, 4, 8];
console.log(arr2.some((el) => (el % 3 == 0)));
// OutPut => true

let arr3 = [1, 2, 4, 5, 7];
console.log(arr3.some((el) => (el % 3 == 0)));
// OutPut => false
```
> [!NOTE]
> ` every() ` works as **logical And**\
> ` some() ` works as **logical Or**

> ### reduce()
```js
let num = [1, 2, 3, 4];
let finalValue = num.reduce((res,el) => { // (accumulator,element)
    return res + el;
});
console.log(finalValue);
// Output => 10
```


