The [_ERRORLINE](_ERRORLINE) function returns the source code line number that caused the most recent runtime error.

## Syntax

> e% = [_ERRORLINE](_ERRORLINE)

## Description

* Used in program error troubleshooting.
* Does not require that the program use line numbers as it counts the actual lines of code.
* The code line can be found using the QB64 IDE (Use the shortcut **Ctrl+G** to go to a specific line) or any other text editor such as Notepad.

## Example(s)

Displaying the current program line using a simulated [ERROR](ERROR) code.

```vb

ON ERROR GOTO DebugLine 'can't use GOSUB 

ERROR 250 'simulated error code 

END 
DebugLine: 
PRINT _ERRORLINE 
RESUME NEXT 

```

## See Also

* [ERL](ERL) (last line number used before an error occurred, when line numbers are used) 
* [ERR](ERR) (error code number) 
* [ERROR](ERROR) (simulates error)
* [_ERRORMESSAGE$](_ERRORMESSAGE$) (last error message or a specific message)
* [_INCLERRORFILE$](_INCLERRORFILE$) (name of [$INCLUDE](INCLUDE) file where error occurred, when $INCLUDE files are used
* [_INCLERRORLINE](_INCLERRORLINE) (returns the line number in an [$INCLUDE](INCLUDE) file that caused the most recent error, when an $INCLUDE file is being used)
* [ON ERROR](ON-ERROR) (calls error handing routine using [GOTO](GOTO) only)
* [Error Codes](ERROR-Codes) (list of all QB64 errors)
