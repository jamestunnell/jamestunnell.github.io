---
layout: post
title:  "The Next Release Problem"
date:   2014-06-25 23:00:00
categories: [Thesis, Optimization, Software Engineering] 
---

I have spent a few months now trying to select a topic for my thesis, and I've settled on the Next Release Problem (NRP). It's one of several problems being worked on in the area of Search-Based Software Engineering (SBSE). I only recently discovered SBSE while I was looking into the possibility of optimizing software development task assignment, as suggested by my thesis advisor, [Dr. John Anvik](http://www.cwu.edu/~janvik/). Already very energized by a recent stumbling onto Operations Research, I was glad to see it being applied in the area of SW engineering (where improvement is definitely needed).

### The Next Release Problem
In 2001 the Next Release Problem (NRP) was first defined by Bagnall et al<sup>[[1]](#Cite1)</sup>. It addresses the need to select some subset of all the possible software improvements (features, requirements, or what have you) in order to maximize profit, while respecting an upper limit on the amount of effort that can be expended (resources) in development.

Now it might seem the NRP is just like a 0-1 knapsack problem at this point, but there's an additional consideration: profit is only achieved by satisfying a customer. Each customer can have a different profit, and a different list of enhancements that they would like to be implemented in order to be satisfied. This makes the NRP a bit more interesting. And the NRP is definitely NP-Hard, like the 0-1 knapsack optimization problem.

#### References
1. <a name="Cite1"/>Bagnall, Anthony J., Victor J. Rayward-Smith, and Ian M. Whittley. "The next release problem." Information and software technology 43.14 (2001): 883-890.

