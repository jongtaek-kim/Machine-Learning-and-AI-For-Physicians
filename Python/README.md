## In Some Ways, Learning Program Language And Coding Is Like Learning A Foreign Language.
### You have to learn the vocabularies, syntax, and semantics.

<p align="center">
  <img width="200" height="200" src="https://github.com/jongtaek-kim/Machine-Learning-and-AI-For-Physicians/blob/065e0b1d867fc918169ba1ea6c4a01a10bd7f7d9/docs/images/python.png">
</p>

## In this Python exercise, we will cover some of basic Python syntax and semantics to understand how a program is written. This will serve as a building block for understanding how ML algorithms run. 

## Excercise 1: Built In Functions
### Import a module (first line of program)
```bash
$ import math
```
&nbsp; 
### Use functions and constants from the module
```bash
$ print(math.sqrt(5))
$ print(math.pi)
```
&nbsp; 
### List everything in the module
```bash
$ print(dir(math))
```
&nbsp; 
### Import a single item 
```bash
$ from math import sqrt
$ print(sqrt(5))
```
&nbsp; 

### "input" function is already built in Python3
```bash
$ print(2*int(input("Enter a number:")))
```
&nbsp; 

### List of Built-in Python Functions [Here](https://docs.python.org/3/library/functions.html#int)

## Excercise 2: Data Type
### type() is another built-in function 
```bash
$ print(type(5))
$ print(type (5.0))
$ print(type("string"))
```
&nbsp; 
### An int is short for integer.
### A float is a number with a decimal place - very useful for representing things like weights or proportions.
### Strings are used in all modern programming languages to store and process textual information
###       


### What is wrong with this code?
```bash
$ print(Hello World)
```
&nbsp; 

### Correct way to print a string.
```bash
$ print("Hello World")
```
&nbsp; 


### True Division uses the slash (/) character as the operator sign. It always gives us a float.
```bash
$ print(10/3)
$ print(10.5/3.5)
$ print(11/3)
```
&nbsp; 

### Floor Division- The operator "//" performs floor division
```bash
$ print(9//3)
$ print(10//3)
$ print(11//3)
```
&nbsp; 

### What is the result from this code?
```bash
$ print(int(7.4))
```
&nbsp; 
### The function int forms an integer by cutting off all digits after the decimal point.


## Excercise 2: Python Variables
### A variable is created the moment you first assign a value to it.
```bash
$ print(type(5))
$ print(type (5.0))
$ print(type("string"))
```
&nbsp; 







