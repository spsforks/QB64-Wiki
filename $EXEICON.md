**$EXEICON** pre-compiler  metacommand embeds a designated icon file into the compiled EXE file to be viewed in Windows Explorer.


## Syntax

>  [$EXEICON]($EXEICON):'iconfile.ico'


## Parameter(s)

* 'iconfile.ico' is a valid [https://en.wikipedia.org/wiki/ICO_(file_format) ICO file]


## Description


* Calling [_ICON](_ICON) without an imageHandle& uses the embeded icon, if available.
** Starting with **build 20170906/64**, the window will automatically use the icon embedded by [$EXEICON]($EXEICON), without having to call _ICON.
* **[Keywords currently not supported](Keywords_currently_not_supported_by_QB64)**.


## Example(s)

## Example(s)
 Embeds a designated icon file into the compiled EXE which can be viewed in Windows Explorer folders.

```vb

$EXEICON:'myexe.ico'
_ICON

```
Code and command by Fellippe Heitor


## See Also

* [_ICON](_ICON)
* [_TITLE](_TITLE)
 




