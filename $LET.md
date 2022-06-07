[$LET]($LET) is precompiler command, which is now usable by modern day [cavemen](cavemen) to help include and exclude which sections of code compiles in their program based on OS/bit-size or other predefined conditions.


## Syntax

>  [$LET]($LET) variable = expression


## Description

* Unlike [LET](LET), [$LET]($LET) is not optional.
* $LET a = 12 sets a precompiler variable "a" to the value of 12.   This variable is only valid for the precompiler itself and does nothing to affect the values of any variable/constant which might also be called "a" in the program.
* Variable names can contain numbers, letters, and periods in any order. [$LET]($LET) **3.2 = TRUE** is a perfectly valid variable and expression.
* Expressions can contain one set of leading and/or trailing quotes; and any number of numbers, letters, and periods, in any order. [$LET]($LET) **3.2 = "TRUE"** is also perfectly valid, but [$LET]($LET) **3.2 = ""TRUE""** will error because of the double quotes.


## Example(s)

* See example 1 in [$IF]($IF).


## See Also

* [$IF]($IF)
* [$ELSE]($ELSE)
* [$ELSEIF]($ELSEIF)
* [$END IF]($END IF)
* [Cavemen](Cavemen)




