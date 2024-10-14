1. anchor : The anchor() method of String values creates a string that embeds this string in an <a> element with a name (<a name="...">str</a>).
```js
let str="Hello";
console.log(str.anchor(test)); // <a name="test">Hello</a>
```
2. at() : this method helps to get the character from the string by giving its position. we can use both positive and negative index.
// positive index starts from the 0 and negative index starts from -1

```js
let str="Hello"
//       01234
console.log(str.at(2)); // l
console.log(str.at(-1)); // o
console.log(str.at(-20)); // undefined
```


3. charAt() : this is used to retrieve the character at a specific position in a string. It only accepts positive integer values for the position and does not support negative indexing like the at() method.
```js
console.log(str.charAt(1)); // e
console.log(str.charAt(-1)); // return nothing because it doesn't work at negative index
console.log(str[4]); // O
console.log(str[-1]); // undefined
```
