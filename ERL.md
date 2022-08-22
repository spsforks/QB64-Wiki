The [ERL](ERL) function returns the closest previous line number before the last error.

## Syntax

> *lastErrorLine&* = [ERL](ERL)

## Description

* Used in an error handler to report the last line number used before the error.
* If the program does not use line numbers, then ERL returns 0.
* Use [_ERRORLINE](_ERRORLINE) to return the actual code line position of an error in a QB64 program.

## Example(s)

Using a fake error code to return the line number position in a program.

```vb

ON ERROR GOTO errorfix
1
ERROR 250
ERROR 250

5 ERROR 250

END
errorfix:
PRINT ERL
RESUME NEXT 

```

```text

1
1
5

```

## See Also

* [ERR](ERR) (error code number) 
* [ERROR](ERROR) (simulates error)
* [_ERRORLINE](_ERRORLINE) (actual text code line)
* [_ERRORMESSAGE$](_ERRORMESSAGE$) (last error message or a specific message)
* [_INCLERRORFILE$](_INCLERRORFILE$) (name of [$INCLUDE](INCLUDE) file where error occurred, when $INCLUDE files are used
* [_INCLERRORLINE](_INCLERRORLINE) (returns the line number in an [$INCLUDE](INCLUDE) file that caused the most recent error, when an $INCLUDE file is being used)
* [ON ERROR](ON-ERROR) (calls error handing routine using [GOTO](GOTO) only)
* [Error Codes](ERROR-Codes) (list of all QB64 errors)
