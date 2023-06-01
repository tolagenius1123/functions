# Introduction to Functions 

Today we will be diving into the world of functions in JavaScript. Having gone through the basics of JavaScript from data types, conditional statements, and variables, we need functions to compute them, change them, and do something with them. 

This lesson is categorized into three segments for every concept of function we are going to learn, we will first start with the explanations, then move to demonstrations, where I will be showing you how to implement what you learnt before we finally move to exercises, here you will be given classwork to help you solidify the concept of functions you just learnt.
  
 Shall we begin? you can fasten your seat belt 🚀🚀🚀
</br>
</br>

## Section 1: What are functions ?
There is no way we can learn about functions without first defining them. We can think of functions as small computer programs although you may not realize it, you have been using functions this entire time. Functions allow us to write code that will be used over and over again, keeping our code DRY. 
DRY is a principle that ensures you do not repeat yourself when writing programs.

A function is a group of reusable code which can be called anywhere in your program. This eliminates the need of writing the same code again and again. Functions are the 
basic building block of JavaScript. Functions allow us to encapsulate a block of code and reuse it multiple times.

### Anatomy of a Function
```
function functionName () {}

```
A function will start with the function keyword. This tells whatever is running your program that what follows is a function and to treat it as such. 
After that comes the name of the function. We like to give functions names that describe what they do. Then comes an open and a close parenthesis which usually takes in a parameter but not in all cases, we will discuss this later in details. And finally, open and close brackets. In between these brackets is where all of our function code will go.

### Function Declaration 
To create a function we can use a function declaration.

It looks like this:
```
function showMessage () {
  console.log("Hello World");
}

showMessage();

//Output
Hello World
```
In this example, we declare a function showMessage and set it up to console.log 'Hello World'. We can then see that in order to run this function, we need to write or invoke its name with the parentheses after it. This is the syntax to run a function. A function always needs parentheses to run.

The call showMessage() executes the code of the function and if we were to call the function twice, we will see the message two times.
This example clearly demonstrates one of the main purposes of functions: to avoid code duplication. If we ever need to change the message or the way it is shown, it’s enough to modify the code in one place: the function which outputs it.

#### Exercise 1: 
Write a function that displays your fullname to the console and call the function after declaring it.
</br>
</br>
</br>
</br>
</br>

## Section 2: Passing Data into Functions

As mentioned before, a big reason we use functions is code re-use. We are always looking for ways to keep our code DRY (Don’t Repeat Yourself). Because of this, functions allow us to pass data into them for use inside the function. We can declare little function variables called parameters and pass that data in when we call the function (the data are then called arguments).

### Parameters
A function parameter will represent the data we pass into a function, for use in the function. Essentially when we write a function we assign the data variable names, even without knowing what the data will be. We set these variables inside of the parentheses when we write the function. There is no limit to the amount of parameters we can include in a function, but each variable name must be separated by a comma. We can then use these variables within our function just as we would any other variable.

```
function myFunction (parameter1, parameter2) {
  //we can use parameter1 and parameter2 just like a variable in this function
}

```
### Arguments
Once we have our parameters set up in our function, we can now pass data into the function. In order to do this, we will use the parentheses we write when we call the function. We call these pieces of data arguments. arguments can be ANY data type (string, number, Boolean, object, array, even other functions!). Unlike other languages, JavaScript does not require us to set the data type when we write the function, although you should make an effort to understand what type of data will be coming into the function (and if you are using pre-built functions, you should know what data type that function expects).

To use an argument, just put the data in the function call parentheses like so:

```
// function declaraction
function printName (name) {
  console.log(name);
}

//function call
printName("Tolani");
printName("James");

//output
Tolani
James
```

If you have more than one parameter, you will use more than one argument:

```
// function declaraction
function printName (name, age) {
  console.log("my name is " +name+ " and I am " +age+ " years old.");
}

//function call
printName("Tolani", 100);

//output
My name is Tolani and I am 100 years old.

```
Arguments will always line up with parameters in order, so the first argument will be the first parameter, and etc.
If an argument is not given for a parameter, the parameter will be equal to undefined. The difference between a parameter and arguement is that a parameter is a placeholder for the data while an argument is the actual data being passed to the function when calling it.

