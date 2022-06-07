The **PRINT USING** statement is used to [PRINT](PRINT) formatted data to the Screen or a file using a [STRING](STRING) template.


## Syntax

> : **PRINT** [*text$*{;|,}] **USING** *template$*; *variable*[; ...][{;|,}]


## Parameter(s)

* Literal or variable [STRING](STRING) *text$* can be placed between PRINT and USING or it can be included in the *template*.
* A [semicolon](semicolon) or [comma](comma) may follow the *text* to stop or tab the print cursor before the *template* [PRINT](PRINT).
* The literal or variable [STRING](STRING) *template* should use the template symbols to display each variable [type](type) in the list following it.
* The list of data *variables* used in the *template* are **separated by semicolons** after the template string value. 
* In **QB64** ONE [semicolon](semicolon) or [comma](comma) may follow the variable list to stop the print cursor for pending prints. QB only allowed a semicolon.


*Usage:*
* The *variables* should be listed in the order that they are used in the template from left to right.
* **If the *template* string is omitted or symbols don't match the *variable(s)* an "Illegal Function Call" [ERROR Codes](ERROR Codes) will occur!**
* No more than 25 # digit places are allowed in a template number or an [ERROR Codes](ERROR Codes) will occur.
* Can convert numerical exponential or [scientific notation](scientific notation) values to normal decimal point values using less digits.
* **NOTE:** If the numerical value exceeds the template's digit range a % symbol will appear in the leftmost digit area.
* **WARNING: The numbers displayed are rounded so the actual values are never changed and are actually more accurate.**


PrintUsingTable


*Example 1:* Printing formatted data using a predefined [STRING](STRING) template variable.

```vb

first$ = "Bobby": last$ = "Smith"
boxes% = 1510: sales! = 4530
tmp$ = "Salesperson: & &  #####,.   $$#####,.##"

PRINT USING tmp$; first$; last$; boxes%; sales!

``` 

```text

Salesperson: Bobby Smith  1,510  $4,530.00

```

*Explanation:* The *Salesperson:* text precedes the formatted data. The name lengths will change the length of the string template accordingly so columns will not all line up. If \  \ was used, the columns would stay the same, but parts of some names might be lost. If the box or sales values exceed 3 digits, a comma is used in the value every 3 digits.


*Example 2:* How to display formatting symbols as normal text using underscores in a PRINT USING template.

```vb

errcode = 35
PRINT USING "Error ## occurred!!"; errcode
'now there are the !! at the end of the printed string
PRINT USING "Error ## occurred_!_!"; errcode
END *

```

```text

Error 35 occurred
Error 35 occurred!!

```
 
>  *Explanation:* The first template will not print the exclamation points or error when the requested text parameters are omitted.


*Example 3:* Exponential notation is designated after the leading digits are formatted. Digit places determine rounded value displayed.

```vb

PRINT USING "##.##^^^^"; 234.56
PRINT USING ".####^^^^-"; -777777
PRINT USING "+.##^^^^"; 123
PRINT USING "+.##^^^^^"; 123 

```

```text

 2.35E+02
.7778E+06-
+.12E+03
+.12E+003

```

>  *Explanation:* Note how 5 carets in the bottom format expands the number of exponent digits to accommodate larger exponent values. 


*Example 4:* USING does not necessarily have to immediately follow PRINT, but it must follow it in the code line.

```vb

money = 12345.45
tmp$ = "$$#######,.##"

PRINT "I have this much money!"; USING tmp$; money 

```
>  *Note:* This can also be used to print the USING formatting characters outside of the template.


*See also:* 
* [PRINT](PRINT), [PRINT USING (file statement)](PRINT USING (file statement))
* [LPRINT](LPRINT), [LPRINT USING](LPRINT USING)




