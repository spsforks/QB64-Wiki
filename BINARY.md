**Binary** is the base 2 numbering system. It is used by computers because the computer consists of switches that are either on or off. The primary purpose of reading bit values is to translate what was sent by a port or register read.



* Base 2 has numerical values of 0 for off or 1 for on. There is no QBasic function to return the binary values.
* A computer register has 8 bit switches for one byte of data. Each register can return values from 0 to 255 just like [ASCII](ASCII).
* Each bit can be read by using an exponent of 2 from 0 to 128(2 ^ 0 to 2 ^ 7) utilizing the AND numerical operator.
* Bit numbers and parallel port pins are designated as exponents of 2 also for clarity.
* The first bit(2 ^ 0) of one byte is called the least significant bit(LSB).
* The highest bit(2 ^ 7) of one byte is called the most significant bit(MSB).
* A four bit reading or writing mode is called a nibble mode.


*Decimal Bit values returned when a bit is on:*

```text

                                    **Exponent of 2 and Bit #  7 6 5 4 3 2 1 0 **

                       Bit 0 = 2 ^ 0 = 1 decimal    binary = 0 0 0 0 0 0 0 1
                       Bit 1 = 2 ^ 1 = 2 decimal    binary = 0 0 0 0 0 0 1 0
                       Bit 2 = 2 ^ 2 = 4 decimal    binary = 0 0 0 0 0 1 0 0
                       Bit 3 = 2 ^ 3 = 8 decimal    binary = 0 0 0 0 1 0 0 0
                       Bit 4 = 2 ^ 4 = 16 decimal   binary = 0 0 0 1 0 0 0 0
                       Bit 5 = 2 ^ 5 = 32 decimal   binary = 0 0 1 0 0 0 0 0
                       Bit 6 = 2 ^ 6 = 64 decimal   binary = 0 1 0 0 0 0 0 0
                       Bit 7 = 2 ^ 7 = 128 decimal  binary = 1 0 0 0 0 0 0 0

                       All_Bits_On = 1 + 2 + 4 + 8 + 16 + 32 + 64 + 128 = 255

```


>  *Explanation:* The table above only displays the binary value of each bit when on. If a value of 255 was read, the binary number = 11111111 (all bits on). If only bits 2, 3 and 4 are on then the value would be 4 + 8 + 16 = 28 or 00011100.



** Truth table of the BASIC Logical Operators:**




> *Explanation:* The Logical Operators can be used to change bit values of a byte when comparing them to another byte value. [AND](AND) can determine if each bit is on using a comparison with exponents of 2 from 0 to 7. [OR](OR) can turn on a bit only when at least one bit is on in a comparison. It cannot turn off a bit! [XOR](XOR) can switch bits on if only ONE of the values has a bit on. Not both! These 3 logical operators are often used to work with register or port readings to turn bits on or off.


> *Example 1:* Converting decimal values to a string binary value. Use [LOCATE](LOCATE) before the SUB call to locate the [PRINT](PRINT).

```vb

DO
  LOCATE 2, 10
  INPUT "Enter a numerical value to convert to binary(0 quits): ", decimal&
  CLS: LOCATE 10, 10 
  Decimal2Binary (decimal&)       'pass number by value using parenthesis
LOOP UNTIL decimal& = 0
END

SUB Decimal2Binary(number&)
 IF number& = 0 THEN EXIT SUB
 DO
   remain% = ABS(number& MOD 2)   ' remainder is used to create binary number
   number& = number& \ 2          ' move up one exponent of 2 with integer division
   Bin$ = LTRIM$(STR$(remain%))   ' make remainder a string number
   Binary$ = Bin$ + Binary$       ' add remainder to binary number
 LOOP UNTIL number& = 0
 PRINT "Binary number = " + Binary$    'binary result
END SUB 

```
> *Explanation:* Displays Binary bits on as 1. Remainder can only be 1 or 0 in each loop. Can return all positive values correctly. The decimal parameter could come from a register return value read by [INP](INP)(address) and 1 would indicate the pins or bits on.


> *Example 2:* Turning flip-flop [BIT](BIT) flags on or off and determining the bits on in a [BYTE](BYTE) of program data.


```vb

_DEFINE B AS _UNSIGNED _BYTE   'unsigned allows byte values from 128 to 255

PRINT "Hit number keys 1 to 8 to turn flags ON or OFF"

DO
  a$ = INKEY$ 'get bit numbers 1 through 8 only
  k = VAL(a$)
  IF k > 0 AND k < 9 THEN 'test for switch on or off
    bitval = 2 ^ (k - 1) 
    IF (byte AND bitval) = 0 THEN byte = byte + bitval ELSE byte = byte - bitval                  
    LOCATE 10, 10: PRINT "Switches on:";
    FOR i = 0 TO 7                      'maximum byte value is 255
      IF (byte AND 2 ^ i) THEN PRINT i + 1;
    NEXT
    PRINT "Byte ="; byte; SPACE$(4)
  END IF
LOOP UNTIL _KEYDOWN(27)
SLEEP
SYSTEM 

```
<sub>Code by Ted Weissgerber</sub>
> *Explanation:* The byte value is checked to see if the switch is already on. If it is not on, then the bit value is turned on by adding that value to the byte value. If it is on, that value is subtracted. The [FOR...NEXT](FOR...NEXT) loop reads each bit and displays the switches on.



## See Also
 
* [_BIT](_BIT), [&B](&B), [_BYTE](_BYTE)
* [_SHL](_SHL), [_SHR](_SHR)
* [AND](AND), [OR](OR), [XOR](XOR), [EQV](EQV), [IMP](IMP)
* [BINARY](BINARY)(file mode), [DO...LOOP](DO...LOOP)
* [FOR...NEXT](FOR...NEXT), [Boolean](Boolean)
* [Mathematical Operations](Mathematical Operations)





