# Introduction to Java Script
## Data Types
- alert(2+5);
- alert("Hello");
- typeof(3);
    - "number"
- typeof("Pratyush");
    - "string"
- typeof(true);
    - "boolean"
## variables
```
var myName = "Pratyush";
var yourName = prompt ("What is your name?") ;
alert ("My Name is " + myName + ". Welcome to our Website " + yourName + "!" );

```
![alt text](image-4.png)
![alt text](image-6.png)
![alt text](image-5.png)
## JavaScript Variables exercise
```
function test() {
    var a = "3";
    var b = "8";
    
var c = a;
a = b ;
b = c ;

alert("a");
alert("b");
    console.log("a is " + a);
    console.log("b is " + b);
}
 ```
## Strings length and Retrieving the Number of Characters
```
var tweet = prompt ("Compose your tweet") ;
alert ("You have written " + tweet.length + " Characters you have " + (140 - tweet.length) + " characters remaining" );
```
![alt text](image-7.png)
![alt text](image-8.png)

## Slicing
```
var tweet = prompt ("Compose your tweet") ;
var tweetUnder140 = tweet.slice(0,140);
alert(tweetUnder140)
       OR
var tweet = prompt ("Compose your tweet") ;
alert(tweet.slice(0,140));
```
![alt text](image-9.png)
![alt text](image-10.png)

## Changing Case in Text 
```
var name = prompt("What is your Name");
var firstChar = name.slice(0,1);
var upperCaseFirstChar = firstChar.toUpperCase();
var restOfTheName = name.slice(1,name.length);
restOfTheName =restOfTheName.toLowerCase();
var capitalisedName = upperCaseFirstChar + restOfTheName;
alert("Hello, " + capitalisedName) ;

```
![alt text](image-11.png)
![alt text](image-12.png)

## Basic Arithimetic and the Modulo Operator in JavaScript
```
var dogAge = prompt ("How old is your dog?");
var humanAge = ((dogAge - 2) * 4) + 21;
alert("Your dog is " + humanAge + " years old in human years");

```
![alt text](image-13.png)
![alt text](image-14.png)

## Increment and Decrement

```
var x = 3;
x++ ;
console.log(x);

var x = 3;
x-- ;
console.log(x);
```

## Function : Creating and Calling Funtion
```
function getMilk () {
    console.log ("leaveHouse");
    console.log ("moveRight");
    console.log ("moveRight");
    console.log ("moveup");
    console.log ("moveLeft";)
    console.log ("moveup");
    console.log ("enterHouse");
}
getMilk();

```

## Output and return value
```
function getMilk(Money, costPerBottles) {   
  console.log("leaveHouse");
  console.log("moveRight");
  console.log("moveRight");
  console.log("moveUp");
  console.log("moveUp");
  console.log("moveUp");
  console.log("moveUp");
  console.log("moveRight");
  console.log("moveRight");
  console.log("buy " + calcBottles(Money, costPerBottles) + " bottles of milk")
  console.log("moveLeft");
  console.log("moveLeft");
  console.log("moveDown");
  console.log("moveDown");
  console.log("moveDown");
  console.log("moveDown");
  console.log("moveLeft");
  console.log("moveLeft");
  console.log("enterHouse");
  return calcChange(Money, costPerBottles);   // remainder of this division 

}
function calcBottles (StartingMoney, costPerBottles)
{
  var numberOfBottles = Math.floor(StartingMoney / costPerBottles);
  return numberOfBottles;
}
function calcChange (startingAmount, costPerBottles){
  var change = startingAmount % costPerBottles ;
  return change;
}
console.log ("Hello Sir/Ma'am, here is your " + getMilk(10,4) +" change.");

```
![alt text](image-15.png)

## Life in weeks coding exercise 
```
function lifeInWeeks(age) {

 
   var remainingYears = 90 - age;
   var days = remainingYears * 365;
   var weeks = remainingYears * 52;
   var months = remainingYears * 12;

    
    console.log("You have " + days + " days, " + weeks + " weeks, and " + months + " months left.");
}

```

## Bmi Calculator Challange
```
function bmiCalculator(weight, height){
 var bmi = weight /(height * height);
    return Math.round(bmi);
}
var bmi = bmiCalculator(65,1.8);

```
# Intermediate JavaScript
## Random number generator in JavaScript (Building a love calculator)
```
alert("Calculate your love percentage ❤️");
var name1 = prompt("Name of the first Person");
var name2 = prompt("Name of the second Person");

  var n = Math.random();
  n = n * 100;
  n = Math.floor(n) + 1;
alert(n + "% ❤️"); 

```
![alt text](image-16.png)
![alt text](image-17.png)
![alt text](image-18.png)
![alt text](image-19.png)

## Control Statement : using if-else conditional and logic
![alt text](image-16.png)
![alt text](image-17.png)
![alt text](image-18.png)
![alt text](image-20.png)

### If less than 70 then,
![alt text](image-16.png)
![alt text](image-17.png)
![alt text](image-18.png)
![alt text](image-21.png)

