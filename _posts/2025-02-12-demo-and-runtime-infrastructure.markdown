---
layout: post
title:  "Demo and Model Runtime Infrastructure on ESP32"
date:   2025-02-12 12:43:53 -0600
---

In our [last update](https://xpyai.github.io/2025-02-03/over-the-air-microcontroller-model-updates), we stood up Spring Boot microservices that our ESP32-S3 microcontrollers reach out to for model updates before downloading the new model. This sets us up nicely for flexible deploys of PyTorch models, and our next step is to implement the model runtime infrastructure to execute the models themselves!
# Model Runtime Infrastructure
We cross-compiled the [executorch](https://pytorch.org/executorch-overview) runtime for the ESP32s and set up an executor runner that allocates the proper memory, creates inputs for the deployed model, and executes the model on these inputs.
# Demo
We did a full demo of this project so far in the video below. This includes a demonstration of the previous two updates on this devlogs site, as well as the model runtime infrastructure:

<div class="iframe-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/bfhv2Isomr4?si=cDXgzBYN_uHp2iQI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<style>
  .iframe-container{
    text-align:center;
  }
</style>
# Next Steps
Now we have:
 
1. Pipelines that export a model to an edge-compatible format,
2. ESP32-S3 microcontrollers downloading new model .pte files,
3. The ESP32-S3 microcontrollers running a deployed model with some predefined inputs.

Our next steps are integrating these three steps and clean up work. There will be updates to come! 