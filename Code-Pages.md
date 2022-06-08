__NOTOC__
<center>**UNICODE CODE PAGES**</center>

This is a list of the current Code Pages supported by the **QB64 IDE**. The data can be copied to a file or made into a [DATA](DATA) field. Each section has a description of the Code Page, the data required for **characters 128 TO 255**, and a LINK to the Code Table.

> ::**NOTE: When copying data to create a CSV file, make sure the cursor ends up below last line at home!**
<center>**See: [Code_Pages#Unicode Mapping](Code_Pages#Unicode Mapping)**</center>

Unicode characters can be inserted in Windows by holding down the **Alt key** and entering a **zero** followed by the character's **three-digit decimal code on the number pad**. By omitting the zero, characters from older code pages can be entered like code page 437 in the US and England or code page 850 in Western Europe. In some versions of Windows it is necessary to change the regional settings to another language before entering that region's page codes.


<center>**Setting up a typing language in the QB64 IDE:**</center>
> ::Step 1: In the OPTIONS menu select **DISPLAY**, then check the CUSTOM FONT check-box.
> ::Step 2: In the OPTIONS menu select **LANGUAGE**, then select a Code Page (CP850 for example) and click OK.

## Code Page Listings:


```text

                                  [Code_Pages#CP_437](Code_Pages#CP_437)

       [Code_Pages#CP_737](Code_Pages#CP_737)     [Code_Pages#CP_860](Code_Pages#CP_860)     [Code_Pages#CP_866](Code_Pages#CP_866)     [Code_Pages#CP_1253](Code_Pages#CP_1253)

       [Code_Pages#CP_775](Code_Pages#CP_775)     [Code_Pages#CP_861](Code_Pages#CP_861)     [Code_Pages#CP_869](Code_Pages#CP_869)     [Code_Pages#CP_1254](Code_Pages#CP_1254)

       [Code_Pages#CP_850](Code_Pages#CP_850)     [Code_Pages#CP_862](Code_Pages#CP_862)     [Code_Pages#CP_874](Code_Pages#CP_874)     [Code_Pages#CP_1255](Code_Pages#CP_1255)

       [Code_Pages#CP_852](Code_Pages#CP_852)     [Code_Pages#CP_863](Code_Pages#CP_863)     [Code_Pages#CP_1250](Code_Pages#CP_1250)    [Code_Pages#CP_1256](Code_Pages#CP_1256)

       [Code_Pages#CP_855](Code_Pages#CP_855)     [Code_Pages#CP_864](Code_Pages#CP_864)     [Code_Pages#CP_1251](Code_Pages#CP_1251)    [Code_Pages#CP_1257](Code_Pages#CP_1257)

       [Code_Pages#CP_857](Code_Pages#CP_857)     [Code_Pages#CP_865](Code_Pages#CP_865)     [Code_Pages#CP_1252](Code_Pages#CP_1252)    [Code_Pages#CP_1258](Code_Pages#CP_1258)

                                  [Code_Pages#CP_MIK](Code_Pages#CP_MIK)

                       [Code_Pages#Unicode_Mapping](Code_Pages#Unicode_Mapping)

```

<center>**See the [Unicode](Unicode) and [_MAPUNICODE](_MAPUNICODE) pages to setup a program language using the data below:**</center>

## CP 437


United States MS DOS


```text


'Microsoft_pc_cp437
199,252,233,226,228,224,229,231,234,235,232,239,238,236,196,197
201,230,198,244,246,242,251,249,255,214,220,162,163,165,8359,402
225,237,243,250,241,209,170,186,191,8976,172,189,188,161,171,187
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_437 Code Table 437]</center>



```text

                               **Western [ASC](ASC) code page differences**

                  "**ä**" is &H84 in **CP437**, &HE4 in Windows-**1252**, &HE4 in Unicode.
                  "**ö**" is &H94 in **CP437**, &HF6 in Windows-**1252**, &HF6 in Unicode.

                  "**÷**" is &HF6 in **CP437**, &HF7 in Windows-**1252**, &HF7 in Unicode.
                  "**Σ**" is &HE4 in **CP437**,                     , &H3A3 in Unicode. 

```


## CP 737


Greek MS DOS displays Greek alphabet for algebraic formulas.


```text


'Microsoft_pc_cp737
913,914,915,916,917,918,919,920,921,922,923,924,925,926,927,928
929,931,932,933,934,935,936,937,945,946,947,948,949,950,951,952
953,954,955,956,957,958,959,960,961,963,962,964,965,966,967,968
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
969,940,941,942,970,943,972,973,971,974,902,904,905,906,908,910
911,177,8805,8804,938,939,247,8776,176,8729,183,8730,8319,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_737 Code Table 737]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 775


