This function returns the hexadecimal (base 16) representation of a numeric value as a [STRING](STRING).

## Syntax

> hexvalue$ = [HEX$](HEX$)(number)

## Parameters

* number can be any [INTEGER](INTEGER), [LONG](LONG) or [_INTEGER64](_INTEGER64) value, positive or negative.
* number can also be any [SINGLE](SINGLE), [DOUBLE](DOUBLE) or [_FLOAT](_FLOAT) value, but only the integer part of the value is converted in that case. That is, from the value *-123.45* the function would convert the *-123* only.

## Description

* The function returns the base 16 (hexadecimal) representation of the given number as [STRING](STRING).
* Different from [STR$](STR$), this function does not return a leading sign placeholder space, so no [LTRIM$](LTRIM$) to strip that space from positive numbers is necessary.
* [VAL](VAL) can convert the returned hex string value back to a decimal value by prefixing the string with "[&H](&H)".
** Eg. `decimal = VAL("&H" + hexvalue$)`.

## Example(s)

Example 1: Comparing decimal, hexadecimal, octal and binary string values from 0 to 15.

```vb

tabletop$ = " Decimal | Hexadecimal | Octal  "
tablesep$ = "---------+-------------+------- "
tableout$ = "  \ \    |      \\     |   \\   " 'the PRINT USING template

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

Example 2:Converting a hexadecimal value to decimal.

```vb

hexvalue$ = HEX$(255)
PRINT "Hex: "; hexvalue$
PRINT "Converting Hex value to Decimal:"; VAL("&H" + hexvalue$)

```

```text

Hex: FF
Converting Hex value to Decimal: 255

```

## See Also

* [OCT$](OCT$), [STR$](STR$), [VAL](VAL)
* [&B](&B) (binary), [&H](&H) (hexadecimal), [&O](&O) (octal)
* [Base Comparisons](Base-Comparisons)
* [HEX$ 32 Bit Values](HEX$-32-Bit-Values)
