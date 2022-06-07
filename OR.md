The [OR](OR) numerical operator returns a comparative bit value of 1 if either value's bit is on.


## Syntax

>  result = firstValue [OR](OR) secondValue



## Description

* If both bits are off, it returns 0.
* If one or both bits are on then it returns 1.
* [OR](OR) never turns off a bit and can be used only to turn a bit on.





## Example(s)

*Example 1:* OR always turns bits on! Never off.

```vb

 a% = 5 ' 101 binary
 b% = 4 ' 100 binary
 results% = a% OR b%  ' still 101 binary using OR
 PRINT "Results% ="; results% 

```

```text


 Results% = 5 

```



*Example 2:* Turning a data register bit on.

```vb
  
   address% = 888    'parallel port data register
   bytevalue% = INP(address%)
   OUT address%, bytevalue% OR 4 

```

> *Explanation:* The third register bit is only turned on if it was off. This ensures that a bit is set. OR could set more bits on with a sum of bit values such as: OUT address%, 7 would turn the first, second and third bits on. 1 + 2 + 4 = 7


## See Also

* [AND](AND), [XOR](XOR) 
* [AND (boolean)](AND (boolean)), [OR (boolean)](OR (boolean))
* [Binary](Binary), [Boolean](Boolean)




