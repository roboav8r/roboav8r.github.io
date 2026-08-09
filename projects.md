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

<section class="wrap section project" id="arwun">
  <div class="project-grid">
    <div class="project-meta mono">
      <span class="tag">Robot</span>
      <span>Jetson Orin Nano</span>
      <span>ROS 2 · Drake</span>
      <span class="status">In development</span>
    </div>
    <div class="project-body">
      <h2>Arwun</h2>
      <p>A small, portable, and highly mobile tracked robot, designed from scratch. Diff drive
         on two long side treads, plus two flipper arms that extend the chassis to climb and
         descend stairs, and let the robot stand upright and balance. A camera and an IMU
         make up the sensor suite, driving a ROS2 navigation and perception stack on a
         Jetson Orin Nano, with offline data recording for development. Actuation is
         gearmotors with integrated encoders and standard hobby servos; the dynamics and
         control work is prototyped in Drake. The whole build is documented in the
         <a href="{{ '/log/' | relative_url }}">build log</a>.</p>
    </div>
  </div>
</section>

<!-- ARCHIVED 2026-07-18 — PRISM entry, kept for later. Uncomment to restore.

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
      <p>Tooling for the physical AI data platform I work on: an object-tracking
         plugin with quality-control facets and a roadmap of tracking-specific operators,
         plus integrations for cloud-hosted datasets.</p>
      <p class="project-links mono">
        <a href="https://github.com/{{ site.github_user }}/fiftyone-object-tracking">fiftyone-object-tracking</a>
        <a href="https://github.com/{{ site.github_user }}/fiftyone-aws">fiftyone-aws</a>
      </p>
    </div>
  </div>
</section>

<section class="wrap section project" id="audio">
  <div class="project-grid">
    <div class="project-meta mono">
      <span class="tag">Open source</span>
      <span>Python · TypeScript</span>
      <span>CLAP · spectrograms</span>
      <span class="status">Released</span>
    </div>
    <div class="project-body">
      <h2>FiftyOne Audio Toolkit</h2>
      <p>A plugin that makes audio a first-class citizen in FiftyOne. A custom renderer
         draws log-power spectrograms so clips are visible in the sample grid, with a
         player and playhead in the modal. An embeddings search panel queries a collection
         by example clip or natural-language prompt, with a distance histogram, a threshold
         slider, and positive/negative mining into saved views. Operators compute the
         embeddings, backed by LAION CLAP, Microsoft MS-CLAP, or your own HTTP endpoint.</p>
      <p>Built for my talk at the Voxel51 Audio and AI Meetup, "Curating, Searching, and
         Evaluating Audio Datasets in FiftyOne" — similarity search on ESC-50, captioning
         on Clotho, and the DCASE 2026 audio moment retrieval challenge.</p>
      <p class="project-links mono">
        <a href="https://github.com/{{ site.github_user }}/fiftyone-audio-toolkit">fiftyone-audio-toolkit</a>
        <a href="https://github.com/{{ site.github_user }}/fiftyone-audio-meetup">fiftyone-audio-meetup</a>
        <a href="https://youtu.be/HFSGU5sQy0k">Talk video</a>
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
      <p>PhD in robotics, focused on multimodal perception. Published work in multi-object tracking
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
