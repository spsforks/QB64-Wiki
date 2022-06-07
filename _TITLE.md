DISPLAYTITLE:_TITLE
The [_TITLE](_TITLE) statement provides the program name in the title bar of the program window.


## Syntax

>  [_TITLE](_TITLE) text$


## Parameter(s)

* text$ can be any literal or variable [STRING](STRING) or [ASCII](ASCII) character value.


## Description

* The title can be changed anywhere in a program procedure.
* The title bar will say "Untitled" if a title is not set.
* Change the title of the [$CONSOLE]($CONSOLE) windows created using [_CONSOLETITLE](_CONSOLETITLE)
* **Note: A [_DELAY](_DELAY) may be required before the title can be set.** See [_SCREENEXISTS](_SCREENEXISTS).


## Example(s)

*Example 1:* How to create the window title bar.

```vb

_TITLE "My New Program" 

```


*Example 2:* How to find the currently running program module name and current path using a Windows API Library.

```vb

_TITLE "My program"
_DELAY 5             '5 second delay

_TITLE MID$(TITLE$, 1, INSTR(TITLE$, ".") - 1)

PRINT PATH$


FUNCTION TITLE$ '###  SHOW CURRENT PROGRAM
SHARED PATH$
DECLARE LIBRARY 'Directory Information using KERNEL32 provided by Dav
  FUNCTION GetModuleFileNameA (BYVAL Module AS LONG, FileName AS STRING, BYVAL nSize AS LONG)
END DECLARE

FileName$ = SPACE$(256)
Result = GetModuleFileNameA(0, FileName$, LEN(FileName$))
IF Result THEN
  PATH$ = LEFT$(FileName$, Result)
  start = 1
  DO
    posit = INSTR(start, PATH$, "\")
    IF posit THEN last = posit
    start = posit + 1
  LOOP UNTIL posit = 0
  TITLE$ = MID$(PATH$, last + 1)
  PATH$ = LEFT$(PATH$, last)
ELSE TITLE$ = "": PATH$ = ""
END IF
END FUNCTION 

```
>  *Note:* The actual module file name is returned. Not necessarily the Title value. The value returned can be used however.


## See Also

* [_TITLE$](_TITLE$) (function)
* [_ICON](_ICON)
* [_DELAY](_DELAY)
* [ASCII](ASCII)
* [_CONSOLETITLE](_CONSOLETITLE)
* [_SCREENEXISTS](_SCREENEXISTS)




