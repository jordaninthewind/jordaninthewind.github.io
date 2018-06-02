---
layout: post
title:      "The Joy of Hoisting and Scope in Javascript"
date:       2018-06-02 16:15:19 +0000
permalink:  the_joy_of_hoisting_and_scope_in_javascript
---



### What is scope and why is it important?

 In Javascript, scope affects where information is available and thus what information you can reference or update when running programs. We're primarily concerned with two types of scope: the global scope, which is outside of functions and in which functions are called, and the function scope, which isolates a space for more central processes that happen within the global execution.

 To oversimplify, information that is 'globally scoped' is available throughout the application. Variable values can be accessed and updated provided that a variable with the same name has not been declared within the function space. When declaring variables with 'var', the pre-ES2015 standard variable declaration, whatever name was assigned to the variable would be held in memory and would remain available in memory until called or updated.
 
 Another important scope level is 'block', where declarations are made within if...else or for... statements. 'Var' variables that are declared within the block are available outside of the block, in contrast with the function scope. This is because they are brought to the top of their function scope and can persist outside of the immediate block.


### What is hoisting and why is it important?

 Hoisting is not something that we do, as programmers, it's a biproduct of how the JS compiler processes data. When code is run, variables throughout the application are mapped and brought to the top of their respective scope, globally scoped variables are brought to the top of the document, and variables within a function will be brought to the top of that function. Because of this, variable declarations can be made anywhere, but the values are not assigned until later.
	
 In most languages, if these variables were called without a value, the program would fail because this is an error. Javascript, on the other hand, holds these variables in memory with a value of  'undefined', one of the seven available data types, until it has a definition.
	
 Declaring two variables and their values:
	
> 	var x = 0;
> 	var y = 1;
	
 At the top of the scope where this is being processed, the variables are named and sit:
	
> 	var x;
> 	var y;
	
	Logging them to the console will yield:
	
>  console.log(x)   //=>  undefined
>  console.log(y)   //=>  undefined

 
 ### Enter 'let' and 'const'
 
  With the entry of ES2015 and a set of features that continue to address concerns that outside libraries, including jQuery have attempted to solve, two new ways of declaring variables, 'let' and 'const'.
	
	'Let' allows the declaration of variables that are strictly scoped to the statement or expression that they are used on. It doesn't get allocated memory space in the global object. Most often 'let' is used when a variable is expected to change, like an index increment. One nuance of this variable type is that is created, in contrast with the hoisting concept, at the point that it is declared. So, referencing a 'let' variable before declaring it will result in an error.
	
	(Another note with 'let' is that it can be declared and used within a single block, declared within an 'if' statement and not accessible in the else statement or anywhere else.)
	
	'Const' is the new standard for declaration of variables that are to be used within the global or function scope. They are a 'constant', so they can only be read after being declared AND initialized. Const is not hoisted in the sense that, even if defined, it is not accessible (or holding an 'undefined') without having both a declaration and an initialized value. Ultimately it is 'read-only' information, as well -- only allowing block level changes, like adding attributes to an object, but not redefining the object.
 
'Var', although still functional and widely used, is less predictable than these counterparts.


### 'Function Statements' versus 'Function Expressions'

With all the scope and hoisting discussion before, with Javascript's first-class functions, one place that this can be most difficult is within the two different ways of declaring functions.

A function statement is declaring a function with the 'function' keyword and giving a block of code to process. 

> function doSomething(num) {
> console.log(num)
> }

When this is declared, at any point in the program, still bound by the constraints of scope, it pulls all of the information with it in the hoisted declaration. So, declaring this anywhere and then invoking it anywhere, the code in it will be accessible.

A function expression is adding a function to a variable. Consider what happens when we hoist a variable -- the variable, when declared with var is brought to the top of scope and doesn't hold a value and when declared with const is added to memory where the value is assigned. So the data in the functions is not available except after declaration and assignment.

Consider the following bit of code: 

> GLOBAL SCOPE                       // 1. 'x' is brought into memory
> const number = 8;                   // 2. 'number' becomes '8' in the global scope/frame
>
>  FUNCTION SCOPE
>   function x(number) {             // (This is invoked at the end)
>         console.log(number)      // 6. Executes this function with a new variable 'number'
>         let number = 1;                  //      in function scope.
>         console.log(number)       // Note: This would throw an error if it were the same number.
>         let number = 3;
>         console.log(number)
> }
> 
> const y = function(num) {      // 3. 'y' is now brought into memory and held
>      console.log(num + 2)         // => 5 
> }                                                       // 4. writes '5' to the console, but returns nothing
> y(3);                                                //
> 
> console.log(number)              // => 8
>                                                         // 5. number hasn't changed, it only console logs its value
> x(2);                                                
>                                                         // => 2
>                                                         // => 1
>                                                         // => 3
>                                                         // 7. Nothing is returned and the program finishes.

There is only one variable name in the above, but it appears in two scopes: first in the global scope and thereafter in the function scope. At first, 'number' is declared and the next step it is assigned '8' as a value. The execution runs linearly, but functions are only executed when they are invoked.

This is no way to handle writing a program, but it's important to understand where subtle differences can have big impacts, so that leads to the way that we make this work as a concept...


### Brief Best Practices

 Best practices are not a new idea. There is a right way to things and a wrong way to do things, but things aren't always that distinct. Enter best practices.
 
 Simple ways that we can avoid getting errors, calling on wrong variables and making bad decisions in programming with dynamic variables like these.

- Use let & const instead of var, anyone who comes from pre-ES6 will find this confusing, but it does help limit the above described unexpected problems.
-  When able, declare variables and functions at the top of their scope. It helps with readability and prevents function expressions from being undefined variables.
-  Use function expressions and place them correctly in code -- it helps readability.
-  Don't declare named functions inside of blocks.

This list by no means comprehensive, and will likely be updated soon, but it is a start as I am working to write better code and make fewer mistakes.
