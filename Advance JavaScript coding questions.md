# Advance JavaScript coding questions

```jsx
//Question:1 Closures and Scope

function outer() {
  var x = 10;

  function inner() {
    console.log(x);
  }

  return inner;
}

var closureFunction = outer();
closureFunction(); // What will be logged and why?

```

```jsx
//Question:2 Promises and Async/Await

function delay(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

async function asyncFunction() {
  console.log("Start");

  await delay(2000);
  
  console.log("End");
}

asyncFunction(); // What will be logged and in what order?


```

```jsx
//Question:3 Prototypes and Inheritance

function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function() {
  console.log(this.name + ' makes a sound');
};

function Dog(name, breed) {
  Animal.call(this, name);
  this.breed = breed;
}

Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;

Dog.prototype.bark = function() {
  console.log(this.name + ' barks');
};

var myDog = new Dog('Buddy', 'Golden Retriever');
myDog.speak(); // What will be logged?
myDog.bark();  // What will be logged?


```

```jsx
//Question:4 Event Handling

const button = document.getElementById('myButton');

button.addEventListener('click', function() {
  console.log('Button clicked');
});

button.click();

```

