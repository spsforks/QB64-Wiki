DISPLAYTITLE:OPTION _EXPLICITARRAY  
[OPTION _EXPLICITARRAY](OPTION _EXPLICITARRAY) instructs the compiler to require arrays be declared with [DIM](DIM), [REDIM](REDIM) or equivalent.

## Syntax

>  [OPTION _EXPLICITARRAY](OPTION _EXPLICITARRAY)


## Description

* Normally statements like `x(2) = 3` will implicitly create an array x(). [OPTION _EXPLICITARRAY](OPTION _EXPLICITARRAY) requires a preceding declaration for the array, helping to catch mistyped array and function names.
* Unlike [OPTION _EXPLICIT](OPTION _EXPLICIT), simple variables can still be used without a declaration. Example: `i = 1`

## Error(s)

* If used, [OPTION _EXPLICITARRAY](OPTION _EXPLICITARRAY) must be the very first statement in your program. No other statements can precede it (except for [$NOPREFIX]($NOPREFIX) or comment lines started with an [Apostrophe](Apostrophe) or [REM](REM)).
* Do not use [OPTION _EXPLICITARRAY](OPTION _EXPLICITARRAY) in [$INCLUDE]($INCLUDE)d modules.


## Example(s)

*Example:* Avoiding simple typos with [OPTION _EXPLICITARRAY](OPTION _EXPLICITARRAY) results shown in the QB64 IDE Status area.

```vb
OPTION _EXPLICITARRAY
x = 1 'This is fine, it's not an array so not affected

DIM z(5)
z(2) = 3 'All good here, we've explicitly DIMmed our array

y(2) = 3 'This now generates an error

```

*QB64 IDE Status will show:*
**Array 'y' (SINGLE) not defined on line 7**


## See Also

* [OPTION _EXPLICIT](OPTION _EXPLICIT)
* [DIM](DIM), [REDIM](REDIM)
* [SHARED](SHARED)
* [STATIC](STATIC)




