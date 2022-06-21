**TYPE** definitions are used to create variables that can hold more than one element.

## Syntax

> **TYPE** typename
>     element-name1 AS type
>     element-name2 AS type
>     .
>     .
>     .
>     element-nameN AS type
> **END TYPE**

> **TYPE** typename
>     AS type element-list1
>     AS type element-list2
>     .
>     .
>     .
>     AS type element-listN
> **END TYPE**

## Description

* Typename is an undefined type name holder as it can hold any variable types.
* TYPE definitions are usually placed in the main module before the start of the program code execution.
* TYPE definitions cam also be placed in [SUB](SUB) or [FUNCTION](FUNCTION) procedures.
* TYPE definitions cannot contain Array variables. Arrays can be [DIMensioned](DIM) as a TYPE definition.
* TYPE definitions cannot be inside of another TYPE definition, but variables can be defined AS another type.(See Example 4)
* TYPE definitions must be ended with [END TYPE](END-TYPE).
* A TYPE variable must be assigned to the type after it is defined. Array variables are allowed.
* Type variables must be defined in every SUB or FUNCTION unless the type variable is [DIMensioned](DIM) as [SHARED](SHARED).
* Type variables use DOT variable names to read or write specific values. They do not use type suffixes as they can hold ANY variable type values! The name before the dot is the one you defined after the type definition and the name after is the variable name used inside of the TYPE. The name of the dimensioned type variable alone can be used to [PUT](PUT) # or [GET](GET) # all of the data at once!
* Once the TYPE variable is created you can find the record or byte size by using [LEN](LEN)(typevariable).
* TYPE definitions can also be placed in [$INCLUDE]($INCLUDE) .BI text files such as [QB.BI](QB) is used by [INTERRUPT](INTERRUPT.html) and [INTERRUPTX](INTERRUPTX).
* You can mix the **element-name AS type** syntax with the **AS type element-list** syntax in the same TYPE block.
* **[_BIT](BIT) is not supported in User Defined TYPEs.**

### Numerical Types

| Type Name | Symbol | Minimum Value | Maximum Value |
| --------- | ------ | ------------- | ------------- |
| _BIT | ` | -1 | 0 |
| _BIT * n | `n | -128 | 127 |
| _UNSIGNED _BIT | ~` | 0 | 1 |
| _BYTE | %% | -128 | 127 |
| _UNSIGNED _BYTE | ~%% | 0 | 255 |
| INTEGER | % | -32,768 | 32,767 |
| _UNSIGNED INTEGER | ~% | 0 | 65,535 |
| LONG | & | -2,147,483,648 | 2,147,483,647 |
| _UNSIGNED LONG | ~& | 0 | 4,294,967,295 |
| _INTEGER64 | && | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 |
| _UNSIGNED _INTEGER64 | ~&& | 0 | 18,446,744,073,709,551,615 |
| SINGLE | ! or none | -2.802597E-45 | +3.402823E+38 |
| DOUBLE | # | -4.490656458412465E-324 | +1.797693134862310E+308 |
| _FLOAT | ## | -1.18E−4932 | +1.18E+4932 |
| _OFFSET | %& | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 |
| _UNSIGNED _OFFSET | ~%& | 0 | 18,446,744,073,709,551,615 |
| _MEM | none | combined memory variable type | N/A |

*Note: For the floating-point numeric types [SINGLE](SINGLE) (default when not assigned), [DOUBLE](DOUBLE) and [_FLOAT](_FLOAT), the minimum values represent the smallest values closest to zero, while the maximum values represent the largest values closest to ±infinity. OFFSET dot values are used as a part of the [_MEM](_MEM) variable type in QB64 to return or set the position in memory.*

### String Text Type

| Type Name | Symbol | Minimum Length | Maximum Length | Size (Bytes) |
| --------- | ------ | -------------- | -------------- | ------------ |
| STRING | $ | 0 | 2,147,483,647 | Use LEN |
| STRING * *n* | $n | 1 | 2,147,483,647 | n |

*Note: For the fixed-length string type [STRING * n](STRING), where n is an integer length value from 1 (one) to 2,147,483,647.*

## Examples

*Example 1:* Creating a mouse [INTERRUPT](INTERRUPT) TYPE definition. Each [INTEGER](INTEGER) value is 2 bytes.

```vb

TYPE RegType
  AX AS INTEGER    ' mouse function to use
  BX AS INTEGER    ' mouse button
  CX AS INTEGER    ' mouse graphic column position
  DX AS INTEGER    ' mouse graphic row position
  BP AS INTEGER    ' not used by mouse, but required *
  SI AS INTEGER    ' not used by mouse, but required *
  DI AS INTEGER    ' not used by mouse, but required *
  Flags AS INTEGER ' not used by mouse but required *
  DS AS INTEGER    ' used by INTERRUPTX only
  ES AS INTEGER    ' used by INTERRUPTX only
END TYPE

DIM SHARED InRegs AS RegType, OutRegs AS RegType ' create dot variables

InRegs.AX = 3 ' sets the mouse function to read the mouse buttons and position.

CALL INTERRUPT(&H33, InRegs, OutRegs)

column% = OutRegs.CX ' returns the current mouse column position

```

*Explanation*: InRegs and OutRegs become the DOT variable prefix name for the TYPE definition's variables.

Each TYPE variable is designated as the DOT variable's suffix.

**Note: Omitting variables in the RegType definition can change other program variable values.**

*Example 2*: Simplifying the TYPE from Example 1 using the alternative TYPE syntax.

```vb

TYPE RegType
  AS INTEGER AX, BX, CX, DX, BP, SI, DI, Flags, FS, ES
END TYPE

```

*Explanation*: By using **AS type element-list** you reduce typing in your TYPE definition, while achieving the same results.

*Example 3*: Creating an addressbook database for a [RANDOM](RANDOM) file.

```vb

TYPE ContactInfo
  First AS STRING * 10
  Last AS STRING * 15
  Address1 AS STRING * 30
  Address2 AS STRING * 30
  City AS STRING * 15
  State AS STRING * 2
  Zip AS LONG   ' (4 bytes)
  Phone AS STRING * 12
END TYPE

DIM Contact AS ContactInfo 'create contact record variable for RANDOM file 
RecordLEN% = LEN(Contact) ' 118 bytes
' define values
Contact.First = "Ted" ' the fixed string length value will contain 7 extra spaces
Contact.Zip = 15236 ' LONG value that can be used to search certain zip code numbers.

PUT #1, 5, Contact  'place contact info into fifth record position

```

*Explanation*: Use the assigned type variable to find the RANDOM record length which is 118 bytes.

