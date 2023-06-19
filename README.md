# Interview Preperation

## Q1. Difference between “ == “ and “ === “ operators.

=== : strict equality or compare both value as well as their data types.

== : loose equality or compare only value and not their data types.

    Example:

    let a = 10;
    let b = "10";
    console.log(a===b); //false
    console.log(a==b); //true

## Q2. What are the differences between var, let and const?

### var -

    1. Var is a keyword used to declare variables in JavaScript.
    2. If Var is declared outside of any function, it becomes globally scoped.
    3. Var is function-scoped as well as Global Scoped, meaning that a variable declared with var inside a function is accessible throughout that entire function.
    4. Hoisting is possible in Var.

### let

    1. Let is block-scoped, meaning that a variable declared with let inside a block (e.g. a loop, an if statement, or a function) is only accessible within that block.
    2. If you declare a variable with Let twice in the same block, an error will be thrown.
    3. Hoisting is not possible in let.

### const

    1. A constant is a variable that cannot be reassigned once it has been initialized.
    2. Like Let, Const is also block-scoped.
    3. When you declare a constant, you must initialize it with a value.
    4. no Hoisting is possible in const.

## Q3. What is hoisting?

Hoisting is method that helps us to take values from a variables and functions before it is Initialized. It allows us to call functions before even writing them in our code.

    console.log(name); // undefined
    let name = 'Sahil Goliwar';

    //hoisting using function
    fun(); // Undefined
    function fun(){

        console.log(true);
    }

## Q4. What is a Temporal Dead Zone?

let and const have two broad differences from var:

They are block scoped.
Accessing a var before it is declared has the result undefined; accessing a let or const before it is declared throws ReferenceError
let and const are hoisted (like var, class and function), but there is a period between entering scope and being declared where they cannot be accessed. This period is the temporal dead zone (TDZ).

    Example:
    let a;
    console.log(a); // undefined
    a = 10;
    console.log(a); // 10

## Q5. What is meant by first class functions.

Assigning a function to a variable is first class function.

    Example:
    function foo(){
        return function(){console.log('working!')};
    }

    var bar = foo();
    bar(); //working!

## Q6. What are pure functions?

A pure function in JavaScript is a function that returns the same result if the same arguments(input) are passed in the function. It does not depend on any state or data change during a program’s execution. Rather, it only depends on its input arguments.

    let a = 20;
    let b = 10;
    function add(a, b) {
        return a+b;
    }
    console.log(add(a,b)) //30
