#  Introduction to objects
 * Objects are key value pair data
 * arrays are used to store data but not suffient for real world entity
```js
// Declaration of object
// Syntax :
const objectName={
    propery1:value1,
    propery2:value2,
    propery3:value3
}
example : 
const person={
    name:"ravi",
    email:"ravi@gmail.com",
    gender:"male"
}

//accesing object value
console.log("accesing object");
console.log(person); // this print whole object
console.log(person.name); //this print the particular value with given key
console.log(person.email);
console.log(person.gender);

//inserting new key value pair
/* syntax :
    objectName.key=value
*/
person.mobile=8787205784

console.log(person);
//inserting attributes as a list
person.hobbies=["singing","dancing","swiming"]

console.log(person);

console.log(person.hobbies);

for (let hobby of person.hobbies){
    console.log(hobby);
}

/**
 * iterating object value
 * 1. for in loop
 * 2. Object.keys
 */
console.log("printing using for in loop");
for(let key in person){
    console.log(`${key} : ${person[key]}`);
}
console.log("printing using the object key");
console.log(Object.keys(person));
for(let key of Object.keys(person)){
    console.log(key , person[key]);
}
//computed properties
let key1='obkey1'
let key2='obkey2'
let value1='obvalue1'
let value2='obvalue2'
const ob={
    [key1]:value1,
    [key2]:value2
}
console.log(ob);

//spread operator for objects
const hello={..."abcdefghijklmnopqrstuvwxyz"};
console.log(hello);

//object destructuring - variable name must be same as the key
const user={name:"ashrith",branch:"cse"}
const {name,branch}=user;
console.log(name,branch);
//changing the name of key
const {name:var1,branch:var2}=user;
console.log(var1,var2);

//object nested in array - all operations perfrom in array are possible in this case.
const users=[
    {userId:1,name:'ashrith',branch:'cse'},
    {userId:2,name:'sam',branch:'me'},
    {userId:3,name:'tom',branch:'cse'},
]
console.log(users);
