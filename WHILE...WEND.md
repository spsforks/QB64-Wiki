The [WHILE...WEND](WHILE...WEND) statement is used to repeat a block of statements while the condition is met.


## Syntax

> [WHILE](WHILE) condition
> .
> .
> .
> [WEND](WEND)


## Description

* condition is a numeric expression used to determine if the loop will execute.
* statements will execute repeatedly while condition is a non-zero value.
* [EXIT](EXIT) WHILE can be used for emergency exits from the loop in QB64 only.
* A [DO...LOOP](DO...LOOP) can use the same DO WHILE condition to get the same results.
* WHILE loops only run if the WHILE condition is True.


RelationalTable


## Example(s)

*Example 1:* Reading an entire file. Example assumes the program has a [OPEN](OPEN) as #1


```vb
  
OPEN "Readme.txt" FOR INPUT AS #1
WHILE NOT EOF(1)
    _LIMIT 1                                    'limit line prints to one per second 
    LINE INPUT #1, text$
    IF INKEY$ = CHR$(27) THEN EXIT WHILE        'ESC key exits
    PRINT text$
WEND 

```

*Example 2:* Clearing the keyboard buffer.

```vb

WHILE INKEY$ <> "" : WEND 

```


## See Also

* [DO...LOOP](DO...LOOP)
* [FOR...NEXT](FOR...NEXT)
* [UNTIL](UNTIL) (condition)
* [_CONTINUE](_CONTINUE)




