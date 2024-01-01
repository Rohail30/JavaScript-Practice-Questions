# Basic JavaScript coding questions

```jsx
//Question:1 Function to find the maximum number in an array

// Function to find the maximum number in an array
function findMaxNumber(arr) {
  // Check if the array is not empty
  if (arr.length === 0) {
    return "Array is empty";
  }

  // Assume the first element is the maximum
  let max = arr[0];

  // Iterate through the array
  for (let i = 1; i < arr.length; i++) {
    // Update max if the current element is greater
    if (arr[i] > max) {
      max = arr[i];
    }
  }

  // Return the maximum number
  return max;
}

// Example usage
const numbers = [12, 5, 27, 8, 15, 3];
const maxNumber = findMaxNumber(numbers);
console.log("The maximum number is:", maxNumber);
```

```jsx
//Question:2 Function to check if a string is a palindrome

// Function to check if a string is a palindrome
function isPalindrome(str) {
  // Convert the string to lowercase
  str = str.toLowerCase();

  // Remove non-alphanumeric characters using regular expression
  const alphanumericStr = str.replace(/[^a-z0-9]/g, '');

  // Compare the original string with its reverse
  return alphanumericStr === alphanumericStr.split('').reverse().join('');
}

// Example usage
const testString1 = "level";
const testString2 = "Hello, World!";

console.log(`${testString1} is a palindrome: ${isPalindrome(testString1)}`);
console.log(`${testString2} is a palindrome: ${isPalindrome(testString2)}`);
```

```jsx
//Question:3 Function to filter even numbers from an array

// Function to filter even numbers from an array
function filterEvenNumbers(numbers) {
  // Use the filter method to create a new array with only even numbers
  const evenNumbers = numbers.filter(number => number % 2 === 0);
  
  return evenNumbers;
}

// Example usage
const numbersArray = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const evenNumbersArray = filterEvenNumbers(numbersArray);

console.log("Original Array:", numbersArray);
console.log("Array with Even Numbers:", evenNumbersArray);
```

```jsx
//Question:4 Function to calculate the factorial of a number

// Function to calculate the factorial of a number
function calculateFactorial(number) {
  // Check if the number is non-negative
  if (number < 0) {
    return "Factorial is not defined for negative numbers.";
  }

  // Base case: factorial of 0 is 1
  if (number === 0 || number === 1) {
    return 1;
  }

  // Recursive case: n! = n * (n-1)!
  return number * calculateFactorial(number - 1);
}

// Example usage
const inputNumber = 5;
const result = calculateFactorial(inputNumber);

console.log(`The factorial of ${inputNumber} is: ${result}`);
```

```jsx
//Question:5 Function to generate Fibonacci sequence up to a given number of terms

// Function to generate Fibonacci sequence up to a given number of terms
function generateFibonacciSequence(terms) {
  // Check if the number of terms is valid
  if (terms <= 0) {
    return "Number of terms should be greater than 0.";
  }

  // Initialize an array to store the Fibonacci sequence
  const fibonacciSequence = [0, 1];

  // Generate the Fibonacci sequence
  for (let i = 2; i < terms; i++) {
    const nextTerm = fibonacciSequence[i - 1] + fibonacciSequence[i - 2];
    fibonacciSequence.push(nextTerm);
  }

  return fibonacciSequence;
}

// Example usage
const numberOfTerms = 8;
const fibonacciSequence = generateFibonacciSequence(numberOfTerms);

console.log(`Fibonacci sequence up to ${numberOfTerms} terms:`, fibonacciSequence);
```

```jsx
//Question:6 Function to convert a string to title case

// Function to convert a string to title case
function toTitleCase(inputString) {
  // Split the string into words
  const words = inputString.split(' ');

  // Capitalize the first letter of each word
  const titleCaseWords = words.map(word => word.charAt(0).toUpperCase() + word.slice(1));

  // Join the words back into a string
  const titleCaseString = titleCaseWords.join(' ');

  return titleCaseString;
}

// Example usage
const inputString = "hello world example";
const titleCaseResult = toTitleCase(inputString);

console.log(`Original string: ${inputString}`);
console.log(`Title case string: ${titleCaseResult}`);
```