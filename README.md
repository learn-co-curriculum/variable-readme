##Objectives

1. Define a variable.
2. Create and reassign variables.

## About Variables

<video controls width="100%">
  <source src="http://learn-co-videos.s3.amazonaws.com/ruby/about-variables-ruby.mp4" type="video/mp4" >
    The video accompanying this lab is best enjoyed on Learn.co
</video>

[MP4](http://learn-co-videos.s3.amazonaws.com/ruby/about-variables-ruby.mp4)

## Introduction

Much like in math, variables are words or characters that hold values. In algebra, however, variables are only placeholders for numbers. In Ruby, a variable can point to almost any type of value including numbers, strings, arrays, and hashes.

## Creation

Variables are assigned values using `=` ("equal sign"), called the assignment operator. Variable names are typically all lower case and, in the case of multiple words, the words are separated by underscores. 

```ruby
current_president = "Barack Obama"
puts "In 2014, the president was #{current_president}."
```
The code above will print `In 2014, the president was Barack Obama.`.


## Reassignment

Now the variable `current_president` is equal to the string Barack Obama. Let's say somehow Stephen Colbert got elected as president for 2016. To update `current_president`, you would just reassign the variable much in the same way that you first defined it:

```ruby
current_president = "Barack Obama"
puts "In 2014, the president was #{current_president}."

current_president = "Stephen Colbert"
puts "Now, it being the year 2016, the president is #{current_president}."
```
This will print out:  

```
In 2014, the president was Barack Obama.
Now, it being the year 2016, the president is Stephen Colbert.
```

## Variable Example

Within this repository is a file named `variables.rb` with some examples you can read and play with.

```ruby
'This is data, it is a string. Strings start with " "'

"Part of being data, or a string, is that ruby doesn't interpret it."

puts 1+1
puts "1+1"

example = "The word 'example' is equal to this sentence, it's a named variable."

puts example
puts example
puts example

puts "variables are any previously undefined word that"
puts "starts with a lowercase letter."
```

Running this file will print:

```bash
2
1+1
The word 'example' is equal to this sentence, it's a named variable.
The word 'example' is equal to this sentence, it's a named variable.
The word 'example' is equal to this sentence, it's a named variable.
variables are any previously undefined word that
starts with a lowercase letter.
```

## Resources

- [ZetCode Ruby Variables](http://zetcode.com/lang/rubytutorial/variables/)
- [Wikibooks: Ruby Programming/Syntax/Variables and Constants](http://en.wikibooks.org/wiki/Ruby_Programming/Syntax/Variables_and_Constants)

