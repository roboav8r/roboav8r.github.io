---
layout: post
title: "I gave a talk on audio ML in FiftyOne"
date: 2026-08-08
summary: "Thirty minutes on curating, searching, and evaluating audio datasets — plus the two repos that came out of it."
tags: [fiftyone, audio]
---

On Thursday I spoke at the Voxel51
[Audio and AI Meetup](https://voxel51.com/events/audio-and-ai-meetup-august-6-2026).
My talk was "Curating, Searching, and Evaluating Audio Datasets in FiftyOne" — about
thirty minutes on treating audio as a first-class citizen in a tool most people reach for
when they have images.

The demo ran three threads:

- **Similarity search** over ESC-50 environmental sounds, using CLAP embeddings to query
  a collection by example clip or by natural-language prompt.
- **Captioning** on Clotho — generating captions with CoNeTTE, then scoring them against
  the human references.
- **Moment retrieval**, the Audio Moment Retrieval challenge from DCASE 2026 — finding a
  described moment inside a long recording and putting it on an interactive timeline.

The [recording is on YouTube](https://youtu.be/HFSGU5sQy0k).

Two public repos came out of it.
[fiftyone-audio-toolkit](https://github.com/roboav8r/fiftyone-audio-toolkit) is the
plugin: a spectrogram renderer so clips are actually visible in the sample grid, an
embeddings similarity-search panel, and the operators that compute the embeddings.
[fiftyone-audio-meetup](https://github.com/roboav8r/fiftyone-audio-meetup) has the slide
deck and the dataset loaders, if you want to reproduce any of it.
