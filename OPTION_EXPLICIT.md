DISPLAYTITLE:OPTION _EXPLICIT  
[OPTION _EXPLICIT](OPTION _EXPLICIT) instructs the compiler to require variable declaration with [DIM](DIM), [REDIM](REDIM) or an equivalent statement.


## Syntax

>  [OPTION _EXPLICIT](OPTION _EXPLICIT)


## Description

* With [OPTION _EXPLICIT](OPTION _EXPLICIT) you can avoid typos by having QB64 immediately warn in the **Status area** of new variables used without previous declaration.
* Enable [OPTION _EXPLICIT](OPTION _EXPLICIT) temporarily even if a program source file doesn't contain the directive by specifying the **-e** switch when compiling via command line (*qb64 -c file.bas -e*).


## Error(s)

* If used, [OPTION _EXPLICIT](OPTION _EXPLICIT) must be the very first statement in your program. No other statements can precede it (except for [$NOPREFIX]($NOPREFIX) or comment lines started with an [Apostrophe](Apostrophe) or [REM](REM)).
* Do not use [OPTION _EXPLICIT](OPTION _EXPLICIT) in [$INCLUDE]($INCLUDE)d modules.


## Example(s)

*Example:* Avoiding simple typos with [OPTION _EXPLICIT](OPTION _EXPLICIT) results shown in the QB64 IDE Status area.

```vb
OPTION _EXPLICIT

DIM myVariable AS INTEGER

myVariable = 5

PRINT myVariabe

```

*QB64 IDE Status will show:*
**Variable 'myVariabe' (SINGLE) not defined on line 4**


## See Also

* [OPTION _EXPLICITARRAY](OPTION _EXPLICITARRAY)
* [DIM](DIM), [REDIM](REDIM)
* [SHARED](SHARED)
* [STATIC](STATIC)




