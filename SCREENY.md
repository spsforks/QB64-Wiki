DISPLAYTITLE:_SCREENY
The [_SCREENY](_SCREENY) function returns the current row pixel coordinate of the program window on the desktop.


## Syntax

>  positionY& = [_SCREENY](_SCREENY)


## Description

* Function returns the current program window's upper left corner row position on the desktop.
* Use [_DESKTOPWIDTH](_DESKTOPWIDTH) and [_DESKTOPHEIGHT](_DESKTOPHEIGHT) to find the current user's Windows desktop resolution to adjust the position with [_SCREENMOVE](_SCREENMOVE).
* [Keywords_currently_not_supported_by_QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions](Keywords_currently_not_supported_by_QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions)


## Example(s)

*Example:* Clicks and opens program window header menu:

```vb
_SCREENMOVE _MIDDLE
_SCREENCLICK _SCREENX + 10, _SCREENY + 10
PRINT "Hello window!" 

```


## See Also

* [_SCREENX](_SCREENX)
* [_SCREENIMAGE](_SCREENIMAGE)
* [_SCREENCLICK](_SCREENCLICK)
* [_SCREENPRINT](_SCREENPRINT)
* [_SCREENMOVE](_SCREENMOVE)




