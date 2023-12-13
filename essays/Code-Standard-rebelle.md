---
layout: essay
type: essay
title: "Code Standard cest un Oiseau Rebelle"
# All dates must be YYYY-MM-DD format!
date: 2023-09-20
published: false
labels:
  - Programming
  - Software Engineering
  - Programming Style
---

## Brief Overview

As per usual, if you want a TL;DR: here it is!

As a (mostly) informative essay, you'll come to learn about what *I* learned from practicing coding standards, more specifically the one featured in ICS-314 here at the University of Hawaii at Manoa. (Despite the fact that I don't know if it varies much from other standards, I am assuming it mostly conforms to most other conventions and varies in a minute way). Also, near the end, I'll be doing an opinion section, so look forward to me whine.
  
## What Even is Coding Standard?

Well- according to Browser Stack:
>Coding standards are a set of guidelines and best practices that are used to create consistent, high-quality code.
>Consider coding standards as rules, techniques, and best practices to develop cleaner, more readable, and more efficient code with minimal errors.
>>[Link to Source](https://www.browserstack.com/guide/coding-standards-best-practices)
>
I think that perfectly summarizes coding standard, but one might ask:
*"How are these standards enforced?"*

These standards ***can*** just be a programmer or software developer/engineer's active attentiveness to adhering to a coding standard by manual checking theirselves... But we all know that isn't feasibly possible and error-prone. So one of the ways that you can enforce coding standards is to have a program that checks your code! And for the instance I am talking about: we have ESLint!

ESLint as a static code-checking program simply just scans your code for anything that violates coding standard like unspaced lists, indents, line length, etc. But ESLint only looks for in-code standard. How do we enforce practices and structure? Well... To be truthful? We haven't gotten that far yet for me to comment~

So please be understanding of my position. 
(Though I would assume that it also might be ESLint again and simply dissuades the usage of certain functions or data-handling practices)

## Why Should I Care About Coding Standards?

One might think to theirselves:
*"Well- nobody else is going to read my code: I don't need to adhere to these standards!"*

You would be correct... If not for the fact that even sometimes you might not be able to read your own code! Seriously! Take it from me who has been programming for a while: not commenting, properly spacing out your lines, or making them ***OBSCENELY*** long will bite you where the sun don't shine! 
(I'm looking at you Java project from high school with that one out-of-context line containing 7 nested functions with 30+ parameters total spanning ~500 characters. [WITHOUT SPACES MIND YOU!] ***DAMN YOU, PAST ME!*** ) 

Plus- let's assume that you are some kind of nerd with photographic memory: practicing it with integrity allows you to subconsciously adhere to them, so that it is not difficult to do so when it is required of you to do so.

So don't be a donkey! Be high-key and comment, comment, comment! 

## Rant Ahead: Read At Your Disgression!

No matter how much I want to scream that the majority of coding standard is brain-numbing minutia that makes me want to commit a virus that'll delete my repo, I still see the uses and advantages to this system. For one: it allows readability and ease of tracing which is perfect for people grading your code and reading it over (or actually seeing if they should continue to pay you... I mean, that also applies I guess).

Sure: I want to pull all my hair off of my body with a pair of tweezers when I see ESLint return a hundred instances of me not using spaces... But that "mindless minutia" makes my code appear cleaner and more professional despite the only differences being spaces. And the bigger things like ensuring my code is immutable to ensure security is important as the scope and size of the project grows (you really don't want some random function in the middle of nowhere managing to dredge up a value out of nowhere and throw your whole software to wack).

Okay, that's all. Be good! See you in my next essay~
