# printing message
```js
console.log("hello world");
```
# different data types in js
* var
* let 
* const
```js
var name="ravi"
console.log(name);
let Name="shyam"
console.log(Name);
```

# string 
```js
let firstName="harsh"
//String.length method is used to find the length of string
console.log(firstName.length);

// trim() - this method is used to remove spaces from the string
let lastName="    kumar"
console.log("length of last name when it contains the space",lastName.length);

lastName=lastName.trim()
console.log("length of last name when it contains the space",lastName.length);

//slice() - this method is used to truncate the string from one point to another pojnt like slice(initial_position, final_position)
let fullName="ravi kumar shastri"
console.log(fullName);
fullName=fullName.slice(0,5)
console.log(fullName);
```
# primitive data types
/**
 * number
 * string
 * booleans
 * undefined
 * null
 * BigInt
 * Symbol
 */

// to know the datatype of any variable we use `typeof' operator

```js
let name1="raju"
console.log(typeof name1);
```

# conversion of string to number and vice-versa
/**
 * number to string
 * method 1= num=num+""
 * method 2= num=String(num)
 * string to number
 * method 1= num=+num
 * method 2= num=number(num)
 * 
 */

```js
let num="55"
console.log("data type of number->",typeof num);
//num=+num
num=Number(num)
console.log("data type of number->",typeof num);
let naam=123
console.log("data type of naam->",typeof naam);
//naam=naam+""
naam=String(name)
console.log("data type of naam->",typeof naam);
```
