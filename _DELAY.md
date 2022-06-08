DISPLAYTITLE:_DELAY
The [_DELAY](_DELAY) statement suspends program execution for a [SINGLE](SINGLE) value of seconds.


## Syntax

> [_DELAY](_DELAY) seconds!


## Description

* seconds! is the time to wait, accurate to nearest millisecond (.001).
* While waiting, cpu cycles are relinquished to other applications.
* Delays are not affected by midnight timer corrections.


## See Also

* [_LIMIT](_LIMIT)
* [TIMER](TIMER)
* [ON TIMER(n)](ON TIMER(n))



