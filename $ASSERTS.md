This metacommand enables debug tests with the [_ASSERT](_ASSERT) statement.


## Syntax

> [$ASSERTS]($ASSERTS)[:CONSOLE]


## Description

* The metacommand does not require a comment or [REM](REM) before it. There is no space after the colon.
* If this metacommand is used in a program and any of the set [_ASSERT](_ASSERT) checkpoints will fail, then the program will stop with an **_ASSERT failed** error.
* Detailed error messages passed to the [_ASSERT](_ASSERT) statement will be displayed in the console window, but only if [$ASSERTS]($ASSERTS) is used.

;Note: This metacommand is the main switch to enable debug tests during development. Later just remove this metacommand to compile the program without debugging code, all the [_ASSERT](_ASSERT) statements may remain in the code for later debugging sessions, they are simply ignored without this metacommand.


## Example(s)

;Example:Adding test checks for parameter inputs in a function.

'''vb

$ASSERTS:CONSOLE

DO
    a = INT(RND * 10)
    b$ = myFunc$(a)
    PRINT a, , b$
    _LIMIT 3
LOOP UNTIL _KEYHIT

FUNCTION myFunc$ (value AS SINGLE)
    _ASSERT value > 0, "Value cannot be zero"
    _ASSERT value <= 10, "Value cannot exceed 10"

    IF value > 1 THEN plural$ = "s"
    myFunc$ = STRING$(value, "*") + STR$(value) + " star" + plural$ + " :-)"
END FUNCTION

'''


## See Also

* [_ASSERT](_ASSERT)
* [$CHECKING]($CHECKING)
* [Relational Operations](Relational Operations)
* [ERROR Codes](ERROR Codes)




