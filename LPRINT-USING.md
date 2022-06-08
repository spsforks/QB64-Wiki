The [LPRINT USING](LPRINT-USING) statement sends formatted data to LPT1, the parallel port printer.

## Syntax

>  **LPRINT** [*text$*{;|,}] **USING** template$; variable[; ...][{;|,}]


## Parameter(s)

* Literal or variable [STRING](STRING) *text$* can be placed between [LPRINT](LPRINT) and USING or it can be included in the template$.
* A [semicolon](semicolon) or [comma](comma) may follow the text$ to stop or tab the print cursor before the template$ [LPRINT](LPRINT).
* The literal or variable [STRING](STRING) template$ should use the template symbols to display each variable [type](type) in the list following it.
* The list of data *variables* used in the template$ are **separated by semicolons** after the template string value. 
* A [semicolon](semicolon) or [comma](comma) may follow the variable list to stop or tab the print cursor for pending prints.

## Description

* The *variable* list should be listed in the order that they are used in the template from left to right.
* **If the *template* string is omitted or symbols don't match the *variable(s)* an "Illegal Function Call" [ERROR Codes](ERROR Codes) will occur.**
* No more than 25 # digit places are allowed in a template number or an [ERROR Codes](ERROR-Codes) will occur.
* Can convert numerical exponential or [scientific notation](scientific notation) values to normal decimal point values using less digits.
* **NOTE:** If the numerical value exceeds the template's digit range a % symbol will appear in the leftmost digit area.

MISSING: Print Using Table

## See Also

* [PRINT USING](PRINT-USING)
* [LPRINT](LPRINT)
* [PRINT](PRINT)
