Welcome to day 7! This is the second part of Python Lists. In this, part I'll cover the remaining portion of the activity: 1 quiz, 1 project, 2 articles, and the video. 



# Operations on Lists

So, now that we know how to create, add, and combine lists together, there's still some more information that we need to know before we can move onto bigger concepts. So, in this section we'll learn how to get the length of a list, select subsets of a list, counting frequency of elements in list, and sorting elements in a list. 

*Length* is the number of items in a list. A function called `len()` exists in Python to find it for us. You can save the result of `len()` to a variable.  Let's use an example to illustrate this: Asia is a librarian at a library and she needs to call a list of people to tell them that the books that have borrowed are overdue. She needs to know how many people she needs to call. 

```
calls = ['Erin', 'Joe', 'Fred', 'Rose', 'Kenny']
print(len(calls))
# returns 5
```

Now that she knows the people she needs to call, she needs to select the first item out of the list. You can use square brackets (`[]`) and the position of the list (called the `index`). One note to keep in mind with indexes is that lists are *zero-induced* meaning that the first element has an index of `0` and not `1`.  So `Erin` has an index (position) of `0`, Joe has an index of `1`, and so on. When you try to get an index outside the bounds of the list (in this case, that would be 5), you will get an `IndexError` exception. 

```
print(calls[0])
#'Erin'
print(calls[1])
#'Joe'
print(calls[2])
# 'Fred'
print(calls[3])
# 'Rose'
```

Asia is on a roll and has one more person to call. How can she get the last element in the list? There are two ways of doing this:

```
print(calls[4])
# returns 'Kenny'
print(calls[-1])
#returns 'Kenny'
```

If you don't know the size of the lists, you can use the `-1` element to get the last item of the list. 

Now, it's another day and both Erin and Kenny have returned their books. Asia wants to call the remaining three people on the list again to remind them to return their books. How would we do that? In Python, we can do a thing called `slicing` to make a sublist. To do that, we use the following syntax `a_list = [start_index:end_index]`. The `start_index` is the element we want to include in the selection, so we put `1`. The `end_index` is the index of one more than the last index, so we use `3`.

```
call_again = calls[1:3]
print(calls)
# ['Joe', 'Fred', 'Rose']
```

What if we just want the first three items of a given list? Then we can omit the `0`. 

```
>>> pokemon = ['Bulbasaur', 'Squirtle', 'Charmander', 'Pikachu']
>>> print(pokemon[0:3])
# ['Bulbasaur', 'Squirtle', 'Charmander']
>>> print(pokemon[:3])
# ['Bulbasaur', 'Squirtle', 'Charmander']
```

For the last three items, you can just omit the end index. 

```
>>> print(pokemon[1:3])
['Squirtle', 'Charmander', 'Pikachu']
>>> print(pokemon[1:])
['Squirtle', 'Charmander', 'Pikachu']
```

If you don't know the size of a list, you can use negative indexes to go back from the last element.

```
>>> print(pokemon[-3:])
```

Now, we have a list called `word` that contains the letters in `Massachusetts`

```
letters = ['m', 'a', 's', 's', 'a', 'c', 'h', 'u', 's', 'e', 't', 't', 's']
```

We would like to know how many times `s` appears in the word, so we use count.

```
s_count = letters.count('s')
print(s_count)
# prints out 4
```

Let's go back to Asia. She wants to keep the list in alphabetical order. To do this, we use `.sort()`. This can be used to keep the list in numerical order, too. If you don't put the name of the list in front of it, it will result to a `NameError`. `sort` doesn't return anything so assigning it to another variable will return `None`.

```
calls = ['Erin', 'Joe', 'Fred', 'Rose', 'Kenny']
calls.sort()
print(calls)
# returns ['Erin', 'Fred', 'Joe', 'Kenny', 'Rose']
```

A second way to do this is `sorted()`. The only differences in function are that it generates a new list based off the given list argument and that it is written like `print()`.

```
calls = ['Erin', 'Joe', 'Fred', 'Rose', 'Kenny']
sorted_calls = sorted(calls)
print(sorted_calls)
# returns ['Erin', 'Fred', 'Joe', 'Kenny', 'Rose']
```

The quiz was mostly reviewing slicing which I think can be a tricky topic for some. I'm not going to cover it here.



# The Project: Len's Slice

This project was centered around a pizza joint that sells slices of pizza (Haha...slicing get it :)).

