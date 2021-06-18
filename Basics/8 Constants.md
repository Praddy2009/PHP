A constant is an identifier (name) for a simple value. The value cannot be changed during the script.

A valid constant name starts with a letter or underscore (no $ sign before the constant name).

To create a constant, use the `define()` function.

**Syntax**
```
define(_name_, _value_, _case-insensitive_)
```

**Parameters:**
-   _name_: Specifies the name of the constant
-   _value_: Specifies the value of the constant
-   _case-insensitive_: Specifies whether the constant name should be case-insensitive. Default is false

<hr>

- **Case-sensitive**
	```
	<?php  
	define("GREETING", "Welcome to W3Schools.com!");  
	echo GREETING;  
	?>
	```

- **Case-insensitive**
	```
	<?php  
	define("GREETING", "Welcome to W3Schools.com!", true);  
	echo greeting;  
	?>
	```

<hr>

### Constant Arrays

```
<?php  
define("cars", [  
 "Alfa Romeo",  
 "BMW",  
 "Toyota"  
]);  
echo cars\[0\];  
?>
```

**Note:** Constants are automatically global and can be used across the entire script.
```
<?php  
define("GREETING", "Welcome to W3Schools.com!");  
  
function myTest() {  
 echo GREETING;  
}  
   
myTest();  
?>
```


