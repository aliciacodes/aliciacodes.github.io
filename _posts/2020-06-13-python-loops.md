---
layout: post
title:  "The Boredless Tourist"
date:   2020-06-13
categories: codecademy
---

Welcome to day 8! Today, we're finally finishing the "Flow, Data, and Iteration" module. We'll be working on Python loops. 

In this section, there are two lessons, a quiz, and a project.



# Loops

![coffee break starbucks GIF](https://media1.giphy.com/media/mriHtoQjgsrQY/giphy.gif?cid=ecf05e47e090510f6f53f6dd7ddb2e0cf25474b59ea1d99a&rid=giphy.gif)

Today, you want to get Starbucks, but you want to see the whole menu first. This is how we would do this with the knowledge we have so far:

```
starbucks_menu = ["vanilla_latte", "caffe_mocha", "flat_white", "chai_latte", "cold_brew", "smores_frap"]
print(starbucks_menu[0])
print(starbucks_menu[1])
print(starbucks_menu[2])
print(starbucks_menu[3])
print(starbucks_menu[4])
```

Well, this seems incredibly inefficient and can lead to messy errors.  Luckily, in Python and most other programming languages, there is an easier way of repeatedly using (*iterating*) or performing certain code on lists called *loops*. There are many kinds of loops:

1. Loops that can move through each item (*for loop*)
2. Ones that go until we give them a condition to stop at (*while loop*)
3. Create new lists through loops (*list comprehension*)

Each of these loops will use *iteration* which takes an element and uses it or modified it in some way. An *iterable* is an object like a list, a string, or a range that contains multiple items you can loop through. 

Let's start with a *for* loop. Here's what it looks like:

```
starbucks_menu = ["vanilla_latte", "caffe_mocha", "flat_white", "chai_latte", "cold_brew", "smores_frap"]
for drink in starbucks_menu:
	print(drink)
```

Here is a formula on how to write it:

```
for <temp variable> in <iterable>:
		<action>
```

Comparing this to the example, we can see that `drink` is the single element we are currently using/modifying (in this case, we are printing it). This is called a *temporary variable*. `starbucks_menu` is the list or iterable that we are using. The `print(item)` is the action we are performing here.

NOTE: 

- Temporary variables can be named whatever you want and don't have to be initialized beforehand. 

- Every action (like print()) must be indented beneath the `for` loop. If elements aren't indented, you receive an `IndentationError`.



We looked at the first four items on the Starbucks menu and they seem the most appealing. How do we limit the menu to those four items? We use the `range` function we learned earlier on. Remember, `range` returns a list from 0 to `n-1`.

```
menu_length = range(4)
for index in <list of length 4>:
	print(starbucks_menu[index])
```

You found a 50% off coupon for your Starbucks drink and now want to divide by the menu by 2.

```
starbucks_cost = [4, 5, 4, 3]

for cost in starbucks_cost:
	starbucks_cost.append(cost/2)
```

Oh no, something went wrong! In this loop, we are dividing the cost by 2 and then appending it back to the `starbucks_cost` so the list keeps growing forever. This is what we call an infinite loop, it never terminates. This is pretty dangerous as it takes up memory in your computer and can cause issues. If this accidentally happens, you can hit `control` + `c` on your keyboard to terminate the program.

Finally, you've decided to order a `chai latte` , we don't want to continue through the menu after that. 

```
starbucks_menu = ["vanilla_latte", "caffe_mocha", "flat_white", "chai_latte", "cold_brew", "smores_frap"]

#We want to order a chai latte
for drink in starbucks_menu:
  if drink == "chai_latte":
    print("Chai latte added to your order!")
```

The code goes through each `drink` in `starbucks_menu` and finds a match. After finding the chai latte, we don't need to continue on in the list.

So, we found it. How can you stop the for loop so it doesn't continue? You can use a `break` statement which goes to the code outside the loop.

```
starbucks_menu = ["vanilla_latte", "caffe_mocha", "flat_white", "chai_latte", "cold_brew", "smores_frap"]

#We want to order a chai latte
for drink in starbucks_menu:
  print(drink)
  if drink == "chai_latte":
  break
print("Chai latte added to your order!")
```

We would get this output, proving the break statement works!

```
vanilla_latte
caffe_mocha
flat_white
chai_latte
Chai latte added to your order!
```

What if we want to skip certain values while iterating?  What if we want to print out all numbers that aren't multiple of two. In Python, we can do this with the `continue` statement to move onto the next element without breaking out of the loop.

```
num_list = range(10)

for i in num_list:
  if i % 2 == 0:
   	 continue
  print(i)
```

```
1
3
5
7
9
```

When we find a multiple of 2, the `continue` moves the index to the next value in the list without printing the value.

The `while` loop performs an action/modifies an element until a condition is reached.

While loops are used to iterate through lists, like loops:

```
legendary_pokemon = ["Articuno", "Zapdos", "Moltres", "Mew, Mewtwo"]

index = 0
while index < len(legendary_pokemon):
	print(legendary_pokemon[index])
	index += 1
```

When the condition (`index < len(legendary_pokemon)`) is satisfied, the code inside the `while` loop runs.

While loops are useful when you don't know how many iterations it will take to satisfy a condition



What we have a list of lists? How can we loop through all the individual elements contained? We can use two for loops which are called *nested for loops*.

```
sinnoh_gym_pokemon = [["Geodude", "Onix", "Cranidos"], ["Turtwig", "Cherubi", "Roserade"], ["Meditite", "Machoke", "Lucario"]]
for team in sinnoh_gym_pokemon:
	for pokemon in team:
		print(pokemon)
```

 The outer `for` loop will read `team` or each individual list contained within `sinnoh_gym_pokemon` element (ex. `["Geodude", "Onix", "Cranidos"]`) and the inner `for` loop will read the individual  `pokemon` elements of that list. (ex. `Geodude`) This is the output of the code we ran above:

```
Geodude
Onix
Cranidos
Turtwig
Cherubi
Roserade
Meditite
Machoke
```

Finally, let's talk about list comprehensions which I mentioned in the beginning. A list comprehension is a precise way to create lists that takes less lines of code. Let's say we just want a list of multiples of 5, to do that we would need to do this:

```
nums = range(20)
divi_by_5 = []
for num in nums:
	if num % 5 == 0:
		divi_by_5.append(num)
print(divi_by_5)
```

The output:

```
[0, 5, 10, 15]
```

Here's the list comprehension:

```
divi_by_5 = [num for num in nums if num % 5 == 0]
```

This list comprehension

1. Takes an element in `words`
2. Assigns the element to a variable called `num`.
3. Checks if `num % 5 == 0`, if it is it adds it to `divi_by_5`. If not, nothing happens.

If there isn't any `if` statements, then there will just be a copy of `divi_by_5`.

What if you wanted to modify each multiple of 5 and add `1` to it? You can do that like this: 

Now, we want to add a string saying  " `num` is a multiple of 5!"

```
nums = [num + " is a multiple of 5!" for num in divi_by_5]
```

This takes a `num` in `divi_by_5` , assigns the integer to a variable `num`, concatenates the `num` with "is a multiple of 5! ", and finally appends to a new list called `nums`. This will repeat for the remainder of the list. You can also do this  with numbers to add, subtract, divide, or multiplying values.

The lesson's finished now! 



# The Project: Carly's Clipper

In this project, you take on the role of a data analyst at a hair salon. You are helping the owner Carly figure out some metrics and you are provided with three lists:

- `hairstyles` : the names of the cuts offered at Carly’s Clippers.
- `prices` : the price of each hairstyle, goes along with the `hairstyle` list. 
- `last_week`: The amount each hairstyle was purchased last week.

This project has twelve steps. The first involves making a variable to calculate the average. Then, you must iterate through the `prices` list and add it to the variable you made in the last step to create a sum of the `prices` list. After that, a new variable is created to take the sum of the `prices` list and divide it by the length of the list. The fourth instruction is to print out the list. Following that step, you must use list comprehension to make a new list where all the `prices` five dollars cheaper. The following step is just printing the list you made. The seventh step is making a variable to keep track of revenue she made last week. In the next few steps, it is making a for loop that goes from 0 to the length of `hairstyles`. Within the `for` loop, you must multiply the `price` by `last_week`. After this, you print the variable, divide by 7 and save that in a new variable, and print again. Lastly, you use list comprehension again to get a list of hairstyles that cost less than 30 dollars. 

This project was pretty basic and easy to figure out. A free, alternative project to this would be the <a href = "https://www.geeksforgeeks.org/python-program-implement-rock-paper-scissor-game/">Rock, Scissors, Python project.</a> 



# Lesson: Python Challenge

This lesson was just a series of ten Python problems. The first function takes a list of integers (numbers) as a parameter and returns a count of how many of those are multiples of ten using a `for` loop. Next, we have a function that takes a list of strings as a parameter that has a list of names, you create an empty list that will store a greeting for each person, and use a `for` loop to append a phrase and a name. The third problem took a integer list as a parameter. It involved using a `while` loop and slicing the list to remove the front element of the list until the first element is even. This is definitely a trickier problem to solve when you don't know how to remove elements from a list. The fourth problem took a list of numbers once again, you had to make a new list to add each element that had an odd index using a for loop. Fifth, a function took two lists, made you make a new list, and required nested for loops to raise all items in the first list to the elements in the second list. Sixth, was creating a function that took two lists and returned whatever list had the greatest sum of elements. To solve this, I needed a for loop and a few `if` statements. The seventh function required taking a list as a parameter and sum the list until the sum is greater than `9000`. So I used a new variable called `sum`, a `for` loop, and an `if` and `else` statement to solve it. The next function takes a list of numbers as a parameter to determine which element is the greatest in the list. I didn't set the variable meant to hold the greatest number equal to the first element of the list argument. Whoops!

The ninth function involved taking two lists of equal size and returning a list of indices where the values were equal. The final function took two lists of the same size and checked if they were reversed. 



I would recommend this <a href = "https://www.w3resource.com/python-exercises/python-conditional-statements-and-loop-exercises.php">W3resource</a> here. This has 44 problems to help you master loops, much more than what Codecademy has!

# Free Alternatives

- Lesson: https://www.codecademy.com/learn/learn-python/modules/learn-python-functions-u-4
- Project: <a href = "https://www.geeksforgeeks.org/python-program-implement-rock-paper-scissor-game/">Rock, Scissors, Python project</a>
- Coding Challenge: <a href = "https://www.w3resource.com/python-exercises/python-conditional-statements-and-loop-exercises.php">W3resource</a>



What an intense few days! I think from here out this challenge is going to get a lot harder. See you tomorrow!
