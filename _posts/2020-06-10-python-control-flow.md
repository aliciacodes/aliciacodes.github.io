---
layout: post
title:  "Python Control Workflow"
date:   2020-06-10
categories: codecademy
---

Welcome to day 5 of the computer science track! Today, we're moving onto the Flow, Data, and Iteration module. The three modules in this section are *Python Control Flow*, *Python Lists*, and *Python Loops*. The first part of the module I'll cover is the *Python Control Flow*. 



Through this section, there will be one lesson, one quiz, two articles, and one project.



# Control Flow Lesson

![title](https://media1.giphy.com/media/h8y265b9iKtzKT0pDj/giphy.gif?cid=ecf05e47601707af035305c97383bc390045901d4bd731c0&rid=giphy.gif)

In every day life, we make many decisions like "Should I eat breakfast?" or "Can I sleep in today?". Depending on your answer, these questions may give different outcomes. Your mornings for example may look like this flowchart:

![Untitled Diagram](/assets/_img/Control_Flow.jpeg)

Programs go through a similar thing that we do. When a program is executed, they need to determine if some condition is met (ex. A number is greater than 4.) and if they are it will do something (ex. print "execute Order 66"). This is called the *Control Flow* of a program. In Python, a program is run from top to bottom.  In most programs, there are gateways (like the questions above) called *conditional statements*. This tells the computer to run certain lines of code. 

To build control flows, you must only see something as `True` or `False`  and a statement that only be true or false is called a *boolean statement*. A statement such as "My name is Jim" is objectively `True` or `False`. Your name is either Jim or not  Jim. A statement such as "Cats are the best mammals." cannot be classified as `True` or `False` since it is an opinion. Someone else might think dogs are the best mammal.

To create these boolean statements, you need to convert them into boolean expressions using *relational operators*. These operators compare two items and return whether they are `True` or `False`. There are two of these `==`  (equals) or `!=` (not equals).

```
>>> 1 == 1
True
>>> 2 != 1
True
>>> 4 == 1
False
>>> 2 != 2
False
```

There are even more relational operators such as greater than (`>`), less than (`<`), greater than or equal to (`>=`), and less than or equal to (`<=`). 

```
#Ex. In a theme park, you must be 40 in. to ride a rollercoaster. This function checks your height and sees if you can ride
def height_check(inches):
	if inches > 40:
		return True
```

Sometimes, conditional statements can include more than one boolean expression. To build larger ones, you can use *boolean operators* or *logical operators* to combine smaller expressions. There are three of these:

-  `and`
- `or`
- `not`

`and` takes multiple expressions and if they are all `True` then the expression returns `True`. If one is false, the entire expression if `False`. 

```
>>> (2 - 1 == 1) and (5 + 2 == 7)
True
>>> (6 - 1 == 5) and (4 < 2)
False 
```

`or` is much different in that if one smaller expression is `True` out of the larger expression, then the entire statement is `True`. 

```
>>> True or (3 + 13 == 8)
True
>>> (4 == 5) or (-1 > 9)
False
```

 `not` just reverses the boolean expression it is applied to. `False` becomes `True` and `True` becomes `False`. 

```
>>> not 3 - 2 == 1
False
>>> not 20 < 10
True
```

In programming, to signal a *conditional statement*, `if` statements are used. You can phrase these statements in an if-then manner. The statement we are checking is the `if` part and the action is in the second part of the statement `then`. 

```
If [it is a workday], then [wakeup at 6AM].
```

Here's how it looks in Python.  The only difference is that instead of a then there is a `:`. 

```
if it_is_a_workday:
	wake_up_6AM()
```

When there are many factors to consider in a function, there can get to be too many `if` statements. To control this, we can use `else` statements which is a blanket condition used when an if statement isn't met.

```
def height_check(inches):
	if inches > 40:
		return True
	else:
		return "Need to be taller to ride the rollercoaster"
```

 There can also be control flow issues when there are too many `if` statements. If two `if` statements meet the same criteria, then both if statements will be triggered. In most cases, only one `if` statement should trigger which is why we use `elif` statements which are triggered after each `if` statement and read top to bottom.

```
#Checking to see if a customer has a certain rewards membership status based on money spent at a makeup store.
def makeup_rewards(money_spent)
if money_spent >= 1000:
	print("Congrats! You have platinum status.")
elif money_spent >= 750:
	print("Congrats! You have gold status.")
elif money_spent >= 350:
	print("Congrats! You have silver status.")
else:
	print("Congrats! You have bronze status")
```

Finally, *try-catch* statements check for possible errors a user may run into. First, the try exception will be executed. If there are no exceptions then the try will terminate. If there is an exception such as a `NameError` or `ValueError` then the `except` will trigger.  

```
def divides(a,b):
	try:
		result = a/b
		print(result)
	except ZeroDivisionError:
		print("Can't divide by zero!")
```

The quiz was pretty much what you would expect so I'm not going to go in-depth about it.

# Python Code Challenges: Control Flow

This article was incredibly interesting since it included five Python emulators with five respective "challenge" problems. 

The first function involved two parameters: `base` and `exponent`, doing exponentiation on these parameters, and checking if the exponent is greater than a given number. 

The second function has five parameters `budget` , `food` , `electricity`, `internet`, and `rent`.  If the `budget` is less than or equal to the sum of the other four parameters, it returns `True`. Otherwise, the function returns `False`. 

The third function takes two parameters: `num1` and `num2` . If `num1` is more than double `num2` , return `True`, otherwise return `False`.

The fourth function takes one parameter `num`. The function returns `True` if `num ` is divisible by 10, otherwise return `False`. 

The fifth and final function has two parameters: `num1` and `num2`. If `num1` and `num2` don't sum to 10, return `True`, otherwise return `False`. 

In this exercises, I was making silly mistakes such as forgetting a `:` after an if statement, misspelling variable names. I was even making logical ones such as using a `>` sign instead of `<`. I looked this up on Google, feeling incompetent for making stupid syntactical errors. However, I found that it's pretty normal no matter how long you have been coding. Don't get discouraged by this!



# Advanced Python Code Challenges: Control Flow

![title](https://media1.giphy.com/media/9JADZJpiRRgUVDWiWs/giphy.gif?cid=ecf05e47dcbccae375529a6731d663316a3e92f0714798e4&rid=giphy.gif)

The first challenge function has three parameters: `num`, `lower`, and `upper`. This should return `True` if `num` is greater than or equal to `lower` and less than or equal to `upper`. Otherwise `False` is returned.

The second function has two parameters: `your_name` and `my_name`. If the names are the same return `True` . Otherwise, you return `False`.

The third function has one parameter: `num`.  For this question , you must use `>` or `<` to make a function tat always returns false. This is called a *contradiction* which you never want to do while programming. 

The fourth function has one parameter: `rating`. These were the instructions:

- If `rating` is between 0 and 5: `Avoid at all costs!`

- If `rating` is between 5 and 9: `This one was fun`
- If `rating` is at 9 or above: `Outstanding!`

The fifth function has three parameters: `num1` , `num2`, and `num3`. The function will return the largest number, if two numbers are tied return `it's a tie`.

I wish that they would split up these code challenges so I didn't have to do them back-to-back. I know these concepts, but for any beginner doing 10 coding challenges might be a bit rough.

# Project: Sal's Shipping

For this project, we want to make sure that any user has the best value in terms of shipping. There were three categories: ground, drone, and premium ground shipping (flat rate) each with different prices for different weight intervals (ex. 2lbs or less). There were two function calculated the price given the respective weight for each category of shipping. At the end, there was a large function created that used the smaller categorical function to determine what the cheapest shipping method was for the user. The steps of the project involved using functions along with `if`,  `elif`, and `else` to define boolean expressions that contained relational operators ( `<`, `>`, `>=`, and `<=`) mixed with logical operators (`and`) . 

If you are looking for an alternative to this project I recommend creating a "Guess the Number" game. In this game, you use the `random` library in Python to pick a random number and you have to guess the number that it picked.  



# Alternatives

There is a course on Conditionals and Control Flows for Python 2 on <a href = https://www.codecademy.com/learn/learn-python/modules/learn-python-functions-u-4>Codecademy</a>. The syntax between Python 2 and Python 3 are slightly different, but the concepts are all the same. 

In case you need a cheatsheet for all the Python operators you have learned so far, W3Schools has an excellent <a href = "https://www.w3schools.com/python/python_operators.asp">one</a>.

If you have any suggestions, be sure to comment down below!

That's another day in the books! See you tomorrow

