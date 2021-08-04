# Introduction to Variables

## Objectives

1. Define a variable.
2. Create and reassign variables.
3. Define pass-by-value as it relates to variables.

## Video

<video width="560" height="315" controls>
  <source src="http://learn-co-videos.s3.amazonaws.com/ruby/about-variables-ruby.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

[Download MP4](http://learn-co-videos.s3.amazonaws.com/ruby/about-variables-ruby.mp4)

This video is meant as optional supplemental material to augment the written curriculum. If you feel you already understand variables, you are welcome to skip the video and continue forward. Feel free to come back here if you ever want a review.

If you would like to code along you can use: [repl.it](https://repl.it/).

## Variables in Ruby

Let's dive right in:

```ruby
first_number = 7
second_number = 14

sum = first_number + second_number

puts sum
```

The code above will print '21'.

```ruby
best_cheese = "cheddar"
puts "The best cheese is obviously #{best_cheese}."
```

This code will print `The best cheese is obviously cheddar.`.

> **Note:** The syntax of `#{best_cheese}` simply injects the value of the
> variable `best_cheese` into the string. This is called [Interpolation][] and
> we'll cover it later — in this case, you can think of it as
> `"The best cheese is obviously " + best_cheese + "."` where you are simply
> adding together multiple strings.

[interpolation]: http://stackoverflow.com/questions/10076579/string-concatenation-vs-interpolation-in-ruby

`first_number`, `second_number`, `sum`, and `best_cheese` are all **variables**.
Much like in math, variables are words or characters that hold values. In
algebra, however, variables are only placeholders for numbers. In Ruby, a
variable can point to almost any type of value including numbers, strings,
arrays, and hashes.

## What is a Variable

As the examples above show, variables allow us to store information. We tell our
computer to set aside some space to hold that information so we can retrieve it
later. A variable is the location where the information resides, when we need it
we know just where to look.

### A Variable has a Name

```ruby
i
result
user1
brkfstCereal
all_words_in_the_dictionary
CountryOfOrigin
FIRST_NAME
age
longest_word
```

These would all be valid variable names in Ruby. They would not all be good
variable names. There is strong convention among Rubyists to use what is known
as _snake case_ `this_is_an_example_of_snake_case` words are separated by
underscores. This is opposed to _camel case_ `thisIsAnExampleOfCamelCase` where
`upcase`d characters indicate word breaks.

Variable names should start with a lowercase letter. A variable that begins with
an uppercase letter is known as a **constant** and has different
characteristics.

There are also some rules that mark invalid variable names:

```ruby
# X Invalid X
1st_place
end
danny's_age
```

A Ruby variable cannot start with a number, be a Ruby reserved word, or have
punctuation or space characters.

### A Variable has a Value

A variable's name is like a label on a container. Its value is what is stored
inside that container. The name points to the value. Above, `best_cheese` holds
onto the value "Barack Obama" and `first_number` has the value of the number 7.
As we will see, the value of a variable can change even when its name stays the
same.

#### A Variable has a Type

A variable's type is the type of the value it holds. Ruby is what is known as a
_dynamically typed_ language. That means the value of a variable can change its
type and does not need to be explicitly and permanently defined. There is
nothing stopping you from changing the value of `sum`, which now is the number
21, to the string "whatever I want".

It is also a _strongly typed_ language. This means a variable will never be
automatically _coerced_ to another type without you explicitly changing the
type. Adding two numbers will return a number, 2 + 2 returns 4; adding two
strings will return a string, "2" + "2" returns "22"; adding a number and a
string will raise an error, 2 + "2" raises a `TypeError`.

When you are building larger programs it is important to have in mind the type
of the value that a variable refers to.

## Creating Variables

Variables are assigned values using `=` ("equal sign"), called the assignment
operator.

```ruby
best_cheese = "cheddar"
puts "The best cheese is obviously #{best_cheese}."
```

## Reassigning Variables

Now the variable `best_cheese` is equal to the string "cheddar". Let's say
somehow we were brainwashed into thinking Swiss cheese was better than cheddar.
To update `best_cheese`, you would just reassign the variable much in the
same way that you first defined it:

```ruby
best_cheese = "cheddar"
puts "The best cheese is obviously #{best_cheese}."

best_cheese = "Swiss"
puts "I've come to my senses and realized the best cheese is #{best_cheese}."
```

This will print out:

```txt
The best cheese is obviously cheddar.
I've come to my senses and realized the best cheese is Swiss.
```

## Variable Example

Within this repository is a file named `variables.rb` with some examples you can
read and play with.
[Fork the repository](https://github.com/learn-co-curriculum/variable-readme)
for this lesson to see how it behaves.

```ruby
'This is data, it is a string. Strings start and end with  " '

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

```txt
2
1+1
The word 'example' is equal to this sentence, it's a named variable.
The word 'example' is equal to this sentence, it's a named variable.
The word 'example' is equal to this sentence, it's a named variable.
variables are any previously undefined word that
starts with a lowercase letter.
```

## Bonus: 'Pass-By-Value'

We have seen that the variable itself, the location where information is stored,
is distinct from the value stored at that location. Let's try something out to
demonstrate this. We'll first declare a new variable with an original value,
then do something to change that value, and finally we'll take a peek at our
variable again.

```ruby
# Open up IRB and follow along
sound = "squeak"

# We can peek at the value of sound by typing its name
sound
# => "squeak"

sound.upcase
# => "SQUEAK"
```

Ok, the moment of suspense has arrived! Now if we type `sound` again what do you
think its value will be?

...

...

```ruby
sound
# => "squeak"
```

Hmmm... `sound` is still pointing to the original lowercased value. What does
this tell us? When `upcase` did its thing to the variable, what MUST `sound`
have handed over to `upcase` for us to see this result?

Only its _value_. In fact it must have made a _copy of that value_ that `upcase`
could operate on while still holding onto the original unaltered value. If this
process did not happen the value 'squeak' wouldn't exist for us to look up and
we'd only be able to see 'SQUEAK'.

This is what we mean by pass-by-value. A variable makes a copy of the value it
holds and passes the copy over to something else that alters or changes it. The
alternative process is known as pass-by-reference. Here, changes to a variable
would alter what is stored in the actual location it refers to. After the
process was complete the variable would be holding a new and different value.

## Resources

- [ZetCode Ruby Variables](http://zetcode.com/lang/rubytutorial/variables/)
- [Wikibooks: Ruby Programming/Syntax/Variables and Constants](http://en.wikibooks.org/wiki/Ruby_Programming/Syntax/Variables_and_Constants)
