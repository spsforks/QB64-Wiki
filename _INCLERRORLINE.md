The _INCLERRORLINE$ function returns the line number in an [$INCLUDE]($INCLUDE) file that caused the most recent error.



## Syntax

>  errline& = [_INCLERRORLINE](_INCLERRORLINE)


## Description

* If the last error occurred in the main module, _INCLERRORLINE returns 0.
* By checking _INCLERRORLINE you can report exactly what line inside an included module caused the last error.


## Availability

* **Version 1.1 and up**.


## Example(s)

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
* [_INCLERRORFILE$](_INCLERRORFILE$) (name of [$INCLUDE](INCLUDE) file where error occurred, when $INCLUDE files are used
* [$INCLUDE]($INCLUDE) (invoke a source code file to be inserted at that point)
* [ON ERROR](ON-ERROR) (calls error handing routine using [GOTO](GOTO) only)
* [Error Codes](ERROR-Codes) (list of all QB64 errors)





