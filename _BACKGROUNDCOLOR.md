The [_BACKGROUNDCOLOR](_BACKGROUNDCOLOR) function returns the current background color.


## Syntax

> BGcolor& = [_BACKGROUNDCOLOR](_BACKGROUNDCOLOR)



## Description

* Use it to get the current background color to restore later in a program.
* Returns the closest attribute value of the background color.


## Example(s)

*Example 1:* Storing a background color for later use.

```vb

SCREEN 0
COLOR 1, 3
CLS
BG% = _BACKGROUNDCOLOR
PRINT BG%

```
OutputStartBG33

```



*Example 2:* Understanding the function output

```vb

SCREEN 0
COLOR 1, 11
CLS
BG% = _BACKGROUNDCOLOR
PRINT BG%                  'prints the attribute as 3 instead of 11

```
OutputStartBG33

```

> *Explanation: SCREEN 0 background colors over 7 will return the lower intensity color attribute values: EX: attribute - 8


## See Also

* [_DEFAULTCOLOR](_DEFAULTCOLOR)
* [COLOR](COLOR), [SCREEN](SCREEN)
* [SCREEN (function)](SCREEN (function))
* [Windows_Libraries#Color_Dialog_Box](Windows_Libraries#Color_Dialog_Box)