Estonian, Lithuanian and Latvian languages.


```text


'Microsoft_pc_cp775
262,252,233,257,228,291,229,263,322,275,342,343,299,377,196,197
201,230,198,333,246,290,162,346,347,214,220,248,163,216,215,164
256,298,243,379,380,378,8221,166,169,174,172,189,188,321,171,187
9617,9618,9619,9474,9508,260,268,280,278,9571,9553,9559,9565,302,352,9488
9492,9524,9516,9500,9472,9532,370,362,9562,9556,9577,9574,9568,9552,9580,381
261,269,281,279,303,353,371,363,382,9496,9484,9608,9604,9612,9616,9600
211,223,332,323,245,213,181,324,310,311,315,316,326,274,325,8217
173,177,8220,190,182,167,247,8222,176,8729,183,185,179,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_775 Code Table 775]</center>

## CP 850


Western Europe, Spain, England


```text


'Microsoft_pc_cp850
199,252,233,226,228,224,229,231,234,235,232,239,238,236,196,197
201,230,198,244,246,242,251,249,255,214,220,248,163,216,215,402
225,237,243,250,241,209,170,186,191,174,172,189,188,161,171,187
9617,9618,9619,9474,9508,193,194,192,169,9571,9553,9559,9565,162,165,9488
9492,9524,9516,9500,9472,9532,227,195,9562,9556,9577,9574,9568,9552,9580,164
240,208,202,203,200,**305**,205,206,207,9496,9484,9608,9604,166,204,9600
211,223,212,210,245,213,181,254,222,218,219,217,253,221,175,180
173,177,8215,190,182,167,247,184,176,168,183,185,179,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_850 Western European Unicode CP850] .......... [http://en.wikipedia.org/wiki/CP858 Western European CP858] (with Euro)</center>

<center>Euro currency sign: ASCII code = 213 Unicode value = 8364 (replaces 305)</center>

<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 852


Central European languages that use Latin script such as Bosnian, Croatian, Czech, Hungarian, Polish, Romanian, Serbian or Slovak.


```text


'Microsoft_pc_cp852
199,252,233,226,228,367,263,231,322,235,336,337,238,377,196,262
201,313,314,244,246,317,318,346,347,214,220,356,357,321,215,269
225,237,243,250,260,261,381,382,280,281,172,378,268,351,171,187
9617,9618,9619,9474,9508,193,194,282,350,9571,9553,9559,9565,379,380,9488
9492,9524,9516,9500,9472,9532,258,259,9562,9556,9577,9574,9568,9552,9580,164
273,272,270,203,271,327,205,206,283,9496,9484,9608,9604,354,366,9600
211,223,212,323,324,328,352,353,340,218,341,368,253,221,355,180
173,733,731,711,728,167,247,184,176,168,729,369,344,345,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_852 Code Table 852]</center>

## CP 855


Cyrillic code page to be used under MS-DOS


```text


'Microsoft_pc_cp855
1106,1026,1107,1027,1105,1025,1108,1028,1109,1029,1110,1030,1111,1031,1112,1032
1113,1033,1114,1034,1115,1035,1116,1036,1118,1038,1119,1039,1102,1070,1098,1066
1072,1040,1073,1041,1094,1062,1076,1044,1077,1045,1092,1060,1075,1043,171,187
9617,9618,9619,9474,9508,1093,1061,1080,1048,9571,9553,9559,9565,1081,1049,9488
9492,9524,9516,9500,9472,9532,1082,1050,9562,9556,9577,9574,9568,9552,9580,164
1083,1051,1084,1052,1085,1053,1086,1054,1087,9496,9484,9608,9604,1055,1103,9600
1071,1088,1056,1089,1057,1090,1058,1091,1059,1078,1046,1074,1042,1100,1068,8470
173,1099,1067,1079,1047,1096,1064,1101,1069,1097,1065,1095,1063,167,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_855 Code Table 855]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 857


Turkish MS DOS


