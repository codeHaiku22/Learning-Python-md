
## Python Arithmetic Operators
Python, like many programming languages, also uses operators to perform mathematical (or arithmetic) calculations.

| Operator | Name           | Example  |
| :------: | -------------- | -------- |
|    +     | Addition       | `x + y`  |
|    -     | Subtraction    | `x - y`  |
|    *     | Multiplication | `x * y`  |
|    /     | Division       | `x / y`  |
|    %     | Modulus        | `x % y`  |
|    **    | Exponential    | `x ** y` |
|    //    | Floor Division | `x // y` |

## Python Assignment Operators
An assignment operator has the potential of changing the value of a variable.

| Operator | Example   | Same As      |
| :------: | --------- | ------------ |
|    =     | `x = 5`   | `x = 5`      |
|    +=    | `x += 3`  | `x = x + 3`  |
|    -=    | `x -= 3`  | `x = x -3`   |
|   \*=    | `x *= 3`  | `x = x * 3`  |
|    /=    | `x /= 3`  | `x = x / 3`  |
|    %=    | `x %= 3`  | `x = x % 3`  |
|   //=    | `x //= 3` | `x = x // 3` |
|  \*\*=   | `x **= 3` | `x = x ** 3` |
|    &=    | `x &= 3`  | `x = x & 3`  |
|   \|=    | `x \|= 3` | `x = x \| 3` |
|    ^=    | `x ^= 3`  | `x = x ^ 3`  |
|   >>=    | `x >>= 3` | `x = x >> 3` |
|   <<=    | `x <<= 3` | `x = x << 3` |

## Python Comparison Operators
Comparison operators compare 2 variables or values and return a result that is in the form of a Boolean.

| Operator | Name                     | Example  |
| :------: | ------------------------ | -------- |
|    ==    | Equal                    | `x == y` |
|    !=    | Not equal                | `x != y` |
|    >     | Greater than             | `x > y`  |
|    <     | Less than                | `x < y`  |
|    >=    | Greater than or equal to | `x >= y` |
|    <=    | Less than or equal to    | `x <= y` |

## Python Logical Operators
There are 3 primary logical operators in Python, much as in almost all programming languages.  They evaluate conditions and return a Boolean.

| Operator | Description                                                                      | Example                 |
| :------: | -------------------------------------------------------------------------------- | ----------------------- |
|   and    | Returns `true` if both statements are true                                       | `x < 5 and x < 10`      |
|    or    | Returns `true` if one of the statements is true                                  | `x < 5 or x < 4`        |
|   not    | Reverses the result and returns the opposite of `true` as `false` and vice-versa | `not(x < 5 and x < 10)` |

## Python Membership Operators
Membership operators simply check whether or not the left variable or value is in (member) or not in (not a member) of the right variable or value.

| Operator | Description                                                                        | Example      |
| :------: | ---------------------------------------------------------------------------------- | ------------ |
|    in    | Returns `true` if a sequence with the specified value is present in the object     | `x in y`     |
|  not in  | Returns `true` if a sequence with the specified value is not present in the object | `x not in y` |


## Python Bitwise Operators
Bitwise operators are used to manipulate actual bits and deal primarily with operations that involve bits, themselves.

| Operator | Name                    | Description                                                                                             |
| :------: | ----------------------- | ------------------------------------------------------------------------------------------------------- |
|    &     | AND                     | Sets each bit to 1 if both bits are 1                                                                   |
|    \|    | OR                      | Sets each bit to 1 if one of two bits is 1                                                              |
|    ^     | XOR                     | Sets each bit to 1 if only one of two bits is 1                                                         |
|    ~     | NOT                     | Inverts all the bits                                                                                    |
|    <<    | Zero fill left shift    | Shift left by pushing zeros in from the right and let the leftmost bits fall off                        |
|    >>    | Signed fill right shift | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |
