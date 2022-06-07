__NOTOC__
QB64 supports several relational operations, which are binary operations that test numeric or string values and return an [INTEGER](INTEGER) value representing a boolean *true* (<tt>-1</tt>) or *false* (<tt>0</tt>) result. These operations are primarily used in expressions where a condition is required, such as the [IF...THEN](IF...THEN) statement.

## List of relational operations

The following table describes the relational operations, where <tt>A</tt> is the left-hand side operand, and <tt>B</tt> is the right-hand side operand:


RelationalOperationsTable


<center>True statements return -1 in [Boolean](Boolean) evaluations. False returns zero.
</center>

## Comparing numerical values and variables

For numeric operands, such as [INTEGER](INTEGER) or [DOUBLE](DOUBLE) values, the relational operations behave as one would expect. For example, the expression (-3.4 [Less_Than](Less_Than) 1.2) evaluates to *true*, and the expression (50 [Equal](Equal) 100) evaluates to *false*.

*Example:* When a user enters a value greater than or equal to 5, the boolean statement returns -1 . Zero is printed otherwise.

'''vb

INPUT "Enter a value from 1 to 10: ", number
PRINT number >= 5 

'''

## Comparing string values and variables

For string operands, the [Equal](Equal) and [Not_Equal](Not_Equal) operators test, respectively, if the operands are of the same or differing length, and that each of the corresponding characters match or don't match. For example, the three expressions ("abc" [Equal](Equal) "abc"), ("abc" [Not_Equal](Not_Equal) "abd") and ("abc" [Not_Equal](Not_Equal) "abcdef") all evaluate to *true*.

When two strings are compared, the left string sets the number of characters to evaluate when not checking for equality. The [Less_Than](Less_Than) and [Greater_Than](Greater_Than) operators find the first set of non-matching characters and test if the [ASCII](ASCII) code values of those characters are less than or greater than each other, respectively. **Equal strings MUST be of the same length with identical [UCASE$](UCASE$) letters or [ASCII](ASCII) characters!**

If one string is identical to part of the other, [Less_Than](Less_Than) returns *false* if the left-hand side string is shorter than the right-hand side string, while [Greater_Than](Greater_Than) returns *true* if the left-hand side string is longer than the right-hand side string. For example, the expressions ("abc" [Less_Than](Less_Than) "abd") and ("abcdef" [Greater_Than](Greater_Than) "abc") both evaluate to *true*. Even [SPACE$](SPACE$) [ASCII](ASCII) character values are evaluated!


*Example:* Shows that the left hand string sets the number of characters to evaluate when using > or < and are not equal when longer.

'''vb

PRINT "abc" < "abcd"
PRINT "abc" = "abc"
PRINT "abc" = "abcd"
PRINT "abcd" > "abc" 

'''

'''text

 0
-1
 0
-1

'''


## Comparing user-defined type variables

Variables of a [TYPE](TYPE) (UDT) cannot be used as operands to the relational operators, but numeric or string type fields can be used as described above. For example:

> : TYPE T
> :: a AS INTEGER
> : END TYPE
 
> : TYPE U
> :: b AS INTEGER
> : END TYPE
 
> : DIM x AS T : x.a = 10
> : DIM y AS U : y.b = 20
 
> : PRINT x < y         ' <- error: type mismatch
> : PRINT x.a < y.b     ' <- outputs "-1"

## Boolean values

The [INTEGER](INTEGER) values for *true* and *false* are such that the bitwise Logical Operators, such as [NOT](NOT), [AND](AND) and [OR](OR) can be used to invert and combine test results. For example, the expression ([NOT](NOT) (10 [Greater_Than_Or_Equal](Greater_Than_Or_Equal) 20)) evaluates to *true*, while the expression ((2 [Less_Than](Less_Than) 1) [AND](AND) ("three" [Equal](Equal) "four")) evaluates to *false*.


Template:LogicalTruthTable

## See also


* [IF...THEN](IF...THEN)
* [DO...LOOP](DO...LOOP), [WHILE...WEND](WHILE...WEND)
* [IS](IS), [NOT](NOT)
* [AND](AND), [OR](OR), [XOR](XOR), [EQV](EQV), [IMP](IMP)




