## Chapter 2 - Program Structure

### <ins>Expressions<ins>:

Any fragment of code that produces a value is referred to as an “expression”. Every value that is written be it (99 or “hello”) is an expression, as is a binary operator applied to two expressions or a unary operator applied to one.

Expressions can contain expressions similar to how sub sentences can contain other sub sentences. This allows us to describe complex computations through code.

If expressions correspond to sub sentences, then a “statement” corresponds to a full sentence. A computer program is made of a list of statements. E.g.

1;
true;
false
99

Above a list of statements, and it can be described as a program, though it doesn’t do anything, other than allocating memory. It is a useless program for explanation purposes.

### <ins>Bindings<ins>

How does a program remember things? How does it keep internal state? To catch and hold values JavaScript gives us a way to store our values using “Bindings” or “Variables” as it is more commonly known.

e.g.

let caught = 1;

In the above example, we are holding the value 1 in a variable called “caught”. Think of “caught” as a tentacle grabbing the number 1. On the left-hand side, we use “Let” (will discuss later what this type of binding is”, then the name we want to assign to our variable, the equals sign (which we use for assignation) and then lastly the value.

Note, when a value is binding to a variable, it doesn’t mean that we cannot later change the value of the variables. Because “caught” is a tentacle that is hypothetically grabbing the value 1, we can change the contents of whatever is being grabbed by that tentacle at any time using the “=” operator. It doesn’t even have to be a number e.g.

Let caught = “some random text”

Two or any number of tentacles can be grabbing the same value. E.g.

caught1 = caught.
Caught2 = caught.

When you have an expression that doesn’t define a tentacle, you are given the value but because you don’t have a tentacle grabbing, that value disappears into thin air. Take the following example.

Let a = 1;
Let b = 2;
A + B – This will result in 3, but 3 is not stored anywhere and thus will be lost

Alternatively, to hold the value of the computation, we should declare another tentacle like so.

Let a = 1;
Let b = 2;
Let c = a + b – C is now a tentacle holding on to the value 3

Binding names can be any text, a combination of number and text (must not start with a number and they may include underscore (_) or dollar signs ($).

There are some keywords reserved by the JavaScript language that may not be used as variables names, have a look at the full list of reserved keywords here.
https://www.w3schools.com/js/js_reserved.asp

The collection of bindings and values that exact at any given time are referred to as the environment. When a JS program starts up this is not empty, as there are some binding provided to you by the JS language, moreover depending on the platform you are running your JS code you other predefined bindings, e.g. if its run in the browser there are functions ready for you to interact with it that are already binded (Bound is the grammatically correct term).

### <ins>Functions<ins>

A function can be defined as a program wrapped in a value. That value can be used to run the program, or “Invoke the function”. E.g. prompt(). You invoke a function by putting a set of parenthesis around its binding. The value’s inside the parenthesis are given to the function and they are referred to as “arguments”.

e.g.

someFunction(1,2);

In the example above we are calling the function and passing in the values 1 and 2 as arguments. “someFunction” receives these arguments and does something to them inside the program.

Different functions might need several different arguments or no arguments at all.

The most common function is “console.log()” (“it’s really a method, but more on that later) and it allows us to print something out into the console. If it’s the browser then it outputs to the browser console or if it’s Node.js its outputs to the terminal.

Whatever we put inside the parenthesis is outputted. E.g. Console.log(“hello”) will output “hello” to the console.

Let a = 100;

Console.log(a) – will return 100.

Printing something to the console or showing us a dialogue box when we invoke the function is a side effect of calling that function. Some functions cause side effects whereas other’s do not.  

Math.max(1,10) – in this example, Math.max is a native JS function that gives us the maximum of two values, so in this case, it will return 10. This is an example of a function that doesn’t cause a side effect.

When a function produces a value, it is said: “the function returns a value”. The keyword being “return”.

The return keyword is a reserved JS keyword, that not only terminates your function, but it is a unary operator that returns something. It could be a simple value, a computation of some sort, nothing at all, or even another function.

### <ins>Conditional execution <ins>

Usually, in JavaScript, the program is executed from top-to-bottom. However, we can branch our code off into different directions by using conditional expressions.

Conditional executions are created with the if/else if/ else syntax in the JS language take the following example.

Check weather

If - it’s raining stay indoors

Else if - it’s sunny, were summer clothing and go outside

Else if – stay indoors

Else - Just go to sleep

In the example above we have a conditional situation in which one of the statements will be executed.

The previous example can be expressed in code like this:

Let weather = “sunny”

If (weather == “sunny”){
   goOutside();
}
else if (weather == “cold”){
 stayIndoors()
}
Else{
Sleep()
}

Each condition calls a function.

Loop

Do-while loop:

A do-while loop is executed at least once. Given that the condition is at the end of the loop it has to execute the code first before evaluating the condition, irrespective of whether it’s true or false.

Var x = false;

do{
console.log(“hello”);
}while(x == true)                         

Even though the condition is false, “hello” will be printed to the screen at least once.

For Loop

For (statement1; statement2; statement3)

In a for loop, first, the loop is initialised through statement 1. Then we have a conditional expression in statement 2, which basically says, keep running this loop until my condition is satisfied or I am no longer true and in statement 3 which is executed after each cycle of the loop. It usually increments or decrements a value, to finally satisfy the condition in statement 2.

Statement 1 – initialises loop
Statement 2 – Condition for the loop, once satisfied loop is terminated.
Statement 3 – evaluated at each cycle, usually increments or decrements a value in the loop to meet the condition in statement 2.
Note – Undefined and null are treated as false values







