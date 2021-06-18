An array is a special variable, which can hold more than one value at a time.

```
<?php  
$cars = array("Volvo", "BMW", "Toyota");  
echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";  
?>
```


<hr>

### Length of array \[count()\]
```
<?php  
$cars = array("Volvo", "BMW", "Toyota");  
echo count($cars);  
?>
```


<hr>

In PHP, there are three types of arrays:

-   **Indexed arrays** - Arrays with a numeric index
-   **Associative arrays** - Arrays with named keys
-   **Multidimensional arrays** - Arrays containing one or more arrays


<hr>

### 1. Indexed Arrays

There are two ways to create indexed arrays. 
- The index can be assigned automatically (index always starts at 0), like this:
	```
	$cars = array("Volvo", "BMW", "Toyota");
	```
- or the index can be assigned manually:
	```
		$cars[0] = "Volvo";  
		$cars[1] = "BMW";  
		$cars[2] = "Toyota";
	```
	
<hr>

### 2. Associative Arrays

Associative arrays are arrays that use named keys that you assign to them.
There are two ways to create an associative array:

- 
  ```
  	$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");
  ```

- 
	```
	$age['Peter'] = "35";  
	$age['Ben'] = "37";  
	$age['Joe'] = "43";
	```
	
**Looping through an array**

```
<?php  
$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");  
  
foreach($age as $x => $x_value) {  
 echo "Key=" . $x . ", Value=" . $x_value;  
 echo "<br>";  
}  
?>
```

<hr>

### 3. Multidimensional Array

A multidimensional array is an array containing one or more arrays.

PHP supports multidimensional arrays that are two, three, four, five, or more levels deep. However, arrays more than three levels deep are hard to manage for most people.

![[Pasted image 20210617131340.png]]

```
$cars = array (  
 array("Volvo",22,18),  
 array("BMW",15,13),  
 array("Saab",5,2),  
 array("Land Rover",17,15)  
);
```


<hr>

### PHP - Sort Functions For Arrays

In this chapter, we will go through the following PHP array sort functions:

-   `sort()` - sort arrays in ascending order
-   `rsort()` - sort arrays in descending order
-   `asort()` - sort associative arrays in ascending order, according to the value
-   `ksort()` - sort associative arrays in ascending order, according to the key
-   `arsort()`- sort associative arrays in descending order, according to the value
-   `krsort()` - sort associative arrays in descending order, according to the key