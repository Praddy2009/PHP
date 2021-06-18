### pi()
The `pi()` function returns the value of PI:

<hr>

### min() max()
The `min()` and `max()` functions can be used to find the lowest or highest value in a list of arguments:

```
<?php  
echo(min(0, 150, 30, 20, -8, -200)); // returns -200  
echo(max(0, 150, 30, 20, -8, -200)); // returns 150  
?>
```

<hr>

### abs()

The `abs()` function returns the absolute (positive) value of a number:

```
<?php  
echo(abs(-6.7)); // returns 6.7  
?>
```

<hr>

### sqrt()

The `sqrt()` function returns the square root of a number:

```
<?php  
echo(sqrt(64)); // returns 8  
?>
```

<hr>

### round()

The `round()` function rounds a floating-point number to its nearest integer:

```
<?php  
echo(round(0.60)); // returns 1  
echo(round(0.49)); // returns 0  
?>
```

<hr>

### rand()

The `rand()` function generates a random number:

```
<?php  
echo(rand());  
?>
```

To get more control over the random number, you can add the optional _min_ and _max_ parameters to specify the lowest integer and the highest integer to be returned.

For example, if you want a random integer between 10 and 100 (inclusive), use `rand(10, 100)`:

```
<?php  
echo(rand(10, 100));  
?>
```
