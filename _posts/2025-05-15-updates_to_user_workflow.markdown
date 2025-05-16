---
layout: post
title:  "Updates to Proposed User Workflow"
date:   2025-05-15 00:43:53 -0600
---

In our last few updates, we demonstrated how a robot developer can use Xpy AI to run experiments and track metrics across runs. This will help robot devs perform integrated real-world robot tests with ease. However, we were continuing to think about the problem of friction in robot software development workflows, and it occurred to us that

- Robot devs have to integrate seperate software systems that can include **multiple ML models** and **traditional rules-based software**; this complicates software maintainability because the current robot software development/deployment process is not modular.
- Robot devs have an uphill battle to fight in terms of setting up **data communication** across this seperate software systems (usually involving ROS).
- There are no **CI/CD solutions** for robot software.

In response to this, we have designed a user workflow with Xpy where the user can create a map of their software systems that link to separate code and model registries/repos. Xpy will automatically generate the ROS (robot operating system) code that connects these systems. Xpy will also maintain CI/CD pipelines for each system (allowing the robot dev to iterate on robot software in a modular way).

# The Outcome

The result is that the user only has to worry about building great ML models and cutting edge robot software, not the connective tissue for these different systems nor the deployment process.

The robot developer is then free to iterate on their modular software and test their changes with our previously demonstrated features (live data-visualizations and cross-run report generation).


<div class="iframe-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/SlzHNKqhCDg?si=ULk09JWowT4Zno5D" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<style>
  .iframe-container{
    text-align:center;
  }
</style>

# Next Steps
We are working to implement this workflow in our MLOps suite now! Feel free to reach out if you're interested or have any questions.
