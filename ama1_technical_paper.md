# AMA Technical Paper-1

### 1. What is the difference between (==) and (===) operator ?

  * '==' compares only values and it performs type conversion if needed and returns true.
  * '===' does not perform type conversion and returns true only if both operands are of same value and same data type.

### 2. Console.log(typeof []) is equals to 'object' why?

- In javaScript 'typeof([])' returns 'object, because arrays are special type of objects in JavaScript. Arrays in JavaScript inherit from 'Array.prototype'.

### 3. What are the disadvantages of using closure?

- Closures in JavaScript have multiple disadvantages :
    * Closures may lead to increased memory usage.
    * They can lead to reduce the performance overhead compared to other functions.
    * Closures can access variables from their outer function's scope.
    * They can make difficulty in understanding code.

### 4. Why using global variables are bad in js ?

- Global variables can be modified from anywhere in the code, and using global variables may lead to naming conflicts.

### 5. How to extract certain properties from an array of objects to create a new array?

- We can use various JavaScript array methods like map or reduce.

### 6.Difference between charAt() and at() method in js?

* chatrAt(): This method only works with strings in JavaScript, and it doesn't accept negative values as arguments.
* at(): The at() method works with any iterable object,and it accepts negative values as arguments.

### 7. How to reset initial or 1st commit in git, if its possible?
 
- We cannot reset the initial commit, so that we can create a new branch and commit from the start.

### 8. Console.log(typeof []) returns 'object', then why can not we use (.) operator in array to access its values just like objects, where we use (.) operator in objects for accessing key and values?

- Although arrays are special type of objects, we cannot access its values using (.) operator, because arrays contains indexed elements, and arrays have length property.

### 9. Why 'forEach' loop skips 'not defined' whereas 'for' loop gives 'undefined'?

- For loop iterates over indices so that if the loop doesn't find element it returns undefined, where as forEach iterates over element.

### 10. How can we mimic the action Array.splice and 'Array.slice' on objects?

- We can implement similar behaviors like Array.splice() and array.slice() using a combination of object spread syntax (...), Object.assign(), and other object manipulation techniques available in JavaScript.

### 11. What is "Callback Hell" problem and how to avoid it?

- The "Callback Hell" is a situation in JavaScript where deeply nested callbacks make the code difficult to read, and understand. To avoid this problem we can use promises or Async?Await.

### 12. Why "Hello" is also printing ? when we have exported array('ar') only!

  /file1.js
  let ar = [1,2,3];
  console.log("Hello");
  module.exports.ar = ar;
  
  //file2.js
  const {ar} = require('file1.js');
  let print = ar;
  console.log(print);
  
  Output: "Hello" 
          [1,2,3]

- Answer: We can limit this behavior by creating a function and call it when needed.
