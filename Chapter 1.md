## Chapter 1 - Values, Types, and Operators

Data is the lifeblood of computers. Inside the Computer’s world, there is only data. You can read data, modify data and create new data. 

This data is stored as long sequences of bits. “Bits” or a “Bit” can be described as the basic unit of information in computing. Bits are any kind of dual valued thing or anything that provides us with two values. Take a light switch e.g. it gives an On and Off option, or a CD that has dull and shiny spots, or a system that gives us either a strong or weak signal. You get the point.

Bits are comprised of Zeroes and One’s. Any piece of information or data in a computer is represented in a series of bits (in a series of ones and zeros). 

We can express the number 14 in bits. It works the same way decimal numbers do but instead of 10 different digits, you only have 2 and the weight of each increase by two as it moves from left to right. 

E.g. the Number 14 would be represented as follows:

0     0     0   0    1  1  1  0
128  64  32  16  8  4  2  1

Thus, the binary representation of the 14 is as follows:

0 0 0 0 1 1 1 0

### <ins>Values<ins>

A modern computer has 30 billion bits in its volatile data storage (RAM) and a whole lot more in its non-volatile data storage (hard disk or equivalent).

To be able to work with such a magnitude of bits we need to separate them into workable chunks. In a JavaScript environment, these chunks are called “values”. Though all values are essentially made up of bits, they carry out different roles. Every value has a different role, it could be a number, some text, a function and so on.

To create a value we simply invoke its name. It’s worth knowing however that values are not plucked out of thin air and they do not need to be stored on the machine. If in the extremely unlikely case, that you want to use a gigantic amount of them at the same time, you might run out of memory. Fortunately, however, this is only an issue if you need to use them simultaneously.

As soon as you no longer need a value it is automatically “garbage collected” by the JavaScript runtime be it in the browser or Node, so you needn’t worry about it.

### <ins>Numbers<ins>

Numbers in JavaScript are numeric values and are written as such. E.g. 14

Use a number in a program and will cause its bit representation to be stored in the computer’s memory.

Previously we saw an 8 binary digit sequence to display the number 14. However, JavaScript uses a 64-bits to store numbers, which is 2^64 different numbers. That is about 18 quintillion (an 18 with 18 zeros after it).

Computers used to be much smaller, people tended to use 8 or 16-bit binary digit sequences to express numbers which would result in accidental overflows (Expressing numbers that don’t fit into the specified numbers of bits). Today even devices that fit in your pocket have plenty of memory, so you needn’t worry about this unless however, you are working with truly astronomical numbers.

Infinity represents positive and negative infinities. 

e.g.

let a = Infinity.
let b =  Infinity

NaN stands for “not a number” which is for errors and other things that don’t yield a result i.e. 0/0.

### <ins>Strings<ins>

Strings are used to represent text. They are written by enclosing their contents in quotes. E.g.

Let a = “You are reading this document”
Let b = ‘You are reading this document’
Let c = `You are reading this document`

You can use double quotes, single quotes and backticks to enclose the text.

Anything can be put between quotes and JavaScript will make a string out of it. However, there are some characters that are difficult. E.g. putting a quote between quotes, or a newline (the characters you get when you press enter. Note however that if you are using backticks you can simply press enter).

To make it possible to use such characters,  the following notation is used (\). Whenever a backslash is found inside the text, it indicates to the system that the character after it has special meaning.

This is called “escaping the character”. A quote (“ or ‘) that is preceded by a backslash will not terminate the string but be a part of it.

e.g.

\n – Is a newline
\t – is a new tab
\” – ignores the quote
\’ ignore the single quote

Let text = “This is the first line \nAnd this is the second”

The following will output.

This is the first line
And this is the second

### <ins>Unary Operators<ins>

Not all operators are symbols. Some are written as words, take “typeof” as an example. Unary operators can be defined as those that operate with only one value.

E.g.

typeof “hello” – returns String

The typeof operator is an example of a unary operator. It takes one value and returns the type of the value.

### <ins>Binary Operators<ins>

Are operators that operate with two values. Common binary operators are &&, ||, !==, ==

Caveat – Minus (-) can be both a unary and binary operator.

e.g.

2 – 1; - Binary

-1; Unary

### <ins>Comparison<ins>

Here is a way to produce a Boolean value.

Console.log( 1 > 2) – returns false
Console.log(2 > 1) – Returns true

The > and < are the traditional symbols for “Is greater than” and “Is less than”. They are binary operators, in that applying results in a binary value.

Strings can be compared in the same way. E.g.

Console.log(“BMW” > “Nissan”) – Returns false

Console.log(“Banana > “Apple”) – Returns true

String are ordered in a roughly alphabetical way. There are a few caveats. Uppercase letters are always less than lowercase ones. So “Z” > “a” results in False.          Symbols are always less than uppercase letters.

See the following:

Table of priority for string comparisons.
lowercase letters
Uppercase letters
numbers as strings
symbols

When comparing strings, JavaScript goes over the Unicode characters from left to right comparing each Unicode one by one.

Other similar operators not previously mentioned are (>=) and (<=), which mean “Greater than or equal to” and “Less than or equal to”.

There is only one value in javascript that is not equal to itself and that is NaN.
Console.log(NaN == NaN) – False.
This is because NaN is supposed to denote a nonsensical value or computation.


### <ins>Logical Operators<ins>

JavaScript supports three logical operators
-      “And” represented as (&&)
-      “Or” represented as (||)
-      “Not” represented as (!)
These can be used to reason about Booleans.

The “And” (&&) operator is a binary operator that results in true if both values given to it are true.

e.g.
console.log(1 == 1) – returns True
console.log(True == False) returns False

The “Or” || operator is a binary operator that results in true if one of both values given to it is true.

console.log(True || False) – returns True
console.log(False || False) – returns False

The “Not” != operator is a unary operator that flips the value given to it. E.g.

!true – results False
!false = returns True

The last logical operator is not unary, not binary, but ternary. The ternary operator operates on three values. It is written with a question mark and a colon as follows:

console.log(true ? 1 : 2);- Returns 1
console.log(false ? 1 : 2); Returns 2

The ternary operator is often referred to as a conditional operator. The value on the left of the question mark is evaluated and picks which of the two values will come out.

### <ins>Empty Values<ins>

The values Null and undefined are used to denote meaningless values. They are themselves values that carry no meaning.

Many operations in the JS language that produce no meaningful value yield “undefined”, simply because it has to yield some value.

The difference between null and undefined is an accident of JavaScripts design and it doesn’t matter most of the time, they are mostly interchangeable.

Short circuit evaluation:

when you compare two things using the || operator it returns the value on the left if it's true otherwise it returns the value on the write. Whereas the && operator returns the value on the left if it's false otherwise it returns the value on the right so its reversed.

With the || if the value on the left is true, it doesn’t check the other value regardless of whatever it is, it just returns the true value on the left same with the && but in the reverse order, hence the name short circuit evaluation, it just evaluates one thing as opposed to two.

Same with the ternary operator or conditional operator, only the value that is returned is evaluated.
