The logical [AND](AND) numerical operator compares two values in respect of their bits. If both bits at a certain position in both values are set, then that bit position is set in the result.


## Syntax

> result = firstvalue AND secondvalue


## Description

* [AND](AND) compares the bits of the firstvalue against the bits of the secondvalue, the result is stored in the result variable.
* If both bits are on (1) then the result is on (1).
* All other conditions return 0 (bit is off).
* AND is often used to see if a bit is on by comparing a value to an exponent of 2.
* Can turn off a bit by subtracting the bit on value from 255 and using that value to AND a byte value.





## Example(s)

*Example 1:*

'''text


         101
         AND
         011
        -----
         001

'''


> The 101 bit pattern equals 5 and the 011 bit pattern equals 3, it returns the bit pattern 001 which equals 1. Only the Least Significant Bits (LSB) match. So decimal values 5 AND 3 = 1.


*Example 2:*

'''text


      11111011
        AND
      11101111
     ----------
      11101011

'''

> Both bits have to be set for the resulting bit to be set. You can use the [AND](AND) operator to get one byte of a two byte integer this way:

> :firstbyte = twobyteint AND 255

> Since 255 is 11111111 in binary, it will represent the first byte completely when compared with AND.

> To find the second (HI) byte's decimal value of two byte [INTEGER](INTEGER)s use: secondbyte = twobyteint \ 256


*Example 3:* Finding the binary bits on in an [INTEGER](INTEGER) value. 

'''vb


 DO
  INPUT "Enter Integer value from -32768 to 32767 (Enter quits): ", INTvalue& 
  IF INTvalue& < -32768 OR INTvalue& > 32767 OR INTval& = 0 THEN EXIT DO
  FOR exponent = 15 TO 0 STEP -1
    IF (INTvalue& AND 2 ^ exponent) THEN PRINT "1"; ELSE PRINT "0";
  NEXT
  PRINT " "
 LOOP UNTIL INTvalue& = 0 'zero entry quits


'''

> Example output for 6055.

'''text


0001011110100111

'''

> :*Note:* The value of 32767 sets 15 bits. -1 sets all 16 bits. Negative values will all have the highest bit set. Use [LONG](LONG) variables for input values to prevent overflow errors.


## See Also

* [OR](OR), [XOR](XOR), [NOT](NOT) (logical operators)
* [AND (boolean)](AND (boolean))
* [Binary](Binary), [Boolean](Boolean)




