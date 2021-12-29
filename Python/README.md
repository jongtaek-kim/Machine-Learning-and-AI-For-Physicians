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
```![paint_room](https://user-images.githubusercontent.com/44178167/147625547-75c15174-f4ff-4b70-805f-b7ed1dd2aecc.png)

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


## Excercise 3: Python Variables
### A variable is created the moment you first assign a value to it.
```bash
x = 5
y = "Elon"
print(x)
print(y)
```
&nbsp; 
### Variables do not need to be declared with any particular type, and can even change type after they have been set.
```bash
x = 4       # x is of type int
x = "Sally" # x is now of type str
print(x)
```
&nbsp; 
## Problem: How many cans of paint do you need for a house with 20 rooms?
<p align="center">
  <img width="596" height="476" src="https://github.com/jongtaek-kim/Machine-Learning-and-AI-For-Physicians/blob/28f2afe5e26a0157dc5b01820e1b8d698fa91bf8/docs/images/paint_room.png">
</p>

```bash
import math               # import a module        
small = 6 * 10            # area to paint for small wall  
big = 8 * 10              # area to paint for big wall
one = 2 *(big + small)    # area to paint for one room
all_rooms = 20 * one      # total area to paint
one_can_coverage = 5 * 350  # one can paint 5 walls, each wall has area of 350
cans = math.ceil(all_rooms / one_can_coverage)    # number of cans needed rounded up
print(cans)
```
&nbsp; 

## Excercise 4: Creating Functions In Python
### A function header specifies the names of the function and parameters.
### A function body is the code that determines the output.
<p align="center">
  <img width="502" height="390" src="https://github.com/jongtaek-kim/Machine-Learning-and-AI-For-Physicians/blob/72c81c356e9f1108b2fd333c9716ad29ead555b3/docs/images/function.png">
</p>

### Python Function #1
```bash
def sub(first, second):
       return first - second

print(sub(10, 5))
```
&nbsp; 
### Python Function #2
```bash
def f(x, y, z):
       A = (x + y + z) ** 2 
       return A

print(f(1, 2, 3))
```
&nbsp; 
### Python Function #3: Calculating Parking Charges.
```bash
WEEK_CHARGE = 100
DAY_CHARGE = 20
DAYS_IN_WEEK = 7

def parking_fee(total_days):
    ## Determine number of weeks, days remaining
    weeks = total_days // DAYS_IN_WEEK
    days = total_days % DAYS_IN_WEEK
    
    ## Calculate cost of weeks, days remaining
    week_cost = weeks * WEEK_CHARGE
    day_cost = days * DAY_CHARGE
    
    ## TOTAL COST
    return week_cost + day_cost

print(parking_fee(31))
```
&nbsp; 

### Python Function #4: Calculating Parking Charges For Each Customer.
```bash
WEEK_CHARGE = 100
DAY_CHARGE = 20
DAYS_IN_WEEK = 7

def parking_fee(total_days):
    ## Determine number of weeks, days remaining print(int(7.4))
    weeks = total_days // DAYS_IN_WEEK
    days = total_days % DAYS_IN_WEEK
    
    ## Calculate cost of weeks, days remaining
    week_cost = weeks * WEEK_CHARGE
    day_cost = days * DAY_CHARGE
    
    ## TOTAL COST
    return week_cost + day_cost

print("You owe $",parking_fee(int(input("How many days did you park?:"))))
print("Cash or Credit Card Accepted")
```
&nbsp; 

### Python Function #5: Determine Targe Heart Rate For An App.
```bash
def target(AGE, REST_HEART, INTENSITY):
    ##DETERMINE MAX HR
    max_heart = 220 - AGE
    
    ##DETERMINE RESERVE
    reserve = max_heart - REST_HEART
    
    ##TARGET HR
    return (REST_HEART + INTENSITY * reserve)

print("Your Target Heart Rate Is:",target((int(input("Enter Your Age:"))), (int(input("Enter Your Rest Heart Rate:"))), (float(input("Enter Workout Intensity (range from 0.1 to 1.0):")))))
```
&nbsp; 

### Python Function #6: Branching and Multiple Sets of Instructions
<p align="center">
  <img width="629" height="463" src="https://github.com/jongtaek-kim/Machine-Learning-and-AI-For-Physicians/blob/2054b8d64549d1bb655acb9df930a489e179cdf4/docs/images/if.png">
</p>

### Python Function #7: Car Safety Recommendation For Your Child.
```bash
### car_safety
def car_safety(weight, height, age):
#kg, cm, years
    if weight >= 36 or height >= 145 or age >= 8:
        return("Seat belt")
    elif 18 <= weight:
        return("Booster")
    elif 9 <= weight:
        return("Forward-facing car seat")
    else:
        return("Backward-facing car seat")

print ("Recommend",car_safety(40, 150, 10))
print ("Recommend",car_safety(35, 150, 8))
print (Recommend",car_safety(20, 140, 5))

#print ("Recommend",car_safety((int(input("Enter Child's Weight in kg:"))), (int(input("Enter Child's Height in cm:"))), (int(input("Enter Child's Age:")))))
```
&nbsp; 

### Python Function #8: Run A Function Using While And A Condition
<p align="center">
  <img width="624" height="408" src="https://github.com/jongtaek-kim/Machine-Learning-and-AI-For-Physicians/blob/dc10341a80de8424fd5f4720ba1bf945423b6a3b/docs/images/while.png">
</p>


```bash
### say_uncle while function
def say_uncle():
    response ='aunt'
    while response != 'uncle':
        response = input("I'll quit if you say 'uncle':")
    print("You said uncle, so I quit")
say_uncle()
```
&nbsp;

### Python Function #9: Write A Function To Replace An Item In A List.
```bash
def replace(List, old, new):
    if old in List:
        where = List.index(old)
        List.remove(old)
        List.insert(where, new)
        return List
    
    else:
        return List
    
print(replace([1,2,3,4], 4, 9))
```
&nbsp;

### Python Function #10: Write A Function To Move An Item In A List.
```bash
def move_to_front(List, item):
    if item in List:
        List.remove(item)
        List.insert(0,item)
        return List
    else:
        return [List, item]
    
print(move_to_front([1,2,3,4], 4))   
```
&nbsp;



### Python Function #11: Making Uses Of Multiple Lists Provided And Making A Function To Spell Out The Number Entered.
```bash
UNITS = ["zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"]

TENS = ["", "", "twenty", "thirty", "forty", "fifty", "sixty", "seventy", "eighty", "ninety"]

TEENS = ["ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "sixteen", "seventeen", "eighteen", "nineteen"]

TWENTY = 20
TEN =10

def two_digit_word(num):
    if num < 10:
        return UNITS[num]
    
    if num < 20:
        return TEENS[num % 10]
    
    else:
        return (TENS[num // 10] + "-" + UNITS[num % 10])
    
print("Your number is spelled",two_digit_word(22))

#print("Your number is spelled",two_digit_word(int(input("Enter a number between 0 and 99:"))))
```
&nbsp;


## Review Writing A Python Program
<p align="center">
  <img width="552" height="442" src="https://github.com/jongtaek-kim/Machine-Learning-and-AI-For-Physicians/blob/391704a663ab19a8ac3bb6d79459ec582ecc3792/docs/images/writing_program.png">
</p>





