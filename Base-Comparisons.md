```text

                        **Comparing the Base Numbering Systems**

     **Decimal (base 10)    Binary (base 2)    Hexadecimal (base 16)    Octal (base 8)**

          0                  0000                  0                     0
          1                  0001                  1                     1
          2                  0010                  2                     2
          3                  0011                  3                     3
          4                  0100                  4                     4
          5                  0101                  5                     5
          6                  0110                  6                     6
          7                  0111                  7                     7 -- maxed
          8                  1000                  8                    10
  maxed-- 9                  1001                  9                    11
         10                  1010                  A                    12
         11                  1011                  B                    13
         12                  1100                  C                    14
         13                  1101                  D                    15
         14                  1110                  E                    16
         15  -------------   1111 <--- Match --->  F  ----------------  17 -- max 2
         16                 10000                 10                    20
        
      When the Decimal value is 15, the other 2 base systems are all maxed out!
      The Binary values can be compared to all of the HEX value digit values so
      it is possible to convert between the two quite easily. To convert a HEX
      value to Binary just add the 4 binary digits for each HEX digit place so:

                        F      A      C      E 
              &HFACE = 1111 + 1010 + 1100 + 1101 = &B1111101011001101

      To convert a Binary value to HEX you just need to divide the number into
      sections of four digits starting from the right(LSB) end. If one has less
      than 4 digits on the left end you could add the leading zeros like below:
 
             &B101011100010001001 = 0010 1011 1000 1000 1001  
                       hexadecimal =  2  + B  + 8 +  8  + 9 = &H2B889 

    See the Decimal to Binary conversion function that uses **[HEX$](HEX$)** on the **[&H](&H)** page,
    but take it for education only.

```

## Example(s)

Example: Comparing decimal, hexadecimal, octal and binary string values from 0 to 15.

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

Note: Although the decimal numbers 0-15 have a maximum width of 2 digits only, an extra space in the *tableout$* template is needed when using the (fixed width string) slash output format, as [STR$](STR$) values contain a leading sign placeholder space.

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

## See Also

* [_BIN$](_BIN$), [HEX$](HEX$), [OCT$](OCT$), [VAL](VAL)
* [&H](&H) (hexadecimal), [&O](&O) (octal), [&B](&B) (binary)   
