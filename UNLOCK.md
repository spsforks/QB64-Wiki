This statement opens access to parts or all of a file to other programs and network users.


## Syntax

>  [UNLOCK](UNLOCK) [#]fileNumber%
>  [UNLOCK](UNLOCK) [#]fileNumber%, record&
>  [UNLOCK](UNLOCK) [#]fileNumber%, [firstRecord&] TO lastRecord&


## Description

* fileNumber% is the file number of the file to unlock.
* In the first syntax, the entire file is unlocked.
* In the second syntax, record& is the record number of the file to unlock.
* In the third syntax, the records or bytes in the range [firstRecord&,lastRecord&] are unlocked. If firstRecord& is omitted, it is assumed to be the first record or byte.
* For files opened in [BINARY](BINARY) mode, each record corresponds to a single byte.
* [LOCK](LOCK) and [UNLOCK](UNLOCK) statements are always used in pairs and each statement must match the other one.
* Files must be unlocked before other programs can access them, and before the file is closed.
* [Keywords_currently_not_supported_by_QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions](Keywords_currently_not_supported_by_QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions)


## See Also

* [LOCK](LOCK)
* [OPEN](OPEN)
* [ACCESS](ACCESS)




