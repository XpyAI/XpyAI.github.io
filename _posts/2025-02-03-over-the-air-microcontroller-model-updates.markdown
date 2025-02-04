---
layout: post
title:  "Over the Air Microcontroller Model Updates"
date:   2025-02-03 15:43:53 -0600
categories: deployment piplines
---

As of our [last update](https://xpyai.github.io/2025-01-15/deployment-pipelines-for-edge-machine-learning), we have already created pipelines that track a github repository, pick up PyTorch model changes, and export a model to an edge-device compatible format. That left us with a crucial question: what do we do next with the output artifacts of our pipelines? 

Ideally, we’d be able to deploy these artifacts, flexibly, to devices in the field. For this reason, we built out a way to download the output artifacts from our pipelines over the air using ESP32-S3 microcontrollers.

# Pushing Model Changes to ESP-32 Microcontrollers
We approached this by using an ESP-32’s MAC address to reach out to a Spring Boot microservice endpoint that returns the assigned model to this specific device. The ESP-32 polls for model updates on an interval and only downloads the model’s .pte file if that file has not already been downloaded. We set up our jenkins pipelines to upload our preprocessed model artifacts to the Spring Boot microservice and voila! 

<div class="iframe-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/r6csqJ1aWiM?si=XxIfBg2YQ0qOBAty" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<style>
  .iframe-container{
    text-align:center;
  }
</style>

# Next Steps
At this point, we have deployment pipelines that pick up changes to a model, export it, and upload to a Spring Boot microservice. We also have microcontrollers picking up these models and downloading them to the device. The next step for flexible, edge ML deployment is the runtime infrastructure for running the downloaded models on the devices!

Feel free to reach out to us and let us know what you think! Our emails are [emmar.goodwill@gmail.com](mailto:emmar.goodwill@gmail.com) and [jamesgoodwill@mac.com](mailto:jamesgoodwill@mac.com).
