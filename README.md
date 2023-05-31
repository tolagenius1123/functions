# Introduction to Functions 

Today we will be diving into the world of functions in JavaScript. Having gone through the basics of JavaScript from data types, conditional statements, and variables, we need functions to compute them, change them, and do something with them. 

This lesson is categorized into three segments for every concept of function we are going to learn, we will first start with the explanations, then move to demonstrations, where I will be showing you how to implement what you learnt before we finally move to exercises, here you will be given classwork to help you solidify the concept of functions you just learnt.
  
 Shall we begin? you can fasten your seat belt 🚀🚀🚀

## What are functions ?
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




