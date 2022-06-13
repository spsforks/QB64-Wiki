This function returns the octal (base 8) representation of any numeric value.

## Syntax

> octvalue$ = [OCT$](OCT$)(number)

## Parameters

* number can be any [INTEGER](INTEGER), [LONG](LONG) or [_INTEGER64](_INTEGER64) value, positive or negative.
* number can also be any [SINGLE](SINGLE), [DOUBLE](DOUBLE) or [_FLOAT](_FLOAT) value, but only the integer part of the value is converted in that case. That is, from the value *-123.45* the function would convert the *-123* only.

## Description

* The function returns the base 8 (octal) representation of the given number as [STRING](STRING).
* Different from [STR$](STR$), this function does not return a leading sign placeholder space, so no [LTRIM$](LTRIM$) to strip that space from positive numbers is necessary.
* [VAL](VAL) can convert the returned oct string value back to a decimal value by prefixing the string with "[&O](&O)".
** Eg. `decimal = VAL("&O" + octvalue$)`.

## Example(s)

Example 1: Comparing decimal, hexadecimal, octal and binary string values from 0 to 15.

```vb

tabletop$ = " Decimal | Hexadecimal | Octal "
tablesep$ = "---------+-------------+-------"
tableout$ = "  \ \    |      \\     |   \\  " 'the PRINT USING template

LOCATE 2, 10: PRINT tabletop$
LOCATE 3, 10: PRINT tablesep$
FOR n% = 0 TO 15
    LOCATE 4 + n%, 10: PRINT USING tableout$; STR$(n%); HEX$(n%); OCT$(n%)
NEXT n%

```

Note: Although the decimal numbers 0-15 have a maximum width of 2 digits only, an extra space in the *tableout$* template is needed when using the (fixed width string) slash output format, as [STR$](STR$) values contain a leading sign placeholder space.

```text

          Decimal | Hexadecimal | Octal 
         ---------+-------------+-------
            0     |      0      |   0   
            1     |      1      |   1   
            2     |      2      |   2   
            3     |      3      |   3   
            4     |      4      |   4   
            5     |      5      |   5   
            6     |      6      |   6   
            7     |      7      |   7   
            8     |      8      |   10  
            9     |      9      |   11  
            10    |      A      |   12  
            11    |      B      |   13  
            12    |      C      |   14  
            13    |      D      |   15  
            14    |      E      |   16  
            15    |      F      |   17  

```

Example 2: Converting a octal value to decimal.

```vb

octvalue$ = OCT$(255)
PRINT "Oct: "; octvalue$
PRINT "Converting Oct value to Decimal:"; VAL("&O" + octvalue$)

```

```text

Oct: 377
Converting Oct value to Decimal: 255

```

## See Also

* [HEX$](HEX$), [STR$](STR$), [VAL](VAL)
* [&B](&B) (binary), [&H](&H) (hexadecimal), [&O](&O) (octal)
* [Base Comparisons](Base-Comparisons)
