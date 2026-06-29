---
layout: post
title: "Arwun, and why I'm putting it on Isaac"
date: 2026-06-17
summary: "Kicking off a public build log for a self-balancing tracked robot — and the reasoning behind moving its perception stack onto NVIDIA Isaac."
tags: [arwun, isaac, perception]
---

This is the first entry in a build log for **Arwun** — a small, self-balancing tracked
robot with flipper-gripper arms — and a place to think out loud while I move its perception
stack onto the NVIDIA Isaac platform.

<!-- This post is a template. Edit it freely or delete it and start your own. The point of
     a build log is to capture decisions and the reasoning behind them, not just results. -->

## Where the robot is right now

Controls are prototyped in Drake with an LQR design, and I'm wrapping up tabletop bench
validation with real servos and an IMU. The plan from here:

- keep Drake as the low-level controls and simulation brain,
- add Isaac ROS perception GEMs on the Jetson Orin Nano as measurement sources,
- feed those into PRISM, my factor-graph world model.

## Why Isaac, and why now

A few reasons, in order of how much they actually drove the decision:

1. **The split is convenient.** Isaac ROS GEMs lean on the GPU; PRISM's GTSAM optimization
   sits on the CPU. On an 8 GB Orin Nano that division of labor matters.
2. **It's the canonical sim-to-real loop.** Simulate in Isaac Sim, generate synthetic data,
   deploy to the edge via Isaac ROS — and I want to measure the gap honestly rather than
   eyeball it.
3. **It speaks the language I'm aiming at.** No sense being coy: this work doubles as a
   portfolio for physical-AI roles, so building on the actual stack is the point.

## What I expect to go wrong

If past Jetson work is any guide: version drift between CUDA, TensorRT, and ROS, and the
usual fight to expose the GPU inside Docker. I'll write those up as I hit them — that's the
part future-me will want.

Next entry: standing up the Isaac ROS container and running a single GEM against a rosbag.