```text


'Microsoft_pc_cp857
199,252,233,226,228,224,229,231,234,235,232,239,238,305,196,197
201,230,198,244,246,242,251,249,304,214,220,248,163,216,350,351
225,237,243,250,241,209,286,287,191,174,172,189,188,161,171,187
9617,9618,9619,9474,9508,193,194,192,169,9571,9553,9559,9565,162,165,9488
9492,9524,9516,9500,9472,9532,227,195,9562,9556,9577,9574,9568,9552,9580,164
186,170,202,203,200,0,205,206,207,9496,9484,9608,9604,166,204,9600
211,223,212,210,245,213,181,0,215,218,219,217,236,255,175,180
173,177,0,190,182,167,247,184,176,168,183,185,179,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_857 Code Table]</center>

## CP 860


Portuguese language. MS DOS


```text


'Microsoft_pc_cp860
199,252,233,226,227,224,193,231,234,202,232,205,212,236,195,194
201,192,200,244,245,242,218,249,204,213,220,162,163,217,8359,211
225,237,243,250,241,209,170,186,191,210,172,189,188,161,171,187
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_860 Code Table 860]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 861


Icelandic language (as well as other Nordic languages). MS DOS


```text


'Microsoft_pc_cp861
199,252,233,226,228,224,229,231,234,235,232,208,240,222,196,197
201,230,198,244,246,254,251,221,253,214,220,248,163,216,8359,402
225,237,243,250,193,205,211,218,191,8976,172,189,188,161,171,187
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_861 Code Table 861]</center>

## CP 862


Hebrew letters in positions 80–9A hex, but otherwise it is identical to [Code_Pages#CP_437](Code_Pages#CP_437). Now obsolete, see [Code_Pages#CP_1255](Code_Pages#CP_1255)


```text


'Microsoft_pc_cp862
1488,1489,1490,1491,1492,1493,1494,1495,1496,1497,1498,1499,1500,1501,1502,1503
1504,1505,1506,1507,1508,1509,1510,1511,1512,1513,1514,162,163,165,8359,402
225,237,243,250,241,209,170,186,191,8976,172,189,188,161,171,187
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_862 Code Table 862]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 863


French language (mainly in Canada). MS DOS


```text


'Microsoft_pc_cp863
199,252,233,226,194,224,182,231,234,235,232,239,238,8215,192,167
201,200,202,244,203,207,251,249,164,212,220,162,163,217,219,402
166,180,243,250,168,184,179,175,206,8976,172,189,188,190,171,187
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_863 Code Table 863]</center>

## CP 864


Arabic MS DOS


```text


'Microsoft_pc_cp864
176,183,8729,8730,9618,9472,9474,9532,9508,9516,9500,9524,9488,9484,9492,9496
946,8734,966,177,189,188,8776,171,187,65271,65272,0,0,65275,65276,0
160,173,65154,163,164,65156,0,0,65166,65167,65173,65177,1548,65181,65185,65189
1632,1633,1634,1635,1636,1637,1638,1639,1640,1641,65233,1563,65201,65205,65209,1567
162,65152,65153,65155,65157,65226,65163,65165,65169,65171,65175,65179,65183,65187,65191,65193
65195,65197,65199,65203,65207,65211,65215,65217,65221,65227,65231,166,172,247,215,65225
1600,65235,65239,65243,65247,65251,65255,65259,65261,65263,65267,65213,65228,65230,65229,65249
65149,1617,65253,65257,65260,65264,65266,65232,65237,65269,65270,65245,65241,65265,9632,0


```



<center>[http://ascii-table.com/codepage.php?864 Code Table 864]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 865


Nordic languages (except Icelandic, for which CP861 is used). MS DOS


```text


'Microsoft_pc_cp865
199,252,233,226,228,224,229,231,234,235,232,239,238,236,196,197
201,230,198,244,246,242,251,249,255,214,220,248,163,216,8359,402
225,237,243,250,241,209,170,186,191,8976,172,189,188,161,171,164
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_865 Code Table 865]</center>

## CP 866


Cyrillic alphabetical order code page to be used with MS-DOS


```text


'Microsoft_pc_cp866
1040,1041,1042,1043,1044,1045,1046,1047,1048,1049,1050,1051,1052,1053,1054,1055
1056,1057,1058,1059,1060,1061,1062,1063,1064,1065,1066,1067,1068,1069,1070,1071
1072,1073,1074,1075,1076,1077,1078,1079,1080,1081,1082,1083,1084,1085,1086,1087
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
1088,1089,1090,1091,1092,1093,1094,1095,1096,1097,1098,1099,1100,1101,1102,1103
1025,1105,1028,1108,1031,1111,1038,1118,176,8729,183,8730,8470,164,9632,160 

```


