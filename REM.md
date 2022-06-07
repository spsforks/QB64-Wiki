**REM** or an apostrophe is used for programmer remarks, comments or to stop the execution of program code.


## Syntax

> : REM program comment or ignore code


## Description

* Comments cannot be read by QBasic correctly and may cause syntax and other errors without REM!
* Instead of REM you can use the [REM](REM) symbol which can be put anywhere.
* Code can also be commented out for program testing purposes.
* QBasic Metacommands such as [$DYNAMIC]($DYNAMIC) and [$INCLUDE]($INCLUDE) require the use of REM or the apostrophe.  


*Example:* Avoiding an END IF error.

'''vb

REM This is a remark...
' This is also a remark...
IF a = 0 THEN REM (REM follows syntax rules)
IF a = 0 THEN '(apostrophe doesn't follow syntax rules, so use END IF after this)
END IF 

'''


## See Also
 
* [Apostrophe](Apostrophe)
* [$DYNAMIC]($DYNAMIC), [$STATIC]($STATIC), [$INCLUDE]($INCLUDE)




