---
layout: post
title:  "Python Lists Part 1"
date:   2020-06-11
categories: codecademy
---

Welcome to day 6! We're moving on from control flow to Python lists. I'm breaking this part of the module into two parts since there are 2 lessons, 2 quizzes, 2 projects, 2 articles, and 1 video. That's nine activities in total! So, in this part I'll cover 1 lesson, 1 quiz, and 1 project.



# Creating and Modifying Lists in Python

![Nope not that kind of list!](https://media.giphy.com/media/B7o99rIuystY4/giphy.gif)

In Python, a *list* is an ordered set of objects. 

Think about ordering people by youngest to oldest in a college classroom.

- Paige is 28 years old.
- Cristine is 20 years old.
- Ben is 25 years old.
- James is 18 years old.

To form this list, you need:

1. It begins with an opening bracket `[`and ends with a square bracket `]`.
2. Each item is separated by a comma (`,`)
3. To make it more readable, a space (` `) should be inserted after the comma. You don't have to, but it does make it easier.

```
ages = [28, 20, 25, 18]
```

A list doesn't just have to have numbers, it can have strings too!

```
names = ['Paige', 'Cristine', 'Ben', 'James']
```

There can even be **multiple** data types in one list.

```
mixed_list = ['James',18]
```

Lists can even have lists in them! If you want to have a small list of student's names and ages you can do that!

```
age = [['Paige',28], ['Ben', 25], ['James', 18], ['Cristine', 20]]
```



What if you have two lists (one with people's name, one with people's ages) how do we add these lists together to create one list that pairs the respective name with their age? 

There is a function in Python called the `zip` function. `zip` can take two (or more) lists as inputs and returns one object that contains each a list of pairs. When using `zip` , a `zip` object is created and is not your usual list in Python. So if you would like to print the list, you must convert it back to a  list using the`list()` functions. 

```
zipped_list = zip(name,age)
print(list(zipped_list))
# returns [('Paige', 28), ('Cristine', 20), ('Ben', 25), ('James', 18)]
```



So far, we've looked at lists that have information already in them. But what if you wanted to make a list that was empty? You can do that in Python and instantiate a list like this:

```
empty_list = []
```



Now that we have an `empty_list `, we want to put stuff in it right? To do that, we use a method called `.append()` . Let's add a `5` to the list.

```
empty_list.append(5)
print(empty_list)
# [5]
```

When a list already has an item, the `.append()` function will simply add it onto the name of the list. 

```
empty_list.append(20)
print(empty_list)
# [5, 20]
```

NOTE: You must put the list name before the function unlike other functions like `zip()` or `print()`.



When you must add two lists or a list and elements together (not in pairs), you can use the plus sign (`+` ) . These lists must be used with already created lists. 

```
#Below, there are a list of cats that are in a rescue shelter. 

cat = ['Oreo', 'Peanuts', 'Rocky']

Two new kittens arrive into the shelter and they are named Sunny and Shadow.

>>> cats_in_shelter = cat + ['Sunny', 'Shadow']
>>> print(cats_in_shelter)
['Oreo', 'Peanuts', 'Rocky', 'Sunny', 'Shadow']
```

To add a single element , you have to put it in a list with brackets (`[]`).

```
mult_of_ten = [10, 20, 30, 40, 50]
mult_of_ten + [60]
>>> [10, 20, 30, 40, 50, 60]
```

In Python, you may need a list of consecutive numbers (ex. list between number 0 - 20). There is a function called `range` that does this and can take 1, 2, or 3 inputs. To print the ranges, you must cast them to a `list`. When using `range` with 1 argument, it generates from `0` to the number **before** the argument. 

```
goes_to_5 = range(6)
>>> print(list(goes_to_5))
[0, 1, 2, 3, 4, 5]
```

If you use two arguments, the first will determine what number the list starts at and the second will go to the number before the argument. 

```
>>> goes_to_four = range(-1, 5)
>>> print(list(a_list))
[-1, 0, 1, 2, 3, 4]
```

If there are three arguments, the third argument will "skip" every nth number

```
>>> a_range = range(1, 10, 3)
>>> print(list(a_range))
[1, 4, 7]
```



# The Quiz

Today, the quiz had nine questions ranging from: *How do make a list of numbers starting at 0 and going up to, but not including 9?* to  *How do you create an empty list?* There were a few code snippet examples thrown in, but all in all this wasn't terribly difficult if you knew the questions

# The Project: Python Gradebook

For this project, there was a pre-existing variable called `last_semester_gradebook` I created a list called `subjects` and `grades`. Then, I used the `zip` function to combine `subjects` and `grades` to a new variable. After that, I used both the `print` and `list` functions to print the result. I used the `append` function to add a subject (`computer science`) and a grade (`100`) to the respective `subjects` and `grades` list. This step of the project was confusing since I had to write this above the `zip` function and backtrack to make this work. During these projects, I have been used to writing in a top-to-bottom way so it was strange I had to go back to writing this below the code I wrote in the beginning.   After this, I went back to the bottom and used the `append` function to add to the zipped list like this: `gradebook.append(("art", 85))`. Finally, I added the zipped_list and `last_semester_gradebook` to create a new variable `full_gradebook` .



This project was a bit more vague than the last one due to the confusing fifth step that was included. If they had worded that part differently than this project may have gone differently.  



Anyway, that's all for today! Be ready for a longer blog post tomorrow, since I'll be tackling the harder part of this module. 