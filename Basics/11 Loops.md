### While Loop

```
while (_condition is true_) {  
 _code to be executed_;  
}
```

### do...while

```
do {  
  code to be executed;
 } while (condition is true);
```

### for Loop

```
for (_init counter; test counter; increment counter_) {  
 _code to be executed for each iteration;_  
}
```

### foreach

```
foreach ($_array_ as $_value_) {  
 _code to be executed;_  
}
```

```
<?php  
$colors = array("red", "green", "blue", "yellow");  
  
foreach ($colors as $value) {  
 echo "$value <br>";  
}  
?>
```

```
<?php  
$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");  
  
foreach($age as $x => $val) {  
 echo "$x = $val<br>";  
}  
?>
```

**Note:** We can use break and continue