#### Exercise 2: 
Write a function that takes in 3 parameters of different data types, concatenates them together and displays it to the console.
</br>
</br>
</br>
</br>
</br>
## Section 3: Scope
Scope is defined as what variables we currently have access to and where. So far in this course, we have been working in Global scope, in that we can access any variable we have created, anywhere in our code. There are a couple different levels of scope: you may have heard of block level scope (used in if statements and for loops) in which a variable using either let or const is only available within the statement or loop.

### Function Level Scope
Functions have something similar, known as function scope. Function scope allows us to create variables inside of functions, that are essentially private to that function. We can not reach into a function from the outside and get access to these variables. But we are free to use these variables anywhere within our function. Conversely, we do have access to variables outside of the function. It is a one-way street. Functions can reach out and grab variables outside of their scope, but we can not reach into a function to get a variable.

```
const var1 = 'Hello';

function showMessage() {
  const var2 = 'World!'; // declare a local variable
  console.log(var1); //Hello
  console.log(var2); //World
}

showMessage();
console.log(var1); //Hello
console.log(var2); //var2 is not defined
```

### Global variables
Variables declared outside of any function, such as the outer userName in the code below, are called global. Global variables are visible from any function (unless shadowed by locals).
It’s a good practice to minimize the use of global variables. Modern code has few or no globals. Most variables reside in their functions. Sometimes though, they can be useful to store project-level data.

```
let userName = 'John';

function showMessage() {
  let userName = "Bob"; // declare a local variable

  let message = 'Hello, ' + userName; // Bob
  alert(message);
}

// the function will create and use its own userName
showMessage();

alert( userName ); // John, unchanged, the function did not access the outer variable
```

</br>
</br>
</br>

### Local variables

A variable declared inside a function is only visible inside that function.

For example:

```
function showMessage() {
  let message = "Hello, I'm JavaScript!"; // local variable

  alert( message );
}

showMessage(); // Hello, I'm JavaScript!

alert( message ); // <-- Error! The variable is local to the function
```

### The return Statement

We will not console.log everything that comes out of a function. Most likely we will want to return something. There is one way we can access data from within a function. In fact, it is the only way for us to get ANY data from a function, and that is to use the keyword return. Think of the return statement as the only way for data to escape a function. 
Nothing other than what is returned can be accessed outside of the function. Also note that when a function hits a return statement, the function immediately stops what it is doing and returns.

We can also assign the value of a return statement to another variable, and we will now have access to the data returned from the function.

```
function sum(a, b) {
  return a + b;
}

let result = sum(1, 2);
alert( result ); // 3
```
The directive return can be in any place of the function. When the execution reaches it, the function stops, and the value is returned to the calling code (assigned to result above).

There may be many occurrences of return in a single function. For instance:

```
function checkAge(age) {
  if (age >= 18) {
    return true;
  } else {
    return confirm('Do you have permission from your parents?');
  }
}

let age = prompt('How old are you?', 18);

if ( checkAge(age) ) {
  alert( 'Access granted' );
} else {
  alert( 'Access denied' );
}
```
It is possible to use return without a value. That causes the function to exit immediately.

For example:

```
function showMovie(age) {
  if ( !checkAge(age) ) {
    return;
  }

  alert( "Showing you the movie" ); // (*)
  // ...
}
```
Note: We will never be able to have access to the actual variable created in the function. We will only have access to the data that variable was assigned to.

#### Exercise 3: 
Write a function called isPrime that takes a positive integer as an argument and returns true if it is a prime number, and false otherwise. A prime number is a number greater than 1 that has no positive divisors other than 1 and itself.
<br/>
<br/>
<br/>
<br/>
## Summary
- A function declaration looks like this:
  ```
  function name(parameters, delimited, by, comma) {
    /* code */
  }
  ```
- Values passed to a function as parameters are copied to its local variables.
- A function may access outer variables. But it works only from inside out. The code outside of the function doesn’t see its local variables.
- A function can return a value. If it doesn’t, then its result is undefined.
- To make the code clean and easy to understand, it’s recommended to use mainly local variables and parameters in the function, not outer variables.
- It is always easier to understand a function which gets parameters, works with them and returns a result than a function which gets no parameters, but modifies outer       variables as a side effect.

- Function naming:
  - A name should clearly describe what the function does. When we see a function call in the code, a good name instantly gives us an understanding what it does and             returns.
  -  A function is an action, so function names are usually verbal.
  - There exist many well-known function prefixes like create…, show…, get…, check… and so on. Use them to hint what a function does.
  - Functions are the main building blocks of scripts. Now we’ve covered the basics, so we actually can start creating and using them. But that’s only the beginning of the      path. 
