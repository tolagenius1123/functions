# Functions Lesson Plan

This markdown file outlines the structure for a 3-hour lesson on functions. The lesson plan follows the given format: explanations, demonstrations, exercises, and then revisiting the explanations. The goal is to provide a clear understanding of functions and their usage in JavaScript.

## 1. Explanations

### 1.1 Introduction to Functions

-   Definition of a function
-   Why functions are important in programming
-   Benefits of using functions
-   Understanding the concept of modular and reusable code

### 1.2 Function Syntax and Declaration

-   Syntax for declaring a function
-   Function name and parameters
-   Function body and return statement
-   Discussing the concept of function scope and local variables

### 1.3 Function Invocation

-   How to invoke (call) a function
-   Passing arguments to functions
-   Returning values from functions
-   Discussing the concept of function stack and call stack

### 1.4 Function Types

-   Built-in functions vs. user-defined functions
-   Discussing the differences between function declarations and function expressions
-   Introducing anonymous functions and arrow functions

## 2. Demonstrations

### 2.1 Simple Function Declaration and Invocation

```javascript
// Demonstrate a simple function declaration and invocation
function greet(name) {
	return "Hello, " + name + "!";
}

const result = greet("John");
console.log(result); // Output: Hello, John!
```

### 2.2 Function with Multiple Parameters and Return Values

```javascript
// Demonstrate a function with multiple parameters and return values
function calculateSum(a, b) {
	const sum = a + b;
	return sum;
}

const result = calculateSum(5, 10);
console.log(result); // Output: 15
```

### 2.3 Function Expressions and Arrow Functions

```javascript
// Demonstrate function expressions and arrow functions
const multiply = function (a, b) {
	return a * b;
};

const divide = (a, b) => a / b;

console.log(multiply(3, 4)); // Output: 12
console.log(divide(10, 2)); // Output: 5
```

## 3. Exercises

### Exercise 1: Temperature Conversion

Write a function called `convertToFahrenheit` that takes a temperature in Celsius as an argument and returns the temperature in Fahrenheit. Use the formula: `F = (C * 9/5) + 32`.

### Exercise 2: Calculate Factorial

Write a function called `calculateFactorial` that takes a positive integer as an argument and returns its factorial. The factorial of a number `n` is the product of all positive integers less than or equal to `n`.

### Exercise 3: Check Prime Number

Write a function called `isPrime` that takes a positive integer as an argument and returns `true` if it is a prime number, and `false` otherwise. A prime number is a number greater than 1 that has no positive divisors other than 1 and itself.

## 4. Revisiting Explanations

Revisit the explanations provided in section 1 to reinforce the understanding of function concepts. Encourage students to ask questions and clarify any doubts they may have.

---

This markdown file presents a structured lesson plan for teaching functions in JavaScript. The theory section explains the fundamental concepts, the demonstration section provides code examples, and the exercise section offers practical problems for students to solve. Revisiting the explanations at the end reinforces the understanding of the covered material.
