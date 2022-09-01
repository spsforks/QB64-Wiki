The [_ERRORMESSAGE$](_ERRORMESSAGE$) function returns a human-readable description of the most recent runtime error, or the description of an arbitrary error code passed to it.

## Syntax

* e$ = [_ERRORMESSAGE$](_ERRORMESSAGE$)
* e$ = [_ERRORMESSAGE$](_ERRORMESSAGE$)(errorCode%)

## Description

* Used in program error troubleshooting.
* The message returned is identical to the message shown in the dialog box that appears if your program has no error handler. See [ERROR Codes](ERROR-Codes) for the full list of error codes and their messages.

## Example(s)

Using an error handler that ignores any error.

```vb

 ON ERROR GOTO Errhandler
   ' Main module program error simulation code
 ERROR 7           ' simulate an Out of Memory Error
 PRINT "Error handled...ending program"
 SLEEP 4
 SYSTEM            ' end of program code

 Errhandler:              'error handler sub program line label
  PRINT "Error"; ERR; "on program file line"; _ERRORLINE
  PRINT "Description: "; _ERRORMESSAGE$; "."
  BEEP             ' warning beep
 RESUME NEXT       ' moves program to code following the error. 

```

## See Also

* [ERL](ERL) (last line number used before an error occurred, when line numbers are used) 
* [ERR](ERR) (error code number) 
* [ERROR](ERROR) (simulates error)
* [_ERRORLINE](_ERRORLINE) (actual text code line)
* [_INCLERRORFILE$](_INCLERRORFILE$) (name of [$INCLUDE](INCLUDE) file where error occurred, when $INCLUDE files are used
* [_INCLERRORLINE](_INCLERRORLINE) (returns the line number in an [$INCLUDE](INCLUDE) file that caused the most recent error, when an $INCLUDE file is being used)
* [ON ERROR](ON-ERROR) (calls error handing routine using [GOTO](GOTO) only)
* [Error Codes](ERROR-Codes) (list of all QB64 errors)
