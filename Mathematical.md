# Java Script Practice questions

```jsx
//Question-1: **[Armstrong Number](https://www.geeksforgeeks.org/problems/armstrong-numbers/0)?

function isArm(x){
    var str = x.toString();
    var digitArray = []; 
    for (var i = 0; i < str.length; i++) {
        var digit = parseInt(str.charAt(i), 10);
        digitArray[i]=digit
    }
    var result = 0;
    var loop=0;
    var j=1;
    while(loop==0 && j<10){
        for(let i=0; i< digitArray.length; i++){
            result = result+(digitArray[i]**j)
        }
        if(x==result){
            loop=1;
            return true
        }
        result=0
        j++
    }
    if(loop==0){
        return false
    }
}

var input = prompt("Enter any number between 0-1000\n");
if (input>=0 && input<=9){
    console.log(input+" is an Armstrong number")
} else if(input<0){
    console.log(input+" is not an Armstrong number")
} else if(input>9){
    if(isArm(input)){
        console.log(input+" is an Armstrong number")
    } else{
      console.log(input+" is not an Armstrong number") 
    }
} else if(input >1000){
    console.log("out of range")
}**

```

```jsx
//Question-2: **[Print the Kth Digit](https://www.geeksforgeeks.org/problems/print-the-kth-digit/0)
var x = prompt("Enter number\n")
var str = x.toString();
var arr = []
for(let i=0; i<str.length; i++){
    var digit = parseInt(str.charAt(i), 10);
    arr.push(digit)
}
for(let i=0; i<arr.length; i++){
    console.log(arr[i]+" is at "+i+" postion")
}**
```

```jsx
//Question-3:  **[Prime Number](https://www.geeksforgeeks.org/problems/prime-number/0)

function isPrime(x){
    var count = 0;
    for(let i=0; i<x; i++){
        if(x%i==0){
            count++
        }
    }
    if(count==1){
        return true
    }else{
        return false
    }
}

var input = prompt("Enter a number\n");
if(input<2){
    console.log(input+" is not a primary number")
}else if(input>=2){
    if(isPrime(input)){
        console.log(input+" is a primary number")
    } else{
        console.log(input+" is not a primary number")
    }
}**
```

```jsx
//Question-3:  **[Sum of all prime numbers between 1 and N](https://www.geeksforgeeks.org/problems/sum-of-all-prime-numbers-between-1-and-n/0)**.

function isPrime(x){
    var count = 0;
    for(let i=0; i<x; i++){
        if(x%i==0){
            count++
        }
    }
    if(count==1){
        return true
    }else{
        return false
    }
}

var input = prompt("Enter a maximum number, and I will calculate the sum of all prime numbers up to that maximum\n");

var sum = 0
for(let i=0; i<=input; i++){
    if(isPrime(i)){
        sum=sum+i
    }
}

console.log(sum)
```