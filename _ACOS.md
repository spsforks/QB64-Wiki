DISPLAYTITLE:_ACOS
The [_ACOS](_ACOS) function returns the angle measured in radians based on an input [COS](COS)ine value ranging from -1 to 1.


## Syntax

>  radian_angle! = [_ACOS](_ACOS)(cosine_value!)

## Description

* The *cosine_value!* must be measured >= -1 and <= 1, or an error will be generated.  (PRINT _ACOS(1.2) would give the result of -1.#IND, which is basically QB64's way of telling us that the number doesn't exist, much like 1/0 would.) 
* ARCCOSINE is the inverse function of [COS](COS)ine, which lets us turn a [COS](COS)ine value back into an angle.
* Note: Due to rounding with floating point math, the _ACOS may not always give a perfect match for the COS angle which generated this.  You can reduce the number of rounding errors by increasing the precision of your calculations by using [DOUBLE](DOUBLE) or [_FLOAT](_FLOAT) precision variables instead of [SINGLE](SINGLE).


## Availability

* **Version 1.000 and up.**


## Example(s)

## Example(s)
 Converting a radian angle to its COSine and using that value to find the angle in degrees again using _ACOS:

```vb

DEFDBL A-Z

INPUT "Give me an Angle (in Degrees) => "; Angle
PRINT
C = COS(_D2R(Angle)) '_D2R is the command to convert Degrees to Radians, which is what COS expects
PRINT "The COSINE of the Angle is: "; C
A = _ACOS(C)
PRINT "The ACOS of "; C; " is: "; A
PRINT "Notice, A is the Angle in Radians.  If we convert it to degrees, the value is "; _R2D(A) 

```
<sub>Example by SMcNeill</sub>

```text


Give me an Angle (in Degrees) => ? 60

The COSINE of the Angle is:  .5000000000000001
The ACOS of  .5000000000000001  is:  1.047197551196598
Notice, A is the Angle in Radians.  If we convert it to degrees, we discover the value is  60

```



## See Also

* [_D2G](_D2G) (degree to gradient, [_D2R](_D2R) (degree to radian)
* [_G2D](_G2D) (gradient to degree), [_G2R](_G2R) (gradient to degree
* [_R2D](_R2D) (radian to degree), [_R2G](_R2G) (radian to gradient
* [COS](COS) (cosine), [SIN](SIN) (sine), [TAN](TAN) (tangent)
* [_ASIN](_ASIN) (arc sine), [ATN](ATN) (arc tangent)
* [_ACOSH](_ACOSH) (arc hyperbolic  cosine), [_ASINH](_ASINH) (arc hyperbolic  sine), [_ATANH](_ATANH) (arc hyperbolic  tangent)
* [_ATAN2](_ATAN2) (Compute arc tangent with two parameters)
* [_HYPOT](_HYPOT) (hypotenuse)
*[Mathematical Operations](Mathematical Operations)
*[Mathematical_Operations#Derived_Mathematical_Functions](Mathematical_Operations#Derived_Mathematical_Functions)




Templates used on this page:

Template:Cl (view source)
Template:CodeEnd (view source)
Template:CodeStart (view source)
Template:OutputEnd (view source)
Template:OutputStart (view source)
Template:PageDescription (view source)
Template:PageExamples (view source)
Template:PageNavigation (view source)
Template:PageSeeAlso (view source)
Template:PageSyntax (view source)
Template:Parameter (view source)
Template:Small (view source)
Template:Text (view source)
Return to ACOS.

Navigation menu
Log inPageDiscussionReadView sourceView historySearch
Search QB64 Wiki
Main page
Recent changes
Random page
Help about MediaWiki
Tools
What links here
Related changes
Special pages
Page information
Privacy policyAbout QB64 WikiDisclaimersPowered by MediaWiki

