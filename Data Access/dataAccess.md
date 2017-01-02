## Accessing Data

This is a major problem in javascript, it is very difficult to do asymptotic analysis of the code. Since it is so hard to tell if the written code is only containing primitive operations or what seems to be primitive would itself have some time complexity attached to it.

Knowledge of Data Structures and Algorithms would definitely help, but it becomes hard to say anything confidently because of the browser implementations. Each engine might have its own way of implementing the standards that it becomes hard to analyze on a white board. It is more brute-ish to implement different Algorithms and test them on multiple browsers.

 There are four basic places from which data can be accessed in JavaScript:

* Literal values
   Any value that represents just itself and isn’t stored in a particular location. JavaScript can represent strings, numbers, Booleans, objects, arrays, functions, regular expressions, and the special values null and undefined as literals.
* Variables
   Any developer-defined location for storing data created by using the var keyword.
* Array items
   A numerically indexed location within a JavaScript Array object.
* Object members
   A string-indexed location within a JavaScript object.

### 1. Literal values and local variables can be accessed quickly, compared to array items and object members.
