# Puzzles

```jsx
//Question:1 Check if four points form a square

function distanceSquared(x1, y1, x2, y2) {
    return Math.pow(x2 - x1, 2) + Math.pow(y2 - y1, 2);
}

function isSquare(x1, y1, x2, y2, x3, y3, x4, y4) {
    const distances = [
        distanceSquared(x1, y1, x2, y2),
        distanceSquared(x1, y1, x3, y3),
        distanceSquared(x1, y1, x4, y4),
        distanceSquared(x2, y2, x3, y3),
        distanceSquared(x2, y2, x4, y4),
        distanceSquared(x3, y3, x4, y4)
    ];

    // Sort the distances to check for equality
    distances.sort((a, b) => a - b);

    // Check if the sides are equal and the diagonals are equal
    return (
        distances[0] > 0 &&
        distances[0] === distances[1] &&
        distances[1] === distances[2] &&
        distances[2] === distances[3] &&
        distances[4] === distances[5] &&
        2 * distances[0] === distances[4]
    );
}

// Take user input
const x1 = parseInt(prompt("Enter x1:"));
const y1 = parseInt(prompt("Enter y1:"));
const x2 = parseInt(prompt("Enter x2:"));
const y2 = parseInt(prompt("Enter y2:"));
const x3 = parseInt(prompt("Enter x3:"));
const y3 = parseInt(prompt("Enter y3:"));
const x4 = parseInt(prompt("Enter x4:"));
const y4 = parseInt(prompt("Enter y4:"));

// Check if the points form a square
const result = isSquare(x1, y1, x2, y2, x3, y3, x4, y4);
console.log(result);  // It will log true or false based on user input
```

```jsx
//Question:2 Day of the week
function getDayOfWeek(d, m, y) {
    const dateObject = new Date(y, m - 1, d);
    const dayOfWeekNumber = dateObject.getDay();
    const daysOfWeek = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
    const dayOfWeekString = daysOfWeek[dayOfWeekNumber];
    return dayOfWeekString;
}

// Get user input
const day = parseInt(prompt("Enter day:"));
const month = parseInt(prompt("Enter month (1-12):"));
const year = parseInt(prompt("Enter year:"));

// Check if the inputs are valid before proceeding
if (isNaN(day) || isNaN(month) || isNaN(year)) {
    console.log("Invalid input. Please enter valid numbers.");
} else {
    const result = getDayOfWeek(day, month, year);
    console.log(`The day of the week for ${month}/${day}/${year} is: ${result}`);
}
```

```jsx
//Question:2 Angle between hour and minute hand

function calculateClockAngle(hours, minutes) {
    // Ensure the inputs are within valid range
    if (hours < 0 || hours > 12 || minutes < 0 || minutes > 59) {
        return "Invalid input. Please enter valid hours (0-12) and minutes (0-59).";
    }

    // Calculate the angle between hour and minute hands
    const angle1 = Math.abs(0.5 * (60 * hours - 11 * minutes));
    const angle2 = 360 - angle1;

    // Print the floor of the result angles
    console.log("Angle 1: " + Math.floor(angle1));
    console.log("Angle 2: " + Math.floor(angle2));
}

// Get user input
const hours = parseInt(prompt("Enter hours (0-12):"));
const minutes = parseInt(prompt("Enter minutes (0-59):"));

// Call the function with user input
calculateClockAngle(hours, minutes);
```