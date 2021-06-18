A PHP script starts with `<?php` and ends with `?>`:

```
<?php  
// PHP code goes here  
?>
```

For ex:
```
<!DOCTYPE html>  
<html>  
<body>  
  
<h1>My first PHP page</h1>  
  
<?php  
echo "Hello World!";  
?>  
  
</body>  
</html>
```

<hr>

### Variables

To declare variable us dollar(`$`) symbol
For ex:

```
<!DOCTYPE html\>  
<html\>  
<body\>  
  
<?php  
$color = "red";  
echo "My car is " . $color . "<br>";  
?>  
  
</body\>  
</html\>
```

**Rules to declare variables**

-   A variable starts with the `$` sign, followed by the name of the variable
-   A variable name must start with a letter or the underscore character
-   A variable name cannot start with a number
-   A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
-   Variable names are case-sensitive (`$age` and `$AGE` are two different variables)

**Note** : 
-	PHP keywords are <u>**not casesensitive**</u>
-	PHP variables are <u>**case sensitive**</u>

### Output the variables

The PHP `echo` statement is often used to output data to the screen.

```
<?php  
$txt = "W3Schools.com";  
echo "I love " . $txt . "!";  
?>
```


<hr>

### Comments

- `//` or `#` : For single line comment.
- `/**/` : For multi line comment.

<hr>

### Variable Scope

#### 1. Global Scope

A variable declared **outside** a function has a GLOBAL SCOPE and can only be accessed outside a function.
```
<?php  
$x = 5; // global scope  
  
function myTest() {  
 // using x inside this function will generate an error  
 echo "<p>Variable x inside function is: $x</p>";  
}  
myTest();  
  
echo "<p>Variable x outside function is: $x</p>";  
?>
```

Workaround for this is to use **global keyword** before the variable
```
<?php  
$x = 5; // global scope  
  
function myTest() {  
	global $x;
	echo "<p>Variable x inside function is: $x</p>";  
}  
myTest();  
  
echo "<p>Variable x outside function is: $x</p>";  
?>
```

PHP also stores all global variables in an array called `$GLOBALS[_index_]`. The `index` holds the name of the variable. This array is also accessible from within functions and can be used to update global variables directly.

```
<?php  
$x = 5;  
$y = 10;  
  
function myTest() {  
 $GLOBALS['y'] = $GLOBALS['x'] + $GLOBALS['y'];  
}  
  
myTest();  
echo $y; // outputs 15  
?>
```

#### 2. Local Scope

A variable declared **within** a function has a LOCAL SCOPE and can only be accessed within that function:
```
<?php  
function myTest() {  
 $x = 5; // local scope  
 echo "<p>Variable x inside function is: $x</p>";  
}  
myTest();  
  
// using x outside the function will generate an error  
echo "<p>Variable x outside function is: $x</p>";  
?>
```

<hr>

### Static Variables

Normally, when a function is completed/executed, all of its variables are deleted. However, sometimes we want a local variable NOT to be deleted. We need it for a further job.

```
<?php  
function myTest() {  
 static $x = 0;  
 echo $x;  
 $x++;  
}  
  
myTest();  
myTest();  
myTest();  
?>
```

