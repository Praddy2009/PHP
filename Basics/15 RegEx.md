A regular expression is a sequence of characters that forms a search pattern. When you search for data in a text, you can use this search pattern to describe what you are searching for.

## Syntax

In PHP, regular expressions are strings composed of delimiters, a pattern and optional modifiers.

```
$exp = "/w3schools/i";
```

In the example above, `/` is the **delimiter**, _w3schools_ is the **pattern** that is being searched for, and `i` is a **modifier** that makes the search case-insensitive.

The delimiter can be any character that is not a letter, number, backslash or space. The most common delimiter is the forward slash (/), but when your pattern contains forward slashes it is convenient to choose other delimiters such as # or ~.

<hr>

## Regular Expression Functions

PHP provides a variety of functions that allow you to use regular expressions. The `preg_match()`, `preg_match_all()` and `preg_replace()` functions are some of the most commonly used ones:

![[Pasted image 20210618204837.png]]

### 1. preg_match()

```
<?php  
$str = "Visit W3Schools";  
$pattern = "/w3schools/i";  
echo preg_match($pattern, $str); // Outputs 1  
?>
```

### 2. preg_match_all()

```
<?php  
$str = "The rain in SPAIN falls mainly on the plains.";  
$pattern = "/ain/i";  
echo preg_match_all($pattern, $str); // Outputs 4  
?>
```

### 3. preg_replace()

```
<?php  
$str = "Visit Microsoft!";  
$pattern = "/microsoft/i";  
echo preg_replace($pattern, "W3Schools", $str); // Outputs "Visit W3Schools!"  
?>
```

![[Pasted image 20210618221504.png]]

![[Pasted image 20210618221521.png]]

![[Pasted image 20210618221644.png]]

![[Pasted image 20210618221734.png]]


## Grouping

You can use parentheses `( )` to apply quantifiers to entire patterns. They also can be used to select parts of the pattern to be used as a match.

```
<?php  
$str = "Apples and bananas.";  
$pattern = "/ba(na){2}/i";  
echo preg\_match($pattern, $str); // Outputs 1  
?>
```