[DEF SEG](DEF SEG) is used to define the area in memory to access QB64's emulated conventional memory.


PageLegacySupport
* **QB64 implements memory access using [_MEM](_MEM) and related functions. For that reason, [DEF SEG](DEF SEG) isn't recommended practice anymore and is supported to maintain compatibility with legacy code.**


## Syntax

>  [DEF SEG](DEF SEG) [=][{segment|VARSEG(variable}]


## Description

* Used to set the pointer to a memory area of a variable/array or register.
* [PEEK](PEEK) and [POKE](POKE) require a segment memory address (often just 0) without using VARSEG.
* Important segments using [PEEK](PEEK) and [POKE](POKE) include &HB800 (text segment) and &HA000 (graphics segment).
* [BSAVE](BSAVE) and [BLOAD](BLOAD) require a VARSEG reference to the grahic array(0 index) used.
* Always use DEF SEG when the procedure is completed, in order to reset the segment to QBasic's default value.
* [DEF SEG](DEF SEG), [VARSEG](VARSEG), [VARPTR](VARPTR), [PEEK](PEEK) and [POKE](POKE) access QB64's emulated 16 bit conventional memory block. **It is highly recommended to use QB64's [_MEM](_MEM) memory system to avoid running out of memory.**

<!--
## Example(s)

*Example:* In a Qbasic(ONLY) file delete, **SEG** forces the parameter to be passed as a far pointer.

```vb

CONST file = "trashme.tmp"  'example temporary file name to delete
DEFINT A-Z
DIM filename AS STRING
DIM result AS LONG
DIM t AS STRING
DIM i AS INTEGER
CONST codelen = 48
DIM code AS STRING * codelen

CLS

t = "5589E51E8B560C8EDA8B5E0A8B5702B441CD218B56088EDA8B5E06720B6631C0"
t = t + "6689071F5DCA0800660D0000FFFFEBF0"

FOR i = 0 TO codelen - 1
MID$(code, i + 1, 1) = CHR$(VAL("&h" + MID$(t, i + i + 1, 2)))
NEXT

OPEN file FOR APPEND AS 1  'create temporary file
PRINT #1, "I am doomed! :-("
CLOSE

PRINT "now you see it:"
SHELL "dir " + file
K$ = INPUT$(1)

filename = file + CHR$(0)  'create zero string name for DOS
DEF SEG = VARSEG(code)
CALL absolute(**SEG** filename, **SEG** result, VARPTR(code))

IF result THEN  'check results
PRINT "oops. error: 0x"; HEX$(result AND &HFFFF&)
ELSE
PRINT "now you don't:"
END IF
SHELL "dir " + file
END 

```
<sub>Code by Michael Calkins as Public Domain(2011)</sub>
-->

*See also:* 
* [DEF SEG = 0](DEF SEG = 0)
* [VARPTR](VARPTR), [VARSEG](VARSEG) 
* [PEEK](PEEK), [POKE](POKE)
* [BSAVE](BSAVE), [BLOAD](BLOAD)




