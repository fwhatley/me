---
title: "How to Stand Out in a Python Coding Interview Summary"
last_modified_at: 2020-07-31T00:00:00-00:00
categories:
  - Blog
tags:
  - jekyll
---

Summary of https://realpython.com/python-coding-interview-tips/

```shell
#################################################
# How to Stand Out in a Python Coding Interview #
#################################################

# Sumary of https://realpython.com/python-coding-interview-tips/

# OUTLINE
# Select the Right Built-In Function for the Job
#     Iterate With enumerate() Instead of range()
#     Use List Comprehensions Instead of map() and filter()
#     Debug With breakpoint() Instead of print()
#     Format strings With f-Strings
#     Sort Complex Lists With sorted()
# Leverage Data Structures Effectively
#     Store Unique Values With Sets
#     Save Memory With Generators
#     Define Default Values in Dictionaries With .get() and .setdefault()
# Take Advantage of Python’s Standard Library
#     Handle Missing Dictionary Keys With collections.defaultdict()
#     Count Hashable Objects With collections.Counter
#     Access Common String Groups With string Constants
#     Generate Permutations and Combinations With itertools
# Built in functions
#    https://docs.python.org/3/library/functions.html#built-in-functions


######### Select the Right Built-In Function for the Job #################
######### Iterate With enumerate() Instead of range() ####################

# numbers = [45, 22, 14, 65, 97.72]

# for i in range(len(numbers)):
#     print(i)
#     print(numbers[i])
    
    
# for i, num in enumerate(numbers):
#     print(i)
#     print(num)

# for i, num in enumerate(numbers, start=50):
#     print(i, num)
    

######### Use List Comprehensions Instead of map() and filter() #############

# numbers = [4, 2, 1, 6, 9, 7]

# def square(x):
#     return x*x

# print(list(map(square, numbers)))
# print([square(x) for x in numbers])

# def is_odd(x):
#     return x % 2 != 0

# print(list(filter(is_odd, numbers)))
# print([x for x in numbers if is_odd(x)])


######### Debug With breakpoint() Instead of print() ########################
# import pdb; pdb.set_trace() # import this if py version < 3.7
# breakpoint() 
    
######### Format strings With f-Strings #########
# def get_name_and_decades(name, age):
#     return f"name: {name}, decades: {age/10:.5f}"

# get_name_and_decades("Maria", 31)
# name: Maria, decades: 3


######### Sort Complex Lists With sorted() #####################################
# print(sorted([6,5,3,7,2,4,1]))
# print(sorted(['cat', 'dog', 'cheetah', 'rhino', 'bear'], reverse=True))

# animals = [
#     { 'type': 'pengin', 'name': 'Steph', 'age': 8 }, 
#     { 'type': 'elephant', 'name': 'Devon', 'age': 3 },
#     { 'type': 'puma', 'name': 'Moe', 'age': 5 },
# ]

# sorted(animals, key=lambda animal: animal['age'])
# [
#     {'type': 'elephant', 'name': 'Devon', 'age': 3},
#     {'type': 'puma', 'name': 'Moe', 'age': 5},
#     {'type': 'penguin', 'name': 'Steph, 'age': 8},
# ]

######### Leverage Data Structures Effectively ####################
############# Store Unique Values With Sets ######################

# import random
# all_words = "all the words in the world".split()
# def get_random_word():
#     return random.choice(all_words)

# def get_unique_words_bad_approach():
#     words = []
#     for _ in range(1000):
#         words.append(get_random_word())
#     return set(words)

# def get_unique_words_worst_approach():
#     words = []
#     for _ in range(1000):
#         word = get_random_word()
#         if word not in words:
#             words.append(word)
#     return words

# def get_unique_words_good_approach():
#     words = set()
#     for _ in range(1000):
#         words.add(get_random_word())
#     return words


# print(get_unique_words_good_approach())



############# Save Memory With Generators ######################
# summing all perfect squares till 1000

# list comprehensions
# sum( [i * i for i in range(1001) ])

# # generators
# sum((i * i for i in range(1001)))


###### Define Default Values in Dictionaries With .get() and .setdefault() ########
# cowboy = { 'age': 32, 'horse': 'mustang', 'hat_size': 'large' }

# returning name or default value

# bad approach
# if 'name' in cowboy:
#     name = cowboy['name']
# else:
#     name = 'The Man with No Name'
    
# # good approach
# name = cowboy.get('name', 'The Man with no Name')


# # setting name if not set

# # bad approach
# if 'name' not in cowboy:
#     cowboy['name'] = 'The Man with No Name'
# name = cowboy['name']

# name = cowboy.setdefault('name', 'The Man with No Name')


######### Take Advantage of Python’s Standard Library ####################
##### Handle Missing Dictionary Keys With collections.defaultdict() ######

# default values the verbose way
# student_grades = {}
# grades = [
#     ('elliot', 91),
#     ('neelam', 98),
#     ('bianca', 81),
#     ('elliot', 88),
# ]

# for name, grade in grades:
#     if name not in student_grades:
#         student_grades[name] = [];
#     student_grades[name].append(grade)

# print(student_grades);

# with collections.defaultdict()
# from collections import defaultdict
# student_grades = defaultdict(list)
# for name, grade in grades:
#     student_grades[name].append(grade)
    
############################# Other stuff ####################
#################### iterate through dictionaries ############

# for name, grades in student_grades.items():
#     print(f"{name}, {grades}")
    
###### ternary operators ##############
# value_if_true if condition else value_if_false

```
