[$COLOR]($COLOR) is a metacommand that adds named color [CONST](CONST) in a program.


## Syntax

>  [$COLOR]($COLOR):0
>  [$COLOR]($COLOR):32


## Description

* [$COLOR]($COLOR):0 adds [CONST](CONST) for colors 0-15. The actual constant names can be found in the file **source/utilities/color0.bi**.
* [$COLOR]($COLOR):32 adds [CONST](CONST) for 32-bit colors, similar to HTML color names. The actual constant names can be found in the file **source/utilities/color32.bi**.
* [$COLOR]($COLOR) is a shorthand to manually using [$INCLUDE]($INCLUDE) pointing to the files listed above.
* Prior to QBPE v0.5 (�), [$COLOR]($COLOR) was not compatible with [$NOPREFIX]($NOPREFIX).
* Since QBPE v0.5, [$COLOR]($COLOR) can now be used with [$NOPREFIX]($NOPREFIX), with a few notable differences to three conflicting colors -- Red, Green, Blue.

> Red would conflict with [_RED](_RED), Green would conflict with [_GREEN](_GREEN), and Blue would conflict with [_BLUE](_BLUE), once the underscore was removed from those commands with [$NOPREFIX]($NOPREFIX).
> 
> To prevent these conflicts, the [COLOR](COLOR) values have had **NP_** prepended to the front of them, to distinguish them from the non-prefixed command names.  All other color names remain the same, with only the three colors in conflict having to use **NP_** (for **N**o **P**refix) in front of them.

(�) QBPE = QB64 Phoenix Edition


## Example(s)

;Example 1:Adding named color constants for SCREEN 0.

```vb

$COLOR:0
COLOR BrightWhite, Red
PRINT "Bright white on red."

```
OutputStartBG4
Bright white on red.

```


;Example 2:Adding named color constants for 32-bit modes.

```vb

SCREEN _NEWIMAGE(640, 400, 32)
$COLOR:32
COLOR CrayolaGold, DarkCyan
PRINT "CrayolaGold on DarkCyan."

```

;Example 3:Adding named color constants for 32-bit modes (with $NOPREFIX in effect).

```vb

SCREEN _NEWIMAGE(640, 400, 32)
$COLOR:32
$NOPREFIX
COLOR NP_Red, White 'notice the NP_ in front of Red?  
'This is to distinguish the color from the command with $NOPREFIX.
PRINT "Red on White."

```


## See Also

* [COLOR](COLOR), [SCREEN](SCREEN) 
* [_NEWIMAGE](_NEWIMAGE), [$INCLUDE]($INCLUDE)
* [Metacommand](Metacommand)




