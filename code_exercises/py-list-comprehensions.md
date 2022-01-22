---
title: Python Code Break 2
layout: default
---

## Working with list comprehensions and formatting output

### exercise 1

Write a list comprehension that takes each word in a list of words and puts it in all caps.

```py
phrases = ["everything is fine", "have a seat", "holy cow"]
# your list comprehension should return:
# => ['EVERYTHING IS FINE', 'HAVE A SEAT', 'HOLY COW']
```

### exercise 2

Rewrite your `remove_from_list function` to use a list comprehension to remove the item.

The `remove_from_list` function should take a list of items and an item to remove from that list, and return a new list that contains everything from the original list except for that item. It should remove every occurrence of the item in the list (if it appears more than once).

### exercise 3

Write a function `print_freq_results(results)`. This function should take an argument `results` that is a list of tuples like the following:

 ```py
 [
     ('her', 33),
     ('all', 12),
     ('which', 12),
     ('she', 7),
     ('their', 7),
 ]
 ```

 This function should print (not return) output like the following:

 ```sh
   her | 33 *********************************
   all | 12 ************
 which | 12 ************
   she | 7  *******
 their | 7  *******
 ```
