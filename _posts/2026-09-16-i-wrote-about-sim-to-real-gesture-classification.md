---
layout: post
title: "New Voxel51 blog post about the sim-to-real gap in gesture classification"
date: 2026-09-16
summary: "Improving a gesture classifier with FiftyOne while exploring the sim-to-real gap."
tags: [fiftyone, hri]
---

I wrote a blog article for Voxel51, and you can check it out here: [Doing It Right with FiftyOne: Sim-to-Real Gesture Classification for Human-Robot Interaction](https://voxel51.com/blog/sim-to-real-gesture-classification-fiftyone)

I made a gesture classifier as part of a human-robot interaction project back in grad school, and it was quite bad. My motivation was initially to improve the gesture classifier, using FiftyOne to help dig in to the specifics and troubleshoot it.

Notably, I trained the gesture classifier using the [Robot Control Gestures v2 dataset](https://github.com/reddyav1/RoCoG-v2), which consists of both synthetic and real videos of standard hand and arm signals.

I had a chance to explore the sim-to-real gap firsthand. The real takeaway wasn't "synthetic data = bad", it's much more nuanced than that. Synthetic data is an excellent resource when used properly, and FiftyOne helped me to diagnose the issues rather than just using synthetic data as-is.

Please [have a read](https://voxel51.com/blog/sim-to-real-gesture-classification-fiftyone) if you're curious.
