---
layout: post
title:  "Introduction to Python Functions"
date:   2020-06-07
categories: codecademy
---

Welcome to day 2 of the Codecademy challenge! We are now in the second part of the "Introduction to Programming" module. Today we'll be covering functions. 

In this module, we'll have a lesson, a quiz, and a project. Let's do this!

# The Lesson on Python Functions
My notes are pretty in-depth and included activities that I did throughout the lesson. You can access the notes <a href = "https://github.com/aliciacodes/codecademy-notes/blob/master/computer-science-track/section-2/python-functions.md">here</a>.

In the lesson, we learned about how functions are just a collection of lines of code that we can repeat over and over again. The simple formula for writing a function header is `def` + function name + parenthesis + colon (`:`).  After this line, all lines below have to be indented, anything not indented is not part of the function. Here is an example:
```
def function_name():
	some code

````
You can add arguments to these functions to modify their operations by adding a variable in between the parenthesis. These are called parameters, and are defined like so:

```
def greet (weather):
    print("Hello!")
    print("It is " + weather + " today.")
    print("Have a great day!")

```
And now you must call the function with that argument.

```
greet("rainy")

```
You can have multiple parameters and even set a default value for them.
```
def greet(weather = "rainy", time_of_day) #not valid

def greet(weather, time_of_day = "day") #valid

```
Functions can return values so they can be modified later, These function values are saved in a variable.

```
# a function with return statement
def multiply_by_two(number):
	return number * 2
# saving result to a variable
result = multiply_by_two(6) #result in variable is 12
```

You can return multiple values and save them to multiple variables.

```
def multi(num1,num2):
    num1 = num1 * 2
    num2 = num2 / 4
    return num1, num2
result1, result2 = multi(3, 8)
``
And that's a really concise summary of what happened this module. If you want a more in-depth review, look at the summary!

# The Quiz
Again, the questions on the quiz are pretty basic and I've provided my own version of them <a href = https://github.com/aliciacodes/codecademy-notes/blob/master/computer-science-track/section-2/Codecademy-Python-3-Functions.apkg>here</a>. 

# The Project
The project was mostly just creating mathematical functions based upon Physics problems and saving the return value into variables. You can find that <a href = "https://github.com/aliciacodes/codecademy-notes/blob/master/computer-science-track/section-2/getting-ready-for-physics-class.py">here</a>

# Alternatives
Most of the information in this module is contained in <a href = "https://www.codecademy.com/learn/learn-python/modules/learn-python-functions-u-4">Python 2 Functions</a> module. Before taking this module, I would recommend taking <a href = "https://www.codecademy.com/learn/learn-python/modules/learn-python-conditionals-and-control-flow-u-4"> Python 2 Conditionals and Control Flow </a>. This course has a bit more extraneous material that are specific to Python 2. However, it still good to learn this stuff since a lot of knowledge is transferrable. 

Thanks for joining me for Day 2. I just finished the Introduction to Programming module and am moving onto Development Skills. So,for the next few days the focus will be on learning terminal commands and Git. Currently, I am about 4% of the way through the course so I still have a ways to go. Join me tomorrow to learn the basics of the terminal. 