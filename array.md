# introduction to array
 * array is collection of hetrogenous type means we can store any type of data in array.
 * array is mutable data type means when we add element the array the it updates the original array.
 * var a=[1,2,3,4] // numbered data type
 * var b=['sh','ee','de'] // string data type
 * var c=[1,1.2,'sfc'] //mixed data type

```js
var a=[1,2,3,4]
console.log(a);
var b=['sh','ee','de']
console.log(b);
var c=[1,1.2,'sfc']
console.log(c);


// adding element - push method is used to add element
a.push(2)
console.log("after adding elemt");
console.log(a);
// removing element from the last -pop method is used and this method return the popped element
let poppedelement=a.pop()
console.log(poppedelement);

//add element from the start we use unshift method
a.unshift(23)
console.log(a);

// removing the element from the start  we use shift method
let shiftpopped=a.shift()
console.log(shiftpopped);

/**
 * push and pop method are faster than shift and unshift,
 * push and pop method use the last index to insert and delete the element,
 * whereas unshift and shift require the shift or unshift whole array
 */

/**
 *  different between primitive and refernce data type wrt to storing variable in memory
 *  primitive data type uses STACK to store the element
 *  whereas refernce data type uses HEAP memory 
 *  in this the reference address store in the STACK
 */

/**
 * Cloning of array
 * there are three ways through which can clone the array
 * 1. by slice method
 * 2. by concat method
 * 3. spread operator
 */
const fruits=["banana", "apple", "mango"]
console.log("fruits array",fruits);
const fruits1=fruits.slice(0);
console.log("fruits1 array",fruits1);
const fruits2=["apple", "mango"]
const fruits3=fruits.concat(fruits)
console.log("fruits2 array",fruits2);
const fruits4=["banana", "mango"]
const fruits5=[...fruits4] // spread operator
console.log("fruits5 array ",fruits5);

/**
 * looping in array
 * 1. for loop
 * 2. while loop
 * 3. for of loop - it return the index value of array
 * 4. for in loop - it returns the index of array
 */
//for loop
console.log('for loop printing');
for(let i=0;i<fruits.length;i++){
    console.log(fruits[i]);
}
//while loop
console.log('while loop printing');
let i=0;
while(i<fruits.length){
    console.log(fruits[i]);
    i++;
}
//for of loop
console.log('for of loop printing');
for(let fruit of fruits){
    console.log(fruit);
}
//for in loop
console.log('for in loop printing');
for(let index in fruits){
    console.log(fruits[index]);
}

/**
 * Array destructring - it concept of assigning variable from array value accoding to our feasibility
 * Traditional way
 *  const fruits=["banana", "apple", "mango"]
 *  const fruit1=fruits[0]
 *  const fruit2=fruits[1]
 * Modern way
 *  const [fruit1,fruit2]=fruits;
 *          0       1
 */
console.log("-traditional way array destructing-");
console.log(fruits);
const f1=fruits[0];
const f2=fruits[1];
console.log(f1,f2);

console.log("-modern way array destructing-");
console.log(fruits);
const[f01,f02]=fruits;
console.log(f01,f02);
# array important method
1. forEach
2. map
3. filter
4. reduce
5. sort
6. find
```
