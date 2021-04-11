# PHP

Content index:

* [Introduction](#introduction)
* [Basic coding standards](#basic-coding-standards)
* [Print-out commands](#print-out-commands)
* [Variables](#variables)
* [Comments](#coments)
* [Operators](#operators)
* [Conditional Statements](#conditional-statements)
* [Loops](#loops)

## Introduction

Definition: PHP (Hyper Text Preprocesor) is backend (server side) programing language.

Prerequisites:

* Basic knowledge about HTML and CSS
* Web Server

Start built-in web server in PHP 5.4+:

``` bash
php -S localhost:8000
```

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

Types of variables:

* String
* Integer
* Float (floating point numbers - also called double)
* Bolean (a Boolean represents two possible states: TRUE or FALSE)
* Array (indexed, associative)
* Object
* NULL
* Resource

Examples of vatiable types:

```php
# String
$sentence = "Hello World";
# Integer
$age = 5;
# Float
$price = 12.58;
# Bolean (have )
$is_logged_in = true;
# Array: Indexed
$mixed = [
  "Hello World",
  12,
  true,
  ["red", "blue", "yellow"]
];
# Array: Associatoive
$car = [
  'Make' => 'Audi',
  'Model' => 'A6',
  'Color' => 'Blue'
];
# Object
class HumanBeing {
  // Properties
  private $gender;
  private $age;
  private $weight;
  private $words;
  // Methods
  public function __construct($gender, $age, $weight) {
    $this->gender = $gender;
    $this->age = $age;
    $this->weight = $weight;
  }
  public function sayWord($word) {
    echo $word;
  }
}
```

## Comments

Use for explaining code.

```php
// This is comment

# This is comment

/*
* This is block commnet
*/
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

* While Loop (first check statement then execute code)

```php
while (statement){
    # code...
}
```

* Do While Loop (first execute code, then check statement)

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
