The [IMP](IMP) logical operator converts the result of two comparative values and returns a bit result.

## Syntax
 
> result = firstValue [IMP](IMP) secondValue

## Description

* Returns a different result from [AND](AND), [OR](OR) or [XOR](XOR) - see truth table below.
* Evaluates if firstValue ***imp**lies* secondValue.
  - If firstValue is true then secondValue must also be true.
  - So if firstValue is true, and secondValue false, then the condition is false, otherwise it is true (see table below).

## See Also

* [Binary](Binary)
* [Boolean](Boolean)
