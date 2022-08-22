The [_INCLERRORFILE$](_INCLERRORFILE$) function returns the name of the original source code [$INCLUDE]($INCLUDE) module that caused the most recent error.



## Syntax

>  errfile$ = [_INCLERRORFILE$](_INCLERRORFILE$)


## Description

If the last error occurred in the main module, [_INCLERRORFILE$](_INCLERRORFILE$) returns an empty string.


## Availability

* **Version 1.1 and up**.


## Example(s)

```vb

ON ERROR GOTO DebugLine

ERROR 250 'simulated error code - an error in the main module leaves _INCLERRORLINE empty (= 0)

'$INCLUDE:'haserror.bi'

END

DebugLine:
PRINT "An error occurred. Please contact support with the following details:
PRINT "ERROR "; ERR; " ON LINE: "; _ERRORLINE
IF _INCLERRORLINE THEN
    PRINT "    IN MODULE "; _INCLERRORFILE$; " (line"; _INCLERRORLINE; ")"
END IF
RESUME NEXT 

```

```text

An error occurred. Please contact support with the following details:
ERROR  250  ON LINE:  6

An error occurred. Please contact support with the following details:
ERROR  250  ON LINE:  9
    IN MODULE haserror.bi ( line 1 )

```



## See Also

* [ERL](ERL) (last line number used before an error occurred, when line numbers are used) 
* [ERR](ERR) (error code number) 
* [ERROR](ERROR) (simulates error)
* [_ERRORLINE](_ERRORLINE) (actual text code line)
* [_ERRORMESSAGE$](_ERRORMESSAGE$) (last error message or a specific message)
* [_INCLERRORLINE](_INCLERRORLINE) (returns the line number in an [$INCLUDE](INCLUDE) file that caused the most recent error, when an $INCLUDE file is being used)
* [ON ERROR](ON-ERROR) (calls error handing routine using [GOTO](GOTO) only)
* [Error Codes](ERROR-Codes) (list of all QB64 errors)






