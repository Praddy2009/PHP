## PHP Data Types

Variables can store data of different types, and different data types can do different things.

PHP supports the following data types:

-   String
-   Integer
-   Float (floating point numbers - also called double)
-   Boolean
-   Array
-   Object
-   NULL
-   Resource

<hr>

### 1. Strings
A string is a sequence of characters, like "Hello world!". A string can be any text inside quotes. You can use single or double quotes:

```
<?php  
$x = "Hello world!";  
$y = 'Hello world!';  
  
echo $x;  
echo "<br>";  
echo $y;  
?>
```

### 2.Integer
An integer data type is a non-decimal number between -2,147,483,648 and 2,147,483,647.

Rules for integers:

-   An integer must have at least one digit
-   An integer must not have a decimal point
-   An integer can be either positive or negative
-   Integers can be specified in: decimal (base 10), hexadecimal (base 16), octal (base 8), or binary (base 2) notation

In the following example $x is an integer. The PHP var_dump() function returns the data type and value:

```
<?php  
$x = 5985;  
var_dump($x);  
?>
```

### 3. Float

A float (floating point number) is a number with a decimal point or a number in exponential form.

```
<?php  
$x = 10.365;  
var\_dump($x);  
?>
```


### 4. Boolean
A Boolean represents two possible states: TRUE or FALSE.

```
$x = true;  
$y = false;
```

### 5. Array
An array stores multiple values in one single variable.

```
<?php  
$cars = array("Volvo","BMW","Toyota");  
var\_dump($cars);  
?>
```

### 6. Object
Classes and objects are the two main aspects of object-oriented programming.

A class is a template for objects, and an object is an instance of a class.

When the individual objects are created, they inherit all the properties and behaviors from the class, but each object will have different values for the properties.

If you create a __construct() function, PHP will automatically call this function when you create an object from a class.

```
<?php  
class Car {  
	 public $color;  
	 public $model;  
	 public function __construct($color, $model) {  
		 $this->color = $color;  
		 $this->model = $model;  
	 }  
	 public function message() {  
	 	return "My car is a " . $this->color . " " . $this->model . "!";  
	 }  
}  
  
$myCar = new Car("black", "Volvo");  
echo $myCar -> message();  
echo "<br>";  
$myCar = new Car("red", "Toyota");  
echo $myCar -> message();  
?>
```

### 7. NULL 

Null is a special data type which can have only one value: NULL.

A variable of data type NULL is a variable that has no value assigned to it.

**Tip:** If a variable is created without a value, it is automatically assigned a value of NULL.

Variables can also be emptied by setting the value to NULL:

```
<?php  
$x = "Hello world!";  
$x = null;  
var_dump($x);  
?>
```


### 8. Resource

The special resource type is not an actual data type. It is the storing of a reference to functions and resources external to PHP.

A common example of using the resource data type is a database call.