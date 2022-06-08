[$COLOR]($COLOR) is a metacommand that adds named color [CONST](CONST) in a program.

## Syntax

>  [$COLOR]($COLOR):0

>  [$COLOR]($COLOR):32

## Description

* [$COLOR]($COLOR):0 adds [CONST](CONST) for colors 0-15. The actual constant names can be found in the file **source/utilities/color0.bi**.
* [$COLOR]($COLOR):32 adds [CONST](CONST) for 32-bit colors, similar to HTML color names. The actual constant names can be found in the file **source/utilities/color32.bi**.
* [$COLOR]($COLOR) is a shorthand to manually using [$INCLUDE]($INCLUDE) pointing to the files listed above.
* Not compatible with [$NOPREFIX]($NOPREFIX).

## Example(s)

Example 1: Adding named color constants for SCREEN 0.

```vb

$COLOR:0
COLOR BrightWhite, Red
PRINT "Bright white on red."

```
OutputStartBG4
Bright white on red.

```

Example 2: Adding named color constants for 32-bit modes.

```vb

SCREEN _NEWIMAGE(640, 400, 32)
$COLOR:32
COLOR CrayolaGold, DarkCyan
PRINT "CrayolaGold on DarkCyan."

```

## See Also

* [COLOR](COLOR), [SCREEN](SCREEN) 
* [_NEWIMAGE](_NEWIMAGE), [$INCLUDE]($INCLUDE)
* [Metacommand](Metacommand)
