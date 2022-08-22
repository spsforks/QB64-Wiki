The [ERROR](ERROR) statement is used to simulate a program error or to troubleshoot error handling procedures.

## Syntax

> [ERROR](ERROR) codeNumber%

## Description

* Can be used to test an error handling routine by simulating an error. 
* Error code 97 can be used to invoke the error handler for your own use, no real error in the program will trigger error 97.
* Use error codes between 100 and 200 for custom program errors that will not be responded to by QB64. 

## Example(s)

Creating custom error codes for a program that can be handled by an [ON ERROR](ON ERROR) handling routine.

```vb

ON ERROR GOTO handler

IF x = 0 THEN ERROR 123
x = x + 1
IF x THEN ERROR 111

END


handler:
PRINT ERR, _ERRORLINE
BEEP
RESUME NEXT 

```

> **Note: Don't use error codes under 97 or over 200 as QB64 may respond to those errors and interrupt the program.**

## See Also



* [ERL](ERL) (last line number used before an error occurred, when line numbers are used) 
* [ERR](ERR) (error code number) 
* [_ERRORLINE](_ERRORLINE) (actual text code line)
* [_ERRORMESSAGE$](_ERRORMESSAGE$) (last error message or a specific message)
* [_INCLERRORFILE$](_INCLERRORFILE$) (name of [$INCLUDE](INCLUDE) file where error occurred, when $INCLUDE files are used
* [_INCLERRORLINE](_INCLERRORLINE) (returns the line number in an [$INCLUDE](INCLUDE) file that caused the most recent error, when an $INCLUDE file is being used)
* [ON ERROR](ON-ERROR) (calls error handing routine using [GOTO](GOTO) only)
* [Error Codes](ERROR-Codes) (list of all QB64 errors)
