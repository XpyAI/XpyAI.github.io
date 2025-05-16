---
layout: post
title:  "User Controls for Robot Data Recording"
date:   2025-05-05 00:43:53 -0600
---

In our [last update](https://xpyai.github.io/2025-05-05/integrating-xpy-into-robot-architecture), we showed how Xpy integrates with the typical robot software architecture. We demonstrated this on a raspberry pi logging data that the Xpy web-app plotted in real time. Notably, it is important for the user to be able to specify when they want data to be recorded from their robot. This allows them to run experiments and prevent extraneous or bad data from clouding their analysis of their robot learning performance. To support this, we have added controls for the user to signal to the Xpy node installed on their robot when to begin and end the recording of robot data, which we demonstrate below:

# Demo Video

<div class="iframe-container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/DSTfCEH1_rk?si=DogRsA6MGdZuUifd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>
<style>
  .iframe-container{
    text-align:center;
  }
</style>

# Next Steps
We intend to flesh out further support for integration with model registries and to work on facilitating robot-software deployment. Feel free to reach out if you have questions!