---
layout: post
title:  "Chaotic Neural Network to Solve the TSP"
date:   2014-06-10 00:19:00
categories: projects 
tags: projects optimization "machine learning"
---

I just finished up work on a school project with my classmate Sami, solving the traveling salesman problem (TSP) using neural networks (NNs). And not just any NN, but a chaotic NN! What? Yes. And it's amazing.

### The Code
The code was written in Python. Go try it out! It's not hard to run, and the README should help you get started.

> [https://github.com/jamestunnell/chaotic_tsp](https://github.com/jamestunnell/chaotic_tsp)

### The Short Story
Hopfield neural networks are being souped up for optimization, by inducing transient chaotic dynamics. That's basically all there is. (see the long story for more details).

### The Long Story
We followed the approach described by Aihara and Chen<sup>[[1]](#Cite1)</sup>. They start with a Hopfield NN (HNN), which is fitting since it was Hopfield and Tank<sup>[[2]](#Cite2)</sup> who first applied NNs to solve combinatorial optimization problems, using the HNN of course. So, we start with a HNN. What's missing? Well, the HNN is typically used because it <i>avoids</i> chaotic dynamics (assuming   weights are symmetric and self-connection weights are 0).

In fact, a HNN is guaranteed to converge to a stable local minimum. Well, that's a good thing, actually, but how will this help us produce chaotic dynamics? Chen and Aihara simply add some self-feedback (non-zero self-connection weight). Now we get attractors, and hence rich chaotic dynamics. Now we've got a mechanism to get our NN to explore the state space (exploratory) instead of going straight for the nearest local minima (greedy). That's what we wanted, but of course this throws the guaranteed convergence right out the window. Hmmm...

Not to worry, the simple trick is to decay the self-feedback amplitude, just like the cooling in simulated annealing. In fact, the authors are calling this <i>chaotic simulated annealing</i> (CSA) because there's no stochastic behavior in a chaotic system. So as the chaos-inducing term decays, the convergent behavior begins to dominate and the system will magically converge to a local minimum (which could also be the global minimum).

### The Long Long Story
If you really want it, here it is, in a <a href="{{'/files/csa_tsp.pdf' | prepend:site.baseurl}}">brief report</a> that Sami and I authored.

#### References
1. <a name="Cite1"/>Chen, Luonan, and Kazuyuki Aihara. "Chaotic simulated annealing by a neural network model with transient chaos." Neural networks 8.6 (1995): 915-930.
2. <a name="Cite2"/>Hopfield, John J., and David W. Tank. "“Neural” computation of decisions in optimization problems." Biological cybernetics 52.3 (1985): 141-152.
