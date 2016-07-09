### 1. Use Bitwise  Operators

Bitwise operators treat their operands as a sequence of 32 bits (zeroes and ones), rather than as decimal, hexadecimal, or octal numbers. - [developer.mozilla.org](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators)


Bitwise operators are frequently misunderstood! They have feelings too you know! :P

So what if they treat any number as a sequence of 32 bits, their prejudice makes them very fast :P
Seriously!!!

They are mostly not used because some feel that all developers don't know them well and confuse them for their boolean equivalents.

Number in JavaScript are stored in [IEEE-754 64-bit format.](https://en.wikipedia.org/wiki/IEEE_754-1985)
For Bitwise operations these are converted to 32 bit signed representation.

Despite this conversion taking place,
#### the process is very fast as when compared to other mathematical and Boolean operations.

how to see a number in binary?
use the toString(2) method with argument 2.

basic description of the operations are as follows:
![Image of bitwise operations](https://github.com/Rahul-Raviprasad/Performance-in-JavaScript/blob/master/images/browserscope.org%7C%7Cscripts.png)

#### Examples

1. use bitwise operations instead of pure mathematical operations. For example, it’s common to alternate table row colors by calculating the modulus of 2 for a given number, such as:
```javascript
for (var i=0, len=rows.length; i < len; i++) {
  if (i % 2) {
    className = "even";
  } else {
    className = "odd";
  }
  //apply class
}
```

Calculating mod 2 requires the number to be divided by 2 to determine the remainder. If you were to look at the underlying 32-bit representation of numbers, a number is even if its first bit is 0 and is odd if its first bit is 1. This can easily be determined by using a bitwise AND operation on a given number and the number 1. When the number is even, the result of bitwise AND 1 is 0; when the number is odd, the result of bitwise AND 1 is 1.
That means the previous code can be rewritten as follows:
```javascript
for (var i=0, len=rows.length; i < len; i++) {
  if (i & 1) {
    className = "odd";
  } else {
    className = "even";
  }
//apply class
}
```

Although the code change is small, the bitwise AND version is up to 50% faster than the original (depending on the browser).
