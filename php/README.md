# PHP

Prerequisites: basic knowledge about HTML and CSS.

PHP (Hyper Text Preprocesor) is backend (server side) programing language.

Start built-in web server in PHP 5.4+:

``` bash
php -S localhost:8000
```

Content:

* [Basic coding standards](#basic-coding-standards)
* [Print-out commands](#print-out-commands)
* [Variables](#variables)
* [Comments](#coments)
* [Internal function in PHP](#internal-function-in-php)
* [Data tupes](#data-types)
* [Operators](#operators)
* [Conditional Statements](#conditional-statements)
* [Loops](#loops)
* [User defined Functions](#user-defined-functions)
* [Include documents in PHP](#include-documents-in-php)
* [Global and Local scope](#global-and-local-scope)
* [Super Globals](#super-globals)
* [Classes](#classes)

## Basic coding standards

PSR-0, PSR-1:

* MUST start and end php code with

  ```php
  <?php
    # code...
  ?>
  ```

* MUST use only UTF-8 without BOM
* For properties SHOULD be used $StudlyCaps, $camelCase or $under_score names
* Method named MUST be declared in camelCase()

## Print-out commands

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

* strlen($str) - length of $str
* str_word_count($str) - numer of words in $str
* strrev($str) - reversing characters in $str
* strpos($str, $x) - position of $x in $str
* str_replace($x, $y, $str) - in $str look for $x and replace with $x
* date()

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

* Aritmetic Operators: +, -, *, /, %, **
* Assigment Operators: =, +=, -=, *=, /=, %=, **=
* Comparison Operators: ==, ===, !=, !==, <, >, >=, =<, !, <>
* Increment/Decrement Operators: ++, --
* Logical Operaters: AND, &&, OR, ||, XOR

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
    # code...
}
```

* Do While Loop

  First execute code, then check statement

```php
do {
    # code...
} while (statement)
```

* For Loop

```php
for (i=0; i<5; i++) {
    # code...
}
```

* Foreach Loop

```php
foreach ($variable as $key => $value) {
    # code...
}
```

## User defined Functions

General rule: "One function done one thing".

```php
function myFunction($arg) { # $arg is optional
    # code
}
```

Rule about arguments:

* function can have argument or arguments, and this is optional
* argument can be non-default, default or optional
* non default arbument/s MUST be first
* default argument must be on the right side of any non-default arguments
* optional arguments must be equal NULL
* max number of arguments is around five

## Include documents in PHP

```php
include 'path_to_file';
include_once 'path_to_file';
require 'path_to_file';
require_once 'path_to_file';
```

## Global and Local scope

Outside functions is Global scope.
Inside functions is Local scope.

## Super Globals

youtube
<https://www.youtube.com/watch?v=sBfSLbMnId0&list=PL0eyrZgxdwhwBToawjm9faF1ixePexft-&index=24>
<https://www.youtube.com/watch?v=MsgJc2Uy-BY&list=PL0eyrZgxdwhwBToawjm9faF1ixePexft-&index=25>

## Classes

What is the difference between public, private, and protected?
<https://stackoverflow.com/questions/4361553/what-is-the-difference-between-public-private-and-protected>
