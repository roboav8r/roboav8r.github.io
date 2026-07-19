---
layout: default
title: Projects
description: Robotics and perception projects — Arwun, PRISM, FiftyOne plugins, research.
---

<section class="wrap section page-head">
  <p class="eyebrow mono">Selected work</p>
  <h1>Projects</h1>
  <p class="lede">A few of the things I'm building. Most live on
     <a href="https://github.com/{{ site.github_user }}">GitHub</a>.</p>
</section>

<!-- ARCHIVED 2026-07-18 — Arwun and PRISM entries, kept for later. Uncomment to restore.

<section class="wrap section project" id="arwun">
  <div class="project-grid">
    <div class="project-meta mono">
      <span class="tag">Robot</span>
      <span>Jetson Orin Nano</span>
      <span>ROS 2 · Drake · Isaac</span>
      <span class="status">In development</span>
    </div>
    <div class="project-body">
      <h2>Arwun</h2>
      <p>A small self-balancing, tracked mobile robot with flipper-gripper arms. A layered
         control stack runs from an ESP32-S3 up to a Jetson Orin Nano, with controls
         prototyped in Drake (LQR) and a perception/world-modeling front-end moving onto
         NVIDIA Isaac. The whole build is documented in the
         build log.</p>
    </div>
  </div>
</section>

<section class="wrap section project" id="prism">
  <div class="project-grid">
    <div class="project-meta mono">
      <span class="tag">World model</span>
      <span>GTSAM · factor graphs</span>
      <span>Scene graph · LLM policy</span>
      <span class="status">Research</span>
    </div>
    <div class="project-body">
      <h2>PRISM</h2>
      <p>A graph-based world-modeling system: a factor-graph estimation backend, a
         hierarchical scene graph, and an LLM-grounded policy layer. Accelerated perception
         sources — visual SLAM, 3D reconstruction, detection — feed it as measurements.
         Supersedes my earlier MaRMOT and C2HI work.</p>
    </div>
  </div>
</section>

-->

<section class="wrap section project" id="fiftyone">
  <div class="project-grid">
    <div class="project-meta mono">
      <span class="tag">Open source</span>
      <span>Python · FiftyOne</span>
      <span>Tracking · evaluation</span>
    </div>
    <div class="project-body">
      <h2>FiftyOne plugins</h2>
      <p>Tooling for the computer-vision data platform I work on: an object-tracking
         plugin with quality-control facets and a roadmap of tracking-specific operators,
         plus integrations for cloud-hosted datasets.</p>
      <p class="project-links mono">
        <a href="https://github.com/{{ site.github_user }}/fiftyone-object-tracking">fiftyone-object-tracking</a>
        <a href="https://github.com/{{ site.github_user }}/fiftyone-aws">fiftyone-aws</a>
      </p>
    </div>
  </div>
</section>

<section class="wrap section project" id="research">
  <div class="project-grid">
    <div class="project-meta mono">
      <span class="tag">Research</span>
      <span>Perception · tracking</span>
    </div>
    <div class="project-body">
      <h2>Research</h2>
      <p>PhD in robotics, focused on perception. Published work in multi-object tracking
         and human–robot interaction.</p>
      <!-- TODO: drop in your real publications (title, venue, year, link) once you send the list.
           Example format:
           <ul class="pub-list">
             <li><strong>Paper title.</strong> Venue, Year. <a href="#">PDF</a> · <a href="#">Code</a></li>
           </ul>
      -->
    </div>
  </div>
</section>
