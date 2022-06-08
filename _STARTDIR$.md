DISPLAYTITLE:_STARTDIR$
The [_STARTDIR$](_STARTDIR$) function returns the path a user called a QB64 program from.

## Syntax

>  callPath$ = [_STARTDIR$](_STARTDIR$)


## Description

* Returns a [STRING](STRING) representing the user's program calling path.


## Example(s)

## Example(s)
 Showcasing QB64 path functions:

```vb

$CONSOLE:ONLY
_DEST _CONSOLE
SHELL "cd"
PRINT _CWD$
PRINT _STARTDIR$
SYSTEM 

```<sub>Code by Galleon</sub>


## See Also

* [_CWD$](_CWD$)
* [SHELL](SHELL)




