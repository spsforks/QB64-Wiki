[CALL ABSOLUTE](CALL-ABSOLUTE) is used to access interrupts on the computer or execute assembly type procedures.

## Syntax

> [CALL ABSOLUTE](CALL-ABSOLUTE)([argumentList,] integerOffset)

PageLegacySupport
* [CALL ABSOLUTE](CALL-ABSOLUTE) is implemented to support older code and is not recommended practice. To handle mouse input, use [_MOUSEINPUT](_MOUSEINPUT) and related functions.

## Description

* [CALL](CALL) and parameter brackets are required in the statement.
* argumentList contains the list of arguments passed to the procedure.
* integerOffset contains the offset from the current code segment, set by [DEF SEG](DEF SEG) and [SADD](SADD), to the starting location of the called procedure.
* QBasic and **QB64** have the ABSOLUTE statement built in and require no library, like QuickBASIC did.
* **NOTE: QB64 does not support INT 33h mouse functions above 3 or [BYVAL](BYVAL) in an ABSOLUTE statement. Registers are emulated.**

## See Also

* [SADD](SADD), [INTERRUPT](INTERRUPT)
* [DECLARE (non-BASIC statement)](DECLARE-(non-BASIC-statement))
* [_MOUSEINPUT](_MOUSEINPUT)
