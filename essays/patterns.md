---
layout: essay
type: essay
title: "In Code There Are Patterns: Oh My!"
# All dates must be YYYY-MM-DD format!
date: 2023-11-29
published: true
labels:
  - Programming
  - Design Patterns
---

## Brief Overview

As per usual, if you want a TL;DR: here it is!

Design patterns are general solutions that solve common problems that occur in software design. However, incorrect use or using generally negative solutions create antipatterns. I use many design patterns to help me make it through the projects I am currently working on.

This essay will be shorter as I am not too well-versed in the specifics of design patterns, but I will attempt to make it fun.

## A product is like a puzzle set, thus coding is solving it.

When someone buys you a puzzle set (admit it, only people who are hyper-fixated on something ever buys these for themselves), you first have to figure out a way to solve the thing. In one common solution: the first thing you do after dumping them out is to find all the edge pieces. After finding all the edge pieces, you find the corner pieces (if applicable) and work outwards from there.

Much in the same vein, when implementing something new in a code or starting out fresh, you may find yourself implementing the same old classes or interactions. You may hate this, as you're pretty sure you know how to do this and wish to curse someone else to do it, but you begrudgingly do so because it's necessary. 

Take note that both situations were patterns. We find patterns and apply a practiced solution or implementation to respond to said patterns. In our latter example, coding, specifically, involves something called design patterns. This is because in coding, in most cases, problems and implementations can be broken down into steps that each may or may not have their own design patterns to reach a solution.

From there we apply and derive a primitive definition:
>Design patterns, in coding, are general solutions that solve common problems that occur in software design. 

So it should not surprise you, in the least, when you find yourself copy-and-pasting certain code blocks into different files due to the seemingly "similar" nature between the two. And to think that you were applying your own design pattern.

However, as with all things, design pattern solutions do have their consequences: if we take our example of starting from the edges of our puzzle piece, the issue arises of having to guess-and-check through the other 90% of the puzzle to work inwards. Comparatively, if you just put like ends together, although you have to initially put more effort into searching, you will create multiple pools of completed parts that will make it easier to find where to put the next piece into. This same balancing of pros and cons applies to coding design patterns.

### A short addendum on Antipatterns

With the prefix '-anti' meaning "opposite of" or "against" (in layman's terms), we can then derive the definition from our definition:
> Antipatterns, in coding, are solutions that fail to, inadequately, or incorrectly solve common problems that occur in software design.

So if you had a design pattern that creates objects optimally, by not creating a new object by using a reference or some other way, an antipattern version would create a new object every call **EVEN** when the object is a temporary one: eating up memory space and processing.

Although the line between antipattern and design pattern are slim, like Singleton patterns being a security hazard but being good at reducing the time required to read, write, and update said value, generally one can tell an antipattern is one by the number of cons they pose compared to the pros they offer.

## In my case?

To avoid yapping on about the coding I do for web design, as everybody and their mom loves to ramble on about the more "practical" usages of coding, I will instead discuss my usages in the Unity engine where I am working on a separate project (I hope I can publish it when I get it in a presentable stage into my projects tab here in my portfolio). In short: the Unity engine creates easy avenues to implement many design patterns, being an engine that serves both as a psuedo-IDE and an active environment that is its own design pattern with built-in Factory designs and Observer designs.

*A little note: Unity uses C#*

With the Prefab and GameObject system, one can instantiate GameObjects during run-time and create prototypes of a desired GameObject(s) to be used later in development or deployed during run-time. This is an example of the Unity engine's usage of Factory design. Factory design, in short, allows use to create objects and other things without invoking the "new" keyword.

On the other hand, the Update(), FixedUpdate(), OnTrigger functions, Start(), and a whole other plethora of observer type functions serve as the basis of Observer patterns one might want to implement.

An example of code that I made that uses both of these, in my FiredShellBehavior script:

    // This function is called when the GameObject collides with another GameObject
    private void OnCollisionEnter(Collision collision)
    {
        Quaternion particleRotation = transform.rotation;

        // Instantiate the particle system at the object's position and rotation
        GameObject particleInstance = Instantiate(particlePrefab, transform.position, Quaternion.Euler(particleTilt, particleRotation.y, particleRotation.z));
        particleInstance.transform.localScale = new Vector3(particleScale, particleScale, particleScale);

        // Destroy the particle after a certain duration (e.g., 1.5 seconds)
        Destroy(particleInstance, particlePlayTime);
        // Destroy the game Object on impact
        Destroy(gameObject);
    }

    void FixedUpdate()
    {
        // Slowly dip the shell forward as it flies
        transform.rotation *= Quaternion.Euler(rotationSpeed, 0f, 0f);
    }

OnCollisionEnter is an Observer that is called when two Colliders (a possible property of GameObjects). And inside that observer, we see the Factory pattern style of Unity take hold as we instantiate a particle that was prototyped somewhere else in the engine and is created. Ignoring the rest, the FixedUpdate is an observer that detects changes in the Physics frames of the engine. 

Throughout my usage of the Unity engine, I've had many times where I made use of these patterns. But I also implemented a few patterns of my own. In my AI series of scripts, I created a Singleton-esque pattern where I created data that is shared between different scripts. However, it differs slightly in the fact that is only known locally in a specified group of GameObjects.  The data is protected: only known to GameObjects that fall within the specified protections. 

And also, as good software designers should be doing, I've made sure to Tree Shake from time to time, where I read through code and "prune" the tree for dead or dated code. This pattern is just good conduct for ensuring that you don't fall into the antipattern of Lava Flow, where old code just piles up and code is built upon foundations which nobody knows how it works. 

And so, design patterns are something that everybody uses. And frankly? I would relate this back to how humans evolved to develop pattern recognition. But who knows? Maybe I'm rambling at this point.