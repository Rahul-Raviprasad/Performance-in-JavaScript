### 1. Use Bitwise  Operators

Bitwise operators treat their operands as a sequence of 32 bits (zeroes and ones), rather than as decimal, hexadecimal, or octal numbers. - developer.mozilla.org
https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators

Bitwise operators are frequently misunderstood! They have feelings too you know! :P

So what if they treat any number as a sequence of 32 bits, their prejudice makes them very fast :P
Seriously!!!

They are mostly not used because some feel that all developers don't know them well and confuse them for their boolean equivalents.

Number in JavaScript are stored in IEEE-754 64-bit format. https://en.wikipedia.org/wiki/IEEE_754-1985
For Bitwise operations these are converted to 32 bit signed representation.

Despite this conversion taking place,
#### the process is very fast as when compared to other mathematical and Boolean operations.

how to see a number in binary?
use the toString(2) method with argument 2.
