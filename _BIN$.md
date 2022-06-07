DISPLAYTITLE:_BIN$
This function returns the binary (base 2) representation of any numeric value.


## Syntax

>  binvalue$ = [_BIN$](_BIN$)(number)


PageParameters
* number can be any [INTEGER](INTEGER), [LONG](LONG) or [_INTEGER64](_INTEGER64) value, positive or negative.
* number can also be any [SINGLE](SINGLE), [DOUBLE](DOUBLE) or [_FLOAT](_FLOAT) value, but only the integer part of the value is converted in that case. That is, from the value *-123.45* the function would convert the *-123* only.


## Description

* The function returns the base 2 (binary) representation of the given number as [STRING](STRING).
* Different from [STR$](STR$), this function does not return a leading sign placeholder space, so no [LTRIM$](LTRIM$) to strip that space from positive numbers is necessary.
* [VAL](VAL) can convert the returned bin string value back to a decimal value by prefixing the string with "[&B](&B)".
** Eg. InlineCodedecimal = VAL("&B" + binvalue$)InlineCodeEnd.


## Example(s)

;Example 1:Comparing decimal, hexadecimal, octal and binary string values from 0 to 15.

```vb

tabletop$ = " Decimal | Hexadecimal | Octal | Binary "
tablesep$ = "---------+-------------+-------+--------"
tableout$ = "  \ \    |      \\     |   \\  |  \  \  " 'the PRINT USING template

LOCATE 2, 10: PRINT tabletop$
LOCATE 3, 10: PRINT tablesep$
FOR n% = 0 TO 15
    LOCATE 4 + n%, 10: PRINT USING tableout$; STR$(n%); HEX$(n%); OCT$(n%); _BIN$(n%)
NEXT n%

```
;Note:Although the decimal numbers 0-15 have a maximum width of 2 digits only, an extra space in the *tableout$* template is needed when using the (fixed width string) slash output format, as [STR$](STR$) values contain a leading sign placeholder space.

```text


          Decimal | Hexadecimal | Octal | Binary
         ---------+-------------+-------+--------
            0     |      0      |   0   |  0
            1     |      1      |   1   |  1
            2     |      2      |   2   |  10
            3     |      3      |   3   |  11
            4     |      4      |   4   |  100
            5     |      5      |   5   |  101
            6     |      6      |   6   |  110
            7     |      7      |   7   |  111
            8     |      8      |   10  |  1000
            9     |      9      |   11  |  1001
            10    |      A      |   12  |  1010
            11    |      B      |   13  |  1011
            12    |      C      |   14  |  1100
            13    |      D      |   15  |  1101
            14    |      E      |   16  |  1110
            15    |      F      |   17  |  1111

```



;Example 2:Converting a binary value to decimal.

```vb

binvalue$ = _BIN$(255)
PRINT "Bin: "; binvalue$
PRINT "Converting Bin value to Decimal:"; VAL("&B" + binvalue$)

```

```text


Bin: 11111111
Converting Bin value to Decimal: 255

```



## See Also

* [HEX$](HEX$), [OCT$](OCT$), [STR$](STR$), [VAL](VAL)
* [&B](&B) (binary), [&H](&H) (hexadecimal), [&O](&O) (octal)
* [Base Comparisons](Base Comparisons)




