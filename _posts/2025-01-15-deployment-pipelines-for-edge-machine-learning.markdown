---
layout: post
title:  "Deployment Pipelines for Edge Machine Learning"
date:   2025-01-15 15:43:53 -0600
categories: deployment piplines
---

Machine learning at the edge is steadily becoming more appealing for fast, secure, and reliable intelligence. At the onset of a robotics and IOT revolution, developers are wanting machine learning that is not dependent on some far-off server that brings with it the pain of rate/capacity limitations, lack of data security, and connectivity issues in the field.

This leaves open a couple of questions for the edge ML developer:

(1) How do I **deploy** my models to edge hardware (microcontrollers, DSPs, etc.) in the field?

(2) How do I **maintain** or **improve** my edge ML systems?

(3) How do I **automate** steps (1) and (2)?

The answer to these questions is a tale as old as time (aka the 1990s)…CI/CD pipelines.

# Exporting and Deploying ML Models
At Xpy AI, we’ve stood up some pipelines plugged into a test GitHub repo with a saved PyTorch model. Our pipelines do the following:

- Monitor for changes to the targeted repo.
- Export the PyTorch models to a portable format for edge ML.

For user convenience, we’ve also set up command line support for locally exporting PyTorch models (including those available in HuggingFace).

<div class="iframe-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/j8MpxPbPYBc?si=HSj4xkmqDUhItAs5" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<style>
  .iframe-container{
    text-align:center;
  }
</style>


With this tooling, we hope that developers can expedite the process of going from ML model on your machine to ML model working in the field.

# Next Steps
Next up, we’re going to deposit the .pte file artifacts into a shared directory and deploy these artifacts to some microcontrollers over the air! This should close the hypothetical circuit from model development to model deployment.

Feel free to reach out to us and let us know what you think! Our emails are [emmar.goodwill@gmail.com](mailto:emmar.goodwill@gmail.com) and [jamesgoodwill@mac.com](mailto:jamesgoodwill@mac.com).