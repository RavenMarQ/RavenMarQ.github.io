---
layout: essay
type: essay
title: "Software Engineering: The Breath of Fresh Air"
# All dates must be YYYY-MM-DD format!
date: 2023-12-11
published: true
labels:
  - Programming
  - Design Patterns
  - Software Engineering
  - Programming Style
  - Agile Project Management

---

## Brief Overview

***As per usual, if you want a TL;DR: here it is!***

Throughout my Software Engineering course, I honestly think I could have learned the programming aspect by myself: it's just HTML/Javascript/CSS. Hell, we learned it through [freeCodeCamp.org](https://www.freecodecamp.org), so that should be a telltale sign that those skills weren't the takeaway from this course. Instead, what I think the course really taught me was universal good habits and practices and understanding that making any piece of software is never a solo mission. From coding standards and design patterns, to open source software development and issue driven project management, I would say those are among the most important takeaways I got from the course.

Fair bit of warning: this essay is ***LONG LONG*** like, ***LONGER***. Read at your own discretion.

## Learning Overarching Practices

Like learning any skill: the basics allow you to do almost any technique under the sun. The same is true with coding. In previous courses, I would learn things in programming like statements, logic, and algorithms. In Software Engineering, you take a step back and learn **WHY** and **WHEN** to use **WHAT** we learned previously and **HOW** to use it, and even finding ways to make our lives easier.

In this case, relating to coding, we were taught habits and certain mindsets to approaching programming regardless of coding language, game engine, integrated development environment, or what have you. Coding standard habits helped me to continue to produce, in eventuality, easily legible and understood code that helps future me, or anyone else, read my code.

On the other hand, I learned about design patterns which gave me a new way at how I approached problems, where, instead of scrambling to apply the first thought to come to my head, I took a step back and analysed all the 'moving parts' of my desired product and attempted to apply a solution I've learned/used before when possible. This, in turn, helps me to not stress about thinking everything out from scratch: experience actually proves valuable.

### Coding Standards

