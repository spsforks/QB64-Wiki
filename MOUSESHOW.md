DISPLAYTITLE:_MOUSESHOW
The [_MOUSESHOW](_MOUSESHOW) statement displays the mouse cursor and can change its shape.


## Syntax

>  [_MOUSESHOW](_MOUSESHOW) [cursorShape$]


## Description

* Simply use the statement whenever [_MOUSEHIDE](_MOUSEHIDE) has been used previously.
* In **version 1.000 and up** the following cursorShape$ can be displayed:
> _MOUSESHOW "LINK" will display an upward pointing hand cursor used to denote hypertext
> _MOUSESHOW "TEXT" will display the I cursor often used in text entry areas 
> _MOUSESHOW "CROSSHAIR" will display a crosshair cursor
> _MOUSESHOW "VERTICAL" will display vertical arrow cursor for movement
> _MOUSESHOW "HORIZONTAL" will display horizontal arrow cursor for movement
> _MOUSESHOW "TOPLEFT_BOTTOMRIGHT" will display bottom diagonal arrow cursor for movement
> _MOUSESHOW "TOPRIGHT_BOTTOMLEFT" will display bottom diagonal arrow cursor for movement
> _MOUSESHOW "DEFAULT" can be used after a mouse cursor statement above was previously used.
* This statement will also disable [_MOUSEMOVEMENTX](_MOUSEMOVEMENTX) or [_MOUSEMOVEMENTY](_MOUSEMOVEMENTY) relative mouse movement reads.
* The mouse cursor will not interfere with any print or graphic screen changes in **QB64**.


### QBasic/QuickBASIC

* _MOUSEHIDE statements do not accumulate like they did with [CALL ABSOLUTE](CALL ABSOLUTE) or [INTERRUPT](INTERRUPT) in QBasic.


## Example(s)

*Example 1:* **QB64 1.000 and up** allow special cursors to be displayed by using special string parameters:

'''vb

_MOUSESHOW "default": _DELAY 0.5
_MOUSESHOW "link": _DELAY 0.5 'a hand, typically used in web browsers
_MOUSESHOW "text": _DELAY 0.5
_MOUSESHOW "crosshair": _DELAY 0.5
_MOUSESHOW "vertical": _DELAY 0.5
_MOUSESHOW "horizontal": _DELAY 0.5
_MOUSESHOW "topleft_bottomright": _DELAY 0.5
_MOUSESHOW "topright_bottomleft": _DELAY 0.5 

'''
>  **Note:** There is no hourglass, stopwatch or spinning colorful wheel in the list. The fact is that these typically only appear in a program when something has gone terribly wrong and the program has crashed or frozen.


## See Also

* [_MOUSEHIDE](_MOUSEHIDE)
* [_MOUSEINPUT](_MOUSEINPUT)
* [_MOUSEMOVE](_MOUSEMOVE)
* [_MOUSEX](_MOUSEX), [_MOUSEY](_MOUSEY)
* [_MOUSEBUTTON](_MOUSEBUTTON)
* [_MOUSEMOVEMENTX](_MOUSEMOVEMENTX), [_MOUSEMOVEMENTY](_MOUSEMOVEMENTY)
* [_DEVICES](_DEVICES), [_DEVICE$](_DEVICE$)




