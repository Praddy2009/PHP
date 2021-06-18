### Function Decleration

```
function functionName() {  
 code to be executed;  
}
```

### Function Arguments

```
<?php  
function familyName($fname) {  
 echo "$fname Refsnes.<br>";  
}  
  
familyName("Jani");  
familyName("Hege");  
familyName("Stale");  
familyName("Kai Jim");  
familyName("Borge");  
?>
```

**Note:** 
- Since PHP is a loosely coupled language so we don't need to declare datatype and we can very easily add a int with string. 
- With PHP 7 we have an option to explicitely declare the datatype for variable. Also `strict` keyword could be used to produce error in case operation is done between mismatched datatype.


To specify `strict` we need to set `declare(strict_types=1);`. This must be on the very first line of the PHP file.

In the following example we try to send both a number and a string to the function, but here we have added the `strict` declaration:

```
<?php declare(strict_types=1); // strict requirement  
  
function addNumbers(int $a, int $b) {  
 return $a + $b;  
}  
echo addNumbers(5, "5 days");  
// since strict is enabled and "5 days" is not an integer, an error will be thrown  
?>
```

<hr>

### Default Argument

```
<?php declare(strict_types=1); // strict requirement  
function setHeight(int $minheight = 50) {  
 echo "The height is : $minheight <br>";  
}  
  
setHeight(350);  
setHeight(); // will use the default value of 50  
setHeight(135);  
setHeight(80);  
?>
```

### Return Values

```
<?php declare(strict_types=1); // strict requirement  
function sum(int $x, int $y) {  
 $z = $x + $y;  
 return $z;  
}  
  
echo "5 + 10 = " . sum(5, 10) . "<br>";  
echo "7 + 13 = " . sum(7, 13) . "<br>";  
echo "2 + 4 = " . sum(2, 4);  
?>
```

**Note:**  PHP 7 provides a method to daclare the datatype of return.

To declare a type for the function return, add a colon ( `:` ) and the type right before the opening curly ( `{` )bracket when declaring the function.

```
<?php declare(strict_types=1); // strict requirement  
function addNumbers(float $a, float $b) : float {  
 return $a + $b;  
}  
echo addNumbers(1.2, 5.2);  
?>
```

<hr>

### Passing arguments by reference
In PHP, arguments are usually passed by value, which means that a copy of the value is used in the function and the variable that was passed into the function cannot be changed.

When a function argument is passed by reference, changes to the argument also change the variable that was passed in. To turn a function argument into a reference, the `&` operator is used:

```
<?php  
function add_five(&$value) {  
 $value += 5;  
}  
  
$num = 2;  
add_five($num);  
echo $num;  
?>
```
