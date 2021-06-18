### The echo

The `echo` statement can be used with or without parentheses: `echo` or `echo()`.

```
<?php  
echo "<h2>PHP is Fun!</h2>";  
echo "Hello world!<br>";  
echo "I'm about to learn PHP!<br>";  
echo "This ", "string ", "was ", "made ", "with multiple parameters.";  
?>
```

### The print

The `print` statement can be used with or without parentheses: `print` or `print()`.

```
<?php  
print "<h2>PHP is Fun!</h2>";  
print "Hello world!<br>";  
print "I'm about to learn PHP!";  
?>
```


### Differences
-	`echo` has no return value while `print` has a return value of 1 so it can be used in expressions.
-	`echo` can take multiple parameters (although such usage is rare) while `print` can take one argument.
-	`echo` is marginally faster than `print`.