First, we made a list of toppings and a list of prices. Then we found the length of the toppings list and stores it in a variable. Next, we printed out a string advertising the different types of pizza (print out the toppings list). After, we zipped the toppings and prices list together, assigned them to a variable, and then print the variable. Now, it's onto slicing. We now sort based on the lowest price. Then we store the first and last variables of the list in two respective variables. Now, the slicing comes into play when we have to store the 3 lowest costing pizzas in a variable and print it. Finally, you come to the end where you have a another array with competing pizza slices and count the number that are $2 using the `count` function and print it out. 



On the whole, this was pretty simple and not really challenging. 



# Python Coding Challenge: List

These challenges are back again! In the first challenge, you create a function that has one parameter `lst`. The function adds the last two elements of `lst` three times and append all the results. This was hard for me!

In the second challenge, the function takes two parameters named `lst1` and `lst2`. The function compares two lists and if one list contains more elements, then it returns the last element of the list. If they are the same size, then automatically default for the first argument.

The third function, has three parameters: a list, an item (could be string or integer), and integer. The function returns `True` if the item appears more than the given integer amount of time. Should return false otherwise.

The fourth function as one parameter that is a list. The function appends the size of the list to the end of the list. This will return a new list.

The final function takes two lists and combines the two lists into one new list, sorts the result, and return new sorted list.

All in all, this was pretty easy. 



# Advanced Python Code Challenges: Lists

Function one has one integer function. This function returns a list of every third number between the integer and 100 (inclusive).

In the second function, there are three parameters: a list, a start integer, and end integer. This returns a list where all elements within an index between start and end (inclusive) is removed. This too was pretty hard and required me to think some.

In the third function, it takes a list, an `item1`, and `item2`. Whichever item appears more, you should return that. Return the first item if they are tied.

The fourth function takes in two parameters: one that is list and one that is an integer named `index`. The function returns a new list where all values are the same, except the location of the `index` value should be doubled. Function should return the original list if it's not a valid index.

The final function for today takes only a list. If there is an odd number, return the middle element. If there are an even number of elements, then the function should return average of middle two elements. This was hard too! I wasn't able to figure it out completely given my own personal time constraints, but I did get very close. 



# The Video: Python Tuples

Finally, there's just a video left! 

- What are tuples?
- Creating a tuple
- Tuples vs Lists

A tuple is a data structure in Python that allows you to store multiple pieces of data. Lists and tuples are similar except tuples are **immutable** meaning the elements inside cannot be changed at all. 

To create a tuple, you must: 

1. Have an opening and closing parenthesis `()` surrounding the tuple
2. Then you can add strings, integers, booleans, etc. . To separate them you use a comma `,` much like in a list.

```
>>> a_tuple = ('schedule', 6, 'wakeup')
>>> print(a_tuple)
# ('schedule', 6, 'wakeup')
```

Accessing individual elements in a tuple is the same as a list

```
>>> a_tuple[0]
# 'schedule'
>> a_tuple[-1]
# 'wakeup'
```

If you try to modify a tuple, you get a `TypeError`:

```
a_tuple[0] = 'my schedule'
# Traceback (most recent call last):
  File "<string>", line 2, in <module>
TypeError: 'tuple' object does not support item assignment
```

We can unpack a tuple if we want to store it in a variable. You must have an equal number of variables so each tuple element can be stored:

```
schedule, time, action = a_tuple
>>> time
6
```

What if you only wanted **one** item in a tuple? 

```
one_item = ('Alicia')
>>> one_item
# 'Alicia'
```

As you can see, the tuple only returns one value like a normal variable, so this way won't work.

There must be another way right?

Yes, using a trailing comma. And this is a special case.

```
one_item = ('Alicia', )
>>> one_item
#('Alicia',)
```

A tuple may come in handy to store data meant to be grouped together (ex. personal information like name, age, etc.) and want everything to stay together, but not categorical data (ex. gpas, names, etc). The order does matter in tuples especially when unpacking it. 

# Free Alternatives

Yesterday, I gave an alternative to this whole module. I found another <a href = "https://www.codecademy.com/learn/learn-python-3/modules/learn-python3-lists/cheatsheet">cheatsheet</a> through the Python 3 course. This <a href = "https://realpython.com/python-lists-tuples/">article</a> goes through the basics of both tuples and lists. It even has a quiz at the end! 



And that's it for today! I'll see you tomorrow for day 8.
