---
layout: post
title:  "Implementing the Genetic Algorithm"
date:   2014-06-13 09:07:00
categories: projects 
tags: projects genetic-algorithm
---

Another project at school this quarter required me to implement the [genetic algorithm](https://en.wikipedia.org/wiki/Genetic_algorithm) (GA). It was a bit of a fun project, mostly because the GA is a metaheuristic, so its ripe for reuse. In fact, I used the same GA library on three separate problems. The satisfaction of reuse really motivates me to provide improvements to the library.

### The Code
The code was written in Ruby. There are a few examples included that you can run right away. The README should help get started.

> [https://github.com/jamestunnell/evolve](https://github.com/jamestunnell/evolve)

### Details
Some details might be worth mentioning.

Only a simple GA is implemented. There's not facilities for multiple populations (islands), nor local searching (like memetic, annealing, etc.), nor co-evolution.

On the other hand, it's quite easy to use any one of the built-in methods for selection, mutation, and crossover. Methods for mutation and crossover are avaible by just including one of the built-in modules, like `UniformMutation` or `OnepointCrossover`. See the examples to get an idea how this is done. The `TournamentSelector` class will give you an idea of how to implement a selection method.

### Finally
In the end, it's not terribly full-featured, but it's easy to use and it may prove useful for quick prototyping of an optimization problem. 
