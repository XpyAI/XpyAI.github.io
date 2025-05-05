---
layout: post
title:  "Integrating Xpy with Robot Architecture"
date:   2025-05-05 00:43:53 -0600
---

As of our [last update](https://xpyai.github.io/2025-04-30/robot-learning-ml-ops-suite), we have created an MLOps suite that manages data from robot experiments and allows the user to compare arbitrary metrics across experiments/runs. We demonstrated this with fake data from a laptop, but in this demonstration, we will be logging data from a raspberry pi running [ROS](https://www.ros.org/), the popular robot meta-operating system. 

We have created an Xpy ROS node that the user downloads to their robot, and this Xpy node will perform the data handling such that the Xpy web-app live plots the users logged data. In short, Xpy integration into real robot software architectures is purely plug-and-play. 

# Demo Video

<div class="iframe-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/xE7F0MXDPpk?si=XWZobman_udo2XoS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<style>
  .iframe-container{
    text-align:center;
  }
</style>

# Next Steps
With this integration step completed, we will now be working on giving the user more control over when the Xpy node listens to their robot and plots the associated data. This will allow the user to run clearly delineated experiments on their robot that gives them data that is easy to analyze.