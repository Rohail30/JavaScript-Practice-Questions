# Advance JavaScript coding questions

```jsx
//Question:1 Write a function that takes an array of objects and a key, and returns a new array sorted based on the values of that key in ascending order.

function sortByKey(arr, key) {
  return arr.slice().sort((a, b) => a[key] - b[key]);
}

// Example usage:
const arrayOfObjects = [
  { name: 'Alice', age: 30 },
  { name: 'Bob', age: 25 },
  { name: 'Charlie', age: 35 }
];

const sortedArray = sortByKey(arrayOfObjects, 'age');
console.log(sortedArray);
```