## Bmi calculator Advanced Exercise
```
function bmiCalculator (weight, height) {
    var interpretation = weight / (height*height);
    
    if(interpretation < 18.5 ){
        return "Your BMI is " + interpretation + ", so you are underweight.";
    
    }
    else if(interpretation >= 18.5 && interpretation <= 24.9){
       return "Your BMI is " + interpretation + ", so you have a normal weight.";
            

    }
    else {
       return "Your BMI is " + interpretation + ", so you are overweight.";
           

    }
    
    return interpretation;
}

```

## Leap Year Challenge Exercise 
```
function isLeap(year) {
    
        if ( year % 4 === 0 ){
        if( year % 100 === 0 ){
            if( year % 400 === 0 ){
                return "Leap year."
            }else{
                 return "Not leap year."
            }
            
        }else{
            return "Leap year."
        }
    }else{
        return "Not leap year."
    }


}
```
## Working with Array 
```
var guestList = ("Ram, Bahun , Hari, Sita, Gita Rita");
var guestName = prompt("What is your name?"); 
if (guestList.includes(guestName)) {
    alert("Welcome");
}
else {
    alert("Sorry, May be next time");
}
```
## Adding elements and Intermediate Array techniques
```
var output = [];
var count = 1;

function fizzBuzz() {
    if (count % 3 === 0 && count % 5 === 0) {
        output.push("FizzBuzz");
    } 
    else if (count % 3 === 0) {
        output.push("Fizz");
    }
    else if (count % 5 === 0) {
        output.push("Buzz");
    } else {
        output.push(count);
    }
    count++;
    console.log(output);
}

```
![alt text](image-22.png)
![alt text](image-23.png)

## Who's Buying lunch challenge
```
function whosPaying(names) {
   
        var numberOfPeople = names.length;
        var randomPersonPosition = Math.floor(Math.random() * numberOfPeople);
        var randomPerson = names[randomPersonPosition];
        return randomPerson + " is going to buy lunch today!"
    }
    
    whosPaying(["Angela", "Ben", "Jenny", "Michael", "Chloe"]);
```
![alt text](image-24.png)
## Control statement: While loop
```
var numberOfBottles = 99
while (numberOfBottles >= 89) {
    var bottleWord = "bottle";
    if (numberOfBottles === 89) {
        bottleWord = "bottles";
    } 
    console.log(numberOfBottles + " " + bottleWord + " of beer on the wall");
    console.log(numberOfBottles + " " + bottleWord + " of beer,");
    console.log("Take one down, pass it around,");
	numberOfBottles--;
    console.log(numberOfBottles + " " + bottleWord + " of beer on the wall.");
}
```
![alt text](image-25.png)
![alt text](image-26.png)

## Control statement: For Loop
```
var output = [];

function fizzBuzz() {
    for (var count = 1; count < 101; count++ ) {
        if (count % 3 === 0 && count % 5 === 0){
            output.push ("fizzBuzz");
        }
        else if (count % 3 === 0){ 
        output.push("Fizz");
    }
    else if (count % 5 === 0) {
        output.push("Buzz");
    } else {
        output.push(count);
    }
    }
    console.log(output);
        
}

```
![alt text](image-27.png)

## Reverse an array without using .reverse()
```
function arrayExercise (Arr){
var array = [1, 2, 3, 4, 5];
var output = [];
for (var i = array.length - 1; i >= 0; i--) {
    output.push(array[i]);
}
console.log(output);
}
        OR
var array = [1, 2, 3, 4, 5];
function reverse(arr) {
for (var start = 0, end = array.length - 1; start < end; start++, end--) {
    var temp = array[start];
    array[start] = array[end];
    array[end] = temp;
}
console.log(array);
}
```
## Find the second largest number in an array

```
var array = [10, 5, 8, 20, 3];
var first = -Infinity;
var second = -Infinity;
for (var i = 0; i < array.length; i++) {
    if (array[i] > first) {
        second = first;
        first = array[i];
    } else if (array[i] > second && array[i] !== first) {
        second = array[i];
    }
}
console.log("Second largest number is:", second);
```

## Remove duplicates from an array
```
var arr =[1,2,3,3,4,5,5,6,10,10];
const removeDuplicate = (array)=> {
    return [...new Set (array)]
}
console.log (removeDuplicate(arr))
```

## Group array items by a property (e.g., group people by age)
```

const people = [
  { name: "Ram", age: 21 },
  { name: "Hari", age: 25 },
  { name: "Carlos", age: 21 },
  { name: "Diya", age: 25 },
  { name: "Ayush", age: 30 }
];
const groupedByAge = people.reduce((group, person) => {
  const age = person.age;
  if (!group[age]) {
    group[age] = [];
  }
  group[age].push(person);
  return group;
}, {});
```

## Explain and create a closure
```
function outerFunction (){
    const outerVariable = "It is outerFunction ";
    function innerFunction (){
        console.log(outerVariable);
    }
    return innerFunction;
}
    const resultFunction = outerFunction();
    resultFunction();
```

## Create a function that returns a counter

```
function createCounter(n) {
	
	let count = n-1;
	function counter(){	
	return count+=1 ;
	}
	return counter;
}
const counter = createCounter(10);
console.log(counter());
console.log(counter());
console.log(counter());
const secondCounter = createCounter(42);
console.log(secondCounter());
console.log(secondCounter());
```

## Factorial using recursion

```
 function factorial (n) {
    if (n===0 || n === 1){
        return 1 ;
}
return n * (factorial(n - 1));
}
console.log(factorial(5));
```
