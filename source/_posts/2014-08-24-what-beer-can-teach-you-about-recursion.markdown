---
layout: post
title: "What Beer Can Teach You About Recursion"
date: 2014-08-24 20:27:23 -0400
comments: true
categories: Recursion Algorithms Computer&nbsp;Science Flatiron&nbsp;School 
---

As the semester at The Flatiron School wraps up, we've been practicing how to solve some pretty common computer science problems that might come up in a technical interview. While these problems can be pretty intimidating at first, one of the best ways to approach them is by breaking them down into smaller pieces that can then be combined to give a solution to the original problem.
<!--more-->
This is typically called a divide and conquer (or D&C) algorithm, and works by using recursion. I thought it'd be helpful to demonstrate one of the simplest implementations of a recursive method that I've come across, since some of the examples out there might be overwhelming to an absolute beginner. Before we get into that, let's define what an algorithm and recursion actually are.

## Definitions

An **algorithm** is a step-by-step set of instructions for solving a problem, while **recursion** is a function that calls itself. You're essentially creating a loop, and there are plenty of arguments out there for why it makes more sense to use an iterator to solve a problem. Recursion is still extremely valuble to learn in that it will help you to understand how looping works.

## Components of Recursive Algorithms

When setting up a recursive algorithm, it's essential to define two things. A **recursive case** that will initiate the recursion, and a **base case** that will break the recursion. If you forget to do that, you'll most likely see a **stack level too deep** or **stack overflow** error. This means either your base case was incorrectly defined, or you ran out of memory.

## Implementing a Recursive Algorithm

Okay, now that we've got that out of the way, let's solve a problem. We're going to define a recursive algorithm called `bottles_of_beer` that takes a number as an argument and prints the number of bottles of beer we have until there aren't any left. Of course, we'll be doing this in the style of a classic song:

```ruby
def bottles_of_beer(n)
  if n == 0 # base case for breaking the recursion
    puts "No more bottles of beer on the wall!"
  else # recursive case for triggering the recursion
    puts "#{n} bottles of beer on the wall, #{n} bottles of beer. Take one down and pass it around, #{n-1} bottles of beer on the wall."
    bottles_of_beer(n-1)
  end
end
```
So we've defined a method above that takes a number `n` as an argument. If `n` is equal to 0, we break our recursion and print the corresponding statement. Otherwise, we trigger the recursion, print a different statement, and then subtract 1 from `n`, thereby passing that new `n` in as our argument to call `bottles_of_beer` again.

Why don't you open up `irb` and try it out? I promise it'll make that beer (or sparkling apple juice) you have afterwards that much sweeter.