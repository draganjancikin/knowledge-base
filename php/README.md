# PHP

Prerequisites: basic knowledge about HTML and CSS.

PHP (Hyper Text Preprocesor) is backend (server side) programing language.

Start built-in web server in PHP 5.4+:

``` bash
php -S localhost:8000
```

## Printout command

``` php
echo "Hi there";
print "Dragan";
```

## Variables

Patern: <variable_name> = "<variable_value>";

``` php
$name = "Dragan";
```

## Comments

Use for explaining code.

```php
// This is comment

/*
* This is block commnet
*/
```

## Internal function in PHP

strlen($str) - length of $str
str_word_count($str) - numer of words in $str
strrev($str) - reversing characters in $str
strpos($str, $x) - position of $x in $str
str_replace($x, $y, $str) - in $str look for $x and replace with $x
date();

## Data tupes

* String

```php
  $name = "Dragan";
```

* Integer (numbers)

```php
  $age = 47;
```

* Float (decimal numbers)

```php
  $price = 25.99;
```

* Boolean (true or false)

```php
  true = 1
  false = 0
```

* Array

```php
  # Indexed Array
  $names = array("Dragan", "Milan", "Mirjana");

  # Associative Array
  $person = array(
    'name' => 'Dragan',
    'age' => 47,
    'city' => 'Tovarisevo'
  );
```

## Operators

* Aritmetic Operators
  +, -, *, /, %, **

* Assigment Operators
  =, +=, -=, *=, /=, %=, **=

* Comparison Operators
  ==, ===, !=, !==, <, >, >=, =<, !, <>

* Increment/Decrement Operators
  ++, --

* Logical Operaters
  AND, &&, OR, ||, XOR

## Conditional Statements

* if

* if-else

* if-elseif-else

* switch

## Loops

* While Loop

  First check statement then execute code

```php
while (statement){
    # code
}
```

* Do While Loop

  First execute code, then check statement

```php
do {
    # code
} while (statement)
```

* For Loop

```php
for (i=0; i< 5; i++) {

}
```

* Foreach Loop

```php
foreach ($variable as $key => $value) {
    # code...
}
```

youtube
<https://www.youtube.com/watch?v=uOLGQ9ZoOSc&list=PL0eyrZgxdwhwBToawjm9faF1ixePexft-&index=22>
