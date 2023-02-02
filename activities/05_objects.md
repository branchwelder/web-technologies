# Objects

Practice working with JavaScript objects using the following problems. The
solutions are hidden below.

```js
/*
Javascript Objects Exercise
*/
​
/*
1. Write a method that verifies whether an argument is a plain object, not an array or null
It should return true for an object, and false otherwise. ({ a: 1 }) => true, ([1, 2, 3]) => false
*/
​
const data = { a: 1 };
const data = [1, 2, 3];
console.log(checkObject(data));
​
function checkObject(element) {
  //put your code here
}
​
/*
2. Change the value of "room" to be correct in the courseInfo object
*/
​
let courseInfo = {
  name: 'HCDE 438',
  instructor: 'Hannah Twigg-Smith',
  room: 'SIEG 128'
};
​
//put your code here
console.log(courseInfo);
​
/*
3. Add a new key/value pair to the courseInfo object
*/
​
//put your code here
console.log(courseInfo);
​
​
/*
4. Iterate over the courseInfo object and print the key/value pairs
*/
​
//put your code here
​
/*
5. Delete a key/value pair in the courseInfo object
*/
​
//put your code here
console.log(courseInfo);
​
/*
6. Iterate through an array of objects and print each object (in this case the objects are coordinate positions)
*/
​
let positions = [
    {x: 200, y: 100},
    {x: 200, y: 200},
    {x: 200, y: 300}
];

```

<details><summary><h3>Solutions</h3></summary>

```js
// 1. Write a method that verifies whether an argument is a plain object, not an array or null
​
function checkObject(element) {
  return typeof element === 'object' && !Array.isArray(element) && element !== null;
}
​
// 2. Update a value in the courseInfo object
​
courseInfo.room = 'SIEG 329'; // or courseInfo['room'] = 'SIEG 329'
​
// 3. Add a key/value pair to the courseInfo object
​
courseInfo.quarter = 'Winter'; // or courseInfo['quarter'] = 'Winter'
​
// 4. Iterate over the courseInfo object and print the key/value pairs
​
// Starting from ECMAScript 2017 we can use the Object.entries method.
// Object.entries() method returns an array of key-value pairs which helps us use the forEach() method -- a way of iterating over elements of an array.
​
Object.entries(courseInfo).forEach(([key, value]) => {
  console.log(`${key}: ${value}`);
});
​
// you can also do this using a for loop
for (var key in courseInfo) {
  console.log(`${key}: ${courseInfo[key]}`);
}
​
// 5. Delete a key/value pair in the courseInfo object
​
delete courseInfo.room;
​
// 6. Iterate through an array of objects and print each object
​
for (var i = 0; i < positions.length; i++) {
    var position = positions[i];
    console.log(`${position.x}: ${position.y}`);
}
​
```

</details>