<center>See [Code_Pages#CP_MIK](Code_Pages#CP_MIK) and [Code_Pages#CP_1251](Code_Pages#CP_1251) below</center>

<center>[http://en.wikipedia.org/wiki/Code_page_866 Code Table 866]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP MIK


Cyrillic Bulgarian Pravetz 16 for MS-DOS 


```text


'Microsoft_pc_cpMIK
1040,1041,1042,1043,1044,1045,1046,1047,1048,1049,1050,1051,1052,1053,1054,1055  
1056,1057,1058,1059,1060,1061,1062,1063,1064,1065,1066,1067,1068,1069,1070,1071  
1072,1073,1074,1075,1076,1077,1078,1079,1080,1081,1082,1083,1084,1085,1086,1087  
1088,1089,1090,1091,1092,1093,1094,1095,1096,1097,1098,1099,1100,1101,1102,1103 
9492,9524,9516,9500,9472,9532,9571,9553,9562,9566,9577,9574,9568,9552,9580,9488  
9617,9618,9619,9474,9508,8470,167,9559,9565,9496,9484,9608,9604,9612,9616,9600  
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745                
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160 

```


<center>See [Code_Pages#CP_866](Code_Pages#CP_866) above and [Code_Pages#CP_1251](Code_Pages#CP_1251) below</center>

<center>[http://en.wikipedia.org/wiki/MIK_Code_page#Code_page_layout Code Table MIK]</center>

## CP 869


Greek MS DOS. Less popular than [Code_Pages#CP_737](Code_Pages#CP_737)


```text


'Microsoft_pc_cp869
0,0,0,0,0,0,902,0,183,172,166,8216,8217,904,8213,905
906,938,908,0,0,910,939,169,911,178,179,940,163,941,942,943
970,912,972,973,913,914,915,916,917,918,919,189,920,921,171,187
9617,9618,9619,9474,9508,922,923,924,925,9571,9553,9559,9565,926,927,9488
9492,9524,9516,9500,9472,9532,928,929,9562,9556,9577,9574,9568,9552,9580,931
932,933,934,935,936,937,945,946,947,9496,9484,9608,9604,948,949,9600
950,951,952,953,954,955,956,957,958,959,960,961,963,962,964,900
173,177,965,966,967,167,968,901,176,168,969,971,944,974,9632,160


```



<center>[http://en.wikipedia.org/wiki/Code_page_869 Code Table 869]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 874


Thai MS DOS and Windows


```text


'Microsoft_pc_cp874
8364,0,0,0,0,8230,0,0,0,0,0,0,0,0,0,0
0,8216,8217,8220,8221,8226,8211,8212,0,0,0,0,0,0,0,0
160,3585,3586,3587,3588,3589,3590,3591,3592,3593,3594,3595,3596,3597,3598,3599
3600,3601,3602,3603,3604,3605,3606,3607,3608,3609,3610,3611,3612,3613,3614,3615
3616,3617,3618,3619,3620,3621,3622,3623,3624,3625,3626,3627,3628,3629,3630,3631
3632,3633,3634,3635,3636,3637,3638,3639,3640,3641,3642,0,0,0,0,3647
3648,3649,3650,3651,3652,3653,3654,3655,3656,3657,3658,3659,3660,3661,3662,3663
3664,3665,3666,3667,3668,3669,3670,3671,3672,3673,3674,3675,0,0,0,0


```



<center>[http://en.wikipedia.org/wiki/Windows-874 Code Table 874]</center>

## CP 1250


WINDOWS in Central European and Eastern European languages that use Latin script, such as Polish, Czech, Slovak, Hungarian, Slovene, Bosnian, Croatian, Serbian (Latin script), Romanian and Albanian. It may also be used with the German language.


```text


'Microsoft_windows_cp1250
8364,0,8218,0,8222,8230,8224,8225,0,8240,352,8249,346,356,381,377
0,8216,8217,8220,8221,8226,8211,8212,0,8482,353,8250,347,357,382,378
160,711,728,321,164,260,166,167,168,169,350,171,172,173,174,379
176,177,731,322,180,181,182,183,184,261,351,187,317,733,318,380
340,193,194,258,196,313,262,199,268,201,280,203,282,205,206,270
272,323,327,211,212,336,214,215,344,366,218,368,220,221,354,223
341,225,226,259,228,314,263,231,269,233,281,235,283,237,238,271
273,324,328,243,244,337,246,247,345,367,250,369,252,253,355,729


```



<center>[http://en.wikipedia.org/wiki/Windows-1250 Code Table 1250]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 1251


Cyrillic alphabet such as Russian, Bulgarian, Serbian Cyrillic and other languages. It is the most widely used for encoding the Bulgarian, Serbian and Macedonian languages.


```text


'Microsoft_windows_cp1251
1026,1027,8218,1107,8222,8230,8224,8225,8364,8240,1033,8249,1034,1036,1035,1039
1106,8216,8217,8220,8221,8226,8211,8212,0,8482,1113,8250,1114,1116,1115,1119
160,1038,1118,1032,164,1168,166,167,1025,169,1028,171,172,173,174,1031
176,177,1030,1110,1169,181,182,183,1105,8470,1108,187,1112,1029,1109,1111
1040,1041,1042,1043,1044,1045,1046,1047,1048,1049,1050,1051,1052,1053,1054,1055
1056,1057,1058,1059,1060,1061,1062,1063,1064,1065,1066,1067,1068,1069,1070,1071
1072,1073,1074,1075,1076,1077,1078,1079,1080,1081,1082,1083,1084,1085,1086,1087
1088,1089,1090,1091,1092,1093,1094,1095,1096,1097,1098,1099,1100,1101,1102,1103 

```


<center>See [Code_Pages#CP_MIK](Code_Pages#CP_MIK) and [Code_Pages#CP_866](Code_Pages#CP_866) above</center>

<center>[http://en.wikipedia.org/wiki/Windows-1251 Code Table 1251]</center>

## CP 1252


Windows Western languages with Latin alphabet, used by default in the legacy components of Microsoft Windows in English.


```text


'Microsoft_windows_cp1252
8364,0,8218,402,8222,8230,8224,8225,710,8240,352,8249,338,0,381,0
0,8216,8217,8220,8221,8226,8211,8212,732,8482,353,8250,339,0,382,376
160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175
176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191
192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207
208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223
224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239
240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255


```



<center>[http://en.wikipedia.org/wiki/Windows-1252 Code Table 1252]</center>



```text

                               **MS DOS [ASC](ASC) code page differences**

                  "**ä**" is &H84 in **CP437**, &HE4 in Windows-**1252**, &HE4 in Unicode.
                  "**ö**" is &H94 in **CP437**, &HF6 in Windows-**1252**, &HF6 in Unicode.

                  "**÷**" is &HF6 in **CP437**, &HF7 in Windows-**1252**, &HF7 in Unicode.
                  "**Σ**" is &HE4 in **CP437**,                     , &H3A3 in Unicode. 

```




<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 1253


Greek (but not polytonic Greek) Not fully compatible with ISO 8859-7 (Ά is located differently).


```text


'Microsoft_windows_cp1253
8364,0,8218,402,8222,8230,8224,8225,0,8240,0,8249,0,0,0,0
0,8216,8217,8220,8221,8226,8211,8212,0,8482,0,8250,0,0,0,0
160,901,902,163,164,165,166,167,168,169,0,171,172,173,174,8213
176,177,178,179,900,181,182,183,904,905,906,187,908,189,910,911
912,913,914,915,916,917,918,919,920,921,922,923,924,925,926,927
928,929,0,931,932,933,934,935,936,937,938,939,940,941,942,943
944,945,946,947,948,949,950,951,952,953,954,955,956,957,958,959
960,961,962,963,964,965,966,967,968,969,970,971,972,973,974,0


```



<center>[http://en.wikipedia.org/wiki/Windows-1253 Code Table 1253]</center>

## CP 1254


Turkish


```text


'Microsoft_windows_cp1254
8364,0,8218,402,8222,8230,8224,8225,710,8240,352,8249,338,0,0,0
0,8216,8217,8220,8221,8226,8211,8212,732,8482,353,8250,339,0,0,376
160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175
176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191
192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207
286,209,210,211,212,213,214,215,216,217,218,219,220,304,350,223
224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239
287,241,242,243,244,245,246,247,248,249,250,251,252,305,351,255


```



<center>[http://en.wikipedia.org/wiki/Windows-1254 Code Table 1254]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 1255


Hebrew Windows. Modern applications prefer [https://en.wikipedia.org/wiki/UTF-8 UTF-8] or [http://www.fileformat.info/info/charset/UTF-16/list.htm UTF-16] to Windows 1255.


```text


'Microsoft_windows_cp1255
8364,0,8218,402,8222,8230,8224,8225,710,8240,0,8249,0,0,0,0
0,8216,8217,8220,8221,8226,8211,8212,732,8482,0,8250,0,0,0,0
160,161,162,163,8362,165,166,167,168,169,215,171,172,173,174,175
176,177,178,179,180,181,182,183,184,185,247,187,188,189,190,191
1456,1457,1458,1459,1460,1461,1462,1463,1464,1465,0,1467,1468,1469,1470,1471
1472,1473,1474,1475,1520,1521,1522,1523,1524,0,0,0,0,0,0,0
1488,1489,1490,1491,1492,1493,1494,1495,1496,1497,1498,1499,1500,1501,1502,1503
1504,1505,1506,1507,1508,1509,1510,1511,1512,1513,1514,0,0,8206,8207,0


```



<center>[http://en.wikipedia.org/wiki/Windows-1255 Code Table 1255]</center>

## CP 1256


Arabic Latin Windows


```text


'Microsoft_windows_cp1256
8364,1662,8218,402,8222,8230,8224,8225,710,8240,1657,8249,338,1670,1688,1672
1711,8216,8217,8220,8221,8226,8211,8212,1705,8482,1681,8250,339,8204,8205,1722
160,1548,162,163,164,165,166,167,168,169,1726,171,172,173,174,175
176,177,178,179,180,181,182,183,184,185,1563,187,188,189,190,1567
1729,1569,1570,1571,1572,1573,1574,1575,1576,1577,1578,1579,1580,1581,1582,1583
1584,1585,1586,1587,1588,1589,1590,215,1591,1592,1593,1594,1600,1601,1602,1603
224,1604,226,1605,1606,1607,1608,231,232,233,234,235,1609,1610,238,239
1611,1612,1613,1614,244,1615,1616,247,1617,249,1618,251,252,8206,8207,1746


```



<center>[http://msdn.microsoft.com/en-us/goglobal/cc305149.aspx Code Table 1256]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## CP 1257


Estonian (although that can also be written with Windows-1252), Latvian and Lithuanian languages under Microsoft Windows. It is also possible to write Polish and German.


```text


'Microsoft_windows_cp1257
8364,0,8218,0,8222,8230,8224,8225,0,8240,0,8249,0,168,711,184
0,8216,8217,8220,8221,8226,8211,8212,0,8482,0,8250,0,175,731,0
160,0,162,163,164,0,166,167,216,169,342,171,172,173,174,198
176,177,178,179,180,181,182,183,248,185,343,187,188,189,190,230
260,302,256,262,196,197,280,274,268,201,377,278,290,310,298,315
352,323,325,211,332,213,214,215,370,321,346,362,220,379,381,223
261,303,257,263,228,229,281,275,269,233,378,279,291,311,299,316
353,324,326,243,333,245,246,247,371,322,347,363,252,380,382,729


```



<center>[http://en.wikipedia.org/wiki/Windows-1257 Code Table 1257]</center>

## CP 1258


Vietnamese. [https://en.wikipedia.org/wiki/UTF-8 UTF-8] is the preferred encoding for Vietnamese in modern applications.


```text


'Microsoft_windows_cp1258
8364,0,8218,402,8222,8230,8224,8225,710,8240,0,8249,338,0,0,0
0,8216,8217,8220,8221,8226,8211,8212,732,8482,0,8250,339,0,0,376
160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175
176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191
192,193,194,258,196,197,198,199,200,201,202,203,768,205,206,207
272,209,777,211,212,416,214,215,216,217,218,219,220,431,771,223
224,225,226,259,228,229,230,231,232,233,234,235,769,237,238,239
273,241,803,243,244,417,246,247,248,249,250,251,252,432,8363,255


```



<center>[http://en.wikipedia.org/wiki/Windows-1258 Code Table 1258]</center>


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## Unicode Mapping

<center>**[_MAPUNICODE](_MAPUNICODE) can place the Unicode characters TO any [ASCII](ASCII) code space you desire (0 to 255)**.</center>

Reading CSV data file: Comma separated values are read using [INPUT (file statement)](INPUT (file statement)). Code Page data is pasted directly into a file as CSV.
<center>**File named CP863.CSV **</center>

```text

Microsoft_pc_cp863
199,252,233,226,194,224,182,231,234,235,232,239,238,8215,192,167
201,200,202,244,203,207,251,249,164,212,220,162,163,217,219,402
166,180,243,250,168,184,179,175,206,8976,172,189,188,190,171,187
9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160 

```

<center>**QB64 BAS module:**</center>

```vb

SCREEN 0
_FONT _LOADFONT("C:\Windows\Fonts\Cour.ttf", 20, "MONOSPACE")  'select monospace font
FileName$ = "CP863.CSV"   **'<<<<<<< Enter Unicode CSV data text file name you created here!**
f = FREEFILE
OPEN FileName$ FOR INPUT AS #f         
INPUT #f, CodePage$                     'read code page ID on first line of file
IF NOT EOF(f) THEN PRINT CodePage$      'display code page number

FOR ascii = 128 TO 255       'assign unicode values to ascii 128 to 255 only
  IF EOF(f) THEN EXIT FOR
  INPUT #f, unicode&
  IF unicode& = 0 THEN unicode& = 9744  'make undefined characters look like a box
  _MAPUNICODE unicode& TO ascii         'replace ascii with unicode value
NEXT
CLOSE #f

FOR code = 128 TO 255
  PRINT code; CHR$(code);               'display unicode characters
NEXT 

END 

```
>  Simply copy the code page data after the page name into a text file, commas and all, and read the file with [INPUT (file statement)](INPUT (file statement)) #.
>  [_MAPUNICODE](_MAPUNICODE) can place the Unicode characters TO any [ASCII](ASCII) code space you desire (0 to 255).


Reading code page as program [DATA](DATA): Simply place DATA before each CSV Code Page data line pasted into a program. 


```vb

SCREEN 0
_FONT _LOADFONT("C:\Windows\Fonts\Cour.ttf", 20, "MONOSPACE")  'select monospace font

RESTORE **Microsoft_pc_cp863**   'or restore single DATA field w/o field name
FOR ascii = 128 TO 255       'assign unicode values to ascii 128 to 255 only
  READ unicode&
  IF unicode& = 0 THEN unicode& = 9744   'make undefined characters look like a box
  _MAPUNICODE unicode& TO ascii          'replace ascii with unicode value 
NEXT

FOR code = 128 TO 255
  PRINT code; CHR$(code);                'display unicode characters
NEXT 

END * *

Microsoft_pc_cp863:         'use as data field line label or comment out code page name
DATA 199,252,233,226,194,224,182,231,234,235,232,239,238,8215,192,167
DATA 201,200,202,244,203,207,251,249,164,212,220,162,163,217,219,402
DATA 166,180,243,250,168,184,179,175,206,8976,172,189,188,190,171,187
DATA 9617,9618,9619,9474,9508,9569,9570,9558,9557,9571,9553,9559,9565,9564,9563,9488
DATA 9492,9524,9516,9500,9472,9532,9566,9567,9562,9556,9577,9574,9568,9552,9580,9575
DATA 9576,9572,9573,9561,9560,9554,9555,9579,9578,9496,9484,9608,9604,9612,9616,9600
DATA 945,223,915,960,931,963,181,964,934,920,937,948,8734,966,949,8745
DATA 8801,177,8805,8804,8992,8993,247,8776,176,8729,183,8730,8319,178,9632,160 

```
>  Simply copy the code page data and paste it into your program then type DATA before each line following the page name.
>  Uncomment the code page name to use it as a [DATA](DATA) field name followed by a colon to [RESTORE](RESTORE) when necessary. 

> Unicode values can be taken from any of the above code page data to make custom extended code characters for a program.


<center>[Code_Pages#Code_Page_Listings:](Code_Pages#Code_Page_Listings:)</center>

## Reference:


## See Also

* [_MAPUNICODE](_MAPUNICODE), [_MAPUNICODE (function)](_MAPUNICODE (function))
* [Unicode](Unicode), [ASCII](ASCII), [CHR$](CHR$), [ASC](ASC)
* [_KEYHIT](_KEYHIT), [_KEYDOWN](_KEYDOWN)
* [Text Using Graphics](Text Using Graphics)



