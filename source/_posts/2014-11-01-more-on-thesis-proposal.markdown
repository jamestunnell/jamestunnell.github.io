---
layout: post
title:  "More on the Thesis Proposal"
date:   2014-11-01 10:46:00
categories: [Thesis] 
---

I've spent some time studying the high-level problem statement outlined in <a href="{{'/blog/2014/06/25/thesis-proposal' | prepend:site.baseurl}}">my last post</a>), and I've identified one of the main obstacles to implementing the Next Release Problem (NRP) in actual software project planning.

<!-- more -->

The obstacle stems from estimating the total cost of project requirements. Of course, the total cost will include implementation cost. But it should also include the cost of fixing software defects (bugs) that arise from the implementation. If bug fixing cost is ignored, then the total cost estimate for each requirement is inaccurate. Thus, there is not a sound sound basis for making optimization decisions involving requirement cost.

So, to overcome this obstacle, [my thesis work](https://github.com/jamestunnell/thesis) will focus on providing a probabilistic model based of project historical data. The goal of the model is predicting the makeup of expected bugs resulting from any software changes. I'm working this quarter to establish a statistical overview of actual project historical data, starting with the [MongoDB](https://www.mongodb.org/) project.
