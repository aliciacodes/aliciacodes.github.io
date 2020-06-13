---
layout: post
title:  "The Boredless Tourist"
date:   2020-06-14
categories: codecademy
---
Welcome to day nine! Today, we're tackling "The Boredless Tourist" project, our first project in the series. In the project, we're expected to use the knowledge of Python, Git, and the command line to create a recommendation service for tourists kind of like Yelp, but much simpler. Overall the things I practiced were:

- The Git workflow: First adding files using `git add .`  to add it to the workspace, then `git commit -m "Whatever message you want"` to get it ready for commit in the remote repository. I did this every time a big change was made.
- Creating Python functions that take lists as arguments
- Creating `for` loops to go through lists
- Using `if-else` and try-except statements control flow within the functions
- Using list comprehension
- Appending to lists using `.append()` and `+=`.
- Using the `print` function
- Using list indexing

I won't be breaking down this project since it's 64 steps, but I will provide the project code. This is the final script:

```
script.py
destinations = ["Paris, France", "Shanghai, China", "Los Angeles, USA", "São Paulo, Brazil", "Cairo, Egypt"]
test_traveler = ['Erin Wilkes', 'Shanghai, China', ['historical site', 'art']]

def get_destination_index(destination):
  destination_index = destinations.index(destination)
  return destination_index
  

print(get_destination_index("Los Angeles, USA")) 
print(get_destination_index("Paris, France"))  
#print(get_destination_index("Hyderabad, India"))

def get_traveler_location(traveler):
    traveler_destination = traveler[1]
    traveler_destination_index = get_destination_index(traveler[1])
    return traveler_destination_index

test_destination_index = get_traveler_location(test_traveler)
print(test_destination_index)

attractions = [[] for i in destinations]

print(attractions)

def add_attraction(destination, attraction):
  try:
    destination_index = get_destination_index(destination)
    attractions_for_destination = attractions[destination_index].append(attraction)
  except SyntaxError:
    return
add_attraction("Los Angeles, USA", ['Venice Beach', ['beach']])
print(attractions)

add_attraction("Paris, France", ["the Louvre", ["art", "museum"]])
add_attraction("Paris, France", ["Arc de Triomphe", ["historical site", "monument"]])
add_attraction("Shanghai, China", ["Yu Garden", ["garden", "historcical site"]])
add_attraction("Shanghai, China", ["Yuz Museum", ["art", "museum"]])
add_attraction("Shanghai, China", ["Oriental Pearl Tower", ["skyscraper", "viewing deck"]])
add_attraction("Los Angeles, USA", ["LACMA", ["art", "museum"]])
add_attraction("São Paulo, Brazil", ["São Paulo Zoo", ["zoo"]])
add_attraction("São Paulo, Brazil", ["Pátio do Colégio", ["historical site"]])
add_attraction("Cairo, Egypt", ["Pyramids of Giza", ["monument", "historical site"]])
add_attraction("Cairo, Egypt", ["Egyptian Museum", ["museum"]])


def find_attractions(destination, interests):
  destination_index = get_destination_index(destination)
  attractions_in_city = attractions[destination_index]
  attractions_with_interest = []
  for attraction in attractions_in_city:
    possible_attraction = attraction
    attraction_tags = attraction[1]
    for interest in interests:
      if interest in attraction_tags:
        attractions_with_interest.append(possible_attraction[0])
  return attractions_with_interest

la_arts = find_attractions("Los Angeles, USA", ['art'])
print(la_arts)

def get_attractions_for_traveler(traveler):
  traveler_destination = traveler[1]
  traveler_interests = traveler[2]
  traveler_attractions = find_attractions(traveler_destination, traveler_interests)
  interests_string = ("Hi " + traveler[0] + ", we think you'll like these places around " + traveler_destination)
  for attraction in traveler_attractions:
	  interests_string += ", " + attraction
  return interests_string


smills_france = get_attractions_for_traveler(['Dereck Smill', 'Paris, France', ['monument']])
print(smills_france)
```

And that's it for today!