Before I begin, below, here is a quote from browserstack that succinctly describes coding standards:
>Coding standards are a set of guidelines and best practices that are used to create consistent, high-quality code.
> 
>Consider coding standards as rules, techniques, and best practices to develop cleaner, more readable, and more efficient code with minimal errors.
>>[Link to Source](https://www.browserstack.com/guide/coding-standards-best-practices)

Taking that definition in mind, we focus on the first line: "to create consistent, high-quality code". The guidelines and practices we as programmers and/or software designers that we follow not only help us, but help others. 

In terms of others, code that adheres to a style helps to not leave others scratching their heads in confusion. To explain this, think about it like this: have you ever seen the most atrocious handwriting? Maybe from a doctor, or a child? Every single time you hold up a piece of paper with their handwriting, you're left wondering something akin to: 

>*"Is that a 'k' or an 'r'?"*
 
**Or even:**

>*"An 'o'? '0'? Wait, maybe it's a 'd'? That's an 'a'!?".*

Like handwriting, coding also has a sort of print of a person's style and approach to coding. In this case, we don't want the part where a person's style hampers the ability to read it from an outsider's perspective. For example, have you ever read someone else's code and been like:

>*"This one line stretches on forever, and the nested statements don't make it any better... There's not even a comment to explain what it does!"*

To prevent that from happening, there are many coding standards, but many of them agree on some basic components like the usage of comments and keeping the length of lines below a certain amount. These help it so that people reading your code have a digestible and explained/context-rich experience rather than being thrown into a war zone of characters that begin to blur together.

In my case, I was taught a little bit of coding standards from my previous courses like indents, commenting, and line lengths, but this course taught me coding standards for JavaScript, json, CSS, HTML, and so much more. Who would have thought that adding a few spaces would, over time, help my code seem more breathable and distinguishable endings from beginnings?

With this in mind, I've come to appreciate the many standards that exist: as they all are there for the sake of improving the reading experience.

In terms of self, the same applies from before: but in a different way. Please consider your future self as another person. Don't believe me? Take a step back and remember a time when you booted up a file that you coded previously and just being molly-whopped by the absolute wall of code: with its uncommented and unformatted moving-parts buried beneath characters created in the heat of an overnight caffeine-fueled coding bender just to push out something for a deadline. Good God, my heart palpitates at the very reminder of it. But now you have a completely unreadable 7.5-ounce beef macaroni and cheese ball in your lap that you have to stick your clean and sober hands through to hopefully derive some meaning and build upon.

Unthinkable. Disgusting even. Also, that ball I described exists:
<img src="../img/software-engineering/macandcheese.jpg">
The ROUNDMEAL: **Heresy.**

Ignoring that and applying it to myself currently: no matter how much I want to scream that the majority of coding standard is brain-numbing minutia that makes me want to commit a virus that'll delete my repo, I still see the uses and advantages of coding standards.

Sure: I want to pull all my hair off of my body with a pair of tweezers when I see ESLint return a hundred instances of me not using spaces... But that "mindless minutia" makes my code appear cleaner and more professional despite the only differences being spaces. And the bigger things like ensuring my code is immutable to ensure security is important as the scope and size of the project grows (you really don't want some random function in the middle of nowhere managing to dredge up a value out of nowhere and throw your whole software to wack).

And, returning to a more professional note: using coding standards helps you in the long run, so don't think that you will always understand what you write. Seriously, my handwriting and old coding designs were so bad I can't read them this far in the future compared to when I wrote it in high/middle school. Plus, having readable code helps you replace or even rid of old code that is outdated or not needed... Which perfectly transitions into our next subsection!

### Design Patterns

Having readable code helps you know what you can copy to use later or what to replace when you come up with a more optimized solution. In this case, this an example of a design pattern: Tree Shaking. Tree Shaking is when you remove old and outdated cold and potentially replace it with something updated or even optimized. This is a pattern that avoids 

Before we get too deep into this, I think you, as the reader, deserve to know what design patterns are. Design patterns, as put very well by me in a previous essay I have written (link below):
>***DESIGN PATTERNS***:
>>Design patterns, in coding, are general solutions that solve common problems that occur in software design.
>
>***ANTIPATTERNS***:
>
>With the prefix '-anti' meaning "opposite of" or "against" (in layman's terms), we can then derive the definition from our definition:
>> Antipatterns, in coding, are solutions that fail to, inadequately, or incorrectly solve common problems that occur in software design.
>
>>[Link to Source](https://ravenmarq.github.io/essays/patterns.html)

*Please read the essay if these definitions go over your head! I give examples and specifics there!*

Apart from the example I put in the essay that I previously wrote about design patterns, where I described its application in the Unity project I was developing, being taught basic patterns and how to recognize other patterns in the work we do that are not explicitly taught gives us such a dynamic way to approach not just programming, but life in general. 

If you approach life like a problem and break it down with algorithms, specific and ordered sets of instructions to carry out (note that algorithms aren't just a computer thing, as such algorithms are specifically called **COMPUTER** algorithms), you will see the many patterns you find yourself doing.

For example: walking has its own pattern that you made and practiced that works best for you. Sometimes, walking isn't the pattern you want to move with. For example, running, jumping, and crawling might be the modes of movement you want to use for other things. And patterns can change and update with time! You have permanent hip damage? Your walking pattern is going to change to accommodate the pain or lack of motility!

So in my case, apart from programming, like when I am writing something creative, if I want to make a young adult story, I can follow the Hero's Journey pattern for creating plot: a pattern of story writing to create generally compelling plots.

*For more information, here's a link to an [in-depth explanation of the Hero's Journey](https://en.wikipedia.org/wiki/Hero%27s_journey).*

And even in that example, the Hero's Journey isn't the only way to write stories, and even the only way to write a young adult story, there are many patterns that I can use to make the plot. And even when using the Hero's Journey, the pattern isn't rigid and can adapt to what you need. You don't want a "revival" in your story? Go ahead! Have things be permanent and have lasting consequences!

Design patterns are just a form of patterns that we use in software engineering and programming, and taking notes from this we can apply it to things outside of Software Engineering.

That's why I believe that many IQ tests test pattern recognition, as they are also a window into looking at the problem-solving intelligence an individual might have. 

## Understanding the People Problem

>**Welcome to the second half of the essay!**
> 
>I promise this section is shorter, as these things I learned are straight forward and principles that cover group-based and/or mid-to-large-scale project management.

Like how humans suffer mentally and/or emotionally from lack of social contact, your skills and understanding will stagnate or even depreciate with lack of external judgement and interaction.

For example, how are you going to get feedback or testing done if you choose to do everything alone? That's why it's important you discuss and compare and contrast with you peers and mentors, because that is the only way you'll learn and improve.

### Open Source Software Development

Open Source Software Development sounds like what it is: software development with open sources. But what is an open source? Well, open source is when the source code is publicly available for viewing and copying.

>*"But what if someone steals my code?"*

Well first off, you don't need to make your code open source if you don't want to, as many developers don't have open source code. But on the off-chance you decide to go open source, there are many positive reasons to do so:

You get free testing, troubleshooting, and compare and contrasting from others who are interested or have code similar in function to yours. This helps you improve compared to having to keep your code closed and bear the burden of having to fix everything and look for errors yourself. 

I've learned that the programming community is generally nice, regardless of the elitists, and are willing to lend a hand. Just take a look at StackOverflow: the leading site where many programmers and such exchange code, post questions, and provide answers. 

Open source software development has its place as a way to open up your project to the community to help improve or even create forks, copies of the code that are changed to function or perform differently from the original, all for the sake of creating a communal improved project. However, there is a reason why some developers are not open source.

If code you are making is for profit, then obviously there are concerns to protecting your intellectual property. However, most people who are doing projects for fun, to learn, or as a hobby should seriously consider open source software development.

### Issue Driven Project Management

Issue driven project management, also, sounds like what it is: project management that is issue driven. In this case, issues being problems to solve, and the project's progress is driven by said issues. 

GitHub serves as an excellent example of issue driven project management, with repositories having an issue tab where contributors can post issues, take on issues, and assign issues to other contributors.

This form of project management is good for maneuvering through a mid-to-large-sized project, where there are many uncertainties and issues are not readily apparent or come up as a natural product of development processes. 

However: I also learned that issue driven isn't the only way to manage a project, and that issue driven isn't infallible. Issue driven requires for the members of the team to know what they're working towards and what the eventual goal is. If a goal isn't able to be precisely discerned and/or set, then groups will flounder through issues slowly until they manage to find the right direction. 

Issue driven also has the problem with being too rigid: if a project has to change scope, then more issues are created while some implementations become obsolete and/or no longer needed. That is why when managing a project, ensure that if you do choose to lead a project: be firm and be sure of every single detail you want fulfilled by the team, or else things get thrown into the pile in a disorderly fashion.

Issue driven project management takes time and manpower, so if you're under crunch, find another project management type or always have backups for your backup plans.

## You don't ***NEED*** a Conclusion! Was this not long enough for your liking!?

And if you do, well... Umm... You might need to get checked for short-term memory loss. But I'm still going to give it to you anyway:

Software Engineering isn't learning something for your sake only: it's about learning to work and adapt to a globalized world where the internet enables almost instantaneous exchange of information. In our field of work, being able to understand and work with each other in a structured and orderly way. From designs and standards to open source and project management, these are values that the Software Engineering course has taught me. 

And frankly? It's refreshing compared to learning hyper-specific code.