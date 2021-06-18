Some of the following:

### Integers
An integer data type is a non-decimal number between -2147483648 and 2147483647 in 32 bit systems, and between -9223372036854775808 and 9223372036854775807 in 64 bit systems.

Here are some rules for integers:

-   An integer must have at least one digit
-   An integer must NOT have a decimal point
-   An integer can be either positive or negative
-   Integers can be specified in three formats: decimal (10-based), hexadecimal (16-based - prefixed with 0x) or octal (8-based - prefixed with 0)

PHP has the following predefined constants for integers:

-   **PHP_INT_MAX** - The largest integer supported
-   **PHP_INT_MIN** - The smallest integer supported
-   **PHP_INT_SIZE** -  The size of an integer in bytes

PHP has the following functions to check if the type of a variable is integer:

-   is_int()
-   is_integer() - alias of is_int()
-   is_long() - alias of is_int()

```
<?php  
$x = 5985;  
var_dump(is_int($x));  
  
$x = 59.85;  
var_dump(is_int($x));  
?>
```

<hr>

### Floats
The float data type can commonly store a value up to 1.7976931348623E+308 (platform dependent), and have a maximum precision of 14 digits.

PHP has the following predefined constants for floats (from PHP 7.2):

-   **PHP_FLOAT_MAX** - The largest representable floating point number
-   **PHP_FLOAT_MIN** - The smallest representable positive floating point number
-   **- PHP_FLOAT_MAX** - The smallest representable negative floating point number
-   **PHP_FLOAT_DIG** - The number of decimal digits that can be rounded into a float and back without precision loss
-   **PHP_FLOAT_EPSILON** - The smallest representable positive number x, so that x + 1.0 != 1.0

PHP has the following functions to check if the type of a variable is float:

-   is_float()
-   is_double() - alias of is_float()

```
<?php  
$x = 10.365;  
var_dump(is_float($x));  
?>
```

<hr>

### Infinity

A numeric value that is larger than PHP_FLOAT_MAX is considered infinite.

PHP has the following functions to check if a numeric value is finite or infinite:

-   [is_finite()](https://www.w3schools.com/php/func_math_is_finite.asp)
-   [is_infinite()](https://www.w3schools.com/php/func_math_is_infinite.asp)

However, the PHP var_dump() function returns the data type and value:

```
<?php  
$x = 1.9e411;  
var_dump($x);  
?>
```

<hr>

### NaN

NaN stands for Not a Number.

NaN is used for impossible mathematical operations.

PHP has the following functions to check if a value is not a number:

-   [is_nan()](https://www.w3schools.com/php/func_math_is_nan.asp)

However, the PHP var_dump() function returns the data type and value:

```
<?php  
$x = acos(8);  
var_dump($x);  
?>
```

<hr>

### Numerical Strings

The PHP is_numeric() function can be used to find whether a variable is numeric. The function returns true if the variable is a number or a numeric string, false otherwise.

```
<?php  
$x = 5985;  
var_dump(is_numeric($x));  
  
$x = "5985";  
var_dump(is_numeric($x));  
  
$x = "59.85" + 100;  
var_dump(is_numeric($x));  
  
$x = "Hello";  
var_dump(is_numeric($x));  
?>
```

<hr>

### Casting

Sometimes you need to cast a numerical value into another data type.

The (int), (integer), or intval() function are often used to convert a value to an integer.

```
<?php  
// Cast float to int  
$x = 23465.768;  
$int_cast = (int)$x;  
echo $int\_cast;  
  
echo "<br>";  
  
// Cast string to int  
$x = "23465.768";  
$int_cast = (int)$x;  
echo $int_cast;  
?>
```

