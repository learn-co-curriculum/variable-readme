---
tags: readme
language: ruby
resources: 0
track: web development
topic: ruby
unit: variables
lesson: what is a variable?, creating, assignment
---

# Variables

## Introduction

Much like in math, variables are words or characters that hold values. However, in algebra, etc. variables usually are placeholders for numbers. In Ruby, a variable can point to almost any type of value including numbers, strings, arrays, and hashes.

## Creation

Variables are assigned values using the = operator. Variable names are typically all lower case, and in the case of multiple words, the words are separated by underscores. 

```ruby
current_president = "Barack Obama"
puts "In 2014, the president was #{current_president}."
```
The code above will print `In 2014, the president was Barack Obama.`.


## Reassignment

Now the variable `current_president` is equal to the string Barack Obama. Let's say somehow Stephen Colbert got elected as president for 2016. To update current_president, you would just reassign the variable, much in the same way you first defined it:

```ruby
current_president = "Barack Obama"
puts "In 2014, the president was #{current_president}."

current_president = "Stephen Colbert"
puts "Now, it being the year 2016, the president is #{current_president}."
```
This will print out:  
```text
In 2014, the president was Barack Obama.
Now, it being the year 2016, the president is Stephen Colbert.
```
