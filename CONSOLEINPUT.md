DISPLAYTITLE:_CONSOLEINPUT
The [_CONSOLEINPUT](_CONSOLEINPUT) function is used to monitor any new mouse or keyboard input coming from a $CONSOLE window. It must be called in order for [_CINP](_CINP) to return valid values. Windows-only.


## Syntax

> infoExists%% = [_CONSOLEINPUT](_CONSOLEINPUT)


## Description

* Returns 1 if new keyboard information is available, 2 if mouse information is available, otherwise it returns 0.
* Must be called before reading any of the other mouse functions and before reading [_CINP](_CINP).
* To clear all previous input data, read [_CONSOLEINPUT](_CONSOLEINPUT) in a loop until it returns 0.
* [Keywords_currently_not_supported_by_QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions](Keywords_currently_not_supported_by_QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions).


## Example(s)

*Example 1:* Reading individual key strokes from a console window (Windows).

'''vb

$CONSOLE:ONLY
_DEST _CONSOLE: _SOURCE _CONSOLE

PRINT "Press any key, and I'll give you the scan code for it.  <ESC> quits the demo."
PRINT
PRINT
DO
    x = _CONSOLEINPUT
    IF x = 1 THEN 'read only keyboard input ( = 1)
        c = _CINP
        PRINT c;
    END IF
LOOP UNTIL c = 1
END

'''


## See Also

* [$CONSOLE]($CONSOLE), [_CONSOLE](_CONSOLE)
* [_CINP](_CINP), [Keyboard_scancodes#INP_Scan_Codes](Keyboard_scancodes#INP_Scan_Codes)
* [_MOUSEX](_MOUSEX), [_MOUSEY](_MOUSEY), [_MOUSEBUTTON](_MOUSEBUTTON), [_MOUSEWHEEL](_MOUSEWHEEL)





