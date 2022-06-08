The [$VERSIONINFO]($VERSIONINFO) [Metacommand](Metacommand) adds text metadata to the resulting executable for identification purposes across the OS. Windows-only.

## Syntax

>  [$VERSIONINFO]($VERSIONINFO):key=value

## Parameter(s)

* Text *keys* can be: **Comments, CompanyName, FileDescription, FileVersion, InternalName, LegalCopyright, LegalTrademarks, OriginalFilename, ProductName, ProductVersion, Web**
* Numeric keys can be:**FILEVERSION#** and **PRODUCTVERSION#** 

## Description

* Text and numerical values are string literals without quotes entered by programmer. **No variables are accepted.** (variable names would be interpreted as literals).
* Numeric key=*value* must be 4 comma-separated numerical text values entered by programmer which usually stand for major, minor, revision and build numbers).
* Keywords_currently_not_supported_by_QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions](Keywords-currently-not-supported-by-QB64#Keywords_Not_Supported_in_Linux_or_MAC_OSX_versions).

## Example(s)

*Example:* Adding metadata to a Windows exe compiled with QB64:

```vb

$VERSIONINFO:CompanyName=Your company name goes here
$VERSIONINFO:FILEVERSION#=1,0,0,0
$VERSIONINFO:PRODUCTVERSION#=1,0,0,0

``` 

## See Also

* [$EXEICON]($EXEICON) 
* [_ICON](_ICON)
* [VERSIONINFO resource (MSDN)](https://msdn.microsoft.com/library/windows/desktop/aa381058(v=vs.85).aspx)
